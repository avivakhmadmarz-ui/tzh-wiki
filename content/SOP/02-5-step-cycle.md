---
aliases: 
updated: YYYY-MM-DD
tags: [education, sop, process]
created: 2026-05-07
date created: 2026-05-07
date modified: 2026-05-13
---

# Пятиступенчатый цикл S&OP

> **TL;DR.** Каждый месяц — 5 шагов: **Product → Demand → Supply → Integrated Reconciliation → Management Business Review**. Это не «совещания подряд», а волна, в которой выход одного шага — вход следующего. Срок одного цикла — обычно 3-4 рабочих недели на 1 календарный месяц.

![[sop-5-step-cycle.png]]

## Общий ритм месяца

Условно, если S&OP-цикл закрывается к концу месяца N (executive review в конце месяца):

| Неделя | Шаг | Что происходит |
|--------|-----|----------------|
| Неделя 1 | Product Review | Портфель, новинки, фазауты |
| Неделя 2 | Demand Review | Консенсус-форкаст |
| Неделя 3 | Supply Review | Проверка плана на capacity |
| Неделя 4 (нач.) | Integrated Reconciliation (Pre-S&OP) | Сводим разрывы, готовим decision papers |
| Неделя 4 (кон.) | Management Business Review (Executive S&OP) | C-level принимает решения |

После executive review план уходит в исполнение (S&OE) и на старт следующего цикла.

---

## Шаг 1. Product Review (Portfolio Review)

**Цель:** управление портфелем продуктов — что запускаем, что снимаем, как меняется ассортимент.

**Когда:** первая неделя цикла.

**Owner:** Product Manager / R&D / Marketing.

**Участники:**
- Product / Marketing (ведут)
- R&D / разработка
- Sales (комментирует канальный fit)
- Operations (даёт реалистичность сроков ввода)
- Finance (NPV/ROI новинок)

**Что обсуждается:**
- Прогресс по запуску новых SKU (NPI — New Product Introduction).
- Решения по фазауту (когда снять с производства/из ассортимента).
- Изменения в ассортименте: переупаковка, ребрендинг, реформулирование.
- ROI/NPV новинок vs план.
- Календарь запусков на 18-24 месяца вперёд.

**Артефакты на выходе:**
- Обновлённый roadmap портфеля.
- Список SKU с датой ввода/вывода (это ВХОД для Demand Review).
- Решения «go/no-go» по новинкам.

**Типичные ошибки:**
- Игнорировать фазауты — копится «зомби-ассортимент» с дорогим инвентарём.
- Запускать новинки без капасити-проверки в Supply Review.
- Не считать каннибализацию (новый SKU съест старый).

> **Типичный пример (товарная beauty-компания).** Каждый сезон новые цвета и форматы продукта, спецколлекции с инфлюенсерами, новые форматы упаковки. Product Review — это форум, где решается «эту коллекцию запускаем в августе с тиражом 5к, эту откладываем на Q1». Без него — запускаются «по фану», склад захлёбывается.

---

## Шаг 2. Demand Review

**Цель:** выработать единый, согласованный, **unconstrained** прогноз спроса на 18-24 месяца.

**Когда:** вторая неделя цикла.

**Owner:** Demand Planner / VP of Sales.

**Участники:**
- Demand Planner (ведёт)
- Sales (по каналам/регионам)
- Marketing (промо-планы, цены)
- Finance (наблюдатель + согласование с бюджетом)
- S&OP Leader

**Что происходит:**
1. **Statistical baseline** — алгоритм даёт «механический» прогноз по истории (МА, экспоненциальное сглаживание, ML-модели типа Prophet/LSTM).
2. **Обогащение sales intelligence** — крупные клиенты, тендеры, новые контракты.
3. **Marketing override** — промо, ребрейтинг, рекламные кампании.
4. **Реконсиляция «снизу-вверх» (по SKU/каналам) и «сверху-вниз» (по бюджету)** — должны сходиться.
5. **Согласование консенсуса** — всеми участниками, под подпись.
6. **Документирование ассампшенов** — чтобы через 3 месяца понять, почему ошиблись.

**Артефакты на выходе:**
- **Consensus demand plan** в штуках и в деньгах.
- KPI: **MAPE / WMAPE / Bias** vs прошлый цикл (см. [[08-Metrics-and-maturity|Metrics]]).
- Decision log: «по каналу Wildberries +15% из-за акции 11.11».
- Это ВХОД для Supply Review.

