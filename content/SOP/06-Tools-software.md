---
aliases: 
updated: YYYY-MM-DD
tags: [education, sop, software, tools]
created: 2026-05-07
date created: 2026-05-07
date modified: 2026-05-13
---

# Платформы и софт для S&OP / IBP

> **TL;DR.** На enterprise-рынке доминируют 6 платформ: **Kinaxis** (леадер по Gartner MQ 2024), **SAP IBP**, **Oracle Cloud SCP**, **Anaplan**, **o9 Solutions**, **OMP**. Выбор зависит от уже стоящего ERP, зрелости процесса и size компании. Малому/среднему бизнесу часто достаточно Excel + dashboard в Power BI, до $100M+ выручки софт не критичен.

> **Главный принцип:** не покупай платформу, пока процесс не работает в Excel. Софт ускоряет хороший процесс и амплифицирует плохой.

<!-- IMG: Gartner Magic Quadrant Supply Chain Planning 2024 | https://www.anaplan.com/wp-content/uploads/2024/gartner-mq-scp-2024.png -->

## Gartner Magic Quadrant for Supply Chain Planning Solutions 2024

Расположение по квадрантам:

| Quadrant | Vendors |
|----------|---------|
| **Leaders** | Kinaxis (highest-ranked), Blue Yonder, RELEX |
| **Challengers** | SAP, Anaplan, OMP |
| **Visionaries** | o9 Solutions (downgrade с leaders 2023), ToolsGroup, Logility |
| **Niche** | Oracle (вырос), John Galt, Solvoyo |

> Гартнер каждый год пересортировывает позиции. Тренд 2024: переоценка o9 (был leader, стал visionary), рост leadership Kinaxis, Blue Yonder укрепляется после поглощения One Network.

## Краткое сравнение топ-6 платформ

### 1. Kinaxis Maestro / RapidResponse

**Профиль.** Канадский вендор, основан 1984. Главная фишка — **concurrent planning** (одновременная переплановка demand-supply-inventory без батчевых пробежек).

**Сила:**
- Самая быстрая re-planning технология на рынке (in-memory).
- Сильная scenario analysis.
- Хорош для сложных, высоко-волатильных supply chains (tech, automotive, pharma).
- Cisco, Unilever, Ford, Lockheed Martin — клиенты.

**Слабость:**
- Дорого.
- Steeper learning curve.
- Финансовая интеграция слабее, чем у Anaplan.

**Идеально для:** mid-to-large enterprise, complex global supply chain, нужна resilience и concurrent planning.

**Pricing (приблизительно):** от $200K/year на старт, миллионы для глобального deployment.

### 2. SAP Integrated Business Planning (IBP)

**Профиль.** SAP IBP — преемник SAP APO (deprecated). Cloud-native, на платформе SAP HANA. Глубоко интегрирован с SAP S/4HANA ERP.

**Сила:**
- Естественный выбор, если у вас SAP S/4HANA ERP.
- Очень глубокая функциональность (demand planning, S&OP, supply planning, inventory optimization, control tower).
- Ecosystem партнёров и консультантов огромный.
- Sound финансовая интеграция через SAP FI.

**Слабость:**
- Сложность внедрения и поддержки.
- Дорогие SAP-консультанты.
- Тяжело, если у вас не-SAP ERP.

**Идеально для:** крупные компании на SAP S/4HANA, которые хотят single-vendor stack.

### 3. Oracle Fusion Cloud Supply Chain Planning

**Профиль.** Часть Oracle SCM Cloud, тесно интегрирован с Oracle ERP/EPM Cloud.

**Сила:**
- Зрелый продукт после многолетней эволюции (Oracle купил множество SCP вендоров).
- Сильная intersection с финансами (Oracle EPM).
- AI/ML встроен.

**Слабость:**
- Не-Oracle компании редко выбирают.
- Пользовательский опыт не самый современный.

**Идеально для:** Oracle ERP shop'ы.

### 4. Anaplan

**Профиль.** Connected Planning platform — гибкий «Excel в облаке на стероидах». Не специализированный SCP, а universal modeling platform для S&OP, FP&A, sales planning, workforce.

