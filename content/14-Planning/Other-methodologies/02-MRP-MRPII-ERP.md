---
title: "MRP / MRP II / ERP — историческая линия систем планирования"
type: note
status: active
domain: education
module: Other-methodologies
aliases: 
updated: 2026-05-13
tags: [education, other-methodologies, mrp, erp]
created: 2026-05-07
date created: 2026-05-07
date modified: 2026-05-13
---

# MRP / MRP II / ERP — историческая линия систем планирования

Линия MRP → MRP II → ERP — это **корни всех современных систем управления производством и закупками**. Внутри SAP, 1C: УПП, Oracle Cloud ERP, Microsoft Dynamics 365 живёт алгоритм, который Joseph Orlicky сформулировал в IBM в 1964 году. Понимание этой линии нужно не для ностальгии, а чтобы видеть **ограничения push-логики**, которые DDMRP пытается решить (см. `[[03-DDMRP-Demand-Driven|DDMRP]]`).

> **TL;DR для руководителя.** MRP-логика отвечает на вопрос «что заказать, сколько и когда». Она работает при стабильном BOM (Bill of Materials — спецификация материалов) и предсказуемом спросе. На быстро меняющихся рынках (beauty, fashion, импорт с длинным lead time) push-логика начинает сыпаться: либо overstock, либо out-of-stock.

## Эволюция: MRP I → MRP II → ERP

| Период | Система | Кто | Что добавилось | Ограничение |
|--------|---------|-----|----------------|-------------|
| **1960-е** | **MRP I** (Material Requirements Planning) | Joseph Orlicky, IBM (1964) | Расчёт потребности в материалах из BOM + MPS | Только материалы, не учитывает мощности |
| **1980-е** | **MRP II** (Manufacturing Resource Planning) | Oliver Wight (1983) | + Capacity planning, finance, master scheduling, замкнутый цикл (closed-loop) | Только производство, не охватывает HR/Finance/CRM |
| **1990-е+** | **ERP** (Enterprise Resource Planning) | SAP (R/3, 1992), Oracle, JD Edwards, Baan | + HR, Finance, CRM, Logistics, единая БД | Тяжеловесность, push-логика остаётся внутри |
| **2010-е+** | **Cloud ERP** | Oracle Cloud, SAP S/4HANA, Microsoft Dynamics 365, NetSuite, Workday | + Облако, real-time analytics, AI | Не решает philosophical-проблему push vs pull |

<!-- IMG: Closed-loop MRP II diagram (BPS → SOP → MPS → MRP → CRP → execution → feedback) | https://en.wikipedia.org/wiki/File:MRP_II.svg -->

## MRP I — материнский алгоритм

**Joseph Orlicky** (engineer в IBM) в 1964 формализовал логику расчёта потребностей. Книга «Material Requirements Planning» (1975) стала библией. К 1975 — 700 компаний внедрили MRP, к 1981 — 8 000.

### Что MRP I делает

Берёт три входа:
- **MPS** (Master Production Schedule) — что и когда производить
- **BOM** (Bill of Materials) — из чего состоит каждый продукт, дерево компонентов
- **Inventory data** — что уже есть на складе, что в пути

И **раскладывает** через explosion (взрыв спецификации) до уровня каждой детали:
- Сколько нужно
- Когда нужно (с учётом lead time)
- Когда заказать (offset back from need date)

### Ограничения MRP I

- **Не учитывает мощности** — может «попросить» 10 000 деталей за неделю, когда станок физически даёт 5 000
- **Push-логика** — план рождается из forecast, а не из реального спроса
- **Чувствителен к изменениям** — пересчёт каскадно меняет всю цепочку (nervousness, system nervousness)
- **Игнорирует variability** — считает lead time константой

## MRP II — добавили мощности и финансы

**Oliver Wight** в 1983 году расширил MRP до **Manufacturing Resource Planning** (специально оставил аббревиатуру MRP II, чтобы не ломать узнавание). Ключевые добавления:

- **Capacity Requirements Planning (CRP)** — проверка, влезает ли план в мощности
- **Rough-Cut Capacity Planning (RCCP)** — быстрая проверка на уровне MPS
- **S&OP integration** — MRP II встроил S&OP-цикл как «крышу» над MPS (см. `[[../SOP/index|S&OP]]`)
- **Финансовый слой** — план в материалах превращается в план в деньгах
- **Closed-loop** — feedback от execution возвращается в planning

Oliver Wight также ввёл **Class A maturity model** — где «Class A» = «ваша MRP II работает корректно, плановая дисциплина высокая, ABC-точность данных >95%».

## ERP — расширение до всей компании

В 1990-х **SAP, Oracle, JD Edwards, Baan, PeopleSoft** расширили MRP II за пределы производства, включив:

- HR / Payroll
- General Ledger / Accounts Payable / Accounts Receivable
- CRM (хоть Salesforce и победил отдельно)
- Sales / Distribution
- Procurement
- Project management

Идея — **единая база данных** для всего предприятия. Запись попала в один модуль — видна везде.

### Современные ERP-лидеры (2026)

