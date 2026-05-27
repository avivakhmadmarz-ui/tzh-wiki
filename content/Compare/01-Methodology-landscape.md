---
aliases: 
updated: YYYY-MM-DD
tags: [education, compare, landscape]
created: 2026-05-07
date created: 2026-05-07
date modified: 2026-05-13
---

# Карта методологического ландшафта

Полная картина управленческих методологий, разложенная по двум главным осям: **что мы планируем** (домен) и **на каком горизонте**. Эта карта — компас, который позволяет понимать, где находится каждая методология относительно других, и какие «стыки» (gap-ы или overlap-ы) могут быть в управленческой системе компании.

> **TL;DR.** Не существует одной методологии «на всё». Любая зрелая система управления — это **стек из 3-5 методологий** на разных горизонтах и доменах. Цель этой заметки — визуализировать этот стек.

![[methodology-landscape.png]]

## Ось 1: Что планируем (домен)

| Домен                    | Методологии                                                                | Owner                     |
| ------------------------ | -------------------------------------------------------------------------- | ------------------------- |
| **Операции / поток**     | Lean (TPS), S&OP, IBP, MRP, DDMRP, ToC, Six Sigma                          | COO / Operations Director |
| **Цели / результаты**    | OKR, KPI, BSC, Hoshin Kanri, 4DX                                           | CEO + functional leaders  |
| **Финансы / бюджет**     | ZBB, Beyond Budgeting, Driver-Based Planning                               | CFO                       |
| **Стратегия / портфель** | BSC Strategy Map, Hoshin breakthrough, IBP PMR, Blue Ocean, Three Horizons | CEO + CSO                 |
| **Структура / роли**     | Holacracy, Spotify Model, Functional, Matrix, EOS People                   | CEO + HR                  |
| **Проекты**              | Critical Chain (CCPM), Agile (Scrum, Kanban), PMI/PMBOK, Stage-Gate        | PMO                       |
| **Качество**             | Six Sigma, TQM, ISO 9001, Hoshin (часть)                                   | Quality Director          |
| **People / OKR**         | OKR (cascade), Hoshin (catchball), Kanban for Work                         | HR + line managers        |

## Ось 2: Горизонт планирования

```
Дневное → Недельное → Месячное → Квартальное → Полугодовое → Годовое → 3-летнее → 5-10-летнее
```

### По шкале горизонта

| Горизонт | Методологии для оперирования | Cadence |
|----------|-------------------------------|---------|
| **День** | Daily management board (Lean), L10 readout (EOS), DBR-execution (ToC) | Утро / каждый день |
| **Неделя** | KPI scoreboard, L10 meetings (EOS), 4DX WIG sessions, sprint review (Agile) | 1×/нед |
| **Месяц** | S&OP, операционные KPI, monthly review | 1×/мес |
| **Квартал** | OKR-cycle, Rocks (EOS), QBR (quarterly business review), 4DX cadence | 1×/кварт |
| **Полугодие** | IBP financial reconciliation, Hoshin mid-year review | 2×/год |
| **Год** | Annual hoshin, IBP MBR, ZBB / Beyond Budgeting, Annual KPI, BSC perspectives | 1×/год |
| **3 года** | Hoshin breakthrough objectives, Strategy Map, IBP strategic horizon | каждые 1-3 года refresh |
| **5-10 лет** | Vision (EOS V/TO 10-year target), Long-term strategy, BHAG | refresh раз в 3-5 лет |

## Большая визуальная таблица: всё в одном

| Методология | Домен | Горизонт | Размер компании | Зрелость |
|-------------|-------|----------|-----------------|----------|
| **Daily Management** (Lean) | Операции | День | Любой | Базовая |
| **Kanban / Visual Mgmt** | Операции | День-неделя | Любой | Базовая |
| **Kaizen** | Операции | Любой | Любой | Базовая |
| **KPI Dashboard** | Цели/Метрики | Неделя-месяц | Любой | Базовая |
| **Six Sigma DMAIC** | Качество | Проект | Mid-large | Средняя-высокая |
| **MRP / MRP II / ERP** | Операции | Месяц-квартал | Mid-large | Средняя |
| **DDMRP** | Операции | Неделя-месяц | Любой с volatility | Средняя |
| **S&OP** | Операции | 18 мес | Mid-large | Средняя |
| **IBP** | Операции+Финансы+Стратегия | 24-36 мес | Large enterprise | Высокая |
| **Theory of Constraints** | Операции / Любой | Любой | Любой | Базовая (как линза) |
| **OKR** | Цели | Квартал-год | Любой | Средняя |
| **Balanced Scorecard** | Цели+Стратегия | Год+ | Mid-large | Средняя-высокая |
| **Hoshin Kanri** | Стратегия+Цели | 3-5 лет | Lean-зрелый mid-large | Высокая |
| **Strategy Map (Kaplan)** | Стратегия | 3-5 лет | Любой | Средняя |
| **EOS** | Operating system (целиком) | Год + квартал + неделя | SMB 50-250 | Базовая |
| **4DX** | Execution | Квартал-год + еженедельно | Любой | Средняя |
| **Holacracy** | Структура | n/a | Маленький, идейный | Высокая (cultural) |
| **ZBB** | Финансы | Год | Любой | Средняя |
| **Beyond Budgeting** | Финансы | Continuous | Mature, trust-culture | Очень высокая |
| **Agile / Scrum** | Проекты | Sprint (2 нед) | Tech / product | Средняя |
| **Critical Chain (CCPM)** | Проекты | Проект | Любой с проектами | Средняя |
| **Lean Six Sigma** | Качество+Поток | Проект-год | Mid-large | Высокая |

