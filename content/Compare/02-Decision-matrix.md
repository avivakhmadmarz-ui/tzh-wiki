---
aliases: 
updated: YYYY-MM-DD
tags: [education, compare, decision-matrix]
created: 2026-05-07
date created: 2026-05-07
date modified: 2026-05-13
---

# Матрица выбора методологии — главная заметка раздела

Это **главная практическая заметка** программы обучения. Она отвечает на вопрос «что мне применять?» по четырём осям: **размер компании, тип бизнеса, стадия, цель руководителя**. На каждое пересечение — конкретный декомпозированный совет.

> **Как пользоваться.** Прочитай 4 секции (по размеру / типу / стадии / цели). На пересечении 4 секций ты получишь свой кластер методологий. В конце — синтезирующий блок «соберём в стек».

<!-- IMG: Decision tree «когда какую методологию выбрать» | https://example.com/methodology-decision-tree.png -->

## Ось 1: Размер компании

### Стартап (5-30 человек)

| Что делать | Методология |
|------------|-------------|
| Целеполагание | **OKR** (минимально, без software — в Notion / Google Doc) |
| Метрики | 5-10 базовых KPI (north-star + leading indicators) |
| Ритм | Weekly all-hands, monthly retro |
| Финансы | Driver-based forecast в Google Sheets, без полного бюджета |
| Операции | Manual processes, не пытайтесь Lean / S&OP |
| **НЕ делать** | IBP, ZBB, Hoshin, EOS, BSC, SAP — overkill |

**Книги для founder**: *The Lean Startup* (Eric Ries), *Measure What Matters* (John Doerr — про OKR), *Traction* — пока **не** надо.

### SMB / Scale-up (30-150 человек)

| Что делать       | Методология                                           |                               |
| ---------------- | ----------------------------------------------------- | ----------------------------- |
| Operating system | **EOS** (`[[../Other-methodologies/07-EOS-and-other   | EOS]]`) ИЛИ OKR + Lean basics |
| Метрики          | Weekly scorecard 10-15 KPI, по командам               |                               |
| Финансы          | Driver-based budget + monthly forecast update         |                               |
| Операции         | Базовый S&OP (упрощённый, монтлийный, 12 мес horizon) |                               |
| ERP              | Dynamics 365 BC, NetSuite, 1С:Предприятие             |                               |
| Стратегия        | Annual + quarterly plan; Strategy Map опционально     |                               |
| **НЕ делать**    | IBP, full Hoshin Kanri, ZBB, Six Sigma certification  |                               |

**Типичный контекст SMB-сегмента 50-150 человек**. Книги: *Traction* (Wickman), *Measure What Matters* (Doerr), *The Goal* (Goldratt).

### Mid-market (150-1000 человек)

| Что делать | Методология |
|------------|-------------|
| Operating system | OKR + KPI scoreboard + S&OP + Lean |
| Метрики | BSC (4 perspectives) + KPI cascade |
| Финансы | Driver-based + опционально ZBB на selectively chosen categories |
| Операции | Полный S&OP (`[[../SOP/index|S&OP]]`), MRP II в ERP, опционально DDMRP в импорте |
| ERP | Dynamics 365 F&O, SAP S/4HANA, Oracle Cloud ERP, Infor |
| Стратегия | Strategy Map + annual planning |
| Improvement | Lean Six Sigma project portfolio |
| Специальное | ToC как cross-cutting линза |

### Enterprise (1000+ человек, public или multi-BU)

| Что делать | Методология |
|------------|-------------|
| Operating system | **IBP** (`[[../Other-methodologies/01-IBP-Integrated-Business-Planning|IBP]]`) + S&OP + Lean Six Sigma |
| Метрики | BSC strategic + KPI operational + OKR (для product / tech parts) |
| Финансы | Driver-based + ZBB на трансформации, иногда Beyond Budgeting в BU |
| Стратегия | Hoshin Kanri (`[[../Other-methodologies/05-Hoshin-Kanri|Hoshin Kanri]]`) + Strategy Map |
| Операции | DDMRP в complex supply, MRP II в стандартном производстве |
| ERP | SAP S/4HANA, Oracle Cloud ERP, Microsoft Dynamics F&O |
| Improvement | Lean Six Sigma DMAIC portfolio, ToC linza |
| Project mgmt | CCPM (`[[../Other-methodologies/04-Theory-of-Constraints|ToC]]`) на critical projects |

