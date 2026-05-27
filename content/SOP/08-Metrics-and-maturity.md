---
aliases: 
updated: YYYY-MM-DD
tags: [education, sop, metrics, maturity]
created: 2026-05-07
date created: 2026-05-07
date modified: 2026-05-13
---

# Метрики успеха и шкала зрелости S&OP

> **TL;DR.** S&OP «работает», когда улучшаются 4 группы метрик одновременно: forecast accuracy (растёт), customer service / OTIF (растёт), inventory turns (растёт), cash-to-cash cycle (сокращается). Если только одна — это локальный sub-optim. Зрелость измеряется по Gartner 5-stage модели или Oliver Wight Class A scorecard. Минимальный мониторинговый dashboard руководителя — 5-7 KPI.

## Базовый принцип: 4 группы метрик

S&OP должен влиять на **систему в целом**, а не один её угол. Если forecast accuracy выросла, но inventory тоже вырос — это не победа, это перемещение проблемы.

| Группа | Главный вопрос | Ключевые KPI |
|--------|----------------|---------------|
| **Demand** | Точно ли прогнозируем? | MAPE, WMAPE, Bias, Forecast Value Added |
| **Supply / Service** | Доставляем то, что обещали? | OTIF, Fill Rate, Perfect Order, Lead Time |
| **Inventory** | Эффективно ли используем кэш? | Inventory turns, DIO, E&O%, Inventory accuracy |
| **Financial / Strategic** | Зарабатываем ли больше? | Working capital, Cash-to-cash, Margin vs plan, ROIC |

К ним — **process health metrics:** S&OP attendance, decision velocity, plan stability.

## Demand-side metrics

### MAPE (Mean Absolute Percent Error)

$$
MAPE = \frac{1}{N} \sum_{i=1}^{N} \frac{|forecast_i - actual_i|}{actual_i} \times 100\%
$$

**Бенчмарк (US):**
- Stage 1: 30-50%+ MAPE — фактически прогноза нет.
- Stage 2: 20-30% MAPE — типичный SMB после первых циклов.
- Stage 3: 15-25% MAPE — Fortune 1000 average.
- Stage 4: 10-15% MAPE — top quartile.
- Stage 5: 5-10% MAPE — world-class (P&G, Coca-Cola с AI).

**Подводный камень:** MAPE плохо работает на low-volume SKU (деление на маленький actual даёт огромный %). Решение — переходить на **WMAPE** (взвешенный по объёму) для агрегатных KPI.

### WMAPE (Weighted MAPE)

$$
WMAPE = \frac{\sum |forecast_i - actual_i|}{\sum actual_i} \times 100\%
$$

Главный KPI крупных компаний. Не зависит от длинного хвоста low-volume SKU.

### Bias / MFE (Mean Forecast Error)

$$
Bias = \frac{1}{N} \sum (forecast_i - actual_i)
$$

Должен быть **близок к 0**. Если устойчиво положительный — мы систематически переоцениваем (перепроизводим). Если отрицательный — недооцениваем (out-of-stock).

**Bias > 5% устойчиво** — это organizational issue (sales занижают для перевыполнения, или маркетинг переоценивает promo lift).

### Forecast Value Added (FVA)

$$
FVA = \frac{Accuracy_{enhanced} - Accuracy_{naive}}{Accuracy_{naive}}
$$

Где naive — простой baseline (last month, prior year same period). Если FVA < 0 — вы добавляете шум, не ценность. Удивительно частая ситуация: «sales-corrected forecast» хуже, чем чисто статистический.

## Supply / Customer Service metrics

### OTIF (On-Time In-Full)

% заказов, доставленных и в срок, и в полном объёме.

**Бенчмарк (PwC):**
- World-class: 95%+
- Champion (top quartile): 90%+
- Average: 70-85%
- Below par: <70%

OTIF — **«gold standard»** customer service KPI. Обычно входит в SLA с retail партнёрами (Walmart, Costco штрафуют за низкий OTIF).

### Fill Rate

% строк заказа, выполненных полностью. Менее строгая метрика, чем OTIF (не учитывает «в срок»).

**Бенчмарк:** 95%+ для FMCG, 90%+ для tech, 85%+ для long-tail запчастей.

### Perfect Order

OTIF + правильная документация + без повреждений. Самая жёсткая метрика. Top performers: 70-85%.

### Lead Time variability

Стандартное отклонение фактического lead time. Чем меньше — тем легче планировать.

## Inventory metrics

### Inventory Turns

$$
Turns = \frac{COGS_{annual}}{Average\ Inventory}
$$

| Тип бизнеса | Хороший inventory turns |
|------------|-------------------------|
| Grocery / fresh FMCG | 15-25 |
| Beauty / personal care | 5-10 |
| Apparel | 4-8 |
| Tech / electronics (Apple) | 50-70 (extreme) |
| Industrial / запчасти long-tail | 2-5 |
| Pharma | 4-7 |

