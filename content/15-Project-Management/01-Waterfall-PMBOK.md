---
title: "01 — Waterfall и PMBOK 7"
aliases: ["Waterfall", "PMBOK", "EVM", "Critical Path"]
type: note
status: active
domain: education
module: 15-Project-Management
tags: [education, project-management, waterfall, pmbok, pmi, evm]
created: 2026-05-19
updated: 2026-05-19
---

# 01 — Waterfall и PMBOK 7

> Waterfall — классический последовательный подход к управлению проектами. PMBOK (Project Management Body of Knowledge — свод знаний по управлению проектами) от PMI (Project Management Institute — институт управления проектами) — стандарт-учебник, 7-е издание (2021) представило переход от process-based к principles-based подходу. Этот раздел — фундамент PM.

## Карта раздела

![](attachments/diagrams/15-pmbok-knowledge-areas.svg)

## 1. Контекст Waterfall и PMBOK

### 1.1 Waterfall — история

**Waterfall** (водопад) — термин из статьи **Winston Royce** «Managing the Development of Large Software Systems» (1970). Идея — последовательное прохождение фаз: requirements → design → implementation → verification → maintenance.

Парадокс: Royce **критиковал** этот подход, считая его упрощённым. Но индустрия восприняла как стандарт.

### 1.2 PMBOK — стандарт PMI

**PMI** (Project Management Institute, основан 1969) — главная глобальная организация PM. PMBOK Guide — флагманский стандарт.

Эволюция:
- PMBOK 1-6 (1996-2017) — **process-based**, 49 процессов в 5 группах × 10 областей знаний
- **PMBOK 7 (2021)** — **principles-based**, переход к 12 принципам + 8 performance domains
- Включает Agile, hybrid, Waterfall — равноправно

### 1.3 Главный сдвиг PMBOK 7

PMBOK 7 признал: **проекты бывают разные**, и один процесс не подходит всем. Главный фокус — на **delivery value**, не на следовании процессу.

12 принципов:
1. Stewardship
2. Team
3. Stakeholders
4. Value
5. Systems thinking
6. Leadership
7. Tailoring
8. Quality
9. Complexity
10. Risk
11. Adaptability and resiliency
12. Change

**Ключевой вывод 1.** PMBOK 7 — переход от **«как делать»** к **«как думать»** о проектах. Современная редакция, совместимая с Agile.

## 2. 10 областей знаний

### 2.1 Полный список

![](attachments/diagrams/15-pmbok-knowledge-areas.svg)

PMBOK 6 (всё ещё актуально для PMP-экзамена):

1. **Integration** — интеграция всех частей
2. **Scope** — границы проекта
3. **Schedule** — сроки, critical path
4. **Cost** — бюджет, EVM
5. **Quality** — качество результата
6. **Resources** — команда и материалы
7. **Communications** — отчётность, stakeholders
8. **Risk** — управление рисками
9. **Procurement** — закупки
10. **Stakeholder** — управление стейкхолдерами

### 2.2 5 групп процессов

- **Initiating** — старт проекта (charter, stakeholder register)
- **Planning** — план (scope, schedule, budget, risks)
- **Executing** — выполнение (team, deliverables, communications)
- **Monitoring & Controlling** — контроль (variances, change requests)
- **Closing** — закрытие (lessons learned, final delivery)

49 процессов = 10 областей × 5 групп (упрощённо).

### 2.3 Главные артефакты

- **Project Charter** — устав проекта
- **Project Management Plan** — главный документ
- **WBS** (Work Breakdown Structure — иерархическая структура работ)
- **Schedule (Gantt chart)** — Gantt-диаграмма
- **Risk Register** — реестр рисков
- **Stakeholder Register** — реестр стейкхолдеров

**Ключевой вывод 2.** 10 областей знаний — **чек-лист**, который должен пройти любой проект, независимо от методологии (Waterfall, Agile, hybrid).

## 3. Critical Path и Schedule

### 3.1 Critical Path Method

**CPM** (Critical Path Method — метод критического пути) — техника поиска **самой длинной цепочки задач**, определяющей минимальный срок проекта.

Логика:
- Каждая задача имеет duration и зависимости
- Critical Path — задачи без slack (запаса)
- Любая задержка на CP = задержка всего проекта

### 3.2 PERT и оценка

**PERT** (Program Evaluation Review Technique — техника оценки и обзора программ) — статистическая оценка времени:

```
Expected time = (Optimistic + 4 × Most Likely + Pessimistic) / 6
```

Используется для проектов с неопределённой длительностью задач.

### 3.3 Современные инструменты

- **MS Project** — стандарт de-facto
- **Primavera** (Oracle) — для крупных проектов
- **Smartsheet, monday.com** — современные облачные
- **Jira с Advanced Roadmaps** — для смешанных
- **Российские:** Yandex.Tracker

**Ключевой вывод 3.** Critical Path — обязательное знание для любого PM. Без него управление сроками = угадывание.