## Стек для разных типов организаций

### Стартап (5-30 человек)

```
└── OKR (квартал)
└── Базовый KPI dashboard (неделя)
└── Agile / Scrum (sprint)
└── Без ERP, без S&OP
```

### Scale-up (30-150 человек)

```
└── EOS или OKR + simplified S&OP
└── KPI dashboard (неделя)
└── Базовый MRP в NetSuite/1С/Dynamics BC
└── Lean basics (5S, daily management) — опционально
```

### Mid-market (150-1000 человек)

```
└── S&OP (месяц)
└── OKR (квартал) или Hoshin Kanri (если Lean-зрелый)
└── KPI / BSC scoreboard
└── ERP (Dynamics 365 F&O / SAP / Oracle / NetSuite)
└── Lean operations + Six Sigma для проектов
└── Опционально: DDMRP в нишевых SKU
```

### Enterprise (1000+ человек)

```
└── IBP (24-36 мес) → S&OP (18 мес)
└── Hoshin Kanri (3-5 лет) + BSC (стратегия)
└── OKR (опционально, для tech / product частей)
└── KPI dashboard + Daily management (везде)
└── ERP (S/4HANA / Oracle / Dynamics F&O) + IBP-platform
└── Lean Six Sigma (фабрика)
└── DDMRP в supply chain
└── ToC как cross-cutting линза
```

## Где обычно gap-ы (типичные ошибки)

### Gap 1: Стратегия → исполнение

**Симптом**: «У нас красивая стратегия в документе, но на земле никто не знает, что делать в понедельник».

**Решение**: Hoshin Kanri (если Lean-зрелый) или OKR + 4DX (если tech-style).

### Gap 2: Бюджет vs план

**Симптом**: «Бюджет утвердили в декабре, а в марте все цифры устарели».

**Решение**: IBP или Beyond Budgeting.

### Gap 3: KPI без действия

**Симптом**: «Дашборд красный, но никто не реагирует».

**Решение**: 4DX cadence of accountability + daily management (Lean).

### Gap 4: Forecast → reality

**Симптом**: «Forecast accuracy 50%, постоянный overstock или out-of-stock».

**Решение**: DDMRP вместо чистого MRP. Если зрелый — IBP.

### Gap 5: Локальная оптимизация без видения целого

**Симптом**: «Каждый отдел оптимизирует своё, общий поток страдает».

**Решение**: ToC (5 focusing steps) + S&OP cross-functional cadence.

### Gap 6: Слишком много KPI

**Симптом**: «Дашборд из 80 индикаторов, никто не знает что важно».

**Решение**: 4DX (1-2 WIGs) или OKR (3-5 Objectives).

### Gap 7: Бесконечное «BAU» без breakthrough

**Симптом**: «Год за годом одни и те же operational KPI, рост 2-3% или нулевой».

**Решение**: Hoshin breakthrough objectives. OKR-стретч-цели.

## Anti-patterns

### «Ванильное» внедрение

Покупка ZBB/IBP/EOS у консультантов без понимания контекста. Ритуалы есть, эффекта нет. Все методологии должны быть **adapted to context**.

### Method-stacking без интеграции

OKR + KPI + BSC + Hoshin одновременно, при этом неинтегрированно. Менеджеры тонут в meetings. Принцип: **выбрать ONE strategic system, ONE execution system, ONE operational system**.

### Tool > Process

Купить Anaplan / SAP IBP / OKR-software и считать, что внедрили методологию. Софт без процесса = красивая БД с устаревшими данными.

### Cargo cult

Копировать Toyota / Google / Spotify без понимания их культуры и контекста. Spotify сам публично сказал, что их «model» не работал даже у них. Toyota Way формировался десятилетиями.

## Связь с другими заметками

- Декомпозированный совет «что выбрать в МОЕЙ ситуации» — `[[02-Decision-matrix|Decision matrix]]`
- Какие методологии хорошо работают в комбинации — `[[03-Combinations-that-work|Combinations that work]]`
- Реальные сценарии для закупок / ритейла / beauty — `[[04-Cases-by-situation|Cases by situation]]`

## Источники

- [HBR — Strategy Execution](https://hbr.org/topic/strategy-execution)
- [Gartner — Five Stages of S&OP Maturity](https://www.gartner.com/en/documents/2587021)
- [McKinsey — Operations Insights](https://www.mckinsey.com/capabilities/operations/our-insights)
- [APICS / ASCM Body of Knowledge](https://www.ascm.org/learning-development/certifications-credentials/)
- [BSC Designer — Hoshin Kanri vs Balanced Scorecard](https://bscdesigner.com/hoshin-kanri.htm)
- [i-nexus — Hoshin vs 4DX vs MBO comparison](https://blog.i-nexus.com/hoshin-4dx-mbo-complementary-strategy-execution-tools)
- Mintzberg, H. (1994). _The Rise and Fall of Strategic Planning_. Free Press.
- Bossidy, L. & Charan, R. (2002). _Execution: The Discipline of Getting Things Done_. Crown Business.