**Целевой принцип:** turns улучшаются при том же или растущем service level — это и есть signature правильно работающего S&OP.

### Days Inventory Outstanding (DIO)

$$
DIO = \frac{365}{Inventory\ Turns}
$$

То же самое в днях. 30-60 дней — типично, 90+ — потенциальная проблема.

### Excess & Obsolete (E&O) %

$$
E\&O = \frac{Inventory\ at\ risk\ of\ markdown/scrap}{Total\ Inventory}
$$

- < 5% — здоровый бизнес.
- 5-10% — повод задуматься.
- 10%+ — структурная проблема (плохой phase-out, плохой forecast, превышенные заказы).

### Inventory accuracy

% SKU, у которых системные остатки совпадают с физическими (по результатам циклической инвентаризации).

**Цель:** 98%+. Без этого forecast и planning — гадание.

## Financial / Strategic metrics

### Cash-to-Cash Cycle (C2C)

$$
C2C = DIO + DSO - DPO
$$

Где:
- DIO — Days Inventory Outstanding
- DSO — Days Sales Outstanding (дебиторка)
- DPO — Days Payables Outstanding (кредиторка)

**Бенчмарк:**
- Apple: ~ -15 дней (отрицательный — деньги поставщикам платят позже, чем получают от клиентов).
- Dell исторически: ~ -20 дней.
- FMCG average: 30-60 дней.
- Plain manufacturing: 60-90 дней.

**Сокращение C2C на 10 дней при $100M revenue освобождает ~$2.7M cash.** Это и есть прямой бизнес-кейс S&OP.

### Working Capital

$$
WC = AR + Inventory - AP
$$

Сжатие WC при том же росте — signature good S&OP.

### Margin vs Plan

Gross margin / EBITDA фактический vs S&OP-плановый. Если расходится >5% устойчиво — process broken.

### ROIC / EVA (для зрелого IBP)

Return on Invested Capital. На уровне Stage 4-5 IBP связывает операционные решения с creating value для shareholders.

## Process Health metrics (часто игнорируются)

| KPI | Как считать | Почему важно |
|-----|-------------|---------------|
| **S&OP attendance rate** | % executive присутствуют на review | Если CEO/COO пропускают — process is dying |
| **Decision velocity** | Дни от поднятия issue до решения | Если >30 дней — process не работает реально |
| **Plan stability (churn)** | % изменения плана от цикла к циклу на 3-мес horizon | High churn = поверхностная подготовка |
| **% of plan locked** | % near-term plan, который зафиксирован | Гигиена plan freeze |
| **Action item completion rate** | % action items выполнены к due date | Accountability indicator |

Эти метрики не про supply chain, а про **здоровье управленческого процесса**. Без них КПЭ supply могут улучшаться, а S&OP-процесс — деградировать.

## Минимальный dashboard руководителя (5-7 KPI)

Для еженедельного / ежемесячного мониторинга:

1. **WMAPE** (forecast accuracy) — главная демо-метрика.
2. **OTIF** — главная supply-метрика.
3. **Inventory Turns** — главная инвентарная метрика.
4. **C2C cycle** — главная финансовая метрика.
5. **Bias** — индикатор системного перекоса прогноза.
6. **E&O %** — индикатор «токсичного» инвентаря.
7. **S&OP attendance** — индикатор здоровья процесса.

Этого достаточно для управленческой картины 95% бизнесов.

<!-- IMG: пример S&OP KPI dashboard с 7 метриками | https://www.kinaxis.com/sites/default/files/sop-kpi-dashboard.png -->

## Шкала зрелости — где мы стоим?

### Gartner 5-stage Maturity Model (см. также [[03-Best-practices-US|Best practices US]])

| Stage | Outcome | Process | Org | Time | Tech | Где обычно |
|-------|---------|---------|-----|------|------|------------|
| **1. React** | Tushim fires | Informal | Нет S&OP role | <3 мес | Excel | SMB ранних стадий |
| **2. Anticipate** | Balance demand-supply | Formal monthly | Part-time S&OP leader | 3-12 мес | Excel + APS | SMB после 1-2 лет S&OP |
| **3. Integrate** | Optimize by segments | P&L involved | Full-time, central | до 18 мес | SCP suite | Большинство Fortune 500 |
| **4. Collaborate** | Single source of truth | Финансы integrated | IBP-структура | 18-24 мес | Advanced analytics, ML | Лидеры индустрий |
| **5. Orchestrate** | Resilience через AI | Algorithmic | Control tower | Real-time + 24+ мес | AI/ML, digital twin | P&G, Apple, Amazon |

### Oliver Wight Class A scoring

