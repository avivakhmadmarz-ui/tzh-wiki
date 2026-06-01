---
title: "DDMRP — Demand Driven Material Requirements Planning"
type: note
status: active
domain: education
module: Other-methodologies
aliases: 
updated: 2026-05-13
tags: [education, other-methodologies, ddmrp]
created: 2026-05-07
date created: 2026-05-07
date modified: 2026-05-13
---

# DDMRP — Demand Driven Material Requirements Planning

DDMRP — это методология планирования материалов, **разработанная как явная альтернатива классическому MRP**. Авторы — **Carol Ptak и Chad Smith**, выпустили первую версию в 2011 через Demand Driven Institute. Ключевая идея: вместо push'а на основе forecast — **pull'и через стратегические буферы в правильно выбранных точках цепочки**.

> **TL;DR для руководителя.** При длинном lead time (импорт из Китая, морская логистика 8-12 недель), волатильном спросе (beauty / fashion / промо) и постоянно врущем MRP в 1С / SAP — DDMRP подходит. Это не замена ERP, это **параметризация стратегии запасов**, которая накладывается поверх. Кейсы Coca-Cola Beverages Africa и Michelin показывают, что DDMRP даёт −20-30% inventory **при росте сервиса до 99%+**.

## Происхождение и контекст

- **2011** — Carol Ptak (бывший APICS president) и Chad Smith публикуют 1-е издание книги «Demand Driven Material Requirements Planning». Книга — продолжение и обновление Orlicky's MRP (3rd edition).
- **Demand Driven Institute (DDI)** — институт, который сертифицирует CDDP (Certified Demand Driven Planner) и CDDL (Leader). Аналог APICS для DDMRP-сообщества.
- **Эволюция мышления**: Carol Ptak пришла из MRP-мира, увидела ограничения, переработала в pull-парадигму. DDMRP формально опирается на 5 теоретических корней: MRP, DRP, Lean, ToC, Six Sigma и **innovation in decoupling**.
- **2017** — APICS / ASCM добавили DDMRP в свои body of knowledge (CPIM, CSCP).

![](attachments/diagrams/14-ddmrp-buffer-zones.svg)

## Пять компонентов DDMRP

### 1. Strategic Inventory Positioning (стратегическое размещение)

Где разместить decoupling points (точки развязки) в цепочке?

**Decoupling point** = точка, в которой ты держишь запас, чтобы развязать вариативность спроса (downstream) от вариативности поставки (upstream). Это «буфер» в цепочке, который разрезает push на pull.

Критерии выбора decoupling points:
- Длительность customer tolerance time vs cumulative lead time
- Variability входа и выхода
- Sales order visibility horizon
- Стоимость хранения vs стоимость лиц-out
- Стратегическая важность в цепочке (узкое место в смысле ToC — см. `[[04-Theory-of-Constraints|ToC]]`)

### 2. Buffer Profiles and Levels (буферные профили)

Каждый decoupling point получает **буфер**, разбитый на три зоны:

| Зона | Что означает | Как считается |
|------|--------------|---------------|
| **Green** | Норма — заказывать не нужно | ADU × Order cycle (или MOQ) |
| **Yellow** | Покрытие lead time | ADU × DLT (Decoupled Lead Time) |
| **Red** | Безопасность от вариативности | (Red base + Red safety), зависит от variability factor |

Где `ADU` = Average Daily Usage, `DLT` = Decoupled Lead Time.

**Buffer profile** = группировка SKU по похожим характеристикам (item type, lead time category, variability category). Внутри одного profile — общие правила расчёта.

### 3. Dynamic Adjustments (динамическая адаптация)

Буферы — не статичные. Они пересчитываются:
- **Recalculated adjustments** — при изменении ADU или DLT
- **Planned adjustments** — под промо, сезонность, NPI
- **Demand adjustments** — при выявленных трендах (рост/падение)

Это критическая разница с safety stock в MRP, который обычно «выставили и забыли».

### 4. Demand-Driven Planning (исполнение через Net Flow Equation)

Каждый день для каждого decoupled SKU считается:

```
Net Flow Position = On-Hand + On-Order – Qualified Sales Order Demand
```

«Qualified» = только spike-демонды (обычно: больше определённого порога в горизонте OST = Order Spike Threshold). Это отсекает шум.

Решение:
- Если Net Flow попадает в **Green zone** → не заказывать
- Если в **Yellow zone** → заказать «to top of green»
- Если в **Red zone** → срочный заказ + alert

<!-- IMG: Net Flow Equation diagram (on-hand + on-order − qualified demand) | https://www.demanddriveninstitute.com/_files/net-flow-equation.png -->

### 5. Visible and Collaborative Execution (визуальное исполнение)

После размещения заказа — мониторинг **on-hand status** в реальном времени по цветам зон. Дашборд показывает:
- Какие буферы в красном (необходим эскалейт)
- Какие в жёлтом (нормальное replenishment)
- Какие в зелёном (всё ок)

Это превращает 8 000 SKU в управляемое visual management.

## Кейсы с цифрами

### Michelin (шины)

- Внедрял DDMRP в нескольких заводах Европы.
- Результаты (по DDI publications): **service levels 99%+, inventory −20%** на decoupled SKU.
- Источник: Demand Driven Institute case studies, выступления Pascal Pennachio.

### Coca-Cola Beverages Africa (CCBA)

- Запустили DDMRP в 2019 в Намибии (через платформу Intuiflow от Demand Driven Technologies).
- До: classic forecast-driven MRP с постоянным firefighting.
- После: «leaner inventory, stronger service levels, freer working capital» — публичный case на demanddriventech.com.
- Сейчас раскатывают по другим африканским рынкам.

### Unilever Mexico

