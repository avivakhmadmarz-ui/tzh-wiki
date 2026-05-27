---
aliases: 
updated: YYYY-MM-DD
tags: [education, okr-kpi, kpi, balanced-scorecard]
created: 2026-05-07
date created: 2026-05-07
date modified: 2026-05-13
---

# 04 — KPI и Balanced Scorecard

> «What you measure is what you get.»
> — Robert S. Kaplan & David P. Norton, HBR 1992

## Что такое KPI

**KPI (Key Performance Indicator)** — ключевой индикатор эффективности. Метрика, по которой постоянно мониторят здоровье бизнеса или процесса.

**Метрика** ≠ KPI.

| Метрика | KPI |
|---------|-----|
| Любое измеримое значение | Метрика, **связанная со стратегической целью** |
| Десятки/сотни | 5-15 на отдел |
| «Можно собрать» | «Должны мониторить, чтобы управлять» |
| Сырое число | Число с **target**, **threshold**, **owner** |

**Шаблон KPI (по британскому Cabinet Office):**
- **Name:** What we measure
- **Definition:** Formula
- **Owner:** Кто отвечает
- **Source:** Откуда данные
- **Target:** Целевое значение
- **Threshold (yellow / red):** Когда тревога
- **Frequency:** Daily / weekly / monthly / quarterly

## Leading vs Lagging indicators

Это **критическое различие**. Половина руководителей не понимают разницу — и поэтому управляют постфактум.

### Lagging indicator (запаздывающий)

Измеряет **результат** — что уже произошло.

- Revenue
- Profit margin
- Customer churn
- Employee turnover
- NPS (по сути уже состоявшаяся реакция)

**Проблема:** на момент измерения уже поздно что-то менять. Это «температура трупа».

### Leading indicator (опережающий)

Измеряет **input** — то, что **сейчас** влияет на будущий результат.

- Pipeline coverage (sales) → влияет на revenue через 1-2 квартала
- Customer health score → влияет на churn через 3-6 мес
- Onboarding completion rate → влияет на retention через 6 мес
- 1:1 frequency (manager to direct report) → влияет на attrition

**Преимущество:** на leading indicator **можно повлиять сейчас**. Это то, чем управляют.

### Правило здорового KPI-дашборда

> На каждый lagging — минимум один leading.
> Соотношение 50/50 или больше leading.

**Пример (e-commerce ритейл):**

| Lagging (что хотим) | Leading (на что влияем) |
|---------------------|--------------------------|
| Monthly revenue | Daily traffic, add-to-cart rate, checkout completion |
| Customer LTV | First-order value, repeat purchase 30/60/90 |
| NPS | Onboarding completion, time-to-first-value, support response time |
| Inventory turnover | Forecast accuracy, OTIF (см. [[../SOP/index\|S&OP]]) |

Amazon строит всю систему на **input metrics** — это их версия leading indicators. Подробнее в [[05-KPI-cases-and-pitfalls|05]].

## Balanced Scorecard — Kaplan & Norton (1992)

В январе-феврале 1992 года в **Harvard Business Review** вышла статья **"The Balanced Scorecard — Measures that Drive Performance"** Robert Kaplan (HBS) и David Norton. Это была реакция на проблему, которая мучила корпоративное управление в 1980-х:

> Компании оптимизируют **финансовые метрики** в ущерб всему остальному. Получают краткосрочный результат — теряют долгосрочный бизнес.

GE, Westinghouse, Xerox в 1980-х — классические примеры: ради квартального EPS жертвовали R&D, обучением, качеством. Через 5-10 лет — кризис.

Kaplan и Norton предложили: **«взвешивать» эффективность по 4 перспективам одновременно»**.

![[balanced-scorecard.png]]

### 4 перспективы

```
                          ┌─────────────────────┐
                          │   FINANCIAL          │
                          │ "How do we look      │
                          │  to shareholders?"   │
                          └──────────┬──────────┘
                                     │
        ┌────────────────────┬───────┴────────┬──────────────────┐
        │                    │                │                  │
┌───────▼──────────┐  ┌──────▼──────────┐  ┌──▼─────────────────────┐
│   CUSTOMER       │  │ INTERNAL         │  │ LEARNING & GROWTH    │
│ "How do          │  │ PROCESS          │  │ "Can we continue     │
│  customers       │  │ "What must we    │  │  to improve and      │
│  see us?"        │  │  excel at?"      │  │  create value?"      │
└──────────────────┘  └──────────────────┘  └──────────────────────┘
```

