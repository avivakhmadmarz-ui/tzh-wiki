---
title: "07 — Внедрение OKR и KPI для руководителя"
module: OKR-KPI
aliases: 
tags: [education, okr-kpi, implementation, leader]
type: note
status: active
domain: education
created: 2026-05-07
updated: 2026-06-01
---

# 07 — Внедрение OKR и KPI для руководителя

> «The biggest reason OKR implementations fail is that leaders treat them as an HR exercise.»
> — Christina Wodtke, *Radical Focus*

Эта заметка — **прикладная**. Если предыдущие отвечали «что» и «почему», эта отвечает на «как».

## С чего начать (первые 90 дней)

### Месяц 1 — diagnostic + foundation

**Цель:** не запустить OKR, а **понять, что сейчас вообще есть в компании**.

#### Шаг 1. Inventory текущих целей и метрик

- Собрать всё, что сейчас называется «целями» или «KPI» в команде.
- Положить в одну таблицу: что именно, кто owner, как часто смотрят, влияет ли на бонус.
- Разделить по столбцам: это KPI (health), это OKR-кандидат (change), это task list (delete).

Как правило, в этом моменте обнаруживается:
- 20-50 «KPI», из которых реально смотрят 3-5.
- «Цели на год», написанные год назад, никем не вспоминаемые.
- Куча task lists, замаскированных под цели.

#### Шаг 2. Сформулировать Annual направление

- 3-5 верхнеуровневых направлений на год (это будут annual OKR).
- Не больше. Если 7 — нет фокуса.
- Каждое направление — на 1 предложение. Качественно. Без чисел (числа в KR).

#### Шаг 3. Определить KPI-дашборд

- 10-15 KPI в 4 перспективах (Financial / Customer / Internal Process / Learning & Growth).
- Каждый KPI: name, definition (формула), owner, source (откуда берётся), target, yellow/red threshold, frequency.
- Положить в одно место — Sheets, Notion, Tableau, Looker — не важно. Главное: **в одном месте, видно всем**.

### Месяц 2 — pilot first quarter OKR

**Не стоит запускать сразу на всю компанию.** Ошибка №1.

#### Шаг 4. Pilot на одной команде

- Выбрать одну команду. Лучше — непосредственную (управленческую) команду руководителя.
- Поставить 3 OKR на этот квартал (нужен фокус для пилота, а не 5).
- Ввести cadence: Monday-commit, Friday-wins.
- Сделать OKR public — все видят, что команда работает.

#### Шаг 5. Communicate, communicate, communicate

- На all-hands: «Мы пилотируем OKR. Это про фокус, а не оценка performance.»
- Объяснить committed vs aspirational. Объяснить 0.6-0.7 sweet spot.
- Объяснить, что **бонусы не привязаны** (если не привязаны — повторить трижды).

### Месяц 3 — first retrospective

#### Шаг 6. Конец квартала

- Каждый KR оценивается 0.0-1.0 публично.
- **Что сработало? Что нет? Почему?**
- Что переносится в следующий квартал, что отбрасывается.
- Корректировка формата: возможно, в данной культуре Friday-celebration не зашёл, а Tuesday-standup лучше работает.

#### Шаг 7. Расширение

- Q+1 — добавить 1-2 команды.
- Q+2 — ещё 2-3.
- Q+3 — компания целиком.

**Не стоит торопиться.** Adobe внедрял Check-in **2 года**. Spotify шлифовал свой подход **5+ лет**. Дедлайна на «всё внедрено за квартал» **нет**.

## Top-down vs bottom-up — баланс

### Anti-pattern: pure cascade

Старая ошибка из MBO-эпохи:
1. CEO формулирует company OKR.
2. KR1 CEO становится Objective head-of-department.
3. KR1 head-of-department становится Objective team lead.
4. KR1 team lead становится Objective contributor.

**Это не работает.** Получается «trickle-down translation», где смысл к низу теряется, а индивид не чувствует владения.

### Right pattern: alignment, not cascade

Google и LinkedIn делают так:

1. **CEO/leadership** формулируют 3-5 company OKR.
2. **Каждая команда** **сама** пишет свои 2-3 team OKR. Они **не должны буквально** повторять company KR. Они должны **поддерживать** company OKR — и это становится отдельным критерием review.
3. **Контрибьюторы** сами пишут свои individual OKR (если эта практика есть в компании). Тоже с linkage к team.
4. На каждом уровне **половина** OKR должна приходить **снизу** (bottom-up) — это правило Google.

**Linkage ≠ duplication.** Это связь «как наш OKR support вышестоящий», а не «наш OKR = нижестоящий KR».

### Caнdour up, support down

Принцип Andy Grove: **«candor up, support down»**. Когда команда пишет OKR, она **открыто говорит руководителю**: вот тут мы не уверены, вот тут нам не хватает ресурсов. Руководитель **поддерживает** (помогает с ресурсами), но не **переписывает** OKR.

Если каждый OKR команды правится менеджером сверху — у команды нет владения, motivation падает.

## Cadence-ритуалы — без них всё мертво

### Weekly

**Monday Commit (30 минут).**
- Каждый член команды: «Что я сделаю на этой неделе для движения KR».
- Confidence check 1-10 на каждый KR (как уверены, что выполним к концу квартала).
- Identification аномалий: «KR2 confidence упал с 8 до 5 — почему?»

**Friday Wins / Demo (30 минут).**
- Что получилось.
- Демо чего-то конкретного.
- Празднование маленьких побед.

Christina Wodtke в *Radical Focus* настаивает: **именно эта пара ритуалов — magic ingredient**. Они дают ритм. Без них OKR превращаются в «set-and-forget» — главный анти-паттерн.

### Mid-quarter

**6 weeks in: confidence review (1 hour).**
- Каждая команда показывает progress per KR.
- Корректировки: что отбросить, что усилить.
- Re-allocation ресурсов.

### End-of-quarter

**Retrospective + grading (2-3 hours).**
- Каждый KR — grade 0.0-1.0.
- Lessons learned: что мешало, что помогло.
- Установка OKR на следующий квартал.

### Annual

**Annual review (1 day).**
- Annual OKR — закрытие.
- Установка annual OKR на следующий год.
- Корректировка KPI-дашборда (если стратегия изменилась).

<!-- IMG: Christina Wodtke Monday-Friday cadence | https://cwodtke.com/wp-content/uploads/cadence.png -->

## Топ-10 ошибок при внедрении

### 1. Set and forget

OKR ставят в начале квартала и не вспоминают до конца. К концу квартала — всё забыли, ничего не выполнили.

**Лечение:** Monday/Friday cadence. Без исключений.

### 2. Слишком много OKR

7-10 целей на команду. Все одинаково «важные». Никакого фокуса.

**Лечение:** Hard rule — 3 OKR maximum per team per quarter. 5 — потолок для company-level. Каждое добавление аргументируется на встрече leadership team.

### 3. OKR как task list

KR пишутся как deliverables: «Запустить фичу X», «Нанять 5 людей», «Провести 3 тренинга».

**Лечение:** на каждом KR следует спросить — *«если мы это сделаем, изменится ли исход для бизнеса?»*. Если ответ «не обязательно» — это не KR. Его переписывают на outcome: «Достичь X retention», «Команда укомплектована для скейла Y».

### 4. OKR theatre

Команды пишут OKR красиво, чтобы хорошо выглядеть на review. Не для дела, а для презентации. CEO видит цветные слайды и доволен.

**Лечение:** OKR пишутся в plain Sheets/Notion, а не в slick PowerPoint. На retrospective честно фиксируется грейд. Если все команды показывают 0.95 — бьём тревогу: либо целей не было, либо все sandbag.

### 5. Привязка к компенсации

Бонус привязан к выполнению OKR. Сразу же люди начинают **sandbag** — занижать амбиции для гарантированного выполнения. Stretch-философия умерла.

**Лечение:** Adobe Check-in модель. Бонус — за **общий вклад**, оцениваемый менеджером в качественной форме (а не за %% выполнения OKR). LinkedIn, Google — то же.

### 6. Top-down dictate