## Ось 2: Тип бизнеса

### Производство (manufacturing)

**Стандартный стек**:
- Lean (TPS) + Six Sigma — операционное совершенство
- S&OP / IBP — планирование
- MRP II в ERP — execution
- ToC + DBR — синхронизация с bottleneck
- Hoshin Kanri — стратегия → daily management (если Lean-зрелый)

**Специфика**:
- Отраслевые ERP (Infor для дискретного, Aspen для process)
- TPM (Total Productive Maintenance) — обслуживание
- Lean accounting / Throughput accounting

### Ритейл / e-commerce

**Стандартный стек**:
- S&OP с фокусом на demand sensing — `[[../SOP/index|S&OP]]`
- ABC/XYZ classification SKU
- DDMRP для long-tail и волатильного спроса (`[[../Other-methodologies/03-DDMRP-Demand-Driven|DDMRP]]`)
- KPI: gross margin, sell-through, sales-per-square-foot, GMROI
- Category management как организационный принцип
- OKR для категорийных менеджеров

**Специфика**:
- Promo / sales planning отдельно от baseline
- Markdown management (особенно fashion, beauty)
- Vendor compliance / OTIF KPI
- Replenishment automation

**Типичные кейсы**: продуктовый retail — replenishment, OTIF поставщиков; категорийный мерчандайзинг.

### Дистрибуция / opt

**Стандартный стек**:
- S&OP / DDMRP (длинный lead time критичен)
- WMS + TMS (warehouse/transport management)
- ABC/XYZ + buffer management
- KPI: turnover, days of inventory, fill rate

### Услуги (B2B services)

**Стандартный стек**:
- OKR + KPI
- ToC + CCPM для проектной части (`[[../Other-methodologies/04-Theory-of-Constraints|CCPM]]`)
- Utilization / billable hours метрики
- Resource management как ключевой процесс

**НЕ нужно**: S&OP, MRP, Six Sigma manufacturing — overkill

### Tech / Product / SaaS

**Стандартный стек**:
- OKR (квартал) + Agile/Scrum/Kanban (sprint)
- DORA metrics для inженерии
- North Star Metric + supporting KPI
- Beyond Budgeting / rolling forecast
- 4DX как execution layer

**НЕ нужно**: S&OP, IBP, Lean Manufacturing, ZBB

### Beauty / Fashion / FMCG (твой текущий контекст)

**Стандартный стек**:
- S&OP с акцентом на demand sensing (промо, сезонность)
- DDMRP для long lead time импорта
- ABC/XYZ + dynamic safety stock / buffers
- Category management
- OKR на бренд / категорию
- KPI: sell-through, fresh vs aged inventory, markdown %

**Специфика**:
- Trend-driven, life cycle короткий
- Сезонность: 2-4 коллекции в год
- Маркетинг и промо влияют на спрос больше, чем стационарный baseline
- Вкус потребителя меняется → forecast accuracy всегда плохой

## Ось 3: Стадия компании

### Рост (быстрый scaling)

**Приоритеты**:
- **Process-as-you-grow**: внедрять методологии **по мере** роста, а не заранее
- 30 → 100 человек: EOS / OKR + базовый KPI
- 100 → 300 человек: добавить S&OP, BSC, Lean basics
- 300 → 1000 человек: full S&OP, Hoshin или OKR-cascade, ERP

**Что НЕ делать**: затратные трансформации (IBP, ZBB) — отвлечение от роста

### Оптимизация (стабильный бизнес, нужно повысить эффективность)

**Приоритеты**:
- **Lean Six Sigma** project portfolio — формальные DMAIC проекты
- **DDMRP** для inventory optimization (`[[../Other-methodologies/03-DDMRP-Demand-Driven|DDMRP]]`)
- **ToC** для bottleneck identification (`[[../Other-methodologies/04-Theory-of-Constraints|ToC]]`)
- **S&OP / IBP** maturity climb (Class B → A по Oliver Wight)
- **KPI sharpening** — фильтр от шума к 5-10 ключевых

