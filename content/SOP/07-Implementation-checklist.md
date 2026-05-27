---
aliases: 
updated: YYYY-MM-DD
tags: [education, sop, implementation, checklist]
created: 2026-05-07
date created: 2026-05-07
date modified: 2026-05-13
---

# Чеклист внедрения S&OP с нуля

> **TL;DR.** Внедрение S&OP — 12-18 месяцев до зрелости (Stage 3 по Gartner). Первый рабочий цикл — 3-6 месяцев. Главное правило: **«не жди совершенства, чтобы начать»** (Tom Wallace, Oliver Wight). Запусти minimum viable cycle на топ-20 SKU и наращивай. Только 15% компаний (Gartner 2024) добиваются успешного adoption — обычно те, у кого был CEO/COO sponsor.

## Этап 0. Pre-launch — диагностика и подготовка (1-2 месяца)

### Чеклист

- [ ] **Self-assessment по Gartner Maturity Model** ([[03-Best-practices-US|Best practices US]]). Определить, на какой стадии находишься (обычно SMB — Stage 1).
- [ ] **Self-assessment по Oliver Wight Class A** (опционально, упрощённая версия). Найти 3-5 главных gaps.
- [ ] **Найти executive sponsor.** Идеально — CEO или COO. Без sponsor процесс не выживет.
- [ ] **Получить mandate.** Письменно или хотя бы устно зафиксированный с executive: «мы запускаем S&OP с такой-то даты».
- [ ] **Назначить S&OP Leader.** Это роль, не должность. Часто — Director of Supply Chain или Director of Operations.
- [ ] **Сформировать Steering Committee** — executive + S&OP leader. Встречается раз в 2-4 недели в pre-launch фазе.
- [ ] **Определить scope пилота:** какой business unit / категория / set of SKU. Нельзя начать со всего сразу.
- [ ] **Бюджет:** time of people (главная статья). Софт пока не покупаем.

### Decision log (зафиксировать письменно)

- Кто sponsor?
- Кто S&OP Leader?
- Что в scope пилота, что нет?
- Какие 3 главные проблемы хотим решить (то, по чему будем мерить успех)?
- Какова дата первого Executive review?

## Этап 1. Foundations — данные и роли (1-2 месяца)

### Data prerequisites

S&OP не запустится без минимального уровня данных. Чеклист:

- [ ] **Master data clean** — единый product catalog, единые units of measure, согласованные family/category группировки.
- [ ] **Sales history** — минимум 12, лучше 24 месяца чистых продаж по SKU/каналу.
- [ ] **Forecast baseline** — текущий прогноз (даже если плохой) сохраняется как baseline.
- [ ] **Inventory snapshot** — точные остатки на дату cut-off.
- [ ] **Capacity data** — что мы можем произвести/привезти в месяц. Если этого нет — собрать с собственных закупщиков и операций.
- [ ] **Supplier lead times** — для топ-50% объёма закупок по value.
- [ ] **Promo/event calendar** — что планируется по маркетингу.
- [ ] **Bill of materials** (если производство) — точные BOM на топ-SKU.

### RACI matrix

Зафиксировать по каждому шагу 5-step cycle (см. [[02-5-step-cycle|Cycle]]). Минимум:

| Роль | Зачем | Кто (пример SMB) |
|------|-------|------------------|
| **Executive Sponsor** | A на all process | CEO / Founder |
| **S&OP Leader** | R на координацию, A на качество цикла | Director of Operations |
| **Demand Planner** | R на demand review | Sales analyst или маркетолог |
| **Supply Planner** | R на supply review | Senior buyer / Head of procurement |
| **Finance Lead** | R на financial reconciliation | CFO или Head of finance |
| **Sales Lead** | C на demand, accountable за forecast accuracy | VP Sales / Head of commerce |
| **Marketing Lead** | C на demand (promo) | Head of marketing |
| **Operations Lead** | C на supply | COO / Head of operations |

В SMB часто 1 человек = несколько ролей. Главное чтобы accountability была чёткой.

### Глоссарий и стандарты

- [ ] **Единый глоссарий** — что значит «forecast accuracy», как считаем MAPE, что такое «family».
- [ ] **Cut-off dates** — какая дата считается «концом месяца» для S&OP (часто не календарный конец).
- [ ] **Cadence calendar** — фиксированные даты review на 12 мес вперёд. Никаких «когда у CEO будет время».
- [ ] **Templates** — для demand review, supply review, executive deck. Single source of truth.

## Этап 2. First Pilot Cycle — minimum viable S&OP (3-6 месяцев)

