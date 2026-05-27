---
title: "04 — Capacity Planning"
aliases: ["Capacity Planning", "Little's Law", "Theory of Swift Even Flow", "Queueing"]
type: note
status: active
domain: education
module: 13-Operations-Excellence
tags: [education, capacity, queueing, littles-law, schmenner, theory-of-swift-even-flow]
created: 2026-05-19
updated: 2026-05-19
---

# 04 — Capacity Planning

> Capacity Planning (планирование мощностей) — это **балансирование** мощностей операций со спросом. Слишком мало мощности — потерянные продажи и недовольные клиенты; слишком много — замороженные инвестиции. Главные инструменты — Theory of Swift Even Flow (Schmenner), Queueing Theory + Little's Law.

## Карта раздела

![](attachments/diagrams/13-littles-law.svg)

## 1. Что такое capacity planning

### 1.1 Контекст

Capacity Planning — фундаментальная дисциплина operations. Каноничные книги — **Sunil Chopra, Peter Meindl, «Supply Chain Management»** (главы по capacity); **Steven Nahmias, «Production and Operations Analysis»** (учебник).

### 1.2 Три горизонта capacity planning

| Горизонт | Решения | Срок |
|----------|---------|------|
| **Strategic** (долгосрочный) | Новые заводы, склады, оборудование | 3-10 лет |
| **Tactical** (среднесрочный) | Изменение смен, найм/увольнения | 6 месяцев - 2 года |
| **Operational** (краткосрочный) | Назначение задач, расписание | Дни-недели |

### 1.3 Главные дилеммы

- **Lead strategy** — мощность опережает спрос (всегда есть избыток)
- **Lag strategy** — мощность догоняет спрос (всегда дефицит)
- **Match strategy** — точный баланс (рискованно)

В практике большинство компаний — гибрид с buffer-stock и аутсорсингом peaks.

**Ключевой вывод 1.** Capacity Planning — это **выбор между упущенной выгодой и замороженными инвестициями**. Нет «правильного ответа» — есть стратегический выбор.

## 2. Little's Law — закон Литтла

### 2.1 Формула

**Little's Law** (John D.C. Little, 1961) — фундаментальный закон queueing theory:

![](attachments/diagrams/13-littles-law.svg)

```
L = λ × W
```

Где:
- **L** — average number in system (среднее количество в системе)
- **λ** — arrival rate (скорость прихода, шт/час)
- **W** — average time in system (среднее время в системе)

### 2.2 Применение

Закон работает **универсально** — для любой системы с входом и выходом в steady state.

**Пример: склад.**
- Скорость прихода заказов λ = 100 заказов/час
- Среднее время обработки W = 4 часа
- → Среднее число заказов в системе (WIP) = 400

**Пример: e-commerce checkout.**
- Скорость прихода λ = 1000 покупателей/час
- Среднее время в воронке W = 6 минут = 0.1 часа
- → Среднее в воронке одновременно = 100

### 2.3 Главное следствие

При **постоянной throughput**:
- WIP ↓ → cycle time ↓
- WIP ↑ → cycle time ↑

Поэтому Lean фокусируется на снижении WIP (work in progress — незавершённого производства).

### 2.4 Использование в управлении

- **Анализ узких мест** — где WIP накапливается, там bottleneck
- **Прогноз impact** — как изменение спроса повлияет на cycle time
- **Размер буфера** — какой запас нужен для абсорбции вариативности

**Ключевой вывод 2.** Little's Law — простая, но мощная формула. Объясняет, **почему загрузить мощности на 100% невозможно** — cycle time стремится к бесконечности при λ → capacity.

## 3. Theory of Swift Even Flow

### 3.1 Контекст

**Roger Schmenner** (Indiana University) в 2000-х предложил теорию: операционная производительность определяется **скоростью и равномерностью** потока. Каноничная статья — **«Looking Ahead by Looking Back: Swift, Even Flow in the History of Manufacturing»** (Production and Operations Management, 2001).

### 3.2 Главный закон

**Productivity = Swift Flow × Even Flow**

- **Swift (быстрый)** — материалы / клиенты движутся через систему быстро
- **Even (равномерный)** — без variability, без stops, без всплесков

### 3.3 Где теряется производительность

Любая остановка / задержка / вариативность снижает производительность. Источники:

- **Variability** в спросе
- **Variability** в processing time
- **Setup times** (переналадки)
- **Breakdowns** (поломки)
- **Quality issues** (брак, переделка)
- **Capacity imbalances** (узкие места)

### 3.4 Связь с Lean и TPS

Theory of Swift Even Flow — академическое обоснование того, что Toyota делает практически:
- JIT (Just-In-Time — точно в срок) → swift flow
- Heijunka (выравнивание) → even flow
- Jidoka (автономизация) → quality at source → меньше variability
- TPM → меньше breakdowns

**Ключевой вывод 3.** Schmenner превратил «делайте как Toyota» в **измеримую теорию**. Productivity = f(speed, variability), и улучшение обеих повышает производительность кратно.

## 4. Queueing Theory — основы

### 4.1 Зачем queueing theory

Очереди везде: клиенты в магазине, заказы на складе, звонки в колл-центре, грузовики у дока. Queueing theory даёт **формулы** для прогноза:
- Сколько ждать в очереди
- Сколько серверов нужно
- Как распределить мощность