#### 1. Financial perspective

Классические финансовые метрики, выражающие интересы акционеров.

Примеры:
- Revenue growth %
- Operating margin %
- ROIC / ROCE
- Cash conversion cycle
- EBITDA

**Это lagging.** Финансы всегда отражают то, что уже произошло.

#### 2. Customer perspective

Как нас видит клиент. Без клиента нет финансов.

Примеры:
- Market share
- Customer satisfaction (CSAT, NPS)
- Customer retention rate
- New customer acquisition rate
- On-time delivery rate

**Mix lagging и leading.** Retention — lagging. Health score — leading.

#### 3. Internal Process perspective

В каких процессах мы должны быть лучшими, чтобы клиент был доволен и финансы были хорошими.

Примеры:
- Cycle time (time-to-market, lead time)
- Defect rate / quality (PPM defects, return rate)
- OTIF (on-time-in-full delivery rate)
- Process compliance %
- Inventory turnover

**В основном leading к customer и financial.**

#### 4. Learning & Growth perspective

Способность компании учиться и развиваться. Самая забываемая, самая важная для долгосрочной устойчивости.

Примеры:
- Employee engagement (Gallup Q12, eNPS)
- Voluntary attrition %
- Training hours per employee per year
- Time-to-productivity для новичков
- % revenue from products <2 years old (innovation rate)

**Это самые leading из всех.** Здоровая Learning & Growth дисциплина даёт результат через 2-5 лет.

### Балансировка

Главная идея — **смотреть все 4 одновременно**. CEO, который в Q1 показал +15% revenue (Financial), но 25% attrition (L&G) — **в красной зоне**, даже если первый KPI зелёный.

В реальном дашборде BSC обычно:
- 5-7 KPI в каждой перспективе → 20-25 KPI всего.
- На executive-уровне — 1 страница (10-15 топовых).
- Цветовая разметка red / yellow / green / blue (blue = превышение целей).

## Strategy Map (Kaplan-Norton, 1996)

Через 4 года после первой статьи Kaplan и Norton поняли, что 4 перспективы — это не просто четыре списка KPI. Между ними есть **причинно-следственные связи**:

```
                           FINANCIAL
                              ↑
             Revenue ←─── Customer satisfaction
                ↑              ↑
                └───── Internal Process ─────┐
                              ↑              │
                  Learning & Growth          │
                  (employees,                │
                  systems, culture)          │
```

Логика:
1. **Инвестируем в людей и системы** (L&G)
2. → **Улучшается качество процессов** (Internal Process)
3. → **Клиенты счастливее** (Customer)
4. → **Финансовые показатели растут** (Financial)

**Strategy Map** — это визуальная схема, на которой рисуют ~15-25 стратегических целей по перспективам и связи между ними. Это **карта бизнес-логики**.

<!-- IMG: Kaplan-Norton Strategy Map (canonical) | https://hbr.org/resources/images/article_assets/2007/05/R0707L_A_LG.gif -->

Пример (упрощённый, для beauty-импортёра):

```
FINANCIAL:        Revenue growth 25% YoY ── Operating margin >15%
                       ↑                          ↑
CUSTOMER:    Net retention 110% ──── Premium category share 40%
                       ↑                          ↑
INTERNAL:   OTIF >95%  ──  New product launches/yr ≥6  ── QC reject <0.5%
                       ↑                          ↑
L&G:         eNPS >40 ── Trained category managers 100% certified
```

Смотрим снизу вверх: чтобы вырастить **revenue**, надо **держать клиентов** (retention) и продавать **премиум** (share). Чтобы держать клиентов, нужны **бесперебойные поставки** (OTIF). Чтобы делать всё это устойчиво, нужны **обученные категорийщики** (L&G).

Это и есть Strategy Map. Каждая стрелка — гипотеза о причинно-следственной связи. KPI — числа, которыми эту гипотезу проверяешь.

## SMART(ER) framework для KPI и целей

Стандарт постановки целей с 1981 (George T. Doran, *Management Review*):

- **S — Specific.** Конкретная. Не «увеличить продажи», а «увеличить выручку премиум-категории в Москве».
- **M — Measurable.** Измеримая. Цифра + единица + точка отсчёта.
- **A — Achievable / Attainable.** Достижимая. Не «вырастем в 10 раз за месяц без бюджета».
- **R — Relevant.** Релевантная стратегии. Связана с тем, что важно.
- **T — Time-bound.** С дедлайном. «к 31 декабря 2026», не «когда-нибудь».

