---
aliases: 
updated: 2026-05-13
tags: [education, compare, cases]
created: 2026-05-07
date created: 2026-05-07
date modified: 2026-05-18
---

# Кейсы по ситуациям — практическое применение методологий

Пять типичных сценариев из мира операционного управления: ритейл, запчасти long-tail, beauty-импорт, SMB с операционной дисциплиной. Каждый кейс — конкретная ситуация → ландшафт методологий → стек → KPI → последовательность действий.

> **Зачем эта заметка.** Декомпозиция от абстрактного («какую методологию выбрать») к конкретному («что я завтра иду делать в офисе»). Каждый кейс — рабочий шаблон, который можно адаптировать под свою задачу.

<!-- IMG: Категорийный менеджер дашборд (KPI assortment) | https://example.com/category-manager-kpi.png -->

---

## Кейс 1. Категорийный менеджер в ритейле

### Контекст

Сеть ~50-200 магазинов non-food (например, drugstore, hard goods, специализированный ритейл). Управление категорией: 200-2000 SKU, 20-100 поставщиков. Цели — gross margin, sell-through, оборачиваемость, доля на полке.

### Симптомы боли (типичные)

- Часть SKU stock-out, часть aged inventory >120 дней
- OTIF поставщиков не отслеживается
- Промо проходят с низкой эффективностью (дискаунт без uplift)
- Forecast accuracy 40-50%
- Категорийный менеджер тонет в Excel

### Стек методологий

| Слой | Метод | Что даёт |
|------|-------|----------|
| Стратегия категории | **Category Strategy + BSC** (4 perspectives, customer + financial) | Roadmap категории |
| Тактическое планирование | **S&OP** (`[[../14-Planning/SOP/index|S&OP]]`) | Ежемесячный demand+supply consensus |
| Классификация | **ABC / XYZ** | Приоритизация управленческого внимания |
| Replenishment | **DDMRP** (`[[../14-Planning/Other-methodologies/03-DDMRP-Demand-Driven|DDMRP]]`) для долгого lead time + B/C-class; MRP для A-class | Pull для волатильных, push для стабильных |
| Складская операция | **Lean** (5S, daily management, kanban для replenishment) | Скорость, точность |
| Цели команды | **OKR** (`[[../17-Goal-Setting/OKR-KPI/index|OKR]]`) на квартал + **KPI** дашборд | Drive улучшения + контроль здоровья |

### Ключевые KPI

| KPI | Цель | Cadence |
|-----|------|---------|
| Gross margin % | По категории | Ежемесячно |
| Sell-through % | По SKU/группе | Еженедельно |
| Inventory days / turns | Days of supply | Еженедельно |
| Forecast accuracy (MAPE) | <30% по топ-ABC | Ежемесячно |
| OTIF поставщиков | >95% | Ежемесячно |
| Aged inventory % | <10% от total | Еженедельно |
| GMROI | >150% | Ежемесячно |
| Promo uplift / lift | >100% (прирост от base) | По акции |

### План внедрения (12 мес)

**Месяцы 1-3**:
- ABC/XYZ classification
- Vendor scorecard (OTIF, lead time, complaints)
- Базовый KPI dashboard в Power BI / Excel

**Месяцы 4-6**:
- Запуск ежемесячного S&OP cycle
- Promo planning template
- Aged inventory action plan

**Месяцы 7-9**:
- DDMRP pilot на B/C-class SKU с длинным lead time
- 5S и daily management на складе
- OKR на квартал

**Месяцы 10-12**:
- Расширение DDMRP
- Category strategy по BSC
- Lean Six Sigma project на самом болезненном процессе

### Типичный контекст применения

Каноничный сценарий для категорийного менеджера в продуктовом или non-food ритейле. Excel-репорты по обороту, частичный demand sensing — то, что часто есть «в зачатке», но без формального S&OP. DDMRP сильно помогает на medium-velocity SKU.

---

## Кейс 2. Импорт товаров с длинным lead time из Китая

### Контекст

Beauty / fashion / electronics / hard goods, импорт из Китая. Lead time 60-90-120 дней (производство + море + растаможка). Контейнеры, MOQ, валютные риски, регуляторные риски.

### Симптомы боли

- Forecast на 90 дней — accuracy 30-40%
- Перезакупки на сезонные позиции
- Stock-out на бестселлерах в пик
- 30-50% оборотного капитала «лежит в море»
- Reactive expediting (air freight emergency) выжигает margin

### Стек методологий

