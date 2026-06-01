---
title: "Модуль 04 — Supply Chain Management"
aliases: ["Module 04", "Supply Chain", "SCM", "Управление цепочками поставок"]
type: hub
status: active
domain: education
module: 04-Supply-Chain
tags: [index, education, supply-chain, scm, logistics, inventory]
created: 2026-05-18
updated: 2026-05-18
---

# Модуль 04 — Supply Chain Management (управление цепочками поставок)

> Сквозное управление потоком товаров, информации и денег от поставщика поставщика до конечного потребителя. Включает проектирование сети, прогнозирование спроса, управление запасами, логистику, обработку возвратов и риск-менеджмент. Один из самых широких и операционно-критичных модулей для COO, директора закупок и директора логистики.

## Карта раздела

![](attachments/diagrams/04-supply-chain-module-map.svg)

## Заметки модуля

1. **[[01-SCOR-Maturity|01 SCOR & Maturity]]** — SCOR (Supply Chain Operations Reference — эталонная модель операций в цепочке поставок) от ASCM (Association for Supply Chain Management — Ассоциация управления цепочками поставок), шесть базовых процессов (Plan / Source / Make / Deliver / Return / Enable), три уровня детализации, Gartner Top 25 как benchmark, модели зрелости
2. **[[02-Network-Design|02 Network Design]]** — проектирование сети дистрибуции: DC location, многоуровневая сеть (echelons), централизация vs децентрализация, Multi-Echelon Inventory Optimization (MEIO), nearshoring / friendshoring
3. **[[03-Demand-Planning-SOP|03 S&OP & Demand Planning]]** — S&OP (Sales & Operations Planning — планирование продаж и операций) как пятишаговый процесс согласования спроса и поставок; методы прогнозирования: Time Series (Holt-Winters, ARIMA — Autoregressive Integrated Moving Average), Croston для прерывистого спроса, ML-методы (Prophet, XGBoost, LSTM — Long Short-Term Memory)
4. **[[04-Inventory-Management|04 Inventory Management]]** — EOQ (Economic Order Quantity — экономически обоснованный размер заказа), Safety Stock, Newsvendor model, политики пополнения (s,Q) / (s,S) / (R,Q) / (R,S), ABC × XYZ матрица сегментации, VMI (Vendor-Managed Inventory) / CMI (Co-Managed Inventory)
5. **[[05-Logistics-Transportation|05 Logistics & Transportation]]** — modes (air / sea / rail / road / pipeline), контейнерная логистика (FCL / LCL — Full / Less than Container Load), 3PL / 4PL / 5PL (Third / Fourth / Fifth-Party Logistics), Reverse Logistics, Cold Chain, WMS (Warehouse Management System) / TMS (Transportation Management System)
6. **[[06-Supply-Chain-Risk|06 Supply Chain Risk Management]]** — категории рисков (geopolitical / natural / financial / operational / regulatory / demand), стратегии митигации, баланс resilience vs efficiency, BCP (Business Continuity Planning), уроки COVID и санкций
7. **[[07-Last-Mile-Delivery|07 Last-Mile Delivery]]** — модели доставки (own fleet / 3PL / ПВЗ / FBO / gig / dark stores / click-and-collect), unit-экономика доставки, drop density, VRP (Vehicle Routing Problem — задача маршрутизации транспорта), возвраты, B2B vs B2C специфика
8. **[[08-Route-Optimization|08 Route Optimization]]** — оптимизация маршрутов вглубь: таксономия задач (TSP → VRP → CVRP / VRPTW / MDVRP / PDPTW / динамический VRP), методы решения (точные, конструктивные эвристики Clarke-Wright, метаэвристики, ML), конвейер динамической маршрутизации (геокодирование → матрица → солвер → диспетчеризация → переоптимизация), солверы (OR-Tools, VROOM, российские), KPI и внедрение
9. **[[09-Logistics-IT-Systems|09 Logistics IT Systems]]** — ИТ-ландшафт логистики: WMS / TMS / OMS / YMS / WES-WCS и Control Tower, поток заказа через системы, сквозная видимость (supply chain visibility), интеграция и выбор, российские системы, цифровой двойник цепочки
10. **[[10-Retail-Network-Logistics|10 Retail Network Logistics]]** — логистика крупных розничных и e-commerce сетей: архитектура сети (РЦ → хабы → сортцентры → ПВЗ), кросс-докинг, омниканальный фулфилмент (ship-from-store, BOPIS, dark store, единый пул запасов), стадии масштабирования сети, кейсы Walmart / X5 / Wildberries / Ozon

