---
title: "07 — IT-стратегия для нон-IT-руководителя"
aliases: ["IT Strategy", "Build vs Buy", "TCO", "Data Governance"]
type: note
status: active
domain: education
module: 12-ERP-Digital
tags: [education, it-strategy, build-vs-buy, tco, governance, transformation]
created: 2026-05-19
updated: 2026-05-19
---

# 07 — IT-стратегия для нон-IT-руководителя

> COO / директор закупок / директор продукта **не должны быть программистами**, но обязаны понимать стратегические вопросы IT: build vs buy vs configure, TCO (Total Cost of Ownership — полная стоимость владения), почему 70% IT-проектов проваливаются, как читать предложения интеграторов, как выбирать вендора. Без этого понимания решения принимаются «по презентации», что приводит к катастрофическим инвестициям.

## Карта раздела

![](attachments/diagrams/12-build-vs-buy-decision.svg)

## 1. Зачем нон-IT-руководителю IT-стратегия

### 1.1 Контекст

В современной компании IT — это не «функция поддержки», а **операционный фундамент**. ERP, WMS, TMS, CRM, BI — все эти системы определяют, как работает бизнес. Решения по их выбору, внедрению, развитию **принимают не IT, а бизнес-руководители**.

Каноничные книги для нон-IT: **Marianne Bradford, «Modern ERP»** (Lulu, 4-е изд. 2020), **Adam Hartung, «Create Marketplace Disruption»** (FT Press, 2008), **George Westerman et al., «Leading Digital»** (HBS Press, 2014).

### 1.2 Главные стратегические вопросы

1. **Build vs Buy vs Configure** — для каждой IT-системы
2. **TCO** — полная стоимость владения, не только лицензия
3. **Vendor selection** — выбор поставщика
4. **Implementation partner** — выбор интегратора
5. **Data governance** — кто управляет данными
6. **Architecture** — как системы связаны между собой
7. **Risk management** — что делать при сбоях, кибератаках

**Ключевой вывод 1.** Нон-IT-руководитель не должен знать «как программируется», но должен знать «как стратегически решается». Это и есть IT-стратегия в его роли.

## 2. Build vs Buy vs Configure

### 2.1 Три варианта

![](attachments/diagrams/12-build-vs-buy-decision.svg)

| Подход | Что значит | Когда применять |
|--------|------------|-----------------|
| **Buy (SaaS)** | Готовое облачное решение | Стандартная задача, быстрый старт |
| **Configure** | Стандартная платформа + настройка | Стандартное решение с уникальными процессами |
| **Build (Custom)** | Своя разработка | Конкурентное преимущество, уникальная задача |

### 2.2 Когда Buy

- **Стандартная функция** — HR, бухгалтерия, email, CRM базовый
- **Нет внутренней экспертизы** — нет команды для поддержки
- **Быстрый ROI важен** — нужно сейчас, не через год
- **Низкий риск** — можно мигрировать на другого вендора

Примеры: Office 365 для email, Salesforce для CRM, NetSuite для ERP в SMB.

### 2.3 Когда Configure

- **Стандартная платформа + специфические процессы** — SAP / Oracle ERP в крупной компании
- **Глубокие индустриальные требования** — фармацевтика с GxP-валидацией
- **Готовность вкладываться в expertise** — нанять / обучить команду

Это **80% корпоративных IT-проектов**. Большинство ERP, WMS, TMS — Configure.

### 2.4 Когда Build

- **Конкурентное преимущество** — алгоритмы рекомендаций, ценообразование
- **Уникальная индустрия / процессы** — нет готового решения
- **Strategic IP** — данные / алгоритмы как актив
- **Готовность инвестировать $$$ и годы**

Примеры: Amazon DynamoDB, Google внутренняя инфраструктура, Netflix recommendation engine, Wildberries собственный e-commerce.

### 2.5 Главные ошибки

- **Build того, что можно купить** — выбрасываются миллионы на «свой Salesforce»
- **Buy того, что нужно build** — потеря конкурентного преимущества
- **Excessive configuration** — превращение стандартного ERP в кастомный франкенштейн

**Правило 80/20:** стандартное — Buy; критичное преимущество — Build; остальное — Configure.

