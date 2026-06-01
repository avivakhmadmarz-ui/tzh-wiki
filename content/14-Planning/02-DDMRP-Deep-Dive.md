---
title: "02 — DDMRP углубление"
aliases: ["DDMRP Deep Dive", "Demand Driven MRP", "Decoupling Points"]
type: note
status: active
domain: education
module: 14-Planning
tags: [education, planning, ddmrp, demand-driven, ptak, smith]
created: 2026-05-19
updated: 2026-05-19
---

# 02 — DDMRP углубление

> DDMRP (Demand Driven Material Requirements Planning — управляемое спросом планирование потребностей в материалах) — современная альтернатива классическому MRP, разработанная **Carol Ptak** и **Chad Smith** в 2010-х. Главное отличие — переход от forecast-driven push к demand-driven pull через стратегические буферы. Этот раздел — детальное углубление в DDMRP методологию.

## Карта раздела

![](attachments/diagrams/14-ddmrp-five-components.svg)

## 1. Зачем нужен DDMRP

### 1.1 Проблема классического MRP

MRP / MRP II — стандарт планирования с 1960-х. Главная проблема в современных условиях:

- **Forecast-driven** — план опирается на прогноз, который **всегда неточен**
- **Nervous system** — небольшое изменение спроса вызывает гигантские пересчёты вниз по цепочке (bullwhip effect)
- **Long lead times** — компоненты заказываются заранее, при изменении спроса — overstock или out-of-stock
- **Working capital tied up** — большие буферы для защиты от ошибок прогноза

В мире VUCA (Volatile / Uncertain / Complex / Ambiguous — изменчивый / неопределённый / сложный / неоднозначный) и BANI MRP плохо работает.

### 1.2 Решение DDMRP

DDMRP заменяет **push** (планирование от прогноза) на **pull** (исполнение от фактического спроса) через **стратегические буферы**.

Каноничная книга — **Carol Ptak, Chad Smith, «Demand Driven Material Requirements Planning»** (Industrial Press, 3-е изд. 2018). Также **«Demand Driven Performance»** (McGraw-Hill, 2013).

### 1.3 Происхождение

- TOC (Theory of Constraints — теория ограничений) от Eliyahu Goldratt — концепция drum-buffer-rope
- Lean — pull-системы, kanban
- Agile — итеративный подход
- DDMRP — синтез этих идей в формальную методологию для supply chain

**Ключевой вывод 1.** DDMRP — это **парадигменный сдвиг** от forecast к flow. Реакция supply chain на VUCA-условия.

## 2. Пять компонентов DDMRP

### 2.1 Полная картина

![](attachments/diagrams/14-ddmrp-five-components.svg)

DDMRP состоит из пяти компонентов:

1. **Strategic Inventory Positioning** — стратегические точки развязки
2. **Buffer Profiles and Levels** — размер буферов
3. **Dynamic Adjustments** — динамическая корректировка
4. **Demand-Driven Planning** — планирование от фактического спроса
5. **Visible and Collaborative Execution** — прозрачное выполнение

### 2.2 Component 1 — Strategic Inventory Positioning

![](attachments/diagrams/14-ddmrp-decoupling-points.svg)

Главная идея: **буфер нужен только в стратегических точках цепочки, а не повсеместно**.

**Decoupling points** (точки развязки) — места в цепочке, где буфер «разрывает» зависимость между sections:
- Часть до decoupling работает на push (forecast)
- Часть после — на pull (по фактическому спросу)

Критерии выбора decoupling points:
- High variability в спросе
- Long lead times до этой точки
- Multiple SKUs share component
- Customer tolerance time (= сколько готов ждать)

Пример: пекарня
- Мука, дрожжи — закуп (push, forecast)
- **Хлеб готовый** — decoupling point (буфер)
- Розничные клиенты — pull от полки

### 2.3 Component 2 — Buffer Profiles and Levels

Каждый decoupling point имеет **буфер** с тремя зонами:

![](attachments/diagrams/14-ddmrp-buffer-zones.svg)