## Зачем модуль руководителю

Цепочка поставок — это «кровеносная система» товарного бизнеса. Все остальные функции (продажи, маркетинг, продукт) могут работать идеально, но если supply chain не доставляет товар вовремя, в нужном объёме и без потерь — компания не зарабатывает.

После COVID-19 и санкций 2022-2024 актуальность модуля выросла резко: компании, годами оптимизировавшие цепочки по эффективности (efficiency: JIT — Just-In-Time, «точно в срок»; single sourcing — закупка у единственного поставщика), оказались неустойчивыми к шокам. Зрелое управление цепочкой требует баланса — достаточная эффективность для конкурентоспособной цены и достаточная устойчивость для выживания при сбоях.

## Применение для руководителя

| Целевая роль | Что взять из модуля |
|--------------|---------------------|
| **COO** (Chief Operating Officer — главный операционный директор) | SCOR как общий язык операций; S&OP как ежемесячный ритм принятия решений; баланс устойчивости и эффективности (resilience vs efficiency) как стратегический выбор; KPI: OTIF (On Time In Full — поставка вовремя и в полном объёме), Perfect Order (идеальный заказ), Cash-to-Cash Cycle (цикл «деньги-в-деньги») |
| **Директор закупок** | Network Design (проектирование сети) для импорта из КНР под санкциями (нужно ли разделять потоки между странами); стратегия с несколькими поставщиками для критичных категорий; интеграция S&OP с планированием поставщиков (supplier planning) |
| **Директор логистики** | Полная архитектура сети распределения; выбор 3PL / 4PL; стратегия последней мили (Last-Mile); внедрение WMS / TMS; обратная логистика (reverse logistics) |
| **Категорийный менеджер** | ABC × XYZ матрица для управления ассортиментом; политика запасов на уровне SKU; влияние lead time на доступность |
| **Финансовый директор** | Working Capital через управление запасами; влияние политики пополнения на Cash-to-Cash; resilience vs efficiency в денежном выражении |

## Связь с другими модулями

- [[../02-Finance/index|Модуль 02 — Corporate Finance]] — Cash-to-Cash Cycle, Working Capital, влияние запасов на ROIC
- [[../03-Management-Accounting/02-Cost-to-Serve|Модуль 03 — Cost-to-Serve]] — большинство buckets CTS приходит из логистики и склада
- [[../05-Procurement/index|Модуль 05 — Strategic Sourcing & Procurement]] — Source как одно из ядер SCOR; integrated procurement planning
- [[../06-Foreign-Trade/index|Модуль 06 — Foreign Trade]] — международная логистика, Инкотермс, валютный контроль
- [[../07-Category-Management/index|Модуль 07 — Category Management]] — ассортиментные решения через ABC / XYZ
- [[../11-Analytics/index|Модуль 11 — Analytics]] — data-инфраструктура для прогнозирования и оптимизации
- [[../12-ERP-Digitalization/index|Модуль 12 — ERP & Digitalization]] — ERP / WMS / TMS как платформа управления цепочкой
- [[../14-Planning-Methodologies/index|Модуль 14 — Planning Methodologies]] — S&OP как часть планировочной иерархии
- [[../22-Risk-Management/index|Модуль 22 — Risk Management]] — supply chain risk как часть общего риск-менеджмента

## Источники

### Книги (приоритет чтения)

- ASCM, **«SCOR Digital Standard»** (последняя версия, обновляется) — официальный стандарт фреймворка SCOR
- Sunil Chopra, Peter Meindl, **«Supply Chain Management: Strategy, Planning, and Operation»** (Pearson, 7-е изд.) — стандартный учебник MBA-программ
- David Simchi-Levi, Philip Kaminsky, Edith Simchi-Levi, **«Designing and Managing the Supply Chain»** (McGraw-Hill, 3-е изд.) — фокус на сетевом дизайне
- Yossi Sheffi, **«The Resilient Enterprise»** (MIT Press, 2005) — каноничная книга про устойчивость, остаётся актуальной после COVID
- Yossi Sheffi, **«The Power of Resilience»** (MIT Press, 2015) — продолжение, разбор современных кейсов
- Donald Bowersox, David Closs, M. Bixby Cooper, **«Supply Chain Logistics Management»** (McGraw-Hill, 5-е изд.) — детальный учебник по логистике
- Rob Hyndman, George Athanasopoulos, **«Forecasting: Principles and Practice»** (OTexts, 3-е изд., бесплатно онлайн) — современный стандарт по прогнозированию
- Carol Ptak, Chad Smith, **«Demand Driven Material Requirements Planning (DDMRP)»** (Industrial Press, 3-е изд.) — современная альтернатива классическому MRP
- Eli Goldratt, **«The Goal»** — Theory of Constraints в применении к производству и цепочкам
- Lyle Ginsburg, **«Last Mile Logistics: A New Era of Distribution»** (2021) — специально для заметки 07