**Ключевой вывод 2.** Build vs Buy — не «технический выбор», а **стратегическое решение**. Главные критерии: даёт ли решение конкурентное преимущество (Build), или это commodity (Buy).

## 3. TCO — Total Cost of Ownership

### 3.1 Что такое TCO

TCO — **полная стоимость** владения IT-системой за период (обычно 5 лет). Включает:

| Категория | Что входит |
|-----------|------------|
| **CAPEX (capital expenditures — капитальные затраты)** | Лицензии (perpetual), оборудование, инфраструктура |
| **Implementation** | Интегратор, консультанты, обучение, миграция данных |
| **Subscriptions** | Облачные лицензии, SaaS-подписки |
| **Support & Maintenance** | Поддержка вендора (обычно 20-25% от лицензии в год) |
| **Internal IT** | Команда поддержки внутри компании |
| **Upgrades** | Обновления платформы, миграции |
| **Indirect costs** | Простои, обучение пользователей, change management |

### 3.2 Типичная структура TCO

Для среднего ERP-проекта на 5 лет:
- Лицензии / подписки: 25-35%
- Implementation: 30-50%
- Support & Maintenance: 15-25%
- Internal team: 10-15%

«Цена лицензии — это 30% реальной стоимости» — поговорка CIO.

### 3.3 SaaS vs On-Premise TCO

| Аспект | SaaS | On-Premise |
|--------|------|------------|
| **Upfront cost** | Низкий (подписка) | Высокий (лицензии + оборудование) |
| **Operating cost** | Стабильный (подписка) | Низкий после внедрения |
| **5Y TCO** | Часто выше | Часто ниже при стабильной нагрузке |
| **10Y TCO** | Дороже | Дешевле |

Поэтому SaaS лучше для **переменной / растущей** нагрузки; On-Premise — для **стабильной**.

### 3.4 Hidden costs

Часто упускают:
- Стоимость **change management** (обучение пользователей)
- Стоимость **миграции данных**
- Стоимость **интеграций** с существующими системами
- Стоимость **upgrade** через 3-5 лет
- **Lost productivity** в период внедрения

Эти «скрытые» затраты часто составляют 30-50% реального TCO.

**Ключевой вывод 3.** TCO — обязательный анализ перед IT-инвестицией. Сравнение по цене лицензии без TCO — типичная ошибка, ведущая к плохим решениям.

## 4. Vendor & Implementation Partner Selection

### 4.1 Vendor selection (выбор вендора)

Стандартный процесс:

1. **Long list** — 10-15 вендоров (Gartner Magic Quadrant, Forrester Wave, отраслевые отчёты)
2. **Short list** — 3-5 после первичного отбора
3. **RFP** (Request for Proposal — запрос предложения) — формальный запрос
4. **Demo / POC** (Proof of Concept — пилот) — увидеть в работе
5. **Reference checks** — общение с существующими клиентами
6. **Negotiations** — переговоры по цене и условиям
7. **Decision** — финальный выбор

### 4.2 Implementation partner

Не путать с вендором! **Implementation partner** — интегратор, который внедряет систему:

- Большая четвёрка (Deloitte, EY, PwC, KPMG) — для enterprise
- Специализированные (Accenture, IBM, TCS) — для крупных проектов
- Среднего размера (российские интеграторы) — для mid-market
- Малые / нишевые — для специфических задач

**Главные критерии выбора:**
- Опыт в индустрии
- Опыт с конкретной платформой
- Команда, которая будет работать (не «продажники»)
- Methodology
- References

### 4.3 Главные ошибки выбора

- **Wow от демо** — все вендоры показывают красивое демо; реальность другая
- **Только по цене** — самый дешёвый интегратор обычно самый дорогой по итогу
- **Без reference checks** — звонок 5 существующим клиентам экономит миллионы
- **Без exit strategy** — что делать, если не получится? Как мигрировать?

### 4.4 Контракты

Главные пункты в контракте с вендором / интегратором:
- **Scope** — что именно делаем
- **Timeline** — milestones и сроки
- **Payment terms** — связь с milestones
- **SLA** (Service Level Agreement) — что и в каком объёме
- **Penalty clauses** — штрафы за провалы
- **Exit clauses** — как выйти из контракта
- **IP rights** — кому принадлежит созданное
- **Data ownership** — кто владеет данными