### Трансформация (стратегический pivot, M&A, новые рынки)

**Приоритеты**:
- **Hoshin Kanri breakthrough** — формализовать pivot
- **OKR** для скорости адаптации
- **ZBB** на post-M&A integration (но не на innovation)
- **IBP strategic review** — ребаланс портфеля
- **Strategy Map** — визуализация новой стратегии для всей организации

### Кризис / санация

**Приоритеты**:
- **ZBB** на cost-out (`[[../Other-methodologies/06-ZBB-Zero-Based-Budgeting|ZBB]]`) — но осторожно, чтобы не разрушить ядро
- **ToC** для quick win по узким местам
- **Cash flow forecasting** weekly (не monthly!)
- **Inventory liquidation / DDMRP**, чтобы освободить кэш
- **Beyond Budgeting** — если есть culture readiness, после кризиса
- **Daily executive war room** (Lean military style)

**Не время для**: Hoshin Kanri (3-5 лет), долгие IBP-внедрения, Holacracy

## Ось 4: Цель руководителя

### Цель: Предсказуемость

«Хочу попадать в план на 90%+».

| Методология | Зачем |
|-------------|-------|
| **S&OP** | One-number plan, единый прогноз |
| **DDMRP** | Buffers поглощают вариативность |
| **Forecast accuracy KPI** | Измерить и улучшить |
| **MRP II discipline** | Master data + closed-loop |

### Цель: Эффективность (cost / margin)

«Хочу сократить cost / повысить margin».

| Методология                     | Зачем                            |
| ------------------------------- | -------------------------------- |
| **Lean**                        | Устранение муда                  |
| **Six Sigma**                   | Снижение вариативности дефектов  |
| **ToC + Throughput Accounting** | Right priorities for product mix |
| **ZBB** (выборочно)             | Cost-out на выбранных категориях |
| **DDMRP**                       | Меньше inventory at same service |

### Цель: Рост (revenue, market share)

«Хочу удвоить выручку за 3 года».

| Методология | Зачем |
|-------------|-------|
| **Hoshin breakthrough** или **OKR stretch** | Формальный breakthrough goal |
| **Strategy Map** | Логика, как рост случится |
| **IBP** | Балансирование инвестиций в рост |
| **Demand sensing в S&OP** | Не упустить пик спроса |
| **NPI process в IBP PMR** | Pipeline новых продуктов |

### Цель: Инновации

«Хочу запустить 5 новых продуктов / выйти в новые рынки».

| Методология                       | Зачем                              |
| --------------------------------- | ---------------------------------- |
| **Stage-Gate**                    | Дисциплина NPI                     |
| **Three Horizons (McKinsey)**     | Балансирование инноваций           |
| **OKR**                           | Quarterly tracking новых инициатив |
| **Beyond Budgeting**              | Гибкое выделение ресурсов          |
| **IBP Product Management Review** | Pipeline integration               |
| **Agile / Scrum**                 | Discovery + delivery               |

### Цель: Скорость / адаптивность

«Рынок меняется быстро, мы за ним не успеваем».

| Методология | Зачем |
|-------------|-------|
| **OKR** | Квартальная пересборка |
| **Agile / Scrum** | Sprint cadence |
| **Beyond Budgeting** | Rolling forecast vs annual freeze |
| **Demand sensing в S&OP** | Sub-monthly signal |
| **Lean Daily management** | Real-time issue resolution |
| **4DX** | Weekly accountability |

## Декомпозированные сценарии «начни с Y, потом добавь Z»

### «У меня beauty-импорт, 50 человек, я только начал управлять закупками»

**Сначала**:
1. **EOS-light** или OKR + weekly KPI scoreboard
2. **Базовый S&OP**: monthly meeting, 12-мес horizon
3. **ABC/XYZ classification** SKU
4. Простой driver-based bydget

**Через 6 мес**:
5. **DDMRP-pilot** на топ-20 SKU с длинным lead time
6. **5S + Daily management** на складе