- **Green (зелёная зона)** — задаёт размер и частоту заказа, нормальная работа
- **Yellow (жёлтая зона)** — ядро покрытия спроса на срок пополнения, зона планирования заказа
- **Red (красная зона)** — страховой запас, защита от вариативности; вход в неё означает срочность

Размер буфера = функция:
- **ADU** (Average Daily Usage — средний дневной расход)
- **Lead time** до пополнения
- **Variability factor**
- **Order minimum**

Формулы — в книге Ptak/Smith.

### 2.4 Component 3 — Dynamic Adjustments

Буферы **не статичны**. Динамические корректировки:

- **Trend-based** — если ADU растёт/падает
- **Event-based** — промо, праздники, запуски
- **Variability-based** — изменение волатильности

Это отличает DDMRP от классического Safety Stock с фиксированным значением.

### 2.5 Component 4 — Demand-Driven Planning

Решение о заказе принимается по **Net Flow Equation** (уравнению чистого потока), а не по прогнозу горизонта:

![](attachments/diagrams/14-ddmrp-net-flow.svg)

**Net Flow Position = On-Hand (физический остаток) + On-Order (уже заказано) − Qualified Demand (подтверждённый спрос с учётом пиков)**. Полученное значение сравнивается с зонами буфера: попадание в жёлтую или красную зону формирует pull-сигнал к пополнению. Планирование опирается на:
- Net Flow Position относительно зон буфера — pull-сигнал
- Реальные клиентские заказы, а не на прогноз горизонта

### 2.6 Component 5 — Visible and Collaborative Execution

Все участники видят **цвет буферов** в реальном времени:
- Red buffers — наивысший приоритет
- Yellow — нормальный workflow
- Green — можно отложить

Это создаёт **общий язык приоритетов** между функциями.

**Ключевой вывод 2.** Пять компонентов DDMRP работают **только вместе**. Применение одного без других не даёт эффекта.

## 3. Сравнение DDMRP с альтернативами

### 3.1 DDMRP vs Classic MRP

| Аспект | Classic MRP | DDMRP |
|--------|-------------|-------|
| Driver | Forecast | Actual demand |
| Approach | Push | Pull |
| Buffer location | Везде | Strategic points |
| Inventory levels | Безопасные запасы по всем SKU | Только в decoupling points |
| Response to demand changes | Долгий пересчёт | Мгновенный |
| Working capital | Высокий | Снижен на 30-50% |

### 3.2 DDMRP vs Kanban (Lean)

| Аспект | Kanban | DDMRP |
|--------|--------|-------|
| Применение | Производство, повторяющиеся продукты | Supply chain end-to-end |
| Sizing buffers | Manual / experience | Formula-based |
| Multi-echelon | Слабо | Сильно |
| Стабильность спроса | Высокая | Volatile тоже |

DDMRP — **scaled Kanban** для сложных цепочек.

### 3.3 DDMRP vs DDS&OP

**DDS&OP** (Demand Driven S&OP) — комбинация DDMRP-исполнения и S&OP-стратегии. Логично применять вместе:
- S&OP — strategy и tactical horizon (months)
- DDMRP — operational execution (days-weeks)

**Ключевой вывод 3.** DDMRP не заменяет S&OP, MRP, Kanban — **дополняет**. Главное преимущество — устойчивость к volatility и снижение working capital.

## 4. Внедрение DDMRP

### 4.1 Standard roadmap

| Фаза | Срок | Результат |
|------|------|-----------|
| Education | 1-3 месяца | Команда понимает методологию |
| Pilot 1 категории / линии | 6-12 месяцев | Working DDMRP на pilot |
| Scaling | 12-24 месяца | Полная supply chain |
| Optimization | Постоянно | Continuous improvement |

Полное внедрение — 2-3 года.

### 4.2 Типичные результаты

После внедрения DDMRP (по данным сертификации DDI — Demand Driven Institute):
- Inventory ↓ 30-50%
- OTD (On-Time Delivery) ↑ 10-20%
- Lead times ↓ 50-80%
- Working capital ↓ 30-50%
- Employee morale ↑ (приоритеты ясны)

### 4.3 Главные сложности