**Ключевой вывод 4.** Vendor selection — **процесс 3-6 месяцев**. Сэкономить на нём — потерять годы и миллионы. Reference checks — самый недооценённый инструмент.

## 5. Архитектура IT-стека

### 5.1 Типовая архитектура современной компании

```
[Customer-facing]
  ├─ Website / Mobile app
  ├─ E-commerce platform
  └─ Customer Service (CRM, chatbots)

[Operations]
  ├─ ERP (1C, SAP, Oracle)
  ├─ WMS, TMS, MES
  ├─ SCM Planning
  └─ HR systems

[Data]
  ├─ Data Warehouse / Lake
  ├─ MDM / PIM / DAM
  ├─ BI tools (Power BI, Tableau)
  └─ ML platforms

[Integration & Automation]
  ├─ iPaaS (integration platform)
  ├─ API gateway
  ├─ RPA platform
  └─ AI agents

[Infrastructure]
  ├─ Cloud (AWS, Azure, GCP, Yandex Cloud)
  ├─ Networking, security
  └─ Monitoring, observability
```

### 5.2 Главные принципы

- **API-first** — все системы интегрируются через API
- **Loose coupling** — системы независимы, можно менять одну без остальных
- **Single source of truth** для каждого типа данных (MDM)
- **Security by design** — встроенная безопасность, не «добавлена потом»
- **Observability** — мониторинг всех систем

### 5.3 Composable architecture

Современный тренд — **composable** (composable enterprise): IT-стек как набор лучших-в-классе компонентов, связанных через API. Альтернатива монолитному «всё в одном вендоре».

Преимущества:
- Best-of-breed для каждой функции
- Гибкость замены компонентов
- Меньше vendor lock-in

Недостатки:
- Больше интеграций для поддержки
- Сложнее операционно

**Ключевой вывод 5.** Архитектура IT-стека — стратегический выбор на 10+ лет. Monolithic vs composable — главный trade-off современности.

## 6. Цифровая трансформация

### 6.1 Что такое цифровая трансформация

**Digital Transformation** (цифровая трансформация) — стратегическое использование цифровых технологий для изменения **бизнес-модели**, не просто автоматизации существующего.

Каноничная книга — **George Westerman, Didier Bonnet, Andrew McAfee, «Leading Digital»** (HBS Press, 2014). Современный анализ — **MIT CISR (Center for Information Systems Research)**.

### 6.2 Уровни трансформации

| Уровень | Что меняем |
|---------|------------|
| **1. Digitization** | Бумажные процессы → цифровые (минимум) |
| **2. Digitalization** | Оптимизация цифровых процессов (RPA, BI) |
| **3. Digital Transformation** | Изменение бизнес-модели (платформы, новые рынки) |

### 6.3 Почему 70% Digital Transformations провалились

Согласно исследованиям McKinsey, BCG, Bain:
- Нет executive sponsorship
- Нет связи с бизнес-стратегией
- Технология вместо процессов и людей
- Нет change management
- Нет measurable outcomes

### 6.4 Best practices

- **Bold vision** — куда идём через 5-10 лет
- **C-level ownership** — CEO / COO лидируют
- **Cross-functional teams** — IT + business вместе
- **Agile delivery** — итеративные релизы
- **Culture transformation** — параллельно с технологией

**Ключевой вывод 6.** Цифровая трансформация — не «IT-проект», а **изменение компании**. Требует C-level лидерства и years инвестиций.

## 7. Кибербезопасность для нон-IT

### 7.1 Стратегические вопросы

Главные вопросы, которые должен понимать любой C-level:

- **Что у нас критичные активы?** — данные, системы, IP
- **Кто наши угрозы?** — внешние атакующие, внутренние
- **Какой план при инциденте?** — recovery time, communications
- **Кто отвечает?** — CISO (Chief Information Security Officer)

### 7.2 NIST Cybersecurity Framework

Стандарт — **NIST Cybersecurity Framework** (US National Institute of Standards and Technology). Пять функций:

1. **Identify** — что у нас есть и что критично
2. **Protect** — защитить
3. **Detect** — обнаружить атаки
4. **Respond** — отреагировать
5. **Recover** — восстановиться

### 7.3 Главные риски 2024-2025

- **Ransomware** — программы-вымогатели
- **Supply chain attacks** — атаки через подрядчиков
- **AI-powered attacks** — фишинг через LLM
- **Insider threats** — внутренние сотрудники
- **Cloud misconfigurations** — простые ошибки в облаке

### 7.4 Подробно — модуль 22

Глубокое погружение — в **[[../22-Risk-BC/index|Модуль 22: Risk Management]]**, где cybersecurity рассматривается как часть risk management.

**Ключевой вывод 7.** Cybersecurity — стратегическая дисциплина уровня C-level, не «техническая поддержка». Стоимость одного крупного инцидента — миллионы или потеря компании.

## Применение для руководителя

| Целевая роль | Главные применения |
|--------------|---------------------|
| **CEO / COO** | Owner IT-стратегии; executive sponsorship проектов; cybersecurity осознанность |
| **CIO** | Архитектура; vendor selection; governance |
| **CFO** | TCO IT-инвестиций; CAPEX vs OPEX outcomes |
| **CDO** | Data governance; MDM; analytics стек |
| **Директор закупок** | Vendor management для IT-вендоров; контракты |

## Связь с другими модулями

- [[01-ERP-Systems|01 ERP-системы]] — главная IT-инвестиция большинства компаний
- [[02-SCM-Planning-Systems|02 SCM Planning]] — следующий слой
- [[../22-Risk-BC/index|Модуль 22: Risk & BC]] — кибербезопасность как часть рисков
- [[../19-Org-Design-Change/index|Модуль 19: Org Design]] — IT-структура и команды
- [[../02-Finance/03-Capital-decisions|Модуль 02: Capital Decisions]] — NPV IT-инвестиций

## Источники

### Книги (приоритет чтения)

- George Westerman, Didier Bonnet, Andrew McAfee, **«Leading Digital»** (HBS Press, 2014) — стандарт digital transformation
- Marianne Bradford, **«Modern ERP»** (Lulu, 4-е изд. 2020) — ERP для бизнес-руководителей
- Mark Schwartz, **«The Art of Business Value»** (IT Revolution, 2016) — IT с точки зрения бизнес-value
- Gene Kim, Kevin Behr, **«The Phoenix Project»** (IT Revolution, 2013) — IT-роман, must-read для CIO
- Eric Ries, **«The Startup Way»** (Currency, 2017) — agile в крупных компаниях
- David Robertson, Karl Ulrich, **«Platform Product Development»** — для платформенной стратегии

### Статьи

- HBR: **«How to Get IT Strategy Right»** — серия
- McKinsey: **«The Three Building Blocks of Successful Customer-Data Strategies»**
- MIT Sloan Review: **«How Digital Leaders Outperform Their Peers»**
- BCG: **«Building the Digital Enterprise»**

### Онлайн-ресурсы

- **Gartner Research** — стандарт по IT-стратегии
- **Forrester Research** — параллельный анализ
- **MIT Sloan CISR** — research, framework, кейсы
- **CIO.com, InformationWeek** — практические статьи
- **TAdviser (Россия)** — российский эквивалент

### Сертификации (для глубокого изучения)

- **TOGAF** — Enterprise Architecture стандарт
- **ITIL Foundation** — IT Service Management
- **PMP / PRINCE2** — для IT-проектов
- **CISA / CISSP** — для cybersecurity governance

### Кейсы

- **GE Digital Transformation** — публичный кейс провала
- **Amazon AWS бизнес-модель** — пример успешной трансформации
- **Российские:** Сбер цифровая трансформация, Yandex экосистема, Wildberries IT-стек
- **MIT CISR working papers** — десятки кейсов
## Связанные документы

- [[index|Модуль 12: ERP & Digital]]
- [[../index|Education Index]]
- [[01-ERP-Systems|01 ERP-системы]]
- [[../22-Risk-BC/index|Модуль 22: Risk Management]]
