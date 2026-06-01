---
aliases: 
updated: 2026-05-13
tags: [education, glossary, operations]
created: 2026-05-07
date created: 2026-05-07
date modified: 2026-05-13
---

# Operations & Supply Chain — метрики операций

Алфавитный справочник англоязычных метрик и сокращений, которые встречаются в S&OP, Lean, DDMRP, ToC, цепочках поставок, ритейле и складских операциях.

## A

### ABC analysis · ABC-анализ
Классификация номенклатуры по вкладу в выручку (или другой ценности).
- **A** — топ ~20% SKU, дают ~80% выручки (правило Парето)
- **B** — следующие ~30% SKU, ~15% выручки
- **C** — остальные ~50% SKU, ~5% выручки

**Зачем:** разная стратегия управления — тщательное планирование A, упрощённое C.
**Где:** [[../Compare/04-Cases-by-situation]] (Кейс 3: 8000 SKU). Часто комбинируется с XYZ.

### AOV — Average Order Value · средний чек
`AOV = Выручка / Количество заказов`
**Зачем:** базовая метрика ритейла и e-commerce; рост AOV — рычаг выручки без роста трафика.

### APS — Advanced Planning and Scheduling · продвинутое планирование
Системы детального планирования и составления расписаний, надстройка над ERP.
**Примеры:** SAP IBP, Kinaxis, o9, OMP, Anaplan, Oracle SCM.
**Где:** [[../14-Planning/SOP/06-Tools-software]]

## B

### Backorder · бэк-заказ
Заказ клиента, который компания не смогла отгрузить из-за отсутствия запасов и ставит «в очередь».
**Метрика:** Backorder rate = backorder $ / total orders $.

### Bias — Forecast Bias · смещение прогноза
Систематическая ошибка прогнозирования (всегда занижаем или всегда завышаем).
`Bias = (Σ Actual − Σ Forecast) / Σ Forecast`
- Bias > 0 → forecast занижен (прогнозируем меньше, чем продаём)
- Bias < 0 → forecast завышен (прогнозируем больше, чем продаём)

**Зачем:** в отличие от MAPE, показывает не «насколько ошиблись», а «в какую сторону». Систематический bias надо чинить, случайные ошибки — норма.
**Где:** [[../14-Planning/SOP/08-Metrics-and-maturity]]

### BOM — Bill of Materials · спецификация
Список компонентов, материалов и количеств, нужных для производства одного изделия.
**Примечание:** «дерево BOM» — иерархическая структура (готовый продукт → узлы → детали → сырьё).

## C

### Capacity · производственная мощность
Максимальный объём, который ресурс/завод/линия может произвести за период.
- **Theoretical capacity** — теоретический максимум 24/7 без потерь
- **Effective capacity** — с учётом плановых остановок (ППР, переналадки)
- **Actual output** — фактический выпуск

### Carrying cost (Holding cost) · стоимость хранения запасов
% от стоимости запасов, который компания тратит на их содержание (склад, страхование, capital cost, устаревание).
**Бенчмарк:** обычно 20-30% годовых от стоимости запасов.

### CCPM — Critical Chain Project Management
Управление проектами по Goldratt: критическая цепочка ресурсов, project buffer, no multi-tasking.
**Где:** [[../14-Planning/Other-methodologies/04-Theory-of-Constraints]]

### Cycle time · время цикла
Время от начала операции до её завершения. Не путать с Lead time.
**Пример:** время сборки одного автомобиля на конвейере = 60 секунд (cycle time). Lead time = от заказа клиента до получения = 6 недель.
**Где:** [[../13-Operations-Excellence/Lean/03-Lean-tools]]

### C2C — Cash-to-Cash Cycle · цикл обращения денег
`C2C = DIO + DSO − DPO`
- **DIO** (Days Inventory Outstanding) — дни запасов
- **DSO** (Days Sales Outstanding) — дни дебиторки
- **DPO** (Days Payable Outstanding) — дни кредиторки

