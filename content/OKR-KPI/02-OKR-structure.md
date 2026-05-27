---
aliases: 
updated: YYYY-MM-DD
tags: [education, okr-kpi, structure]
created: 2026-05-07
date created: 2026-05-07
date modified: 2026-05-13
---

# 02 — Структура OKR: Objective + Key Results

> «An Objective is *what* is to be achieved, no more and no less. Key Results benchmark and monitor *how* we get to the objective.»
> — John Doerr, *Measure What Matters*

OKR состоит из двух частей. Жёстко. Ничего лишнего.

```
OBJECTIVE  → качественное, амбициозное, вдохновляющее (1 строка)
  ├── KEY RESULT 1 → количественный, измеримый, с дедлайном
  ├── KEY RESULT 2 → ...
  ├── KEY RESULT 3 → ...
  ├── KEY RESULT 4 → (опционально)
  └── KEY RESULT 5 → (опционально, обычно последний)
```

![[okr-pyramid.png]]

## Objective — «куда идём»

**Что это.** Качественная, амбициозная, эмоционально цепляющая формулировка. Описывает **направление**, не число.

**Правила.**
- 1 предложение, в идеале до 10 слов.
- Глагол + прилагательное + существительное («Become the dominant 16-bit microprocessor family»).
- Не должен содержать чисел (числа — в KR).
- Должен звучать так, чтобы команда хотела его рассказать друзьям. Если «не стыдно повторить вслух — это не Objective».
- Не должен быть про deliverable («Запустить продукт X») — должен быть про **исход** («Сделать X любимым продуктом наших пользователей»).

**Хорошие примеры.**
- «Establish the 8086 as the highest-performance 16-bit microprocessor family» (Intel, 1980).
- «Crush Motorola» (внутренний слоган того же Operation Crush — слишком короткий для канонического Objective, но зато сразу мобилизует).
- «Make Chrome the dominant browser by 2010» (Google, 2008).
- «Delight customers in our top 10 markets» (Airbnb).

**Плохие примеры.**
- «Increase revenue by 20%» — это число, это KR, не Objective.
- «Launch new pricing model» — deliverable, не outcome.
- «Be more efficient» — нет конкретики, нельзя проверить.

## Key Results — «как поймём, что дошли»

**Что это.** Количественные, измеримые показатели, которые в конце квартала имеют однозначный ответ: достигнуты или нет.

**Правила.**
- 3-5 KR на один Objective. Не больше. Если 7, ты не сфокусирован.
- Каждый KR содержит число и дату.
- KR — это **outcome**, не **activity**. «Опубликовать 5 бенчмарков» — activity. «Получить top-1 в трёх независимых benchmark-обзорах» — outcome.
- Шаблон Гроува: *«[Метрика] from [X] to [Y] by [Date]»*.
- Если можно достичь KR, не достигнув Objective — KR неправильный.

**Test для KR (test by Doerr):**
- Specific?
- Time-bound?
- Aggressive yet realistic?
- Measurable & verifiable?

**Хорошие примеры (под Objective Intel выше):**
- Develop and publish 5 benchmarks showing superior 8086 performance by June 1.
- Win 2,000 design wins by end of Q4 1980.
- Get the 8MHz part into production by July 15.
- Sample arithmetic coprocessor by June 15.

**Плохие примеры.**
- «Hire a sales team» — не число, не дата, не outcome.
- «Improve user experience» — без метрики ничего не значит.
- «Be #1 in the market» — без определения «#1 как меряем» это не KR.

## Грейдинг 0.0-1.0 — Google-стандарт

В конце квартала каждый KR оценивается числом от 0.0 до 1.0:

| Грейд | Что значит |
|-------|------------|
| **0.0** | Никакого прогресса |
| **0.3** | Минимальный прогресс, на грани провала |
| **0.5** | Прогресс есть, но цель не достигнута |
| **0.6-0.7** | **Sweet spot — здоровый stretch** |
| **0.8-0.9** | Цель достигнута, но это значит, что цель была недостаточно амбициозной |
| **1.0** | Полная победа — но в Google это **подозрительно** |

**Почему 0.6-0.7 — это «правильно»:**

> «If you got 100%, you didn't set the bar high enough. We want our targets to be just out of reach — uncomfortable.»
> — Larry Page

Если команда регулярно делает 1.0, в следующем квартале планку поднимают. Если регулярно делает <0.3, команда теряет мотивацию — снижают.

<!-- IMG: Google OKR grading scale 0.0-1.0 | https://rework.withgoogle.com/static/images/okr-grading.png -->

## Committed vs Aspirational OKRs (Google split)

Google ввёл важное разделение, которое спасает команды от выгорания:

### Committed OKRs (обязательства)
- Должны быть выполнены **на 100%** к дедлайну.
- Связаны с операционкой: SLA, безопасность, релизы, compliance.
- Грейд <1.0 = провал, требует root cause analysis.
- Пример: «Поддерживать аптайм Search 99.99% в Q3» — это **обязательство**, не амбиция.

