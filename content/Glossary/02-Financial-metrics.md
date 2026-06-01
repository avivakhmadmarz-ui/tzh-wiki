---
aliases: 
updated: 2026-05-13
tags: [education, glossary, financial]
created: 2026-05-07
date created: 2026-05-07
date modified: 2026-05-13
---

# Financial — финансовые метрики и термины

Алфавитный справочник финансовых терминов из корпоративной отчётности, бюджетирования и инвестиционного анализа. Те, что встречаются в [[../17-Goal-Setting/OKR-KPI/04-KPI-and-Balanced-Scorecard]], [[../14-Planning/Other-methodologies/06-ZBB-Zero-Based-Budgeting]] и кейсах.

## A

### AOP — Annual Operating Plan · годовой операционный план
Годовой бюджет компании, обычно утверждается осенью на следующий календарный год. Антипод [[../14-Planning/Other-methodologies/07-EOS-and-other|Beyond Budgeting]].

### ARR — Annual Recurring Revenue · годовая повторяющаяся выручка
Аннуализированная выручка от subscriptions / контрактов на обслуживание. Базовая метрика SaaS / B2B-софта.
**Не путать с MRR** (Monthly Recurring Revenue) × 12.

## C

### CapEx — Capital Expenditure · капитальные расходы
Расходы на основные средства (здания, оборудование, ПО лицензии long-term), амортизируются за несколько лет.
**Противоположно OpEx** (operating expense — расходы текущего периода).

### COGS — Cost of Goods Sold · себестоимость проданных товаров
Прямые затраты на производство/закупку проданных товаров. В ритейле = закупочная цена + логистика. В производстве = материалы + прямой труд + производственные накладные.
**Метрика:** Gross Margin = (Revenue − COGS) / Revenue.

### Contribution Margin · маржинальная прибыль
`Contribution Margin = Revenue − Variable Costs`
**Зачем:** сколько денег остаётся на покрытие fixed costs и формирование прибыли. Решения по продуктовому миксу принимают по contribution per constraint hour (Throughput Accounting в ToC).

## D

### D&A — Depreciation & Amortization · амортизация
- **Depreciation** — амортизация материальных активов (станки, здания)
- **Amortization** — амортизация нематериальных активов (бренды, лицензии, гудвилл)

**Зачем:** non-cash expense (бухгалтерская, не движение денег). Поэтому EBITDA «возвращает» её обратно при расчёте операционной прибыли.

### DCF — Discounted Cash Flow · дисконтированный денежный поток
Метод оценки актива/проекта/компании: будущие cash flows дисконтируются к сегодняшней стоимости через ставку дисконтирования (WACC).
`PV = Σ CF_t / (1+r)^t`

## E

### EBIT — Earnings Before Interest and Taxes · операционная прибыль
`EBIT = Revenue − COGS − OpEx (без процентов и налогов)`
Также называется Operating Income. Показывает прибыльность операций до структуры капитала.

### EBITDA — Earnings Before Interest, Taxes, Depreciation, and Amortization
`EBITDA = EBIT + D&A` или `EBITDA = Net Income + Interest + Taxes + D&A`
**Зачем:** прокси для operating cash flow. Сравнивать компании из разных стран (разная налоговая среда) и с разной капитализацией.
**Минусы:** Уоррен Баффет называет EBITDA «прибылью без расходов на оборудование» — компании capital-intensive (телеком, металлургия) могут выглядеть лучше, чем они есть.

### EPS — Earnings Per Share · прибыль на акцию
`EPS = Net Income / Weighted Average Shares Outstanding`
**Зачем:** ключевая метрика публичных компаний. Wall Street следит за «EPS beat» каждый квартал.
**Где:** [[../17-Goal-Setting/OKR-KPI/05-KPI-cases-and-pitfalls]] — гонка за EPS убила R&D в GE/Westinghouse в 1980-х.

## F

### FCF — Free Cash Flow · свободный денежный поток
`FCF = OCF − CapEx`
Деньги, которые остаются после поддержания бизнеса — можно платить дивиденды, выкупать акции, приобретать компании. **«Cash is king»** — в кризис смотрят на FCF, не на прибыль.

## G

### GMV — Gross Merchandise Value · валовая стоимость товаров
Общая сумма продаж через площадку (включая НДС, до возвратов и комиссий).
**Зачем:** базовая метрика маркетплейсов (Amazon, Wildberries, Ozon, Etsy).
**Не путать с выручкой** — компания может зарабатывать только комиссию (10-30% от GMV).

### Gross Margin · валовая маржа
`Gross Margin = (Revenue − COGS) / Revenue × 100%`
**Бенчмарк:** SaaS 70-90%, brand-FMCG 50-70%, ритейл 20-40%, distribution 10-20%, supermarkets 25-35%.

## I

### IRR — Internal Rate of Return · внутренняя норма доходности
Ставка дисконтирования, при которой NPV проекта = 0. Если IRR > WACC, проект создаёт стоимость.

## M

### Margin · маржа
Общий термин для % прибыли. Без уточнения может означать gross / operating / net / contribution. Уточняй.

## N

### Net Income · чистая прибыль
`Net Income = Revenue − COGS − OpEx − Interest − Taxes`
Финальная строка P&L. То, что достаётся акционерам.

