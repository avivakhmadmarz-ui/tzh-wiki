---
title: "05 — MDM, PIM, DAM"
aliases: ["MDM", "Master Data Management", "PIM", "DAM"]
type: note
status: active
domain: education
module: 12-ERP-Digital
tags: [education, mdm, pim, dam, master-data, akeneo, inriver]
created: 2026-05-19
updated: 2026-05-19
---

# 05 — MDM, PIM, DAM

> Мастер-данные — это **справочники критичных сущностей** компании (клиенты, продукты, поставщики, локации). Их качество определяет работу всех остальных систем (ERP, WMS, TMS, аналитики). MDM (Master Data Management — управление мастер-данными), PIM (Product Information Management — управление информацией о продукте) и DAM (Digital Asset Management — управление цифровыми активами) — три специализированные системы для разных аспектов.

## Карта раздела

![](attachments/diagrams/12-mdm-pim-architecture.svg)

## 1. Что такое мастер-данные

### 1.1 Контекст и легитимность

Концепция MDM оформилась в 2000-х как ответ на проблему «у одного клиента 50 разных написаний в разных системах». Каноничные книги — **Allen Dreibelbis et al., «Enterprise Master Data Management»** (IBM Press, 2008), **John Ladley, «Data Governance»** (Morgan Kaufmann, 2-е изд. 2020).

В 2024 году глобальный рынок MDM — ~$4 млрд, растёт 13% годовых.

### 1.2 Что такое мастер-данные

Мастер-данные — **критичные справочники**, которые используются во многих системах и процессах:

- **Customers (клиенты)** — кто покупает
- **Products (продукты / SKU)** — что продаём
- **Suppliers (поставщики)** — у кого закупаем
- **Locations (локации)** — где работаем
- **Employees (сотрудники)** — кто работает
- **Assets (активы)** — оборудование, машины

В отличие от **транзакционных данных** (отдельные заказы, отгрузки), мастер-данные **меняются медленно** и должны быть согласованы по всей компании.

### 1.3 Проблема без MDM

В типичной компании средний клиент существует в виде:
- 5-15 записей в разных системах
- С разными написаниями имени, ИНН, адреса
- Без общего идентификатора

Это приводит к:
- Неточным KPI («сколько у нас клиентов?»)
- Дублированию маркетинговых рассылок
- Невозможности 360°-view клиента
- Регуляторным рискам (GDPR, 152-ФЗ)

MDM решает через **единый Golden Record** — авторитетную запись для каждой сущности.

**Ключевой вывод 1.** MDM — фундамент всей data-driven компании. Без качественных мастер-данных аналитика, BI, AI работают на мусоре.

## 2. MDM — Master Data Management

### 2.1 Архитектура MDM

![](attachments/diagrams/12-mdm-pim-architecture.svg)

Главные компоненты MDM-системы:

- **Data Hub** — центральное хранилище golden records
- **Matching engine** — определение «один и тот же объект или разные»
- **Stewardship workflows** — процессы для data stewards (хранителей данных)
- **API / интеграции** — sync с другими системами
- **Audit trail** — история изменений

### 2.2 Подходы к MDM

| Подход | Описание | Когда применять |
|--------|----------|-----------------|
| **Registry style** | MDM как индекс; данные остаются в source systems | Низкое влияние на legacy |
| **Centralized** | Все мастер-данные в MDM, остальные — копии | Максимум контроля |
| **Coexistence** | Гибрид: master в MDM, изменения в source | Стандартный подход |
| **Transactional** | MDM как источник для новых транзакций | Зрелые компании |

### 2.3 Matching и Deduplication

Главная техническая сложность MDM — **fuzzy matching** (нечёткое сопоставление):
- «ООО Ромашка» = «Ромашка ООО» = «O.O.O. Romashka»?
- Иван Петров с адресом X = Иван Петров с адресом Y?

Методы:
- **Deterministic matching** — точные правила (ИНН совпадает → один объект)
- **Probabilistic matching** — статистические модели (Felligi-Sunter)
- **ML matching** — современные нейросетевые методы

Качество matching критично — ошибки дают либо ложные слияния, либо упущенные дубликаты.

### 2.4 Главные платформы

| Платформа | Сегмент |
|-----------|---------|
| **Informatica MDM** | Enterprise лидер |
| **SAP Master Data Governance** | На SAP-стеке |
| **Stibo Systems** | Multi-domain MDM |
| **Tibco EBX** | Гибкая платформа |
| **Reltio** | Cloud-native MDM |
| **Российские** | Юнидата, Турбо MDM |

**Ключевой вывод 2.** MDM — серьёзная инвестиция (10-100 млн руб) с долгосрочным ROI. Без MDM data-driven стратегия невозможна.

## 3. PIM — Product Information Management

### 3.1 Зачем PIM

PIM — специализированная MDM для **продуктов**. Современный e-commerce требует:
- 50-200 атрибутов на SKU (размеры, материалы, состав, инструкции)
- Локализации для разных стран и языков
- Версионирование (новый сезон, новая упаковка)
- Workflow согласования (бренд-менеджер, юрист, маркетинг)
- Каналы: сайт, маркетплейсы, B2B-каталог, печатные каталоги

ERP с этим не справляется — нужен специализированный PIM.

### 3.2 Главные платформы

| Платформа | Сегмент |
|-----------|---------|
| **Akeneo** | Лидер mid-market и open-source |
| **inRiver** | Enterprise PIM |
| **Salsify** | E-commerce PIM |
| **Pimcore** | Open-source, гибкая |
| **Plytix** | SMB-friendly |
| **Российские** | NORBIT, кастомные на 1С |

### 3.3 Применение PIM