Менеджер пишет OKR за подчинённых, спускает. Подчинённые исполнители, не владельцы. Mотивация нулевая.

**Лечение:** правило 50/50. Половина OKR — bottom-up. Менеджер ставит **направление** (Objective), команда сама определяет KR.

### 7. Игнорирование KPI ради OKR

«Мы теперь делаем OKR! KPI — старьё». Дашборд забыт. Через 2 квартала — операционный кризис, потому что никто не следил за здоровьем.

**Лечение:** KPI и OKR параллельно. WBR (Weekly Business Review) для KPI. OKR — отдельный документ и процесс.

### 8. OKR без Owner

KR висит в воздухе. Никто конкретно не отвечает. На retrospective все указывают друг на друга.

**Лечение:** каждый KR имеет одного, **именно одного**, owner. Single-Threaded Leader (Amazon-философия).

### 9. Неправильный mix committed vs aspirational

Все OKR aspirational → ничего не сделано (нет committed-обязательств по операционке). Или все committed → нет амбиции.

**Лечение:** правило mix: 60-70% committed (то, что обязаны сделать), 30-40% aspirational (стрейч). Чётко промаркированы. На retrospective committed ≠1.0 = root cause analysis.

### 10. Нет cultural buy-in от leadership

CEO декларирует OKR на all-hands и забывает. Сам не пишет публичных OKR. Не приходит на quarterly review. Команда видит: «это не серьёзно».

**Лечение:** **CEO пишет первым**. Публично. На каждом quarterly review CEO презентует свои grades первым. Перед своими вопросами к командам. Без этого OKR — culture theatre.

## Tools — что использовать

### Для старта (free / cheap)

- **Google Sheets / Notion / Coda.** Самый простой start. Один документ, видно всем.
  - Шаблоны: гугли «OKR template Sheets» — десятки бесплатных.
- **Slack / Telegram-канал** — для еженедельных Monday/Friday updates.

Adobe в 2012 запустил Check-in **именно в Sheets**. Только потом перешли на purpose-built tooling. Doerr в *Measure What Matters* советует: «not the tool, the discipline».

### Specialized OKR software (когда команда >100)

| Tool | Сильные стороны | Цена (примерно) |
|------|-----------------|------------------|
| **Workboard** | Enterprise, AI-features, deep integrations | $$$ |
| **Lattice** | OKR + perf review + 1:1 в одном | $$ |
| **Ally.io** (часть Microsoft Viva Goals) | Native в M365 | $$ |
| **Gtmhub / Quantive** | Гибкие OKR + KPI dashboards | $$ |
| **Perdoo** | Хорошие шаблоны и обучающие материалы | $ |
| **Weekdone** | Простой, для команд до 100 | $ |
| **15Five** | Mix OKR + employee engagement | $$ |

**Не стоит выбирать tool первым.** Сначала год работы в Sheets/Notion. Когда боль из «не помещается в таблицу» становится ощутимой — тогда можно выбирать. Большинство команд **никогда** не дорастают до specialized software.

### Для KPI-дашборда

- **Google Sheets / Excel** — start.
- **Tableau / Power BI / Looker** — enterprise BI.
- **Geckoboard / Klipfolio / Databox** — простые дашборды для команд.
- **Grafana** — для технических команд, любой источник данных.

## Pre-launch checklist для руководителя

- [ ] Есть 3-5 annual OKR на уровень компании, сформулированных лично руководителем.
- [ ] Есть KPI-дашборд с 10-15 health-метриками в 4 перспективах.
- [ ] Каждый KPI имеет owner, target, yellow/red threshold, frequency.
- [ ] Команде объяснено: OKR ≠ performance review, не привязан к бонусу.
- [ ] Pilot выбран — 1 команда, 3 OKR.
- [ ] Cadence ритуалов — Monday + Friday в календаре, регулярно.
- [ ] Документ с OKR — public для всей команды (не только CEO видит).
- [ ] Руководитель лично написал свои публичные OKR и показал их первым.
- [ ] Есть план retrospective в конце квартала.
- [ ] Mix committed vs aspirational — обозначен явно.