| Слой | Метод | Что даёт |
|------|-------|----------|
| Стратегическое позиционирование | **DDMRP strategic decoupling points** | Где держать «firewall» против variability |
| Buffer management | **DDMRP red/yellow/green zones** | Динамическая alternative к safety stock |
| Demand sensing | **S&OP demand review** + statistical baseline | Лучше forecast |
| Promo / NPI integration | **Planned adjustments в DDMRP buffers** | Подготовиться к промо |
| Vendor mgmt | **Vendor scorecard + Kraljic matrix** | Дифференцированная стратегия по поставщикам |
| Cash flow | **Throughput accounting** (`[[../14-Planning/Other-methodologies/04-Theory-of-Constraints|ToC]]`) | Приоритеты по cash impact |
| Cross-functional | **Базовый S&OP** | Закупки + маркетинг + финансы |

### Ключевые KPI

| KPI | Цель |
|-----|------|
| In-stock rate (на бестселлерах) | >97% |
| Days of inventory on hand | По velocity tier |
| Air freight ratio | <5% от total freight cost |
| Forecast accuracy (3-мес horizon) | MAPE <35% |
| Buffer breach rate (DDMRP red zone hits) | <10% buffer-month |
| Vendor OTIF | >90% |
| Working capital в товаре | По financial target |

### План внедрения (6 мес pilot, 12 мес расширение)

**Месяцы 1-2**:
- Identify decoupling points в цепочке (workshop с supply chain + finance + sales)
- ABC/XYZ classification по venders + SKU
- Considera ADU и DLT для топ-50 SKU

**Месяцы 3-4**:
- Параметризация буферов (red/yellow/green)
- Visual dashboard (Power BI или специализированный, как Intuiflow / Slim4)
- Запуск daily Net Flow review

**Месяцы 5-6**:
- Динамические корректировки buffers под промо
- Связка с monthly S&OP

**Месяцы 7-12**:
- Расширение на 100% portfolio импортных SKU
- Integration с ERP (1С / Dynamics / SAP)
- Vendor development — сокращение lead time с 90 до 60 дней

### Применимость

Beauty-импорт из Китая — каноничный DDMRP-кейс. Coca-Cola Beverages Africa, Michelin, Unilever Mexico — все начинали с похожих симптомов.

**Quick win** без полноценного DDMRP — начать с двух вещей:
1. ABC/XYZ топ-100 SKU
2. Заменить flat safety stock на buffer-style (red/yellow/green) хотя бы вручную в Excel

Это даст immediate visibility и foundation для дальнейшего внедрения.

---

## Кейс 3. Закупки с long-tail (8 000+ SKU)

### Контекст

Производственный или дистрибутивный бизнес с **очень длинным tail**: 8 000-50 000 SKU, разная velocity (от тысяч единиц/мес до 1 единицы/год). Запчасти, MRO, B2B distribution, industrial.

### Симптомы боли

- Невозможно forecast'ить каждый SKU
- Большая часть movement — slow movers
- Inventory огромный, oboroachivaemost низкая
- Spec changes, инженерные изменения постоянны
- Поставщиков сотни, разный уровень service

### Стек методологий

| Слой | Метод | Что даёт |
|------|-------|----------|
| Сегментация | **ABC** (по value), **XYZ** (по variability), **9-cell matrix** | Кто заслуживает внимания |
| A-class (топ 20% SKU = 80% value) | **MRP II + active forecast + S&OP** | Tight control |
| B-class | **DDMRP buffer management** | Pull-based replenishment |
| C-class (long tail) | **(s, S) policy / min-max + alerting** | Автоматизация без ручного forecast |
| Vendor segmentation | **Kraljic matrix** (strategic / leverage / bottleneck / non-critical) | Дифференцированный подход |
| Strategic vendors | **Long-term contracts + collaborative forecasting** | Lead time reduction |
| Bottleneck vendors | **Multi-sourcing development** | Risk mitigation |
| KPI | **Vendor scorecard + supply review** | Performance management |
| Цели команды | **OKR на категорию + KPI каскад** | Performance tracking |

### Ключевые KPI

| KPI | Цель |
|-----|------|
| OTIF поставщиков | >90% (target 95%+) |
| Lead time variability | Снижение year-over-year |
| Inventory turns | По tier (A=12, B=6, C=2) |
| Stock-out rate (A-class) | <2% |
| Excess / obsolete inventory % | <5% |
| Vendor compliance (specs, docs) | >98% |
| Cost reduction year-over-year | 2-5% |
| Number of vendors per category | Снижение (consolidation) |

### План внедрения

**Месяцы 1-3**:
- ABC/XYZ classification
- Kraljic matrix для vendors
- Master data cleanup в ERP

**Месяцы 4-6**:
- A-class — формальный S&OP demand+supply review
- Vendor scorecard launch
- Базовая обзор OTIF

**Месяцы 7-12**:
- B-class — DDMRP buffers
- C-class — автоматизированный (s, S)
- Strategic sourcing для top vendors