### Aspirational / Stretch OKRs (амбиции)
- Достижение 0.6-0.7 — успех. 1.0 — выдающийся результат.
- Связаны с ростом, инновациями, новыми рынками.
- В команде должна быть **хотя бы одна** aspirational OKR в квартал.
- Пример: «Достичь 100M DAU Chrome к концу 2010» (был аспиршн, оказалось — стретч в 1.6x от плана).

**Соотношение в команде.** Google рекомендует ~50/50 или 60/40 (committed/aspirational), в зависимости от стадии бизнеса. У зрелых операций больше committed; у растущих продуктов больше aspirational.

**Худшая ошибка:** пометить committed как aspirational (тогда команда расслабляется и не выполняет SLA) или наоборот (тогда команда не ставит амбициозных целей).

## Каденс: company → team → individual

OKR существуют на трёх уровнях:

```
COMPANY OKR (CEO + leadership team) — на год + квартал
   │
   ├── TEAM OKR (head of department) — квартал
   │      │
   │      └── INDIVIDUAL OKR (контрибьютор) — квартал [опционально]
   │
   └── ...
```

**Важно:** это **не строгий каскад**, при котором KR-команды становится Objective-индивида. Это **alignment** — индивид сам пишет свои OKR, но они должны явно поддерживать команду или компанию (linkage, не trickle-down).

Подробно про каскадирование vs alignment — в [[07-Implementation-for-leader|07 — Внедрение]].

## Quarterly + Annual

Большинство компаний используют двойной горизонт:

| Цикл          | Кто ставит      | Что ставит                                                       |
| ------------- | --------------- | ---------------------------------------------------------------- |
| **Annual**    | Leadership team | 3-5 company-level Objectives на год — стратегические направления |
| **Quarterly** | Все уровни      | 3-5 OKR каждый квартал, поддерживающих annual + текущий контекст |

Annual OKR пересматривают раз в год (но мониторят прогресс ежеквартально). Quarterly — каждые 3 месяца с retrospective.

Christina Wodtke в [[index|Radical Focus]] вводит ритуалы:

- **Понедельник, 30 мин:** Monday Commitments — что сделаем эту неделю для KR.
- **Пятница, 30 мин:** Friday Wins — что получилось, демо, празднование.
- **Каждые 6 недель:** mid-quarter review — confidence check (1-10), корректировки.
- **Конец квартала:** retrospective + grading + установка следующих OKR.

**Без каденса OKR не работает.** Это самая частая причина провала внедрения. Подробно в [[07-Implementation-for-leader|07]].

## Сколько OKR на единицу

| Уровень | Objectives | Key Results на каждый |
|---------|-----------|----------------------|
| Company | 3-5 | 3-5 |
| Team | 2-3 | 3-5 |
| Individual | 1-3 | 3-5 |

**Главное:** **меньше — лучше**. Гроув: «If everything is a priority, nothing is.» Если у команды 8 Objectives, фокус нулевой.

## Anti-pattern: «KPI с бантиком»

Самая частая ошибка пост-MBO компаний — **превратить старые KPI в OKR, переписав форматирование**.

Было:
```
KPI: Revenue $50M в квартал
KPI: Customer churn <5%
KPI: NPS >40
```

Стало (имитация OKR):
```
Objective: Hit our financial targets
KR1: Revenue = $50M
KR2: Churn = 5%
KR3: NPS = 40
```

Это **не OKR**. Это переименованные KPI. Тут нет stretch, нет качественного Objective, нет амбиции. Это просто план.

**Настоящий OKR:**
```
Objective: Become the must-have product for SMB CFOs in EU
KR1: Increase paid SMB customers from 1,200 to 2,500 by Q4
KR2: Move EU revenue share from 18% to 30% of total
KR3: Achieve net retention 115%+ on EU SMB cohort
```

Здесь Objective задаёт **направление и амбицию**, KR измеряют **исход**, а revenue $50M превратился из «KPI-цели» в «индикатор здоровья», который остаётся в [[04-KPI-and-Balanced-Scorecard|KPI-дашборде]].

## Что читать дальше

- [[03-OKR-cases|03 — Кейсы OKR]] — как это работало в Intel, Google, LinkedIn.
- [[06-OKR-vs-KPI-the-difference|06 — OKR vs KPI]] — почему KR ≠ KPI.
- [[07-Implementation-for-leader|07 — Внедрение]] — как запустить.
- [[index|OKR-KPI Index]]

## Источники

- [Google re:Work — Set goals with OKRs](https://rework.withgoogle.com/intl/en/guides/set-goals-with-okrs)
- [What Matters — Google OKR Playbook](https://www.whatmatters.com/resources/google-okr-playbook)
- [How Google sets goals with OKRs — Weekdone](https://blog.weekdone.com/how-google-sets-goals-with-okrs-objectives-and-key-results/)
- [Committed vs Aspirational OKRs — whatmatters.com](https://www.whatmatters.com/faqs/committed-aspirational-okrs)
- John Doerr, *Measure What Matters* (Portfolio, 2018), chapters 1-4
- Andy Grove, *High Output Management* (1983), ch. 6
- Christina Wodtke, *Radical Focus* 2nd ed. (2021)