**Зачем:** сколько дней деньги «заперты» в операционном цикле. Меньше = лучше (Apple исторически C2C отрицательный — поставщики финансируют их операции).
**Бенчмарк:** топ-25% Gartner Supply Chain — C2C ≤ 30 дней; средний — 60-90; плохо — 120+.
**Где:** [[../14-Planning/SOP/08-Metrics-and-maturity]]

## D

### DDMRP — Demand-Driven Material Requirements Planning
Pull-альтернатива MRP. Buffer profile (red/yellow/green) вместо safety stock.
**Где:** [[../14-Planning/Other-methodologies/03-DDMRP-Demand-Driven]]

### DIH — Days Inventory on Hand = DIO — Days Inventory Outstanding · дни запасов
`DIO = (Среднее значение запасов / COGS) × 365`
**Что показывает:** сколько дней запасов хватит на продажи при текущей скорости.
**Бенчмарк:** retail FMCG ~30-45 дней, beauty / cosmetics ~60-120 дней (длинный lead time CN), medical devices ~150+.

### DPO — Days Payable Outstanding · дни кредиторки
Среднее время оплаты поставщикам. Большое DPO = поставщики финансируют операции (хорошо для cash, плохо для отношений).

### DSO — Days Sales Outstanding · дни дебиторки
Среднее время получения денег от клиентов после отгрузки.

### Drum-Buffer-Rope (DBR)
Метод ToC для синхронизации производства с узким местом.
**Где:** [[../14-Planning/Other-methodologies/04-Theory-of-Constraints]]

## E

### E&O — Excess & Obsolete · излишки и неликвиды
Запасы, которые либо превышают разумную потребность, либо устарели и не будут проданы по полной цене.
**Метрика:** E&O ratio = (Excess + Obsolete inventory) / Total inventory.
**Зачем:** killer cash flow в beauty / fashion / electronics с короткими циклами.

### EOQ — Economic Order Quantity · экономически обоснованный размер заказа
Формула Уилсона (1934):
`EOQ = √(2 × D × S / H)`, где D = годовой спрос, S = стоимость размещения заказа, H = carrying cost на единицу.
**Где:** базовая модель из MRP, иногда упоминается в [[../14-Planning/Other-methodologies/02-MRP-MRPII-ERP]]

## F

### Fill rate · уровень удовлетворения спроса
% спроса, удовлетворённого из имеющихся запасов (без backorder).
- **Line fill rate** — % строк заказа, отгруженных полностью
- **Order fill rate** — % заказов, отгруженных полностью
- **Unit fill rate** — % единиц товара, отгруженных от заказанного

**Не путать с OTIF** — OTIF учитывает ещё и время.

### FIFO / LIFO / FEFO · правила движения запасов
- **FIFO** (First-In, First-Out) — первым пришёл, первым ушёл. Стандарт для скоропорта.
- **LIFO** (Last-In, First-Out) — последним пришёл, первым ушёл. Запрещён в IFRS, разрешён в US GAAP.
- **FEFO** (First-Expired, First-Out) — первым истекает срок, первым ушёл. Для фарма / косметики / еды.

### FPY — First Pass Yield · выход с первого прохода
% продукции, прошедшей все операции без переделок и брака.
`FPY = Units passing without rework / Units started`
**Где:** [[../13-Operations-Excellence/Lean/06-Lean-Six-Sigma]]; ключевая метрика TPS / LSS.

### Forecast Accuracy · точность прогноза
Часто выражается через `100% − MAPE` или `100% − WMAPE`.
**Бенчмарк:** топ-25% mature companies — 80%+ на месяц вперёд по SKU-location уровню; средний — 60-70%.
**Где:** [[../14-Planning/SOP/08-Metrics-and-maturity]]

## G