**Ключевой принцип — «Unconstrained».** Demand Review даёт «что хочется продать», без оглядки на то, можем ли мы это произвести/привезти. Constrain даст следующий шаг.

**Типичные ошибки:**
- Sales занижают прогноз, чтобы потом «перевыполнить план» — это разрушает S&OP. Решение: KPI на forecast accuracy, а не на «перевыполнение».
- Один демпленнер сидит и «угадывает» — без участия sales и marketing.
- Не фиксируются ассампшены — невозможно учиться на ошибках.

---

## Шаг 3. Supply Review (Operations Review)

**Цель:** проверить, реалистичен ли demand-плана с точки зрения capacity, поставок, рабочей силы, складов.

**Когда:** третья неделя цикла.

**Owner:** Supply / Operations Manager.

**Участники:**
- Supply Planner (ведёт)
- Manufacturing / производство
- Procurement (закупки)
- Logistics (склад, транспорт)
- Inventory Manager
- Finance (стоимость capacity)

**Что происходит:**
1. **Constraints check** — Demand-плана прогоняется через RCCP (Rough-Cut Capacity Planning): хватит ли мощностей, людей, складов, поставщиков?
2. **Bottleneck identification** — где именно упрёмся (например, «у поставщика X лидтайм 16 недель на упаковку»).
3. **Mitigation scenarios** — варианты решений:
   - Овертайм / 3-я смена.
   - Альтернативный поставщик.
   - Перенос объёмов между периодами (build-up inventory заранее).
   - Outsourcing / контрактное производство.
4. **Inventory plan** — целевые уровни запасов на 18 мес.
5. **Capex/Opex implications** — какие инвестиции нужны.

**Артефакты на выходе:**
- **Constrained supply plan** — что физически можно поставить.
- **Gap analysis** — где demand > supply и наоборот.
- **Scenario book** — 2-3 варианта с ценой решений.
- Это ВХОД для Integrated Reconciliation.

**Типичные ошибки:**
- Operations говорят «можем всё» (политически удобно) — потом срывают сроки.
- Не учитываются supplier constraints (закупки — это часто main bottleneck).
- Сценарии без цифр в деньгах — executive не сможет выбрать.

> **Типичный пример (long-tail запчасти).** Long-tail SKU, лидтаймы по импорту 12-20 недель, плюс неустойчивые российские поставщики. Supply Review — это форум, где говорится «вот этого мы не привезём в Q3, потому что в Китае фабрика на reset, давайте build-up в Q2 или ищем альтернативу». Без этого — постоянный backorder по полугоду.

---

## Шаг 4. Integrated Reconciliation (Pre-S&OP)

**Цель:** свести demand, supply и финансы в один план; подготовить decision package для executive review.

**Когда:** начало 4-й недели.

**Owner:** **S&OP Leader** (отдельная роль, часто — Director of Supply Chain или Director of Planning).