| Score | Status | Что означает |
|-------|--------|--------------|
| 4.5-5.0 | **Class A** | Excellence; eligible for OW certification |
| 3.5-4.5 | **Capable** | Хороший процесс, есть отдельные gaps |
| 2.5-3.5 | **In Transition** | На пути, многое нужно достроить |
| 1.5-2.5 | **Not Capable** | Процесс есть, но не работает как задумано |
| 0-1.5 | **No Process** | Запуск ещё не произошёл |

**Class A** — высокая планка. По миру несколько сотен сертифицированных компаний (P&G, Cisco, Heineken, многие Fortune 500). Но даже самооценка по чеклисту полезна для diagnostic.

## Целевые показатели по этапам внедрения

Для типичного SMB запускающего S&OP с нуля:

| Месяц цикла | WMAPE | OTIF | Inventory Turns | E&O % |
|-------------|-------|------|----------------|-------|
| Старт (baseline) | 35-40% | 70-80% | 3-4 | 10-15% |
| Месяц 6 | 25-30% | 80-85% | 4-5 | 7-10% |
| Месяц 12 | 20-25% | 85-90% | 5-6 | 5-7% |
| Месяц 24 | 15-20% | 90%+ | 6-8 | <5% |

> **Реалистичная амбиция: за 24 месяца внедрения качественного S&OP — улучшить все 4 метрики на 30-50%.** Это не теория, это бенчмарки McKinsey/Gartner для среднестатистических внедрений с executive sponsorship.

## Anti-patterns: KPI которые ВЫГЛЯДЯТ полезными, но врут

1. **«Перевыполнение плана продаж».** Это **anti-KPI** для S&OP — поощряет занижение forecast.
2. **Service level в одной точке.** «У нас OTIF 100% по топ-10 SKU» — а на остальных 90% портфеля 60%.
3. **Inventory $ value без сравнения с COGS / sales** — рост абсолютного inventory может быть просто следствием роста бизнеса.
4. **Forecast accuracy на агрегированном уровне.** На уровне «вся компания» легко получить 95%, но на SKU-level всё разваливается. Смотреть always по уровню гранулярности, на котором принимаются решения.
5. **Single-period KPI без trend.** Forecast accuracy 80% в одном месяце — может быть случайностью. Trend на 6-12 мес — реальный сигнал.

## Continuous Improvement — рутина

Каждый цикл S&OP должен включать:

1. **Forecast accuracy review** — что предсказывали, что получилось, причины отклонений (post-mortem).
2. **Decision review** — что решали в прошлом цикле, выполнено ли, как сработало.
3. **Process retrospective** — что в самом процессе можно улучшить (1-2 действия в цикл).

**Quarterly:** более глубокий retrospective с участием executive sponsor.

**Annually:** Maturity self-assessment (Gartner или OW), формирование improvement roadmap на следующий год.

## Связанные заметки

- [[03-Best-practices-US|Best practices US]] — Gartner Maturity Model в деталях
- [[04-Cases|Cases]] — какие KPI достигли лидеры
- [[07-Implementation-checklist|Чеклист внедрения]] — где KPI вписаны в roadmap
- [[index|S&OP Index]]

## Источники

- [ORI — Most common KPIs for S&OP](https://www.ori.io/ori-blog-posts/what-are-the-most-common-kpis-metrics-for-s-op-and-which-ones-really-matter)
- [Acterys — S&OP Metrics That Matter (CFO Guide)](https://acterys.com/blog/sales-and-operations-planning-metrics-and-kpis/)
- [Intuendi — Demand Planning KPIs](https://intuendi.com/resource-center/kpi-demand-planning/)
- [Imperia — Forecast Accuracy KPIs](https://imperiascm.com/blog/forecast-accuracy-connect-demand-forecasting-business-outcomes)
- [Demand-Planning blog — 8 KPIs Every Demand Planner Should Know](https://demand-planning.com/2020/06/01/8-kpis-every-demand-planner-should-know/)
- [Slimstock — S&OP KPIs](https://www.slimstock.com/blog/sop-kpis/)
- [Farseer — Forecast Accuracy KPIs](https://www.farseer.com/blog/4-demand-forecast-accuracy-kpis-youll-actually-use/)
- [LMA Consulting — 5 Key SIOP Metrics](https://www.lma-consultinggroup.com/siop-metrics-5-key-baseline-measurements/)
- [OneStream — KPIs for S&OP for Manufacturing Finance](https://www.onestream.com/blog/kpis-for-sales-and-operations-planning-for-manufacturing-finance/)
- [Elisa IndustriQ — Supply Chain KPIs that connect operations to profitability](https://www.elisaindustriq.com/resources/blog/supply-chain-kpis-that-connect-operations-to-profitability-clone)
- [Gartner — Five-Stage S&OP Maturity Model](https://www.gartner.com/en/documents/2587021)

<!-- IMG: KPI-pyramid: leading vs lagging indicators в S&OP | https://acterys.com/wp-content/uploads/sop-kpi-pyramid.png -->