### Статьи

- HBR, **«Building a More Intelligent Supply Chain»** (различные годы) — серия аналитических статей
- McKinsey Quarterly, **«The future of supply chains: 2030 outlook»** — стратегические прогнозы
- McKinsey, **«The future of last-mile delivery: 2025 vision»** — last-mile тренды
- MIT Sloan Management Review, **«Building the Resilient Supply Chain»** — после COVID
- Gartner, **«Top 25 Supply Chains»** — ежегодный рейтинг с разбором практик лидеров
- HBR, **«The Acceleration Imperative: How Supply Chains Can Be Built for Speed»**

### Онлайн-ресурсы

- ASCM (Association for Supply Chain Management, ascm.org) — официальный источник SCOR
- CSCMP (Council of Supply Chain Management Professionals, cscmp.org) — отраслевые исследования и метрики
- Gartner Supply Chain Research — отчёты и методологии
- MIT Center for Transportation & Logistics (ctl.mit.edu) — академические исследования
- SCM World / Gartner Supply Chain Symposium — конференции и материалы
- Российская логистическая ассоциация — кейсы и стандарты для РФ
- ИНКОТЕРМС 2020 (ICC) — официальные правила международных торговых терминов
- Statista E-commerce Reports — последние мили в РФ и мире

### Сертификации

- **CSCP** (Certified Supply Chain Professional, ASCM) — основной сертификат по цепочке поставок
- **CPIM** (Certified in Planning and Inventory Management, ASCM) — углублённо по планированию и запасам
- **CLTD** (Certified in Logistics, Transportation and Distribution, ASCM) — логистическая специализация
- **SCOR Professional** — официальная сертификация по SCOR
- **CILT** (Chartered Institute of Logistics and Transport) — британская сертификация, признана международно

### Кейсы

- **Walmart** — каноничный пример эффективной цепочки: кросс-докинг (cross-docking — перевалка без длительного хранения), VMI с поставщиками, мощная аналитика
- **Zara (Inditex)** — гибкая короткоцикловая (short-cycle) цепочка: 2-недельный модный цикл (fashion cycle), нершорное (близкое к рынку) производство в Испании / Португалии / Марокко
- **Toyota** — Toyota Production System (TPS — производственная система Toyota) как философия Lean и JIT
- **Amazon** — сеть фулфилмента (fulfillment network) с FBA (Fulfillment by Amazon — хранение и доставка Amazon), последняя миля через Amazon Logistics
- **Apple** — стратегический сорсинг у Foxconn, тщательный контроль качества, вертикальная интеграция (vertical integration) в дизайн чипов
- **Maersk** — кейс крупнейшего контейнерного перевозчика, переход в 4PL / интегрированную логистику
- **Wildberries / Ozon** — российские маркетплейсы как пример быстро растущих фулфилмент-сетей
- **Boeing 787 Dreamliner** — антипример: чрезмерный аутсорсинг привёл к срывам сроков и качества
- **Кейсы COVID-19** — массовые сбои в глобальных цепочках поставок 2020-2022 (блокировка Суэцкого канала, дефицит полупроводников — semiconductor shortage)
## Связанные документы

- [[../index|Education Index]]
- [[../02-Finance/index|Модуль 02: Corporate Finance]]
- [[../03-Management-Accounting/index|Модуль 03: Management Accounting]]
- [[../05-Procurement/index|Модуль 05: Procurement]]
- [[../06-Foreign-Trade/index|Модуль 06: Foreign Trade]]
- [[../07-Category-Management/index|Модуль 07: Category Management]]
- Методология Education