**Через 12 мес**:
7. Full S&OP cycle Class B
8. Lean retail / category management practices

### «У меня 200-человечный ритейл, нужно повысить эффективность»

**Сначала**:
1. KPI sharpening — фильтр до 10 операционных метрик
2. ABC/XYZ + DDMRP на медленных SKU
3. ToC на cross-functional bottlenecks
4. S&OP cycle (если ещё нет)

**Через 6 мес**:
5. Lean Six Sigma project portfolio
6. Category management formalization
7. Vendor scorecard + OTIF tracking

**Через 12 мес**:
8. Hoshin Kanri или OKR cascade
9. BSC strategic dashboard

### «Я директор закупок в производстве, 8000 SKU»

**Сначала**:
1. ABC/XYZ — обязательно
2. Vendor segmentation (Kraljic matrix)
3. KPI: OTIF, vendor performance, inventory turns
4. MRP II discipline в ERP — clean BOM, accurate lead times

**Через 6 мес**:
5. DDMRP на B-class и C-class (где MRP плохо работает)
6. ToC на supply review в S&OP

**Через 12 мес**:
7. Strategic sourcing для A-class
8. Vendor development programs

### «Стартап, 25 человек, ищу operational discipline»

**Сначала**:
1. OKR (1-2 на квартал, 3 KR each)
2. Weekly all-hands with KPI scoreboard (north-star + 3-5 leading)
3. Monthly retro
4. Driver-based forecast в Sheets

**НЕ делать**: EOS целиком (overkill), S&OP (overkill), Hoshin (overkill)

**Через 6-12 мес**, при росте >50 человек:
5. Добавить EOS V/TO + Rocks
6. Базовый S&OP если есть физический продукт
7. Сильный financial controller

### «Mid-market 500 человек, готовлюсь к IPO»

**Сначала**:
1. **Hoshin Kanri** или OKR cascade
2. **BSC** для investor narrative
3. **IBP-light** (S&OP + financial reconciliation)
4. ERP audit + clean master data

**Через 6 мес**:
5. Full IBP внедрение
6. Driver-based budget + 24-мес rolling forecast

**Через 12 мес**:
7. Class A maturity (Oliver Wight)
8. Lean Six Sigma certified team

## Чеклист «прежде чем выбирать методологию»

- [ ] Я ясно понимаю **проблему**, которую хочу решить (не «давайте внедрим OKR», а «у нас execution gap»)
- [ ] Есть **CEO sponsor** или это моя ответственность как руководителя?
- [ ] Размер компании учтён (не overkill / underkill)
- [ ] Стадия учтена (не ZBB во время роста)
- [ ] Тип бизнеса учтён (не Six Sigma в SaaS)
- [ ] Готовность культуры (Beyond Budgeting / Holacracy требуют trust)
- [ ] Есть ресурс на 6-12 мес внедрения, не «решим на этой неделе»
- [ ] Меньше — лучше: 1 strategic + 1 execution + 1 operational методология максимум

## Связь с другими заметками

- Полная карта ландшафта — `[[01-Methodology-landscape|Methodology landscape]]`
- Какие комбинации работают — `[[03-Combinations-that-work|Combinations that work]]`
- Реальные кейсы для закупок / ритейла / beauty — `[[04-Cases-by-situation|Cases by situation]]`

## Источники

- [HBR — Strategy Execution archive](https://hbr.org/topic/strategy-execution)
- [McKinsey — Operations Insights](https://www.mckinsey.com/capabilities/operations/our-insights)
- [Gartner — Maturity Models](https://www.gartner.com/en/research/methodologies)
- [Bain — Operating model design](https://www.bain.com/insights/topics/operating-model/)
- [BCG — Operations](https://www.bcg.com/capabilities/operations/overview)
- Bossidy, L., Charan, R. (2002). _Execution_. Crown Business.
- Mankins, M., Steele, R. (2005). «Turning Great Strategy into Great Performance» — _HBR_, July 2005.
- Doerr, J. (2018). _Measure What Matters_. Portfolio.
- Wickman, G. (2011). _Traction_. BenBella Books.
- Goldratt, E. (1984). _The Goal_. North River Press.