**Сила:**
- Невероятная гибкость моделирования (бизнес-пользователи строят модели сами без IT).
- Сильнейшая финансовая интеграция (FP&A natural).
- Отличный для xP&A (extended planning) — связывает supply, finance, sales planning.
- Быстрое внедрение (3-9 мес).

**Слабость:**
- Не специализированный SCP — для оптимизации и concurrent planning слабее Kinaxis/SAP IBP.
- Производительность на big data — challenge.

**Идеально для:** компании, у которых сильная FP&A culture, или те, кто хочет S&OP + financial planning в одном месте.

### 5. o9 Solutions

**Профиль.** «Digital Brain» — relatively new (основан 2009), AI-first платформа. Унифицированный graph-based data model.

**Сила:**
- AI/ML built-in everywhere.
- End-to-end охват: demand, supply, finance, IBP.
- Современный UX.
- Быстрый рост клиентской базы (Walmart, Mondelez, Anheuser-Busch).

**Слабость:**
- Молодой вендор — меньше зрелости, выше риск изменений.
- Падение в Gartner MQ 2024 (с leader → visionary) — tracking watch.
- Pricing высокий.

**Идеально для:** компании, которые делают «greenfield» replatforming и хотят AI-first stack.

### 6. OMP (Plus One)

**Профиль.** Бельгийский вендор, очень специализированный на complex manufacturing (chemicals, paper, metals).

**Сила:**
- Глубокая экспертиза в process industries.
- Сильная оптимизация production scheduling.
- Сильная репутация в Европе.

**Слабость:**
- Niche player — не для всех индустрий.
- Меньше know-how в FMCG/retail.

**Идеально для:** chemicals, metals, paper, food processing — где сложный multi-stage manufacturing.

## Дополнительные категории — для специфических задач

### Demand sensing / short-term forecasting
- **ToolsGroup (включая Terra)** — лидер в demand sensing, P&G клиент.
- **John Galt Solutions** — Atlas Planning Suite, для mid-market.

### Mid-market / SMB
- **Logility** — давно на рынке, аффордабельный.
- **Solvoyo** — turkish vendor, AI-driven.
- **Streamline (GMDH)** — для SMB, retail/distribution focus.
- **Slimstock (Slim4)** — strong в Европе, inventory optimization focus.

### Cloud-native новички
- **NETSTOCK** — для SMB, очень доступный.
- **Anaplan** (см. выше) для гибридного S&OP/FP&A.
- **Pigment** — challenger, набирает обороты в FP&A+S&OP.

### Open source / DIY
- **Python ecosystem:** Prophet (Facebook), Nixtla, GluonTS — для статистики.
- **Power BI / Tableau + Excel** — реалистичный stack для $5-50M бизнеса.
- **Microsoft Dynamics 365 SCM** — если уже на Microsoft stack.

## Матрица выбора по стадии и размеру

| Стадия / размер | $0-10M | $10-100M | $100M-1B | $1B+ |
|-----------------|--------|----------|----------|------|
| **Stage 1 (React)** | Excel | Excel | ERP-native + Excel | not realistic |
| **Stage 2 (Anticipate)** | Excel + 1 dashboard | Power BI / Tableau + ERP | Mid-market SCP (Logility, John Galt) | Mid SCP или начало enterprise |
| **Stage 3 (Integrate)** | Power BI + специализированный модуль | Anaplan, Logility, Slim4 | Anaplan, SAP IBP, Kinaxis | Kinaxis, SAP IBP, o9 |
| **Stage 4 (Collaborate)** | редко достижимо | Anaplan / Kinaxis lite | Kinaxis, SAP IBP, o9 | Kinaxis, SAP IBP, o9 |
| **Stage 5 (Orchestrate)** | n/a | n/a | ToolsGroup + Kinaxis | Custom + AI/ML pipeline |

> **Вывод.** Beauty-бренд $5-30M ARR — Excel + Power BI + одна demand-planning надстройка (например, Slim4 или Streamline). Платформа за $200K в год не окупится.

## Что делает софт vs что не делает

### Софт ХОРОШО решает:
- Сбор и консолидация данных из ERP/CRM/WMS.
- Statistical forecasting и ML-модели.
- Scenario / what-if анализ.
- Visibility в реальном времени.
- Reporting и dashboards.
- Workflow и approval flows.

