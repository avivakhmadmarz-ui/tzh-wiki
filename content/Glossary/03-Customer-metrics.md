---
aliases: 
updated: 2026-05-13
tags: [education, glossary, customer]
created: 2026-05-07
date created: 2026-05-07
date modified: 2026-05-13
---

# Customer & Growth — клиентские, продуктовые и growth-метрики

Метрики, которые встречаются в Customer perspective Balanced Scorecard, в OKR продуктовых и маркетинговых команд, в e-commerce и SaaS.

## A

### AOV — Average Order Value · средний чек
`AOV = Revenue / Number of orders`
**Зачем:** базовая метрика ритейла и e-commerce.
**См. также:** [[01-Operations-metrics|Operations]] глоссарий.

### ARPU — Average Revenue Per User · средняя выручка на пользователя
`ARPU = Revenue / Number of users`
**Зачем:** SaaS, telecom, mobile games. Можно считать ARPU monthly (ARPMU) или ARPU per active user (ARPDAU).

## C

### CAC — Customer Acquisition Cost · стоимость привлечения клиента
`CAC = Sales & Marketing Spend / New Customers Acquired`
**Зачем:** базовая unit-economics. CAC vs LTV — главный экзамен на здоровый бизнес.

### CES — Customer Effort Score · оценка усилий клиента
«Насколько легко вам было решить вашу проблему?» (шкала 1-7).
**Зачем:** альтернатива NPS, особенно для customer support / B2B. Дикхард-фанаты CES (CEB / Gartner) утверждают, что снижение усилий лояльнее, чем wow-эффект.

### Churn — отток · % потери клиентов
`Churn rate = Customers lost / Customers at start of period × 100%`
**Виды:**
- **Customer churn** — % клиентов, ушедших за период
- **Revenue churn** — % выручки, потерянной (с учётом downsells)
- **Net revenue retention (NRR)** — обратная метрика: 100% + upsells − churn − downsells

**Бенчмарк SaaS:** SMB ~3-5% monthly, enterprise 0.5-1% monthly. Высокий churn убивает CAC unit-economics.

### Conversion Rate · конверсия
`Conversion = Number of conversions / Number of visitors × 100%`
**Где:** на каждом шаге воронки. E-commerce средняя конверсия в покупку 2-3%, лучшие 5-10%.

### Cohort Analysis · когортный анализ
Группируем клиентов по дате первой покупки/регистрации и смотрим их retention/revenue с течением времени. Стандарт продуктовой аналитики и SaaS.

### CSAT — Customer Satisfaction Score · удовлетворённость клиента
«Насколько вы довольны?» (шкала 1-5 или 1-10). % выбравших top-2 box.
**Зачем:** post-transaction (после звонка в support, после покупки). Не путать с NPS (тот меряет общее отношение).

### CTR — Click-Through Rate · кликабельность
`CTR = Clicks / Impressions × 100%`
Реклама, email, поиск.

## D

### DAU — Daily Active Users · ежедневные активные пользователи
Количество уникальных пользователей в день.

### DAU/MAU ratio · stickiness
`DAU/MAU = «коэффициент липкости»`. % monthly активных, которые заходят каждый день.
**Бенчмарк:** Facebook ~65%, Twitter ~50%, TikTok ~40%. Для большинства продуктов 20% = очень хорошо, 10% = норма.

## L

### LTV — Lifetime Value · пожизненная ценность клиента
`LTV = ARPU × Gross Margin × (1 / Churn rate)`
Или для контракт-driven: `LTV = Σ Cash Flow from customer over their lifetime`.

**Главное правило unit-economics:** `LTV / CAC > 3` — здоровый бизнес. <1 — теряете деньги на каждом клиенте. 1-3 — выживаете, не растёте.

### Loyalty Programs метрики
- **Enrollment rate** — % покупателей, ставших участниками программы
- **Active member rate** — % активных в программе
- **Member lift** — насколько чаще покупают участники vs не-участники

## M

### MAU — Monthly Active Users · ежемесячные активные пользователи
Уникальные пользователи за 30 дней.
**Зачем:** базовая метрика social / consumer apps. Но MAU не показывает stickiness и engagement.

### Market Share · доля рынка
`Market Share = Company Sales / Total Market Sales × 100%`
**Бенчмарк:** №1 на рынке = 25%+ обычно. Apple в smartphones ~17% global, в US ~55%.

## N

### NPS — Net Promoter Score · индекс лояльности
«Какова вероятность, что вы порекомендуете нас другу/коллеге?» (шкала 0-10).
- **Promoters** (9-10) — лояльные
- **Passives** (7-8) — нейтральные
- **Detractors** (0-6) — критики

`NPS = % Promoters − % Detractors` (от −100 до +100)

**Бенчмарк:** Apple ~70, Tesla 90+, Costco 80, средний US business ~30, плохо < 0.
**Минусы:** одна цифра без контекста ничего не значит. Тренд во времени важнее абсолютного значения.

### NRR — Net Revenue Retention · чистая выручка-удержание
См. Churn. NRR > 100% = бизнес растёт даже без новых клиентов (топ SaaS — 120-130%).

## R

### Repeat Rate · повторные покупки
`Repeat rate = % customers with 2+ purchases`
**Бенчмарк ритейла:** beauty / fashion 30-40%, FMCG 60-80%, мебель 10-15%.

### Retention · удержание (антипод churn)
`Retention = Customers retained / Customers at start of period`
- **Logo retention** (B2B SaaS) — % компаний, которые остались
- **Revenue retention** — % выручки, которая осталась
- **Net retention** — с учётом upsells

## S

### Sell-through · скорость распродажи
См. [[01-Operations-metrics|Operations]] глоссарий — это скорее operations-метрика, но в beauty/fashion ритейле она и про клиента (что покупают).

### Stickiness
См. DAU/MAU ratio.

## T

### Time to Value (TTV) · время до первой ценности
Как быстро новый клиент получает первую пользу от продукта. Критично для onboarding в SaaS.
**Бенчмарк:** Slack <1 day, Zoom <10 minutes, complex CRM 30-90 days.

## Связанные документы

- [[index|Glossary Index]]
- [[01-Operations-metrics|Operations & Supply Chain]]
- [[02-Financial-metrics|Financial]]
- [[../OKR-KPI/04-KPI-and-Balanced-Scorecard|Customer perspective в BSC]]

## Источники

- [Reforge](https://www.reforge.com/) — engagement / retention frameworks
- [First Round Review](https://review.firstround.com/) — продуктовые / growth метрики
- [Lenny's Newsletter](https://www.lennysnewsletter.com/) — growth и продукт
- [Clayton Christensen — Jobs to be Done](https://www.christenseninstitute.org/jobs-to-be-done/) — альтернативный взгляд на сегментацию клиентов
- [Net Promoter System (NPS) — Bain](https://www.netpromotersystem.com/) — оригинальная методология NPS