**Год 2**:
- Vendor development programs (lead time reduction)
- Lean Six Sigma на receiving / inspection processes
- Возможно — IBP layer над S&OP

### Применимость

Long-tail SKU + многие поставщики — каноничная задача дистрибуционного и B2B-бизнеса (автозапчасти, MRO, industrial). ABC/XYZ + Kraljic + DDMRP для B/C — основа методологического стека.

---

## Кейс 4. Beauty-импорт с сезонностью

### Контекст

Импорт beauty-продуктов из Китая / Кореи / Европы. **Высокая сезонность**: косметика для маникюра → пик к Новому году и Дню Матери; маникюрная техника → меньшая сезонность. Trend-driven (что в Instagram сегодня — продаётся завтра). 50-200 человек в команде, 1000-5000 SKU.

### Симптомы боли

- Forecast accuracy 30-40% (даже на топ-SKU)
- Сезонные колебания: пик 3х от base, провал 0.5х
- Trend-driven: новый цвет от инфлюенсера → 10x спрос за 2 недели → невозможно успеть
- Lead time 60-90 дней не совпадает с горизонтом trend (4-8 недель)
- Маркетинг и закупки не разговаривают

### Стек методологий

| Слой | Метод | Что даёт |
|------|-------|----------|
| Cross-functional planning | **S&OP с акцентом на demand sensing** | Маркетинг + закупки + финансы синхронизированы |
| Demand sensing | **Promotional / trend module в S&OP** + базовый AI/ML forecast | Раннее обнаружение трендов |
| Inventory management | **DDMRP с dynamic buffer adjustments** | Buffers adapt to seasonality |
| Сезонные SKU | **Seasonal buffers + planned adjustments** | Готовность к пику |
| Trend SKU | **Short lead time альтернатива** (Air freight на trend, sea freight на base) | Скорость реакции |
| Категорийная стратегия | **OKR на категорию (бренд / линию)** | Бренд-целеполагание |
| Структура | **EOS-light** или **OKR + L10** | Operating discipline для 50-200 человек |
| Финансы | **Driver-based forecast** | Лучше cash management |

### Ключевые KPI

| KPI | Цель |
|-----|------|
| In-stock rate на топ-100 SKU | >95% |
| Sell-through по новинкам | По target |
| Aged inventory % | <10% |
| Forecast accuracy на topsellers | MAPE <30% |
| Promo uplift achievement | >80% от target |
| Time-from-trend-detection-to-product-launch | По target tier |
| Working capital в inventory | По target |
| OKR completion rate | 70%+ (стретч) |

### План внедрения

**Месяцы 1-3**:
- Базовый S&OP cycle (monthly demand + supply review)
- ABC/XYZ + sezonality flagging
- KPI dashboard еженедельный

**Месяцы 4-6**:
- DDMRP pilot на топ-100 SKU
- Vendor segmentation (с акцентом на дифференциацию по responsiveness)
- OKR cascade (бренд / категория / индивидуал)

**Месяцы 7-12**:
- Расширение DDMRP, dynamic adjustments
- Trend detection process (соц.сети → buying decision → fast-track procurement)
- Collaborative forecasting с маркетингом
- Lean на складе (5S, daily management)

**Месяцы 12+**:
- Возможно — IBP-light (если выросли > 500 человек)
- AI/ML demand sensing
- Vendor development для lead time reduction

### Применимость

Главный совет: **не пытаться внедрить всё сразу**. S&OP cadence + ABC/XYZ + базовый KPI dashboard как foundation на 6-12 месяцев. Дальше — DDMRP для buffers (особенно сезонные), OKR для команды.

---

## Кейс 5. Малый бизнес 50 человек — EOS vs полный S&OP

### Контекст

SMB / family-business / scale-up. 50 человек. Distribution, services, или базовый retail. Founder в роли CEO. Был хаос, нужна operating discipline.

### Два альтернативных пути

#### Путь A: EOS

| Слой | Что |
|------|-----|
| Vision | V/TO 2 страницы |
| People | Right people in right seats (RPRS-tool) |
| Data | Scorecard 5-15 KPI weekly |
| Issues | IDS в L10 |
| Process | 6-10 core processes documented |
| Traction | Quarterly Rocks + L10 weekly |

**Ритуал**: L10 еженедельно (90 минут), quarterly Rocks планирование, annual planning session.

**Преимущества**: cheap, fast, книжный шаблон.

**Ограничения**: не для tech / product (нет sprint cadence), не для complex supply chain (нет S&OP).

#### Путь B: OKR + базовый S&OP

