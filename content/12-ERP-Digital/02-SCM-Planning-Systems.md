---
title: "02 — SCM Planning-системы"
aliases: ["SCM Planning", "Kinaxis", "Blue Yonder", "o9", "SAP IBP", "APS"]
type: note
status: active
domain: education
module: 12-ERP-Digital
tags: [education, scm, planning, kinaxis, blue-yonder, sap-ibp, aps]
created: 2026-05-19
updated: 2026-05-19
---

# 02 — SCM Planning-системы

> SCM Planning-системы — это слой **тактического и операционного планирования** над ERP. ERP записывает «как есть»; SCM Planning отвечает на вопрос «что делать дальше». Главные платформы — Kinaxis RapidResponse, Blue Yonder, o9 Solutions, SAP IBP (Integrated Business Planning — интегрированное бизнес-планирование). Эти системы — реализация S&OP / IBP-методологий на технологическом уровне.

## Карта раздела

![](attachments/diagrams/12-erp-digital-module-map.svg)

## 1. Что такое SCM Planning-системы

### 1.1 Контекст

SCM (Supply Chain Management) Planning-системы появились как ответ на ограничения ERP в планировании. ERP сильна в **транзакционных операциях** (записать продажу, провести оплату), но **слаба** в плановой логике (что произвести, что закупить, где разместить запасы).

Каноничные книги — **Sunil Chopra, Peter Meindl, «Supply Chain Management»** (Pearson, главы по planning); **Gartner Magic Quadrant for Supply Chain Planning** (ежегодно).

### 1.2 Разница ERP vs SCM Planning

| Аспект | ERP | SCM Planning |
|--------|-----|--------------|
| **Цель** | Транзакции, учёт | Планирование, оптимизация |
| **Горизонт** | Сейчас / последний период | 12-24 месяца вперёд |
| **Данные** | Реальные операции | Прогнозы, гипотезы, сценарии |
| **Пользователь** | Бухгалтер, кладовщик, продажник | Планировщик спроса, supply planner |
| **Логика** | Записать факт | Оптимизировать решение |

### 1.3 Главные применения

- **Demand Planning** — прогноз спроса (см. модуль 11.05 ML)
- **S&OP** (Sales & Operations Planning — планирование продаж и операций) — ежемесячный согласованный план (см. модуль 04.03)
- **Inventory Optimization** — MEIO (Multi-Echelon Inventory Optimization — многоуровневая оптимизация запасов)
- **Supply Planning** — оптимизация поставок при ограничениях
- **APS** (Advanced Planning & Scheduling — продвинутое планирование и расписание) — производственное расписание

**Ключевой вывод 1.** SCM Planning — не альтернатива ERP, а **дополнение**: ERP даёт данные, SCM Planning делает из них решения.

## 2. Главные платформы

### 2.1 Kinaxis RapidResponse

**Kinaxis** (Канада, основана 1984) — лидер концепции **Concurrent Planning** (параллельного планирования). Главная фишка — **what-if сценарии в реальном времени**: меняешь параметр → видишь последствия на всей цепочке за секунды.

**Сильные стороны:**
- Скорость симуляции
- Сценарный анализ как core competency
- Концепция «what-if branches» — параллельные виртуальные миры планов

**Когда выбирать:** компании с высокой волатильностью спроса, требующие быстрого пересчёта планов. Apple, Cisco, Toyota — клиенты.

### 2.2 Blue Yonder (бывшая JDA)

**Blue Yonder** (приобретена Panasonic в 2021) — широкая платформа с модулями:
- **Luminate Demand** — прогнозирование с AI
- **Luminate Planning** — supply planning
- **Luminate Logistics** — TMS, WMS

**Сильные стороны:**
- Глубина функционала, особенно для retail и FMCG
- Сильная аналитика на AI
- Интеграция WMS + TMS + Planning

**Когда выбирать:** retail, FMCG, complex omnichannel-сети.

### 2.3 o9 Solutions

**o9** (основана 2009 в Далласе) — современная платформа на cloud-native архитектуре. Главное отличие — **Enterprise Knowledge Graph** (корпоративный граф знаний) — данные + связи + правила в одной модели.

**Сильные стороны:**
- Современная архитектура
- IBP-фокус (полная интеграция Sales / Marketing / Supply / Finance в одном цикле)
- Активный рост (2024-2025)