### 4.2 Базовая нотация Kendall

Очередь обозначается **A/B/c**:
- **A** — распределение прихода (M = Poisson, D = детерминистичное, G = общее)
- **B** — распределение обслуживания
- **c** — число серверов

Примеры:
- **M/M/1** — Poisson arrivals, exponential service, 1 server
- **M/M/c** — c серверов
- **G/G/c** — общий случай (требует симуляции)

### 4.3 Главные результаты

Для **M/M/1**:
- **Utilization** ρ = λ/μ (где μ — service rate)
- **Average WIP** L = ρ/(1-ρ)
- **Average wait** W = 1/(μ-λ)

При ρ → 1 (полная загрузка) L → ∞, W → ∞. Это математическое объяснение, почему **100% загрузка невозможна**.

### 4.4 Эмпирическое правило

В большинстве сервисных систем:
- Целевая загрузка **75-85%**
- Выше — резкий рост waits
- Ниже — недогрузка ресурсов

### 4.5 Современные инструменты

- **AnyLogic, Arena, Simul8** — симуляция queueing systems
- **Excel queueing калькуляторы** — для базовых M/M/c
- **R queueing package** — для аналитического анализа

**Ключевой вывод 4.** Queueing theory — математический фундамент capacity planning. Без её понимания решения принимаются «по интуиции», что обычно даёт либо перегрузку, либо избыточную мощность.

## 5. Capacity Planning на практике

### 5.1 Стандартный процесс

1. **Спрогнозировать спрос** (см. модуль 04.03)
2. **Оценить текущую capacity** (с учётом OEE)
3. **Identify gaps** — где capacity не хватает
4. **Сгенерировать варианты** — больше смен, новое оборудование, аутсорсинг, контракты с partner
5. **Финансовая оценка** — NPV каждого варианта (см. модуль 02.03)
6. **Выбрать оптимальный mix**
7. **Реализовать**

### 5.2 Главные KPI

- **Capacity utilization** — загрузка
- **Cycle time** — время прохождения заказа
- **Throughput** — пропускная способность
- **Service level** — % заказов в SLA

### 5.3 Балансирование 5 факторов

При выборе capacity strategy балансируем:
- Spend (CAPEX + OPEX)
- Service (cycle time, OTD)
- Quality
- Flexibility
- Risk

Optimal point зависит от стратегии (cost leader vs differentiator).

### 5.4 Adapting to volatility

Современные стратегии:
- **Flexible workforce** — staff augmentation
- **Modular capacity** — добавляемые блоки
- **Outsourcing peaks** — 3PL для пиков
- **Pricing as lever** — динамические цены для сглаживания спроса
- **Postponement** — отложенная финальная сборка

**Ключевой вывод 5.** Capacity Planning — это **continuous discipline**. Не «один раз спроектировали и забыли», а ежеквартальный пересмотр с реакцией на изменения.

## Применение для руководителя

| Целевая роль | Главные применения |
|--------------|---------------------|
| **COO** | Strategic capacity decisions; CAPEX-планирование |
| **Директор производства** | Tactical capacity; смены, найм |
| **Директор склада** | Capacity utilization; bottleneck analysis |
| **CFO** | NPV CAPEX-проектов; ROI capacity expansion |
| **Категорийный менеджер** | Влияние объёмов на capacity costs |

## Связь с другими модулями

- [[../04-Supply-Chain/02-Network-Design|Модуль 04: Network Design]] — где разместить capacity
- [[../04-Supply-Chain/04-Inventory-Management|Модуль 04: Inventory]] — buffer-stock vs capacity
- [[../02-Finance/03-Capital-decisions|Модуль 02: Capital Decisions]] — NPV capacity investments
- [[../14-Planning/index|Модуль 14: Planning]] — capacity в S&OP
- [[02-Reliability-Engineering|02 Reliability]] — OEE влияет на effective capacity

## Источники

### Книги (приоритет чтения)

- Steven Nahmias, **«Production and Operations Analysis»** (McGraw-Hill, 7-е изд.) — стандарт
- Wallace Hopp, Mark Spearman, **«Factory Physics»** (Waveland Press, 3-е изд. 2011) — глубокий queueing для производства
- Sunil Chopra, Peter Meindl, **«Supply Chain Management»** (Pearson) — capacity в supply chain
- Roger Schmenner, **«Service Operations Management»** (Wiley) — для services

### Статьи

- John Little, **«A Proof for the Queuing Formula L = λW»** (Operations Research, 1961)
- Schmenner, **«Looking Ahead by Looking Back»** (POM, 2001)
- HBR: **«Capacity Planning for the Long Term»**

### Онлайн-ресурсы

- **MIT OCW Operations Management** — бесплатные курсы
- **AnyLogic / Simul8 учебные материалы** — для симуляции
- **APICS / ASCM** — capacity в CSCP / CPIM

### Сертификации

- **APICS CPIM** — capacity planning внутри
- **MBA с Operations Management**

### Кейсы

- **Disney FastPass / Genie+** — queueing optimization в реальном мире
- **Amazon fulfillment scaling** — capacity planning at scale
- **Российские:** Wildberries pickup network capacity planning
## Связанные документы

- [[index|Модуль 13: Operations Excellence]]
- [[../index|Education Index]]
- [[03-Operations-Strategy|03 Operations Strategy]]