- DDMRP-pilot 2014-2016, опубликован Demand Driven Institute.
- Результаты: сокращение out-of-stock с ~10% до <2%, сокращение запасов на 30%, lead time компонентов −50%.

### LeTourneau Technologies (heavy equipment)

- Производство тяжёлого горного оборудования.
- DDMRP помогла справиться с extreme variability спроса в commodity-cycle.
- Результаты: rotating service level 95%+, reduction in expediting on 60%+.

### Across DDMRP implementations (DDI aggregate data)

Демон-дривен институт публикует агрегированные результаты:
- **Service levels:** 97-100%
- **Lead time reduction:** 25-50%
- **Inventory reduction:** 25%+
- **Expediting reduction:** значительное (вплоть до 70%)

## DDMRP vs MRP — ключевые различия

| Параметр | MRP | DDMRP |
|----------|-----|-------|
| Логика | Push (forecast-driven) | Pull (demand-driven) |
| База расчёта | MPS + BOM | Net Flow Equation в decoupling points |
| Запас «безопасности» | Safety stock (плоский) | Buffer (3 зоны, динамический) |
| Реакция на изменения | Recalculation каждой недели | Только когда Net Flow пересекает порог |
| Nervousness | Высокая | Низкая (буферы поглощают шум) |
| Forecast accuracy | Критично | Менее критично |
| Visibility | Через отчёты | Real-time visual (color-coded) |

## Когда DDMRP оправдан

- **Длинный lead time** (импорт, морская логистика) — твой beauty-кейс
- **Variability спроса** > 20-30% (CV: coefficient of variation)
- **Многоуровневый BOM** с компонентами разной критичности
- **Семисезонные продажи** или промо-driven рост
- **Long tail** SKU (10 000+) — не успеваешь forecast'ить каждый
- **Bullwhip effect** виден в цепочке

## Когда DDMRP **не** даст эффекта

- Стабильный спрос + короткий lead time (классический MRP справляется)
- Make-to-order бизнес без запасов готовой продукции
- Сервисные / project-based бизнесы (там нужен ToC + CCPM, см. `[[04-Theory-of-Constraints|ToC]]`)

## Платформы, поддерживающие DDMRP

- **Intuiflow / Replenishment+** (Demand Driven Technologies, флагман)
- **SAP IBP for Inventory** (DDMRP modules с 2019)
- **Microsoft Dynamics 365 SCM** (DDMRP support с 2020) — `[Buffer profile and levels — MS Learn](https://learn.microsoft.com/en-us/dynamics365/supply-chain/master-planning/planning-optimization/ddmrp-buffer-profile-and-levels)`
- **Oracle Demantra / SCM Cloud**
- **Kinaxis RapidResponse** (intuiflow integration)
- **B2Wise** — French DDMRP-native vendor
- **Slim4** (OMP-owned), **Streamline** — для SMB
- **1C: ERP** — частичная поддержка через AddOn

## Чеклист внедрения DDMRP (для руководителя)

- [ ] Определить 1-2 пилотных family / product line
- [ ] Найти decoupling points в цепочке (workshop с supply chain team)
- [ ] Считать ADU и DLT по реальным данным 12+ месяцев
- [ ] Сделать buffer profile-классификацию (по lead time, variability, item type)
- [ ] Параметрировать первые буферы (red/yellow/green)
- [ ] Запустить визуальный дашборд (можно начать с Excel/Power BI)
- [ ] Считать KPI: service level, inventory days, expediting count
- [ ] Через 3-6 месяцев — расширять

**Сертификация**: CDDP (Certified Demand Driven Planner) от DDI — 5 дней курс + экзамен. Для руководителя достаточно прочитать книгу и пройти CDDL (Leader).

## Связь с другими методологиями

- **DDMRP + S&OP / IBP**: тактический план в IBP, исполнение через DDMRP (см. `[[01-IBP-Integrated-Business-Planning|IBP]]`)
- **DDMRP vs MRP**: pull-альтернатива (см. `[[02-MRP-MRPII-ERP|MRP/MRP II/ERP]]`)
- **DDMRP + ToC**: decoupling points часто ставятся в bottleneck (см. `[[04-Theory-of-Constraints|ToC]]`)
- **DDMRP + Lean**: Kanban — это «pre-DDMRP» pull-сигнал (см. `[[../../13-Operations-Excellence/Lean/index|Lean]]`)
- В разделе сравнения `[[../../Compare/03-Combinations-that-work|Combinations that work]]` см. связку IBP+DDMRP

## Источники

- [Demand Driven Institute — DDMRP overview](https://www.demanddriveninstitute.com/ddmrp)
- [Demand Driven Institute — Case Studies](https://www.demanddriveninstitute.com/case-studies)
- [Demand Driven Tech — Coca-Cola Beverages Africa case](https://demanddriventech.com/case-studies/coca-cola-beverages-africa-ccba/)
- [Microsoft Learn — DDMRP buffer profile in Dynamics 365](https://learn.microsoft.com/en-us/dynamics365/supply-chain/master-planning/planning-optimization/ddmrp-buffer-profile-and-levels)
- [IFS Blog — Five steps of DDMRP](https://blog.ifs.com/2018/10/the-five-steps-of-ddmrp/)
- [B2Wise — DDMRP method in 5 steps](https://www.b2wise.com/the-ddmrp-method-in-5-steps-a-comprehensive-guide/)
- Ptak, C. & Smith, C. (2018). _Demand Driven Material Requirements Planning (DDMRP), Version 2_. Industrial Press.
- Ptak, C. & Smith, C. (2011). _Orlicky's Material Requirements Planning, 3rd Edition_. McGraw-Hill.
- Smith, C. (2016). _Demand Driven Performance: Using Smart Metrics_. McGraw-Hill.