**Когда выбирать:** компании, ищущие IBP-зрелость, готовые к современной технологии.

### 2.4 SAP IBP

**SAP IBP** (Integrated Business Planning) — модуль SAP, преемник SAP APO. Интегрирован с SAP S/4HANA, что даёт преимущество для уже SAP-клиентов.

**Сильные стороны:**
- Интеграция с SAP S/4HANA
- Стандартный SAP-стек
- IBP-методология

**Когда выбирать:** компании на SAP, не хотящие best-of-breed.

### 2.5 Российский ландшафт

В РФ западные SCM Planning-системы либо ушли (Blue Yonder), либо доступны через серые каналы (Kinaxis, o9). Российские альтернативы:

- **Forecast NOW!** — российская платформа прогнозирования
- **Optimacross** — для розницы
- **1С: УПП / 1С: ERP с надстройками** — для базового planning
- **Кастомные решения** на open-source (Anaplan workaround, Python + Airflow)

**Ключевой вывод 2.** Top-3 мировых платформ — Kinaxis, Blue Yonder, o9 — лидеры Gartner Magic Quadrant 2024. Российские компании сейчас работают через workaround или собственные решения.

## 3. APS — Advanced Planning & Scheduling

### 3.1 Контекст

**APS** (Advanced Planning & Scheduling) — специализация для **производственного планирования**: какой заказ когда производить, на каком оборудовании, в каком порядке.

Каноничный учебник — **Hartmut Stadtler, Christoph Kilger, «Supply Chain Management and Advanced Planning»** (Springer, 5-е изд. 2014).

### 3.2 Главные функции APS

- **Production Scheduling** — расписание производства с учётом мощностей
- **Sequencing** — последовательность заказов с минимизацией переналадок
- **Capacity Planning** — что делать при превышении мощности
- **Order Promising** — реальные обязательства по срокам клиенту (ATP — Available-to-Promise — обещание доступности)

### 3.3 Решения

- **Asprova** (Япония) — лидер в дискретном производстве
- **Preactor** (Siemens) — для среднего сегмента
- **SAP PP/DS** (Production Planning and Detailed Scheduling) — модуль SAP
- **OptiPlant** (Российская) — для российского рынка

### 3.4 Когда нужен APS

APS критичен в компаниях с:
- Дискретным производством (электроника, машиностроение)
- Многими заказами с разными сроками
- Сложными переналадками
- Capacity constraints

Для FMCG / непрерывного производства APS менее критичен.

**Ключевой вывод 3.** APS — отдельная категория, не «модуль SCM Planning». В производственных компаниях APS внедряется параллельно с ERP, требует отдельной экспертизы.

## 4. Внедрение SCM Planning

### 4.1 Главные сложности

- **Качество данных** — SCM Planning «срабатывает» только на чистых master data из ERP
- **Доверие пользователей** — планировщики привыкли к Excel, не доверяют системе
- **Configuration vs Customization** — баланс
- **Интеграция с ERP** — данные туда-сюда, потенциальные конфликты

### 4.2 Стандартный roadmap

| Этап | Срок | Артефакт |
|------|------|----------|
| Pilot Demand Planning | 3-6 месяцев | Прогноз для ТОП-50 SKU |
| Roll-out Demand Planning | 6-12 месяцев | Полный ассортимент |
| Supply Planning | 6-12 месяцев | Интегрированный план поставок |
| S&OP Cycle | 3-6 месяцев | Стандартизированный месячный цикл |
| Advanced (MEIO, simulation) | 12+ месяцев | Зрелое использование |

Стандартный сценарий — 18-36 месяцев до зрелого SCM Planning.

### 4.3 ROI SCM Planning

Типичный ROI (по данным Gartner / McKinsey):
- Снижение запасов 10-25%
- Улучшение fill rate 5-15%
- Снижение upchain costs 5-10%
- Снижение времени на планирование 30-50%

При правильном внедрении окупается за 12-18 месяцев.

**Ключевой вывод 4.** SCM Planning — высокоокупаемая инвестиция при условии **зрелой data infrastructure** и **change management**. Без них — потерянный бюджет.

## 5. Тренды 2024-2025

### 5.1 AI в SCM Planning