- **Cultural shift** — переход от forecast к pull
- **IT support** — большинство ERP не поддерживают DDMRP «из коробки»
- **Sponsor commitment** — без C-level не работает
- **Training** — команда должна понять методологию

### 4.4 IT-инструменты

- **B2Wise** — лидер DDMRP-software
- **R+ (Replenishment+)** — Demand Driven Technologies
- **SAP IBP DDMRP module** — официально с 2021
- **Custom Excel** — для pilot

**Ключевой вывод 4.** DDMRP — высокоокупаемая методология, но требует **3-летнего пути** и cultural change. Большинство компаний сначала пробуют, потом серьёзно внедряют.

## 5. Когда DDMRP подходит / не подходит

### 5.1 Подходит для:

- Производство со сложной BOM (Bill of Materials — спецификацией изделия)
- Длинные lead times компонентов
- Volatile спрос
- Многоуровневая цепочка (multi-echelon)
- Многоиндексные SKU

### 5.2 Не подходит:

- Чистый make-to-order (нет потребности в decoupling)
- Очень стабильный спрос (классический MRP справится)
- Очень короткие lead times (нет смысла в буфере)
- Project-based (engineer-to-order)

### 5.3 Российский контекст

Для российских компаний после 2022 года DDMRP особенно актуален:
- Volatility спроса резко выросла
- Lead times от китайских поставщиков непредсказуемы
- Working capital дорог (высокая ставка)

Активное внедрение DDMRP в РФ в 2023-2025 годах.

**Ключевой вывод 5.** DDMRP — не silver bullet. Серьёзный анализ применимости перед запуском.

## Применение для руководителя

| Целевая роль | Главные применения |
|--------------|---------------------|
| **COO** | Решение о DDMRP-трансформации |
| **Директор supply chain** | Daily владение DDMRP-методологией |
| **Директор закупок** | Buffer-driven sourcing вместо forecast-based |
| **CFO** | Working capital impact |
| **CIO** | Выбор IT-платформы |

## Связь с другими модулями

- [[01-IBP-Connected-Planning|01 IBP]] — комплементарны
- [[03-Hoshin-Kanri-Strategic|03 Hoshin Kanri]] — strategic layer
- [[../Other-methodologies/03-DDMRP-Demand-Driven|Other-meth: DDMRP базовый]]
- [[../Other-methodologies/04-Theory-of-Constraints|Other-meth: TOC]] — фундамент DDMRP
- [[../04-Supply-Chain/04-Inventory-Management|Модуль 04.04: Inventory]] — buffer sizing

## Источники

### Книги (приоритет чтения)

- Carol Ptak, Chad Smith, **«Demand Driven Material Requirements Planning»** (Industrial Press, 3-е изд. 2018)
- Carol Ptak, Chad Smith, **«Demand Driven Performance»** (McGraw-Hill, 2013)
- Eliyahu Goldratt, **«The Goal»** — фундамент TOC, лежащий в основе DDMRP
- Carol Ptak, Chad Smith, **«Orlicky's Material Requirements Planning»** (McGraw-Hill, 3-е изд.) — современное переиздание классики

### Статьи

- Carol Ptak, **«The Demand Driven Adaptive Enterprise»** — серия в DDI publications
- Industry Week — кейсы DDMRP

### Онлайн-ресурсы

- **Demand Driven Institute (DDI, demanddriveninstitute.com)** — официальная организация
- **B2Wise resources** — публикации по DDMRP
- **DDLeader.com** — кейсы внедрений

### Сертификации

- **CDDP (Certified Demand Driven Planner)** — DDI
- **CDDL (Certified Demand Driven Leader)** — продвинутая

### Кейсы

- **Polartec** — каноничный кейс DDMRP в текстиле
- **Vermeer Corporation** — manufacturing DDMRP
- **Российские:** появляются кейсы в FMCG, машиностроении
## Связанные документы

- [[index|Модуль 14: Planning]]
- [[../index|Education Index]]
- [[01-IBP-Connected-Planning|01 IBP]]
- [[../Other-methodologies/04-Theory-of-Constraints|TOC]]