| Слой | Что |
|------|-----|
| Стратегия | Annual + quarterly OKR |
| Метрики | KPI dashboard weekly |
| Операции | Monthly S&OP-light: demand review, supply review, financial check |
| Ритуал | Weekly all-hands + KPI; monthly S&OP; quarterly OKR review |

**Преимущества**: подходит для tech-friendly culture; гибче, чем EOS; готовит к росту >150 человек.

**Ограничения**: меньше готовых шаблонов; требует self-direction.

#### Какой путь выбрать?

| Признак | EOS | OKR + S&OP |
|---------|-----|-----------|
| Founder любит ритуалы | Да | Нет |
| Бизнес — services / distribution / традиционный retail | EOS | EOS или OKR |
| Бизнес — tech / product / SaaS | НЕТ | OKR |
| Длинный supply chain | EOS + S&OP | OKR + S&OP |
| Готовы инвестировать в EOS Implementer | EOS быстрее | — |
| Команда self-directed | OKR | OKR |
| Хаос, нужны жёсткие ритуалы | EOS | — |

### Что НЕ делать в SMB 50 человек

- Полный S&OP class A
- IBP
- Hoshin Kanri
- BSC с 4 perspectives и 30 KPI
- Holacracy
- Six Sigma certification

Эти инструменты — для зрелых mid-large компаний. В SMB они отвлекают.

### Ключевые KPI (любой путь)

| KPI | Cadence |
|-----|---------|
| Revenue / month | Месячно |
| Gross margin % | Месячно |
| Cash position / runway | Еженедельно |
| Customer NPS / retention | Месячно |
| Employee NPS / retention | Квартально |
| OKR / Rock completion rate | Квартально |
| Forecast accuracy (если применимо) | Месячно |

### План внедрения

**Месяцы 1-3**:
- Выбор пути (EOS or OKR + S&OP)
- Vision / Annual plan
- KPI dashboard
- Weekly rhythm

**Месяцы 4-6**:
- Quarterly Rocks или OKR
- Process documentation (топ-5 critical processes)
- People review (RPRS)

**Месяцы 7-12**:
- Annual planning (real, не шаблон)
- Возможно — добавить S&OP-light если physical product
- Lean basics на складе / в производстве

---

## Сводная таблица всех кейсов

| Кейс | Базовый стек | KPI приоритет | Quick win |
|------|--------------|---------------|-----------|
| 1. Категорийный менеджер | ABC/XYZ + S&OP + KPI | Gross margin, sell-through, OTIF | Vendor scorecard |
| 2. Импорт длинный lead time | DDMRP + S&OP + Throughput accounting | In-stock rate, days of inventory, air freight % | ABC/XYZ + buffer pilot |
| 3. 8000 SKU закупки | ABC/XYZ + MRP II + DDMRP + Kraljic + OKR | OTIF, turns by tier, stock-out (A-class) | ABC/XYZ + Kraljic |
| 4. Beauty с сезонностью | S&OP + DDMRP + OKR + EOS-light | In-stock на топ-100, sell-through новинок, MAPE | Monthly S&OP + ABC/XYZ |
| 5. SMB 50 человек | EOS или OKR + S&OP-light | Revenue, gross margin, cash, OKR completion | Weekly rhythm + KPI dashboard |

## Связь с другими заметками

- Карта ландшафта — `[[01-Methodology-landscape|Methodology landscape]]`
- Decision matrix — `[[02-Decision-matrix|Decision matrix]]`
- Комбинации, которые работают — `[[03-Combinations-that-work|Combinations that work]]`

## Источники

- [APICS / ASCM — CSCP body of knowledge](https://www.ascm.org/learning-development/certifications-credentials/cscp/)
- [Demand Driven Institute — Case studies](https://www.demanddriveninstitute.com/case-studies)
- [Inventory Planner — Seasonal demand](https://www.inventory-planner.com/seasonal-inventory/)
- [Toolio — Demand Forecasting in Retail](https://www.toolio.com/post/demand-forecasting-in-retail-methods-tools-and-tips)
- [Clarkston Consulting — Managing Seasonal Demand](https://clarkstonconsulting.com/insights/managing-seasonal-demand-in-retail/)
- [Lokad — ABC XYZ analysis](https://www.lokad.com/abc-xyz-analysis-inventory/)
- [ASCM — XYZs of Inventory Management](https://www.ascm.org/ascm-insights/the-xyzs-of-inventory-management/)
- Kraljic, P. (1983). «Purchasing Must Become Supply Management» — _Harvard Business Review_, Sept-Oct 1983.
- Wickman, G. (2011). _Traction_. BenBella.
- Doerr, J. (2018). _Measure What Matters_. Portfolio.
- Goldratt, E. (2009). _Isn't It Obvious?_ — про ритейл (NA Publishing).