### Принцип «start ugly»

Tom Wallace (классик S&OP): не пытайся сделать идеальный процесс с первого раза. Запусти грубую версию, выживи 3 цикла, потом улучшай.

### Чеклист первых 3 циклов

- [ ] **Cycle 1 (месяц 1):** провести все 5 шагов, даже если данные плохие. Главный output — пройти по процессу до executive review.
- [ ] **Cycle 2 (месяц 2):** улучшить templates и data quality, focus на demand-supply gap analysis.
- [ ] **Cycle 3 (месяц 3):** добавить financial reconciliation, начать tracking forecast accuracy.
- [ ] **Retrospective после каждого цикла** — что не работает, что улучшить.
- [ ] **Decision log** — все решения executive review письменно фиксируются.
- [ ] **KPI tracking** начинается с цикла 2: forecast accuracy, OTIF, inventory turns.

### Артефакты, которые должны появиться

После 3 циклов в наличии должно быть:
- Demand plan template (Excel/Sheets) с consensus forecast.
- Supply plan template с capacity check.
- Executive deck template (10-15 слайдов).
- Decision log (Notion/Confluence).
- KPI dashboard (Power BI / Looker Studio).
- Cadence calendar на 12 мес.
- Cycle minutes (фиксация решений и actions).

## Этап 3. Stabilization — встраивание в культуру (3-6 месяцев)

### Чеклист

- [ ] **Расширить scope** — с пилотного set на полный портфель.
- [ ] **Подключить дополнительные функции** — marketing (promo planning), R&D (new products).
- [ ] **Формализовать KPI и target'ы** — не только tracking, но и goals (например, «MAPE < 25% к концу года»).
- [ ] **Continuous improvement loop** — quarterly retrospective процесса.
- [ ] **Onboarding новых участников** — материалы, тренинги, mentor для новичков.
- [ ] **Celebrating wins** — публично отмечать улучшения KPI. Это часть cultural change management.
- [ ] **Integrate with strategic planning** — годовая стратегия проходит через S&OP-цикл.

## Этап 4. Maturity — переход к Stage 3-4 / IBP (6-18 месяцев)

### Чеклист

- [ ] **Финансовая интеграция углубляется** — план в долларах основной язык.
- [ ] **Scenario planning** — не один base case, а 2-3 (base/upside/downside).
- [ ] **Product portfolio review** становится отдельным шагом 1 (см. [[05-IBP-evolution|IBP evolution]]).
- [ ] **External integration** — collaborative forecast с key customers/suppliers.
- [ ] **Software upgrade** — если Excel перестаёт хватать (см. [[06-Tools-software|Tools]]).
- [ ] **Class A audit** — формальный или informal по чеклисту Oliver Wight.
- [ ] **Талант** — найм/обучение людей с APICS CSCP/CPIM.

## Топ-15 типичных ошибок внедрения

Из Gartner, Oliver Wight, Solvoyo и десятков case studies:

1. **Нет executive sponsor.** Самая частая причина провала. Без CEO/COO ownership — процесс умирает за 6-12 мес.
2. **Pursuit of perfection.** «Сначала наладим данные, потом запустим» = никогда не запустят. Start ugly.
3. **Только supply chain функция тащит.** Если sales/marketing/finance не вовлечены — это не S&OP, а improved supply planning.
4. **Слишком детально.** Executive review разбирает SKU вместо families — 2-часовое совещание превращается в 6-часовое.
5. **Sales занижают forecast.** KPI на «перевыполнение плана» убивает forecast accuracy. Менять KPI на bias и accuracy.
6. **Нет decision log.** Через месяц никто не помнит, что решили. Решения «растворяются».
7. **Cadence нарушается.** «Этот месяц пропустим, executive в отпуске». Один пропуск = три месяца восстановления.
8. **Tech ahead of process.** Купили Kinaxis, но процесс не отлажен — софт амплифицирует хаос.
9. **Один человек делает всё** (S&OP leader пишет все decks). Не масштабируется. Нужен team и distributed accountability.
10. **Demand review без sales.** Demand planner один прогнозирует — это статистика, не consensus.
11. **Supply review без поставщиков.** Внешние lead times не учтены. План невыполним.
12. **Finance — наблюдатель.** Без финансового sign-off Executive review не меняет реальность.
13. **Scope creep.** Запустили на одной категории, через месяц пытаются на 5 — никакая не работает.
14. **Игнорировать retrospective.** «У нас всё ОК» — нет улучшений = stagnation.
15. **Внедрять годами.** Если за 6 месяцев нет видимого progress — что-то структурно неправильно. Stop, reassess.