## Чек-лист до начала каждого квартала

- [ ] Annual OKR пересмотрены, актуальны.
- [ ] Quarterly OKR команд связаны с annual (linkage написана явно).
- [ ] Каждое OKR имеет single owner.
- [ ] 3 OKR на команду, не больше.
- [ ] Каждое KR — outcome, не activity.
- [ ] Mix committed/aspirational обозначен.
- [ ] Confidence на старте 1-10 на каждый KR.

## Чек-лист каждый понедельник

- [ ] 30 минут на team Monday Commit.
- [ ] Каждый говорит, что сделает на этой неделе для движения KR.
- [ ] Confidence check на каждый KR (1-10).
- [ ] Identification аномалий — confidence упал?

## Чек-лист каждую пятницу

- [ ] 30 минут на team Friday Wins.
- [ ] Demo чего-то конкретного.
- [ ] Что получилось — поздравляем.
- [ ] Что не получилось — коротко, без шейминга.

## Чек-лист в конце квартала

- [ ] Grade каждый KR 0.0-1.0 публично.
- [ ] Committed KR <1.0 — root cause analysis.
- [ ] Lessons learned — что переносим, что отбрасываем.
- [ ] Q+1 OKR установлены (3 на команду).
- [ ] Retrospective public для всей компании.

## Связь с типовой ситуацией (beauty-импорт, ритейл, операционка)

Для **операционного руководителя в ритейле/импорте** разумная стартовая конфигурация:

**KPI-доминантная база (60-70% управления):**
- OTIF, GMROII, inventory turnover, forecast accuracy, gross margin, voluntary attrition.
- Pulled из Balanced Scorecard (см. [[04-KPI-and-Balanced-Scorecard|04]]).
- Weekly review с командой.

**OKR на change-инициативы (30-40%):**
- Запуск новой категории.
- Расширение в новый канал (B2C, маркетплейс).
- Внедрение S&OP (см. [[../../14-Planning/SOP/index|S&OP]]).
- Capability-building (обучение категорийщиков, S&OP-литературы).
- Quarterly cycle.

**Не стоит заменять весь management OKR-ами.** Ритейл живёт на KPI. OKR — для change.

## Что читать дальше

- [[06-OKR-vs-KPI-the-difference|06 — OKR vs KPI]] — фундамент решений.
- [[03-OKR-cases|03 — Кейсы]] — что было у других.
- [[05-KPI-cases-and-pitfalls|05 — Pitfalls]] — что не делать.
- [[../../14-Planning/Compare/index|Compare]] — общая матрица всех методологий.
- [[index|OKR-KPI Index]]

## Источники

- [Quantive — 20 most common OKR mistakes](https://quantive.com/resources/articles/okr-mistakes)
- [Perdoo — common OKR mistakes](https://www.perdoo.com/resources/blog/common-okr-mistakes-and-how-to-overcome-them)
- [Workpath — 8 most common OKR pitfalls](https://www.workpath.com/en/magazine/okr-pitfalls)
- [Sara Lobkovich — 8 OKR mistakes](https://saralobkovich.com/nobsokrs-blog/okr-mistakes-to-avoid)
- [Mooncamp — 11 most common OKR mistakes](https://mooncamp.com/blog/okr-mistakes)
- [Jeff Gothelf — Aligning, not Cascading OKRs](https://jeffgothelf.com/blog/aligning-not-cascading-okrs-with-an-okr-lineage/)
- [whatmatters.com — Top-down OKR cascading examples](https://www.whatmatters.com/faqs/cascading-top-down-okr-examples)
- [whatmatters.com — Bottom-up goal setting](https://www.whatmatters.com/faqs/bottom-up-okrs-definition-examples)
- [Caroli — Radical Focus Monday Commitments](https://caroli.org/en/radical-focus/)
- Christina Wodtke, *Radical Focus* 2nd ed. (2021), parts II-III
- John Doerr, *Measure What Matters* (2018), ch. 7-13
- Adobe Check-in: [whatmatters.com — why Adobe killed reviews](https://www.whatmatters.com/articles/why-adobe-killed-performance-reviews)