**SMARTER** добавляет:
- **E — Evaluated.** Регулярно пересматривается (каденс).
- **R — Reviewed / Re-adjusted.** Корректируется по ходу.

### SMART для KPI vs SMART для OKR

| | KPI | OKR Key Result |
|---|---|---|
| **S** Specific | Да | Да |
| **M** Measurable | Обязательно | Обязательно |
| **A** Achievable | Да, реалистично | **НЕТ — должно быть стрейч (60-70%)** |
| **R** Relevant | Да | Да |
| **T** Time-bound | Постоянная (continuous) | Квартальная |

Это и есть тонкое отличие: **KPI должен быть достижим (это план), OKR-KR должен быть некомфортно амбициозным (это стрейч)**. Подробно в [[06-OKR-vs-KPI-the-difference|06]].

## Где KPI чаще всего нужны

| Функция | Типичные KPI |
|---------|--------------|
| **Sales** | Pipeline coverage, win rate, ASP, sales cycle, quota attainment |
| **Marketing** | CAC, LTV/CAC, MQL→SQL conversion, attribution by channel |
| **Operations / Supply** | OTIF, inventory turnover, forecast accuracy, FIFO compliance |
| **Customer Success** | Net retention, gross retention, CSAT, NPS, time-to-resolve |
| **Product / Engineering** | DAU/MAU, feature adoption, time-to-first-value, defect escape rate |
| **Finance** | Cash burn, runway, DSO, gross margin, EBITDA |
| **HR / People** | eNPS, attrition (voluntary / regretted), time-to-hire, internal mobility |

## Антипаттерны KPI

(Подробно — в [[05-KPI-cases-and-pitfalls|05]], но коротко тут.)

1. **Vanity metrics.** Followers, downloads, page views — не привязаны к бизнес-результату.
2. **Слишком много KPI.** Если на дашборде >25 — никто не смотрит.
3. **Только lagging.** Управляешь по зеркалу заднего вида.
4. **KPI без owner.** «Все смотрят, никто не отвечает» = никто не отвечает.
5. **KPI как цель сама по себе.** Это **Goodhart's law** — раздел [[05-KPI-cases-and-pitfalls|05]].
6. **KPI без threshold.** «Revenue $50M» — это target. А что плохо? $48M? $30M? Нужны жёлтые/красные зоны.

## Связь с другими методологиями

- [[02-OKR-structure|OKR]] — комплементарны KPI: KPI следят за здоровьем, OKR двигают вперёд.
- [[../SOP/index|S&OP]] — даёт ритм для измерения KPI (monthly cycle).
- [[../Lean/index|Lean]] — Hoshin Kanri X-Matrix объединяет годовые цели и KPI.

## Что читать дальше

- [[05-KPI-cases-and-pitfalls|05 — Кейсы KPI и ловушки]] — Walmart, Amazon, GE, Wells Fargo, Goodhart's law.
- [[06-OKR-vs-KPI-the-difference|06 — OKR vs KPI]] — центральная заметка.
- [[index|OKR-KPI Index]]

## Источники

- [Kaplan & Norton, "The Balanced Scorecard" — HBR 1992 (PDF)](https://www.steinbeis-bi.de/images/artikel/hbr_1992.pdf)
- [Balanced Scorecard Institute — basics](https://balancedscorecard.org/bsc-basics-overview/)
- [HBS Online — What is a Balanced Scorecard](https://online.hbs.edu/blog/post/balanced-scorecard)
- [Conceptual Foundations of the BSC — HBS working paper](https://www.hbs.edu/ris/Publication%20Files/10-074_0bf3c151-f82b-4592-b885-cdde7f5d97a6.pdf)
- [Geckoboard — leading vs lagging](https://www.geckoboard.com/blog/leading-lagging-or-lost-how-to-find-the-right-key-performance-indicators-for-your-sales-team/)
- [Bernard Marr — leading and lagging indicators](https://bernardmarr.com/what-is-a-leading-and-a-lagging-indicator-and-why-you-need-to-understand-the-difference/)
- George T. Doran, "There's a S.M.A.R.T. Way to Write Management's Goals and Objectives" — *Management Review*, Nov 1981
- Robert S. Kaplan, David P. Norton, *The Balanced Scorecard: Translating Strategy into Action* (HBR Press, 1996)
- Kaplan, Norton, *Strategy Maps* (HBR Press, 2004)