## Roadmap внедрения 12 месяцев (типовой)

| Месяц | Фокус | Артефакты |
|-------|-------|-----------|
| 1 | Diagnostic, sponsor, scope | Charter, RACI |
| 2 | Data prerequisites, templates | Master data, templates |
| 3 | First cycle (rough) | Cycle 1 deck, action log |
| 4 | Cycle 2, KPI tracking starts | Dashboard v1, retrospective |
| 5 | Cycle 3 + financial reconciliation | Financial templates, cycle minutes |
| 6 | Stabilization, expand scope | Quarterly review, retro, action plan |
| 7-9 | Cycles 7-9, KPI improvements | Trend on FA, OTIF, inventory |
| 10-12 | Maturity push, IBP introduction | Product review шаг, scenarios, Class A self-assessment |

## Минимальная команда для запуска S&OP в SMB

| Роль | Time commitment в месяц | В SMB кем закрывается |
|------|------------------------|----------------------|
| Executive Sponsor | 4-6 часов (steering, executive review) | CEO/Founder |
| S&OP Leader | 30-60% FTE первые 6 мес, потом 20-30% | Director of Operations |
| Demand Planner | 20-40% FTE | Marketing analyst или ассистент head of commerce |
| Supply Planner | 20-40% FTE | Head of procurement / senior buyer |
| Finance Lead | 10-20% FTE | CFO или его deputy |

**Всего:** 1-1.5 FTE «извлечения» из текущих ролей. Это и есть «бюджет» внедрения для SMB.

## Типовой план изучения и применения

**Сценарий: руководитель в SMB beauty / FMCG / e-com на 50-200 человек:**

1. **Месяц 1:** прочитать [[01-What-is-SOP|What is S&OP]] + [[02-5-step-cycle|Cycle]]. Поговорить с founder'ом, получить «карт-бланш» на пилот.
2. **Месяц 2:** собрать чистый dataset (12 мес продаж по SKU, остатки, lead times). Сделать Excel-template для demand review.
3. **Месяц 3:** провести «нулевой» demand review — закупки + руководитель, без sales (как self-test).
4. **Месяц 4:** пригласить sales / marketing на mini-демо, начать ежемесячный cadence.
5. **Месяц 5-6:** добавить supply review с поставщиками, executive review с founder'ом.
6. **Месяц 7-12:** стабилизировать cycle, добавить финансовую интеграцию, начать KPI tracking.
7. **Месяц 12+:** оценить переход к product portfolio review и IBP.

**Параллельно:** к месяцу 6 — записаться на APICS CSCP, чтобы получить теоретическую рамку.

## Связанные заметки

- [[02-5-step-cycle|5-step cycle]] — что именно делать в каждом цикле
- [[03-Best-practices-US|Best practices US]] — куда стремиться
- [[06-Tools-software|Tools]] — когда и какой софт
- [[08-Metrics-and-maturity|Metrics]] — что мерить
- [[index|S&OP Index]]

## Источники

- [Solvoyo — 7 Reasons Why S&OPs Fail](https://www.solvoyo.com/blogs/supply-chain/why-s-op-fail/)
- [Colibri — S&OP Mistakes to Avoid](https://www.colibri-snop.com/sop-process-all-the-mistakes-you-mustnt-make/)
- [Boundev — S&OP Implementation Guide](https://www.boundev.com/blog/sales-operations-planning-implementation-guide)
- [Maine Pointe — Six Critical Success Factors for S&OP](https://www.mainepointe.com/blog/sales-and-operations-planning-six-critical-success-factors-for-successful-implementation)
- [Demand Planning blog — Don't Wait for Perfection](https://demand-planning.com/2025/12/08/implementing-sop-dont-wait-for-perfection-to-get-started/)
- [Simplement — Starting an S&OP Roadmap](https://www.simplement.us/guides/practical-how-tos-starting-an-sop-roadmap)
- [Owl Solutions — S&OP Challenges and Solutions](https://theowlsolutions.com/salesandoperationsplanning/)
- [InstinctTools — How to Implement S&OP](https://www.instinctools.com/blog/how-to-implement-s-op-process/)
- [Logistics Bureau — S&OP Interpersonal Element](https://www.logisticsbureau.com/sales-and-operations-planning-the-interpersonal-element/)

<!-- IMG: 12-month implementation roadmap timeline | https://www.boundev.com/wp-content/uploads/sop-roadmap-12-months.png -->