| Решение | Сегмент | Сильные стороны |
|---------|---------|-----------------|
| **SAP S/4HANA** | Enterprise | Глобальный стандарт, особенно для производства; in-memory HANA database |
| **Oracle Cloud ERP / Fusion** | Enterprise | Финансы, public sector |
| **Microsoft Dynamics 365** | Mid-market + enterprise | Лучшая интеграция с MS-стеком; F&O для производства, BC для SMB |
| **Oracle NetSuite** | Mid-market, SaaS-companies | Cloud-native, быстрое внедрение |
| **Infor CloudSuite** | Manufacturing, distribution | Отраслевые конфигурации |
| **Epicor / IFS / Sage** | Mid-market manufacturing | Нишевые лидеры |
| **1C:ERP / 1C:УПП** | Россия / СНГ | Локализация, бухучёт |

### Cloud ERP — что нового

С 2015+ происходит миграция on-premise → cloud:
- **SaaS deployment** (NetSuite, Dynamics 365 BC) — не нужен IT-департамент для серверов
- **Real-time analytics** через embedded BI
- **AI / ML** — прогнозирование спроса, anomaly detection в платежах
- **API-first** — интеграция с e-commerce, логистикой, банками

## Ограничения push-логики MRP

Это критическая часть для понимания, **почему появились DDMRP, Lean, ToC**:

1. **Variability убивает план** — реальный спрос не равен прогнозу, реальный lead time не равен plan-time
2. **Bullwhip effect** — небольшое колебание спроса в downstream усиливается вверх по цепочке
3. **System nervousness** — пересчёт каждую неделю меняет приоритеты, ломает execution
4. **Локальные оптимумы** — каждое подразделение выполняет «свой» MRP-план, без видения целого
5. **Forecast зависимость** — чем длиннее lead time, тем хуже forecast (а его и закладываем)

Это и пытается решить **DDMRP** через pull-логику и buffer profiles — `[[03-DDMRP-Demand-Driven|см. отдельную заметку]]`.

## Кейсы

### SAP внедрения

- Mars (FMCG): глобальный SAP-rollout 2010-х
- Walmart: микс ERP-систем, основной — Oracle
- Apple: Oracle Cloud ERP (с миграции с SAP)
- Российские: ЛУКОЙЛ, Газпром, Сбер исторически на SAP, но с 2022 — миграции на 1С/российские

### Microsoft Dynamics 365 внедрения

- Coca-Cola Bottlers (некоторые)
- BMW (часть глобального ландшафта)
- HP Inc.

### Известные провалы ERP-внедрений (важно учитывать)

- **Hershey 1999** — провал SAP внедрения накануне Halloween, потеряли $100M+ продаж
- **Nike 2001** — i2 / SAP problems, потеряли ~$100M
- **HP 2004** — миграция SAP стоила квартал и ~$160M
- **National Grid** — 2012-2014, $585M overrun на SAP
- Урок: ERP-внедрение — это **business transformation**, а не IT-проект

## Что это значит для руководителя

### При работе с MRP / ERP-системой (SAP, 1С: УПП, NetSuite)

- Внутри — push-логика. При volatile demand или импорте forecast'у нельзя доверять вслепую
- ABC/XYZ-классификация SKU критична: для AX — по MRP, для CZ — иначе
- Master Data — фундамент. Грязные BOM = грязный план

### При выборе ERP

- SMB до 200 человек: Microsoft Dynamics 365 BC, NetSuite, 1С: Предприятие
- Mid-market 200-2000: Dynamics 365 F&O, NetSuite, Infor, Epicor
- Enterprise 2000+: SAP S/4HANA, Oracle Cloud ERP

### Для highly volatile или import-heavy бизнеса (например, beauty-сегмент)

- Опираться только на MRP недостаточно — нужен DDMRP layer (см. `[[03-DDMRP-Demand-Driven|DDMRP]]`)
- Buffer-based replenishment важнее MRP-калькуляций для топ-SKU
- Forecasting горизонт сокращается, demand sensing критичен

## Связь с другими методологиями

- **MRP II → S&OP**: S&OP родился внутри MRP II как executive-крыша (см. `[[../SOP/index|S&OP]]`)
- **MRP vs DDMRP**: DDMRP — pull-альтернатива (см. `[[03-DDMRP-Demand-Driven|DDMRP]]`)
- **MRP vs Lean**: TPS отказывается от MRP в favor of Kanban-pull (см. `[[../../13-Operations-Excellence/Lean/index|Lean]]`)
- **ERP + IBP**: SAP IBP надстраивается над S/4HANA (см. `[[01-IBP-Integrated-Business-Planning|IBP]]`)

## Источники

- [Joseph Orlicky: Hero of MRP — QAD Blog](https://www.qad.com/blog/2018/05/joseph-orlicky-hero-materials-requirements-planning)
- [Material Requirements Planning — Wikipedia](https://en.wikipedia.org/wiki/Material_requirements_planning)
- [MRP vs MRP II vs ERP — User Solutions](https://usersolutions.com/blog/mrp-vs-mrp2-vs-erp)
- [Difference Between MRP and MRP II — Brightwork Research](https://www.brightworkresearch.com/mrp-ii-oliver-wight/)
- [The Evolution of ERP Systems — Addovation](https://www.addovation.com/blog/the-evolution-of-erp-systems/)
- [From BOMP to SaaS — e2b teknologies](https://e2btek.com/bomp-saas-beyond-1960s/)
- Orlicky, J. (1975). _Material Requirements Planning_. McGraw-Hill.
- Wight, Oliver (1984). _Manufacturing Resource Planning: MRP II_. Oliver Wight Publications.
- Plossl, G. (1995). _Orlicky's Material Requirements Planning_, 2nd ed.
