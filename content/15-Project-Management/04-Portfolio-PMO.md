---
title: "04 — Portfolio Management и PMO"
aliases: ["Portfolio Management", "PMO", "Program Management"]
type: note
status: active
domain: education
module: 15-Project-Management
tags: [education, project-management, portfolio, pmo, governance]
created: 2026-05-19
updated: 2026-05-19
---

# 04 — Portfolio Management и PMO

> Portfolio Management — это **управление совокупностью проектов** компании: какие запускать, какие останавливать, как приоритизировать. PMO (Project Management Office — офис управления проектами) — структура, обеспечивающая стандарты и governance. Этот раздел — про корпоративный уровень PM.

## Карта раздела

![](attachments/diagrams/15-portfolio-management.svg)

## 1. Иерархия: Project / Program / Portfolio

### 1.1 Три уровня

![](attachments/diagrams/15-portfolio-management.svg)

- **Project** — временное усилие для уникального результата (1-12 месяцев типично)
- **Program** — связанные проекты с общими целями (1-3 года)
- **Portfolio** — все программы и проекты компании

### 1.2 Главные различия

| Аспект | Project | Program | Portfolio |
|--------|---------|---------|-----------|
| **Цель** | Конкретный deliverable | Strategic outcome | Maximize value |
| **Срок** | Defined | 1-3 года | Continuous |
| **Менеджер** | Project Manager | Program Manager | Portfolio Manager |
| **Метрики** | On-time, budget, scope | Benefits, outcomes | ROI, alignment |
| **Управление** | Tactical | Strategic | Strategic |

**Ключевой вывод 1.** Три уровня требуют **разных компетенций**. Хороший PM — не обязательно хороший Portfolio Manager.

## 2. Portfolio Management

### 2.1 Концепция

Каноничная книга — **PMI, «The Standard for Portfolio Management»** (4-е изд. 2017). Цель portfolio management — **максимизировать value** компании через правильный выбор проектов.

### 2.2 Шесть процессов

1. **Identification** — все потенциальные проекты
2. **Categorization** — группировка (strategic / cost-saving / regulatory)
3. **Evaluation** — оценка ценности и риска
4. **Selection** — выбор подмножества
5. **Prioritization** — порядок выполнения
6. **Authorization** — формальное одобрение

### 2.3 Selection criteria

Главные критерии оценки проекта:

- **Strategic alignment** — соответствие стратегии
- **Financial value** — NPV, IRR, payback (см. модуль 02.03)
- **Risk** — вероятность успеха
- **Resource availability** — есть ли люди и деньги
- **Dependencies** — связи с другими проектами

### 2.4 Portfolio Balance

Хороший portfolio балансирует:
- **Strategic vs operational** проекты
- **Short-term vs long-term** results
- **Low-risk vs high-risk**
- **Different business units / functions**

Часто используется матрица типа BCG: high-impact / low-impact × high-risk / low-risk.

**Ключевой вывод 2.** Portfolio Management — **отдельная дисциплина** от PM. Главная компетенция — selection и stopping, не execution.

## 3. PMO — Project Management Office

### 3.1 Типы PMO

| Тип | Функция |
|-----|---------|
| **Supportive** | Templates, training, advice |
| **Controlling** | Standards, compliance, audit |
| **Directive** | Direct management проектов |

### 3.2 Главные функции PMO

- **Methodology** — стандарты PM в компании
- **Training** — обучение PMs
- **Tools** — MS Project, Jira, Azure DevOps
- **Reporting** — portfolio dashboards
- **Governance** — selection и review
- **Best practices** — lessons learned, templates

### 3.3 Когда PMO нужен

- **>10 проектов одновременно**
- **Низкая дисциплина PM**
- **Регуляторные требования**
- **M&A integration** проекты
- **Digital transformation**

### 3.4 PMO anti-patterns

- **Bureaucracy без value** — PMO как paper-pusher
- **Ивора-башня** — disconnected от бизнеса
- **Слишком много standards** — деморализация PMs
- **Без executive sponsor** — игнорируется

**Ключевой вывод 3.** PMO работает, если **создаёт value**, а не только compliance. Зрелый PMO — coach, не контролёр.

## 4. Governance

### 4.1 Steering Committee

Для каждого крупного проекта / программы — **Steering Committee** (управляющий комитет):
- Executive sponsor (CEO / COO)
- Business owners
- IT / functional leads
- Финансовый представитель

Встречается ежемесячно для review и принятия решений.

### 4.2 Stage Gates

Между фазами проекта — **stage gates** (контрольные точки):
- Gate 1 — Charter approval
- Gate 2 — Design / blueprint approval
- Gate 3 — Build approval
- Gate 4 — Go-live approval
- Gate 5 — Closure

На каждом gate — решение **GO / NO-GO / RE-PLAN**.

### 4.3 Portfolio Review

Ежеквартально:
- Все проекты status
- Performance vs plan
- Selection corrections (stop / start)
- Resource reallocation

**Ключевой вывод 4.** Governance — фрейм для **decision-making**. Без него проекты живут «своей жизнью», без стратегического согласования.

## 5. Stopping Bad Projects

### 5.1 Sunk cost fallacy

Главная проблема — продолжать **failing projects** только потому, что «уже потрачено».

Каноничный кейс — Concorde (отсюда «Concorde fallacy»).

### 5.2 Когда останавливать

- ROI не подтверждается
- Технологически невозможно
- Рыночные условия изменились
- Лучшая альтернатива появилась
- Команда не достигает прогресса

### 5.3 Как останавливать

- **Pre-mortem** перед началом — что бы означало «провал»?
- **Kill criteria** в charter
- **Regular reviews** с независимыми участниками
- **No-blame culture** для остановки — это нормально

**Ключевой вывод 5.** Остановка failing project — **сложнее**, чем запуск. Зрелые компании имеют culture, поощряющую raising concerns.

## Применение для руководителя

| Целевая роль | Главные применения |
|--------------|---------------------|
| **CEO** | Portfolio decisions; sponsor крупных программ |
| **COO** | Portfolio review; PMO governance |
| **CIO** | IT portfolio; balancing run vs change |
| **CFO** | Financial value tracking; budget allocation |
| **PMO Director** | Полный набор: стандарты, обучение, governance |

## Связь с другими модулями

- [[01-Waterfall-PMBOK|01 Waterfall]] — методология для проектов
- [[02-Agile-Scrum-Kanban|02 Agile]] — для tech-проектов
- [[../02-Finance/03-Capital-decisions|Модуль 02.03: Capital]] — NPV для selection
- [[../14-Planning/index|Модуль 14: Planning]] — strategy → portfolio

## Источники

### Книги (приоритет чтения)

- PMI, **«The Standard for Portfolio Management»** (4-е изд. 2017)
- Harvey Levine, **«Project Portfolio Management»** (Jossey-Bass, 2005)
- John Knutson, **«Project Management for Business Professionals»** (Wiley)
- Geoff Reiss, **«Programme Management Demystified»** (Routledge)

### Сертификации

- **PMI-PfMP (Portfolio Management Professional)**
- **PgMP (Program Management Professional)**
- **MoP (Management of Portfolios)** — UK стандарт

### Кейсы

- **GE Six Sigma как portfolio** — публичные доклады
- **3M innovation portfolio** — каноничный
- **Российские:** Сбер trans-формация, Yandex проектная культура
## Связанные документы

- [[index|Модуль 15: PM]]
- [[../index|Education Index]]
- [[../02-Finance/03-Capital-decisions|Capital Decisions]]