**Участники:**
- S&OP Leader (ведёт)
- Demand Planner
- Supply Planner
- Finance Lead
- Functional managers (по приглашению, для своих gap'ов)

**Что происходит:**
1. **Сведение discrepancies** — где demand расходится с supply, где сценарии расходятся с бюджетом.
2. **Quantification of gaps** — каждый разрыв оценён в деньгах (revenue at risk, cost of inaction, working capital impact).
3. **Trade-off matrix** — варианты решений с pros/cons:
   - Option A: накопить inventory заранее → +$2M working capital, но +99% сервис.
   - Option B: упустить пик спроса → -$5M revenue, но кэш свободен.
   - Option C: outsource → +$1M COGS, средний уровень риска.
4. **Recommendation** — что предлагает S&OP Leader.
5. **Decision papers** — 1-2 страницы на каждое решение, готовые к подписи.

**Артефакты на выходе:**
- **Reconciled plan** (один набор цифр).
- **Decision agenda** для Executive S&OP — 5-10 решений, требующих C-level.
- **What-if scenarios** с финансовыми последствиями.
- **Issues escalated** — что не смогли решить на уровне ниже.

**Это самый недооценённый шаг.** Если его сделать плохо — Executive S&OP превратится в «прочитайте PDF и моргните» вместо принятия решений. По Oliver Wight, IBP отличается от S&OP именно тем, что Integrated Reconciliation — обязательный, отдельный, регулярный шаг (не подсуедет к executive meeting).

---

## Шаг 5. Management Business Review (Executive S&OP)

**Цель:** executive level принимает решения по escalated trade-offs и подписывает план на следующие 18-24 мес.

**Когда:** конец 4-й недели.

**Owner:** **Executive Sponsor** (CEO / COO / GM).

**Участники:**
- CEO/COO (председатель)
- CFO
- VP Sales / Commercial
- VP Operations / SCM
- VP Marketing
- VP R&D / Product
- HR (если capacity workforce decision)
- S&OP Leader (фасилитирует)

**Длительность:** 1.5-3 часа. Не больше — иначе теряется фокус.

**Структура встречи (типичная agenda):**
1. **Performance review (10 мин)** — KPI прошлого цикла: forecast accuracy, OTIF, inventory, margin vs plan.
2. **Demand outlook (15 мин)** — изменения в прогнозе, ключевые ассампшены.
3. **Supply outlook (15 мин)** — capacity, риски, сценарии.
4. **Financial reconciliation (15 мин)** — план vs бюджет, profitability outlook.
5. **Decisions (60 мин)** — обсуждение и решение по escalated items из Integrated Reconciliation.
6. **Action items & owners** — кто что делает к следующему циклу.

**Артефакты на выходе:**
- **Approved plan** — «one number» на 18-24 месяца, утверждённый CEO/COO.
- **Decision log** — что решено, кто ответственный, due dates.
- **KPI targets** на следующий цикл.
- **Escalations** — если что-то требует board / external партнёров.

**Типичные ошибки:**
- Executive sponsor не приходит / делегирует — процесс умирает за 6-12 мес.
- Встреча превращается в demand review v2 (детали, а не решения).
- Нет decision log — через месяц никто не помнит, что решили.
- Нет accountability — решение принято, но никто не следит за исполнением.

---

## Полная RACI-матрица 5-step S&OP

(R = Responsible, A = Accountable, C = Consulted, I = Informed)

| Шаг / Роль | S&OP Leader | Demand Plan | Supply Plan | Finance | Sales | Marketing | Operations | R&D | CEO/COO |
|------------|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 1. Product Review | C | I | I | C | C | A/R | C | R | I |
| 2. Demand Review | A | R | I | C | R | C | I | I | I |
| 3. Supply Review | A | I | R | C | I | I | R | I | I |
| 4. Integrated Reconciliation | A/R | C | C | C | I | I | I | I | I |
| 5. Executive Review | R (facilitator) | I | I | C | C | C | C | C | A |

<!-- IMG: RACI-матрица в виде цветной таблицы | https://umbrex.com/wp-content/uploads/sop-raci-matrix.png -->

## Ключевые принципы цикла

1. **Каждый шаг имеет clear owner** — нельзя «коллективно» отвечать.
2. **Вход одного шага = выход предыдущего** — нет параллельных потоков с разными цифрами.
3. **One number** — на executive review приходит уже согласованный план, а не «у продаж — одно, у операций — другое».
4. **Time-boxed** — каждое совещание ≤ 2 часов. Если не уложились — проблема в подготовке.
5. **Decision log + accountability** — каждое решение трекается до исполнения.

## Связанные заметки

- [[03-Best-practices-US|US best practices]] — как это устроено у лидеров
- [[07-Implementation-checklist|Чеклист внедрения]] — как поставить такой цикл с нуля
- [[08-Metrics-and-maturity|Метрики]] — что измерять на каждом шаге
- [[index|S&OP Index]]

## Источники

- [Umbrex — Demand/Supply/Executive S&OP Meetings playbook](https://umbrex.com/resources/inventory-management-playbook/demand-review-supply-review-and-executive-sop-meetings/)
- [Anaplan — S&OP Process Guide](https://www.anaplan.com/blog/sales-operations-planning-sop-guide/)
- [Mastering SAP — 5 Steps of S&OP](https://masteringsap.com/five-essential-steps-of-sales-and-operations-planning-to-achieve-an-integrated-business-plan/)
- [DBMSys — Effective S&OP Monthly Process](https://www.dbmsys.com/post/effective-s-op-monthly-process)
- [Logility — 5 Steps to S&OP Success (whitepaper)](https://www.supplychainbrain.com/ext/resources/secure_download/KellysFiles/WhitePapersAndBenchMarkReports/Logility/S-OP+5+Steps+to+Success+Logility.pdf)
- [Demand Planning blog — Preparing for Executive S&OP](https://demand-planning.com/2018/08/03/preparing-for-a-succesfull-executive-sop-review/)