### NPV — Net Present Value · чистая приведённая стоимость
`NPV = Σ CF_t / (1+r)^t − Initial Investment`
Если NPV > 0, проект создаёт стоимость; если < 0, теряет.

### NWC — Net Working Capital · чистый оборотный капитал
`NWC = Current Assets − Current Liabilities`
Или, в operations-смысле: `NWC ≈ AR + Inventory − AP`.
**Зачем:** сколько денег связано в операционном цикле. Снижение NWC = высвобождение кэша. S&OP/IBP проекты часто измеряются по NWC reduction.
**Где:** [[../14-Planning/SOP/04-Cases]] — кейсы P&G, Cisco, Unilever — все про NWC.

## O

### OCF — Operating Cash Flow · операционный денежный поток
Кэш, генерируемый основной деятельностью (после изменения working capital).
`OCF = Net Income + D&A + Δ NWC`

### OpEx — Operating Expenses · операционные расходы
Расходы текущего периода: зарплата, аренда, маркетинг, R&D. Списываются в P&L целиком.
**Противоположно CapEx**.

## P

### P&L — Profit and Loss statement · отчёт о прибылях и убытках
Один из трёх главных отчётов (P&L + Balance Sheet + Cash Flow Statement). Показывает доходы и расходы за период.

## R

### Revenue · выручка
Деньги от продажи товаров/услуг. Также называется sales (продажи), top line. Не путать с GMV (для маркетплейсов).

### ROA — Return on Assets · доходность активов
`ROA = Net Income / Total Assets × 100%`
**Зачем:** сколько прибыли генерирует каждый рубль активов.

### ROCE — Return on Capital Employed · доходность задействованного капитала
`ROCE = EBIT / (Total Assets − Current Liabilities)`
**Зачем:** альтернатива ROIC. Часто используется в UK / финансовых отчётах.

### ROE — Return on Equity · доходность капитала акционеров
`ROE = Net Income / Shareholders Equity × 100%`
**Зачем:** сколько прибыли генерируется на каждый рубль, вложенный акционерами. Дюпон-разложение: ROE = Net Margin × Asset Turnover × Financial Leverage.

### ROI — Return on Investment · окупаемость инвестиций
`ROI = (Gain − Cost) / Cost × 100%`
Простая метрика для проектов. Не учитывает время (для этого — IRR / NPV).

### ROIC — Return on Invested Capital · доходность инвестированного капитала
`ROIC = NOPAT / Invested Capital × 100%`
**Зачем:** ключевая метрика value creation. Если ROIC > WACC, компания создаёт стоимость; если ROIC < WACC, разрушает.
**Бенчмарк (Damodaran):** топ-25% public companies — ROIC > 15%; средний S&P 500 ~10%.

## S

### SG&A — Selling, General & Administrative Expenses · коммерческие, общие и административные расходы
OpEx за вычетом R&D и COGS — зарплата офисных сотрудников, маркетинг, юристы, аудит.
**Зачем:** в ZBB первая цель — снижение SG&A. ABInBev и Kraft Heinz сокращали SG&A на 30-40%.
**Где:** [[../14-Planning/Other-methodologies/06-ZBB-Zero-Based-Budgeting]]

## T

### TSR — Total Shareholder Return · общая доходность акционеров
`TSR = (Price End − Price Start + Dividends) / Price Start`
**Зачем:** мерило long-term performance компании на фондовом рынке. Включает price appreciation и dividends.

## W

### WACC — Weighted Average Cost of Capital · средневзвешенная стоимость капитала
`WACC = (E/V × Re) + (D/V × Rd × (1−Tc))`
- E/V — доля equity, D/V — доля debt
- Re — стоимость equity (CAPM), Rd — стоимость debt
- Tc — налоговая ставка

**Зачем:** ставка дисконтирования для NPV; «hurdle rate» для проектов. ROIC > WACC = компания создаёт стоимость.

### Working Capital · оборотный капитал
См. NWC.

## Z

### ZBB — Zero-Based Budgeting · бюджетирование с нуля
Бюджет верстается с нуля, а не от прошлого года + индексация.
**Где:** [[../14-Planning/Other-methodologies/06-ZBB-Zero-Based-Budgeting]]

## Связанные документы

- [[index|Glossary Index]]
- [[01-Operations-metrics|Operations & Supply Chain]]
- [[03-Customer-metrics|Customer & Growth]]
- [[04-Methodology-acronyms|Methodology Acronyms]]
- [[../17-Goal-Setting/OKR-KPI/04-KPI-and-Balanced-Scorecard|KPI и Balanced Scorecard]]
- [[../14-Planning/Other-methodologies/06-ZBB-Zero-Based-Budgeting|ZBB]]

## Источники

- [Investopedia — Financial Statements](https://www.investopedia.com/articles/04/031004.asp) — все базовые понятия
- [Aswath Damodaran — Stern NYU](https://pages.stern.nyu.edu/~adamodar/) — открытый учебник по корпоративным финансам
- [McKinsey — Valuation: Measuring and Managing the Value of Companies](https://www.mckinsey.com/capabilities/strategy-and-corporate-finance/our-insights/the-valuation-handbook) — стандарт корпоративных финансов
- [CFA Institute Glossary](https://www.cfainstitute.org/) — академический стандарт финансов