### GMROI — Gross Margin Return on Inventory Investment · доходность инвестиций в запасы
`GMROI = Gross Margin $ / Average Inventory at Cost`
**Зачем:** ритейл-метрика. Сколько маржи приносит каждый рубль, замороженный в запасах.
**Бенчмарк:** супермаркеты ~3-4, fashion 1.5-2, beauty 2-3.

## H

### Heijunka · хейдзунка · выравнивание производства
Японский принцип TPS — выравнивание объёма и mix производства, чтобы избежать Mura (неравномерности).
**Где:** [[../13-Operations-Excellence/Lean/01-Toyota-Production-System]] · [[../13-Operations-Excellence/Lean/02-8-wastes-Muda-Mura-Muri]]

## J

### JIT — Just-In-Time · точно вовремя
Один из двух столпов TPS: производить только то, что нужно, когда нужно, в нужном количестве. Минимизирует запасы и WIP.
**Где:** [[../13-Operations-Excellence/Lean/01-Toyota-Production-System]]

### Jidoka · дзидока · автономизация с человеческим разумом
Второй столп TPS: останавливать процесс при обнаружении проблемы, чтобы не передавать дефект дальше. Andon, Poka-Yoke.
**Где:** [[../13-Operations-Excellence/Lean/01-Toyota-Production-System]]

## K

### Kanban · канбан · карточка
Сигнал-карточка для pull-производства. Когда запас падает — карточка возвращается upstream и триггерит пополнение.
**Где:** [[../13-Operations-Excellence/Lean/03-Lean-tools]]

## L

### Lead time · время выполнения
Время от запуска заказа до его получения. Не путать с Cycle time.
- **Customer lead time** — от размещения заказа клиентом до получения
- **Manufacturing lead time** — от запуска производства до готовности
- **Supplier lead time** — от заказа поставщику до получения сырья

### LSS — Lean Six Sigma
Гибрид Lean (поток, муда) и Six Sigma (вариативность, дефекты). DMAIC цикл.
**Где:** [[../13-Operations-Excellence/Lean/06-Lean-Six-Sigma]]

## M

### MAPE — Mean Absolute Percentage Error · средняя абсолютная процентная ошибка
`MAPE = (1/n) × Σ |Actual − Forecast| / |Actual| × 100%`
**Зачем:** базовая метрика точности forecast. Чем ниже — тем точнее.
**Минусы:** ломается при Actual = 0, искажается на низкомоментных SKU. Поэтому часто используют WMAPE.
**Бенчмарк:** топ-25% Gartner — 15-25% (т.е. accuracy 75-85%); средний — 30-40%.
**Где:** [[../14-Planning/SOP/08-Metrics-and-maturity]]

### MOQ — Minimum Order Quantity · минимальная партия
Минимум, который поставщик соглашается отгрузить за один заказ. Часто навязывается из Китая (например MOQ 1000 шт).
**Конфликт с DDMRP:** большие MOQ ломают pull-логику. Договариваться о снижении или buffer green zone = MOQ.

### MRP — Material Requirements Planning · планирование потребности в материалах
Push-планирование: forecast спроса → расчёт потребности в материалах → закупки/производство. Joseph Orlicky, IBM, 1960-е.
**MRP II** (1980-е, Oliver Wight) — расширенный: добавляет capacity, finance.
**Где:** [[../14-Planning/Other-methodologies/02-MRP-MRPII-ERP]]

### Muda / Mura / Muri · 3M потерь
- **Muda** (無駄) — потери (TIMWOODS)
- **Mura** (斑) — неравномерность
- **Muri** (無理) — перегрузка

**Где:** [[../13-Operations-Excellence/Lean/02-8-wastes-Muda-Mura-Muri]]

## N

### Net Flow Equation · уравнение чистого потока (DDMRP)
`Net Flow = On-hand + On-order − Qualified Spike Demand`
Если Net Flow ≤ Top of Yellow → размещаем заказ пополнения.
**Где:** [[../14-Planning/Other-methodologies/03-DDMRP-Demand-Driven]]

## O