- **E-commerce контент** — описания, фото, видео для сайта и маркетплейсов
- **Локализация** — для разных стран
- **Cross-channel consistency** — одинаковый контент везде
- **Time-to-market** — быстрый запуск новых SKU
- **Compliance** — обязательные атрибуты по регуляторам

### 3.4 ROI PIM

Типичные результаты:
- Time-to-market сокращён 30-50%
- Conversion rate ↑ 5-15% (за счёт качественного контента)
- Возвраты ↓ 5-10% (точное описание = правильные ожидания)
- Costs of content production ↓ 30%

Окупаемость 12-24 месяца.

**Ключевой вывод 3.** PIM — обязательная система для серьёзного e-commerce с >1000 SKU и работой на маркетплейсах. Без PIM контент-функция съедает огромные ресурсы.

## 4. DAM — Digital Asset Management

### 4.1 Зачем DAM

DAM — система для **цифровых активов**: изображения, видео, документы, презентации, шрифты, логотипы. Каждый актив — с метаданными, версиями, правами использования.

### 4.2 Главные функции DAM

- **Centralized storage** — единое хранилище для всех ассетов
- **Metadata management** — теги, категории, права
- **Search** — поиск по метаданным и содержимому (AI распознавание лиц, объектов)
- **Versioning** — история изменений
- **Approvals workflow** — согласование перед использованием
- **Distribution** — публикация по каналам
- **Rights management** — лицензии, сроки действия

### 4.3 Главные платформы

- **Bynder** — лидер mid-enterprise
- **Adobe Experience Manager Assets** — для Adobe-стека
- **Widen Collective** — enterprise
- **Brandfolder** — для брендового контента
- **Open-source: ResourceSpace**

### 4.4 PIM vs DAM

| Аспект | PIM | DAM |
|--------|-----|-----|
| **Что управляет** | Атрибуты продуктов | Файлы (медиа) |
| **Главный объект** | SKU | Asset (image, video) |
| **Связь** | PIM ссылается на DAM | DAM хранит файлы |

Зрелые компании используют **обе системы**, интегрированные между собой.

**Ключевой вывод 4.** DAM — фундамент маркетинговой и продуктовой функции в эру визуального контента. Без DAM маркетинг работает с хаосом папок.

## 5. Data Governance

### 5.1 Зачем Data Governance

Data Governance — это **система правил** для управления данными:
- Кто владелец каждой сущности
- Какие правила качества (минимальный набор атрибутов, форматы)
- Кто имеет доступ
- Что делать при изменениях

Без governance MDM / PIM / DAM становятся «системами без правил».

### 5.2 Роли

- **CDO (Chief Data Officer — директор по данным)** — стратегический owner
- **Data Owner** — бизнес-владелец сущности (например, директор клиентского отдела для клиентов)
- **Data Steward** — оператор поддержания качества
- **Data Custodian** — техническая поддержка

### 5.3 DAMA-DMBOK

Стандарт по управлению данными — **DAMA-DMBOK** (Data Management Body of Knowledge) от Data Management Association. Покрывает 11 областей: governance, architecture, modeling, security, integration, MDM, и т.д.

### 5.4 Practical Steps

1. Определить критичные сущности
2. Назначить data owners
3. Установить правила качества
4. Внедрить инструмент (MDM / PIM / DAM)
5. Мониторить качество (Data Quality KPIs)
6. Continuous improvement

**Ключевой вывод 5.** Data Governance — это люди и процессы, не только технология. MDM-инструмент без governance быстро деградирует.

## Применение для руководителя

| Целевая роль | Главные применения |
|--------------|---------------------|
| **COO** | Стратегия master data; инвестиции в MDM / PIM / DAM |
| **CDO / Head of Data** | Полный стек MDM, governance, качество данных |
| **Директор маркетинга** | DAM + PIM для маркетингового контента |
| **Категорийный менеджер** | PIM как daily tool для управления карточками |
| **Директор закупок** | MDM поставщиков как фундамент SRM |

## Связь с другими модулями

- [[01-ERP-Systems|01 ERP-системы]] — ERP как потребитель master data
- [[03-WMS-Warehouse-Systems|03 WMS]] — мастер-данные продуктов и локаций
- [[../09-Ecom-Marketplaces/01-Marketplaces-Operations|Модуль 09: Marketplaces]] — PIM критичен для маркетплейсов
- [[../11-Analytics-BI/02-SQL-Databases|Модуль 11.02: SQL]] — качество master data = качество BI

## Источники

### Книги (приоритет чтения)

- John Ladley, **«Data Governance»** (Morgan Kaufmann, 2-е изд. 2020) — стандарт по governance
- Allen Dreibelbis et al., **«Enterprise Master Data Management»** (IBM Press, 2008) — стандарт MDM
- DAMA International, **«DAMA-DMBOK»** (DMBoK, 2-е изд. 2017) — энциклопедия управления данными
- Andy Hayler, **«Master Data Management and Customer Data Integration»** (Wiley, 2009)

### Статьи

- Gartner Magic Quadrant for MDM, PIM, DAM (ежегодно)
- Forrester Wave for MDM
- HBR: «Data Governance: An Essential Element»

### Онлайн-ресурсы

- **DAMA International (dama.org)** — глобальное сообщество data professionals
- **Informatica MDM Learning** — официальные курсы
- **Akeneo Academy** — для PIM
- **Российские:** Russian Data Management Association

### Сертификации

- **CDMP (Certified Data Management Professional)** — DAMA-сертификация
- **Informatica MDM Specialist**
- **Akeneo Certified**

### Кейсы

- **Procter & Gamble MDM** — публичные доклады
- **Российские:** Сбер, X5 MDM трансформации (TAdviser)
## Связанные документы

- [[index|Модуль 12: ERP & Digital]]
- [[../index|Education Index]]
- [[01-ERP-Systems|01 ERP-системы]]