## 4. EVM — Earned Value Management

### 4.1 Концепция

**EVM** (Earned Value Management — управление освоенным объёмом) — стандарт оценки прогресса проекта по **денежному выражению выполненной работы**.

Три базовых показателя:
- **PV** (Planned Value) — запланированная стоимость работы к дате
- **EV** (Earned Value) — фактическая стоимость выполненной работы
- **AC** (Actual Cost) — фактически потраченные деньги

### 4.2 Главные метрики

- **CV (Cost Variance)** = EV - AC. Если CV < 0 — перебор бюджета
- **SV (Schedule Variance)** = EV - PV. Если SV < 0 — отставание по графику
- **CPI (Cost Performance Index)** = EV / AC. Если CPI < 1 — превышение бюджета
- **SPI (Schedule Performance Index)** = EV / PV. Если SPI < 1 — отставание

### 4.3 Прогноз завершения

- **EAC (Estimate at Completion)** = BAC / CPI — прогноз финального бюджета
- **ETC (Estimate to Complete)** = EAC - AC — сколько ещё нужно потратить

### 4.4 Применение

EVM критичен для:
- Крупных контрактных проектов (defense, construction)
- Проектов с фиксированным бюджетом
- M&A integration
- ERP-внедрения

**Ключевой вывод 4.** EVM — единственная количественная методология контроля проекта. Без него «как у нас дела» = subjective opinions.

## 5. Risk Management

### 5.1 Risk register

Каждый риск:
- **Описание**
- **Probability** (1-5)
- **Impact** (1-5)
- **Risk Score** = P × I
- **Mitigation strategy** (4 стратегии: avoid / transfer / mitigate / accept)
- **Owner**

### 5.2 Стратегии митигации

- **Avoid** — устранить причину
- **Transfer** — передать (страховка, contracts)
- **Mitigate** — снизить probability или impact
- **Accept** — принять (с contingency plan)

### 5.3 Risk Triggers

Каждый риск имеет **trigger** (триггер) — событие, после которого риск активируется. Заранее определённый response plan.

**Ключевой вывод 5.** Risk management — главная защита проекта. Без risk register проект работает на удачу.

## 6. Когда Waterfall работает

### 6.1 Подходящие сценарии

- **Стабильные требования** — компания знает, что нужно
- **Compliance / regulatory** — нужна документация
- **Большой scope** — нужна полная картина заранее
- **External vendor contracts** — фиксированные scope/price
- **Construction / engineering** — физические ограничения

### 6.2 Не подходит

- Software development с эволюционирующими требованиями
- Innovation проекты
- Стартапы
- Когда заказчик не знает чего хочет

### 6.3 Hybrid подход

В современном мире — **Wagile**: Waterfall верхнего уровня, Agile в реализации. Стандарт для большинства крупных IT-проектов.

**Ключевой вывод 6.** Waterfall не «устарел» — он эволюционировал в hybrid. PMBOK 7 это признаёт.

## Применение для руководителя

| Целевая роль | Главные применения |
|--------------|---------------------|
| **COO** | EVM для крупных проектов; risk governance |
| **PMO Director** | PMBOK стандарты; обучение PMs |
| **CIO** | EVM для IT-проектов; risk register |
| **CFO** | EVM как финансовый контроль; budget compliance |
| **CEO** | Стратегические проекты через portfolio |

## Связь с другими модулями

- [[02-Agile-Scrum-Kanban|02 Agile]] — альтернативный подход
- [[04-Portfolio-PMO|04 Portfolio Management]]
- [[../12-ERP-Digital/01-ERP-Systems|Модуль 12.01: ERP]] — крупные проекты
- [[../22-Risk-BC/index|Модуль 22: Risk Management]] — углубление рисков
- [[../19-Org-Design-Change/index|Модуль 19: Change Management]]

## Источники

### Книги (приоритет чтения)

- PMI, **«PMBOK Guide 7th Edition»** (PMI, 2021) — стандарт
- Harold Kerzner, **«Project Management: A Systems Approach»** (Wiley, 13-е изд.) — учебник
- Andy Crowe, **«The PMP Exam: How to Pass on Your First Try»** (Velociteach, 8-е изд.) — для PMP
- Quentin Fleming, **«Earned Value Project Management»** (PMI, 4-е изд.)

### Сертификации

- **PMP** — главная сертификация
- **PRINCE2** — европейский стандарт
- **PMI-RMP** — Risk Management Professional
- **Российские:** «Project Manager» от ВШЭ, AIPM

### Кейсы

- **NASA Project Management** — публичные стандарты EVM
- **Boeing 787 Dreamliner** — каноничный антипример (см. модуль 12)
- **Olympics Games preparation** — масштабное PM
## Связанные документы

- [[index|Модуль 15: PM]]
- [[../index|Education Index]]
- [[02-Agile-Scrum-Kanban|02 Agile]]