### OEE — Overall Equipment Effectiveness · общая эффективность оборудования
`OEE = Availability × Performance × Quality`
- **Availability** — % времени, когда оборудование работало (vs плановое время)
- **Performance** — % реальной скорости от nominal
- **Quality** — % годных от выпущенных

**Бенчмарк:** мировой класс ~85%, средний завод ~60%, плохой ~40%.
**Где:** [[../13-Operations-Excellence/Lean/03-Lean-tools]]

### OOS — Out-of-Stock · отсутствие на полке/складе
% случаев, когда товар запрошен, но недоступен.
- **Phantom OOS** — есть на складе, но нет на полке
- **Real OOS** — нет на складе

**Бенчмарк ритейла:** 5-8% — норма, 10%+ — проблема.

### OTIF — On-Time In-Full · вовремя и в полном объёме
% заказов, отгруженных вовремя И в полном объёме (оба условия).
`OTIF = (Orders delivered on-time AND in-full) / Total orders × 100%`
**Зачем:** ключевой service-level метрик в ритейле и B2B. Walmart штрафует поставщиков за OTIF < 98%.
**Бенчмарк:** топ-25% — 95%+, средний — 85-92%.
**Где:** [[../14-Planning/SOP/08-Metrics-and-maturity]]

## P

### Pareto Principle · принцип Парето · 80/20
20% причин дают 80% результата. Используется для приоритизации (топ-20% SKU = ABC class A; топ-20% клиентов = key accounts).
**Где:** [[05-Concepts-and-laws]]

### PDCA — Plan-Do-Check-Act · цикл Деминга
Базовый цикл непрерывного улучшения: спланируй → сделай → проверь → закрепи.
**Где:** [[../13-Operations-Excellence/Lean/03-Lean-tools]]

### Poka-Yoke · защита от ошибок
Японский TPS-инструмент: устройства/процессы, которые делают невозможным совершить ошибку (USB-разъём нельзя вставить вверх ногами; SIM-карта влезает только в одну сторону).
**Где:** [[../13-Operations-Excellence/Lean/01-Toyota-Production-System]]

## R

### RACI — Responsible, Accountable, Consulted, Informed
Матрица распределения ответственности по задачам/решениям.
- **R** (Responsible) — кто делает
- **A** (Accountable) — кто отвечает за результат (всегда один!)
- **C** (Consulted) — с кем консультируемся (двусторонне)
- **I** (Informed) — кого информируем (одностороннее)

**Где:** [[../14-Planning/SOP/02-5-step-cycle]] · [[../14-Planning/SOP/07-Implementation-checklist]]

## S

### Safety Stock · страховой запас
Запас, держащийся «на всякий случай» — для защиты от вариативности спроса/lead time.
**Классическая формула:** `SS = Z × σ × √LT`, где Z = Z-score сервис-уровня (1.96 для 95%), σ = СКО спроса, LT = lead time.
**Минус:** без учёта correlation, для всех SKU считается отдельно. DDMRP заменяет это buffer profiles.

### SMED — Single-Minute Exchange of Die · быстрая переналадка
Метод TPS для сокращения времени переналадки оборудования до < 10 минут (single-digit minute). Shigeo Shingo.
**Где:** [[../13-Operations-Excellence/Lean/03-Lean-tools]]

### S&OP — Sales and Operations Planning
Ежемесячный кросс-функциональный процесс согласования планов продаж, операций, финансов на 18-24 мес.
**Где:** [[../14-Planning/SOP/index]]

### S&OE — Sales and Operations Execution
Краткосрочный (недели/0-3 мес) аналог S&OP — для исполнения, не планирования. Дополняет S&OP.

### Sell-through · скорость распродажи
% полученных товаров, проданных за период.
`Sell-through = Units sold / Units received × 100%`
**Зачем:** beauty / fashion ритейл. Низкий sell-through = риск E&O.