### Софт ПЛОХО решает:
- **Executive sponsorship.** Если CEO не приходит на review — никакой Kinaxis не поможет.
- **Cross-functional accountability.** Если sales не хотят отвечать за forecast accuracy — система не заставит.
- **Качество данных.** Garbage in, garbage out — Kinaxis тоже жрёт мусор и выдаёт мусор.
- **Process discipline.** Если нет cadence — софт превращается в репорт-инструмент.
- **Trade-off decisions.** Платформа покажет options, выбрать должны люди.

## Стек, который реально работает в SMB

Для компании размера $5-30M ARR (типовой SMB-сегмент с маркетплейсами) реалистичный стек на 2026 год:

| Слой | Инструмент | Назначение |
|------|-----------|------------|
| ERP / OMS | 1С / RetailCRM / iiko / Бизнес.Ру | мастер-данные, заказы, инвентарь |
| Маркетплейсы | сборщики типа Mpstats / Маяк | продажи Wildberries, Ozon |
| Хранилище | PostgreSQL / Google BigQuery (sandbox) | unified data warehouse |
| Statistical forecast | Python (Prophet/NeuralProphet) или Streamline | demand planning |
| Сценарии / S&OP-модели | Excel / Google Sheets / Power BI | constraint check, gap analysis |
| Dashboards | Power BI / Looker Studio | KPI monitoring (FA, inventory, OTIF) |
| Workflow | Notion / ClickUp + Telegram | meeting cadence, decision log |

**Cost:** $0-2k/мес. Полностью покрывает Stage 1-3 maturity.

Когда переходить на enterprise SCP — когда:
1. Excel-модели стали >50K строк и ломаются.
2. Forecast и план обновляются вручную >3 человека-дней в месяц.
3. Размер бизнеса >$50-100M, где даже малая ошибка стоит дороже лицензии.
4. Multi-region / multi-warehouse / multi-channel сложность даёт ROI.

## Глобальные тренды в S&OP-софте 2025-2026

1. **AI/ML — стандарт, а не differentiator.** Везде встроены transformer-модели и foundation models для forecast.
2. **Concurrent planning** — становится нормой (после Kinaxis), batch processing уходит.
3. **Digital twins** — моделирование supply chain в реальном времени.
4. **xP&A (extended planning & analysis)** — Anaplan, o9 двигают объединение S&OP + FP&A + sales planning в один процесс.
5. **Autonomous planning** — алгоритмическое принятие решений на низком уровне (replenishment), human-in-the-loop на высоком.
6. **Composable architecture** — vendors открывают API, хорошо интегрируются с best-of-breed.
7. **Ускорение time-to-value** — от 2-3 лет внедрения SAP APO до 6-12 месяцев на cloud SCP.

## Связанные заметки

- [[03-Best-practices-US|Best practices US]] — Gartner Maturity Model (по уровню зрелости — какой класс софта подходит)
- [[04-Cases|Cases]] — P&G использует ToolsGroup, Cisco/Unilever — Kinaxis
- [[07-Implementation-checklist|Чеклист внедрения]] — софт идёт после процесса
- [[index|S&OP Index]]

## Источники

- [SolutionsReview — 2024 Gartner MQ for SCP Solutions](https://solutionsreview.com/enterprise-resource-planning/whats-changed-2024-magic-quadrant-for-supply-chain-planning-solutions/)
- [Anaplan — 2024 Gartner MQ for SCP Solutions](https://www.anaplan.com/blog/2024-gartner-magic-quadrant-for-supply-chain-planning-solutions/)
- [Kinaxis — What is S&OP](https://www.kinaxis.com/en/sop)
- [Supply Chain Digital — Top SCP Vendors](https://supplychaindigital.com/supply-chain-risk-management/key-supply-chain-planning-vendors)
- [Involvation — End of SAP APO, what's next](https://articles.involvation.com/with-the-end-in-sight-for-sap-apo-whats-next)
- [Supply Chain Digital — Top 10 SC Analytics Software](https://supplychaindigital.com/technology/top-10-supply-chain-analytics-software)
- [o9 Solutions — IBP](https://o9solutions.com/solutions/integrated-business-planning)
- [Anaplan — S&OP Process Guide](https://www.anaplan.com/blog/sales-operations-planning-sop-guide/)