- **AI-Powered Demand Forecasting** — улучшение точности на 5-15% vs классические методы
- **Reinforcement Learning для inventory** — оптимальные правила пополнения
- **Causal AI для disruptions** — понимание, почему упали продажи (см. модуль 11)

### 5.2 Concurrent Planning

Концепция Kinaxis: все плановщики работают **в одной модели одновременно**, видя изменения друг друга в реальном времени. Заменяет последовательный workflow «demand → supply → finance».

### 5.3 Digital Twin Supply Chain

Полная цифровая модель цепочки поставок, синхронизированная с реальностью. Симуляция «что если» — открытие склада, новый поставщик, санкции.

### 5.4 Sustainability в planning

ESG-метрики (Environmental, Social, Governance) встроены в планирование:
- Углеродный след каждого плана
- Trade-off между cost и emissions
- Optimization с ESG-constraints

**Ключевой вывод 5.** SCM Planning эволюционирует от «правил и оптимизации» к «AI + симуляция + sustainability». Лидеры (Apple, Walmart, P&G) уже там; большинство компаний на 5-10 лет позади.

## Применение для руководителя

| Целевая роль | Главные применения |
|--------------|---------------------|
| **COO** | Стратегия SCM Planning; выбор платформы; интеграция с S&OP |
| **Директор supply chain** | Daily владение планированием; зрелость S&OP / IBP |
| **Директор закупок** | Supply Planning + supplier collaboration |
| **CFO** | ROI SCM Planning; CAPEX оценка внедрения |
| **Категорийный менеджер** | Demand Planning по категории |

## Связь с другими модулями

- [[01-ERP-Systems|01 ERP-системы]] — данные для SCM Planning
- [[../04-Supply-Chain/03-Demand-Planning-SOP|Модуль 04: S&OP]] — методология, реализуемая в SCM Planning
- [[../04-Supply-Chain/04-Inventory-Management|Модуль 04: Inventory Management]] — MEIO как часть SCM Planning
- [[../11-Analytics-BI/05-Machine-Learning-Operations|Модуль 11.05: ML]] — AI в demand forecasting
- [[../14-Planning/index|Модуль 14: Planning Methodologies]] — IBP, DDMRP, Hoshin Kanri

## Источники

### Книги (приоритет чтения)

- Hartmut Stadtler, Christoph Kilger, **«Supply Chain Management and Advanced Planning»** (Springer, 5-е изд. 2014) — стандарт по APS
- Sunil Chopra, Peter Meindl, **«Supply Chain Management»** (Pearson, главы по planning) — учебник MBA
- Carol Ptak, Chad Smith, **«Demand Driven Material Requirements Planning»** (Industrial Press, 3-е изд. 2018) — альтернатива классическому MRP
- Robert Handfield, **«The LIVING Supply Chain»** (Wiley, 2017) — концепция living supply chain

### Статьи

- Gartner Magic Quadrant for Supply Chain Planning (ежегодно)
- Forrester Wave for Supply Chain Planning Solutions
- HBR: «How AI Is Transforming Supply Chain Management»
- McKinsey: «The next-generation operating model for supply chain»

### Онлайн-ресурсы

- **Kinaxis Learning (kinaxis.com/learning)** — официальные курсы
- **Blue Yonder University** — официальное обучение
- **SAP IBP Learning Hub** — официальные ресурсы
- **APICS / ASCM** — методология SCM Planning
- **Российские:** TAdviser SCM Planning, профильные конференции

### Сертификации

- **APICS CSCP (Certified Supply Chain Professional)** — широкая SCM-сертификация
- **APICS CPIM (Certified in Planning and Inventory Management)** — фокус на планировании
- **Kinaxis Certified Planner** — для Kinaxis
- **SAP IBP Certified Application Associate**

### Кейсы

- **Apple — Kinaxis** — публичные доклады о concurrent planning
- **P&G — Blue Yonder** — каноничный кейс
- **Walmart — собственные системы** — публичные доклады
- **Toyota — Kinaxis** — после Тохоку
- **Российские:** X5 на Forecast NOW, кейсы Сбер Маркет
## Связанные документы

- [[index|Модуль 12: ERP & Digital]]
- [[../index|Education Index]]
- [[01-ERP-Systems|01 ERP-системы]]
- [[../14-Planning/index|Модуль 14: Planning]]