### SKU — Stock Keeping Unit · единица учёта запасов
Уникальный идентификатор товара (комбинация артикул × цвет × размер × упаковка).
**Пример:** Один и тот же лак в 6 ml и 12 ml — это два SKU.

## T

### Takt time · такт-время
Темп, с которым продукт должен выходить с линии, чтобы соответствовать спросу.
`Takt = Available production time / Customer demand`
**Пример:** 480 минут в смене / 240 заказов в смене = 2 минуты на единицу.
**Где:** [[../13-Operations-Excellence/Lean/03-Lean-tools]]

### Throughput · пропускная способность
В ToC: выручка минус truly variable costs. Не путать с output (просто объём).
**Где:** [[../14-Planning/Other-methodologies/04-Theory-of-Constraints]]

### TIMWOODS — 7+1 видов потерь
**T**ransport, **I**nventory, **M**otion, **W**aiting, **O**verproduction, **O**verprocessing, **D**efects, **S**kills.
**Где:** [[../13-Operations-Excellence/Lean/02-8-wastes-Muda-Mura-Muri]]

### ToC — Theory of Constraints · теория ограничений
Goldratt: в любой системе есть bottleneck, и пропускная способность системы определяется им.
**Где:** [[../14-Planning/Other-methodologies/04-Theory-of-Constraints]]

### TPM — Total Productive Maintenance · всеобщий уход за оборудованием
TPS-инструмент: операторы сами обслуживают оборудование, плановое профилактическое обслуживание, нулевые поломки как цель.

### TPS — Toyota Production System
Корни современного Lean. Два столпа JIT и Jidoka, центр — kaizen, фундамент — стабильность и стандарт.
**Где:** [[../13-Operations-Excellence/Lean/01-Toyota-Production-System]]

## V

### Velocity (inventory velocity) · скорость оборачиваемости запасов
`Inventory turns = COGS / Average Inventory`
Сколько раз в год запасы «прокручиваются». Высокая velocity = меньше замороженного capital.
**Бенчмарк:** беспроигрышный ритейл (Walmart) ~8-10 turns/год, beauty ~3-5, медицинское оборудование ~1-2.

### VSM — Value Stream Mapping · картирование потока ценности
Lean-инструмент: рисуем все шаги процесса, отделяем value-add от non-value-add (waste).
**Где:** [[../13-Operations-Excellence/Lean/03-Lean-tools]]

## W

### WMAPE — Weighted MAPE · взвешенная MAPE
`WMAPE = Σ |Actual − Forecast| / Σ |Actual|`
**Зачем:** в отличие от классической MAPE, не «взрывается» при малых Actual. Используется для портфеля разнокалиберных SKU.
**Где:** [[../14-Planning/SOP/08-Metrics-and-maturity]]

## X

### XYZ analysis · XYZ-анализ
Классификация SKU по стабильности спроса (variability):
- **X** — стабильный спрос (CV < 10%) — легко прогнозировать, MRP работает
- **Y** — умеренная вариативность (CV 10-25%) — нужен safety stock
- **Z** — высокая вариативность (CV > 25%) — DDMRP buffers, не доверять forecast

**Где:** комбо ABC/XYZ — мощный инструмент сегментации. [[../Compare/04-Cases-by-situation]] (Кейс 3).

## Связанные документы

- [[index|Glossary Index]]
- [[02-Financial-metrics|Financial]]
- [[03-Customer-metrics|Customer & Growth]]
- [[04-Methodology-acronyms|Methodology Acronyms]]
- [[../14-Planning/SOP/08-Metrics-and-maturity|S&OP Metrics & Maturity]]

## Источники

- [ASCM Supply Chain Dictionary](https://www.ascm.org/learning-development/ascm-publications/) — отраслевой стандарт
- [Investopedia — Operations Management](https://www.investopedia.com/operations-management-4427876)
- [Lean Lexicon — LEI](https://www.lean.org/lexicon-terms/)
- [Demand Driven Institute Glossary](https://www.demanddriveninstitute.com/glossary)
