---
title: "04 — Сравнение методологий планирования"
aliases: ["Planning Comparison", "Methodology Choice", "Hybrid Planning"]
type: note
status: active
domain: education
module: 14-Planning
tags: [education, planning, comparison, hybrid, maturity]
created: 2026-05-19
updated: 2026-05-19
---

# 04 — Сравнение методологий планирования

> После рассмотрения S&OP, IBP, DDMRP, Hoshin Kanri, MRP — главный вопрос: **что когда выбирать**? Этот раздел даёт сравнительную таблицу и руководство по построению **гибридной** системы планирования под конкретную компанию.

## Карта раздела

![](attachments/diagrams/14-planning-methodologies-comparison.svg)

## 1. Главное сравнение

### 1.1 Сводная таблица

![](attachments/diagrams/14-planning-methodologies-comparison.svg)

| Методология | Главная идея | Горизонт | Lean compatibility | Когда выбирать |
|-------------|--------------|----------|---------------------|----------------|
| **MRP / MRP II** | Material requirements от BOM | Weeks-months | Низкая | Стабильное производство |
| **S&OP** | Monthly cross-functional alignment | 12-24 мес | Средняя | Корпоративный стандарт |
| **IBP** | S&OP + Finance + Strategy | 24-36 мес | Средняя | Top 25 лидеры |
| **DDMRP** | Demand-driven pull через буферы | Days-weeks | Высокая | Volatile спрос |
| **Hoshin Kanri** | Strategic deployment X-Matrix | 3-5 лет + годовой | Очень высокая | Lean-зрелые |
| **TOC / DBR** | Drum-Buffer-Rope, узкие места | Days-weeks | Высокая | Bottleneck-driven |
| **OKR** | Quarterly objectives + KR | Quarter | Средняя | Tech / scale-ups |
| **OGSM** | One-pager strategy cascade | Annual | Низкая | FMCG corporate |
| **Agile / Scrum** | Sprint-based iteration | Weeks | Высокая | Software / R&D |
| **ZBB** | Budget from zero | Annual | Низкая | Cost transformation |

### 1.2 По индустриям

| Индустрия | Главные методологии |
|-----------|---------------------|
| **Manufacturing / Auto** | TPS, Hoshin Kanri, DDMRP, MRP |
| **FMCG / CPG** | S&OP, IBP, OGSM |
| **Tech / SaaS** | OKR, Agile, Connected Planning |
| **Retail / E-commerce** | S&OP, DDMRP, Connected Planning |
| **Pharma / Medical** | IBP, S&OP (с regulatory layer) |
| **Banking / Financial** | OKR, ZBB, OGSM |
| **Services** | Agile, OKR, Hoshin (для Lean services) |

### 1.3 По размеру компании

| Размер | Рекомендация |
|--------|--------------|
| **Startup** | OKR (квартальные циклы), Lean Canvas |
| **SMB (до $50M)** | S&OP базовый + OGSM |
| **Mid-market ($50M-1B)** | S&OP / IBP + OGSM / OKR |
| **Enterprise ($1B+)** | IBP + Hoshin Kanri + Connected Planning |
| **Top 25** | Connected Planning + IBP + Hoshin |

**Ключевой вывод 1.** Нет «лучшей» методологии — есть **подходящая под контекст**. Главные факторы: индустрия, размер, культура, зрелость.

## 2. Иерархия планирования — гибридный подход

### 2.1 Многослойная система

![](attachments/diagrams/14-planning-hierarchy.svg)

Зрелые компании используют **разные методологии на разных горизонтах**:

| Горизонт | Методология | Цель |
|----------|-------------|------|
| **5-10 лет** | Vision / Strategic Planning | Видение и долгосрочные цели |
| **3-5 лет** | Hoshin Kanri или OGSM | Стратегические цели и метрики |
| **1 год** | AOP / Annual Plan + Budget | Операционный план года |
| **12-24 мес** | IBP / S&OP | Месячное согласование |
| **3-12 мес** | MPS (Master Production Schedule) | График производства |
| **1-12 недель** | MRP / DDMRP | Материалы, закупки |
| **Дни-часы** | Scheduling / Dispatching | Операционные команды |
| **Квартально (cross-cutting)** | OKR (для tech-функций) | Квартальные цели |

### 2.2 Пример гибрида в крупной FMCG

- **Strategic:** Hoshin Kanri X-Matrix на 5 лет, корпоративно
- **Annual:** AOP + годовой OGSM
- **Tactical:** IBP с monthly cycle
- **Execution:** DDMRP в supply chain
- **Tech / Digital:** OKR для IT-проектов

Каждая методология **дополняет**, не конфликтует.

### 2.3 Anti-pattern: смешивание ради смешивания

Главная ошибка — внедрить все методологии сразу:
- OKR + S&OP + IBP + Hoshin одновременно
- Каждая требует ритуалов, отчётов
- Команда тонет в meetings

**Правило:** одна методология на горизонт. Если есть Hoshin для long-term — не добавляйте OGSM. Если есть IBP для месячного — не добавляйте классический S&OP отдельно.

**Ключевой вывод 2.** Гибрид — это **разные методологии для разных горизонтов**, не «всё сразу». Зрелые компании выбирают **1-2 на горизонт**.

## 3. Maturity Path

### 3.1 Эволюция компании

Типичный путь от стартапа к лидеру:

| Стадия | Размер | Методологии |
|--------|--------|-------------|
| **1. Стартап (0-50)** | OKR + Lean Canvas | Простота, скорость |
| **2. Growth (50-500)** | + S&OP базовый, OGSM | Структура |
| **3. Mature (500-5000)** | + IBP, кросс-функциональные процессы | Интеграция |
| **4. Scale (5000+)** | + Hoshin Kanri, Connected Planning | Зрелость |
| **5. Leader (Top 25)** | + AI-augmented, real-time | State-of-the-art |

### 3.2 Прыгать через стадии не стоит

Типичная ошибка — внедрить IBP в SMB. Не работает потому что:
- Нет инфраструктуры данных
- Нет культуры процессов
- Нет ресурсов для поддержки

Каждая стадия — **6-24 месяца зрелости** перед следующей.

### 3.3 Критические переходы

- **OKR → S&OP** — переход от tech-стиля к manufacturing
- **S&OP → IBP** — добавление финансов и стратегии
- **IBP → Connected Planning** — технологический скачок
- **Reactive → Hoshin** — культурный переход

**Ключевой вывод 3.** Maturity path — это **5-10-летний путь**. Лидеры (P&G, Toyota) проходили его 20-30 лет.

## 4. Выбор методологии — practical guide

### 4.1 Чек-лист выбора

Прежде чем выбрать методологию:

1. **Что мы решаем?**
   - Strategy deployment → Hoshin / OGSM
   - Operational alignment → S&OP / IBP
   - Execution speed → DDMRP / Agile
   - Goal setting → OKR

2. **Какая культура?**
   - Lean → Hoshin
   - Agile / Tech → OKR
   - Corporate / FMCG → OGSM / S&OP
   - Manufacturing → MRP / DDMRP

3. **Какой размер?**
   - Startup → OKR
   - Mid → S&OP
   - Enterprise → IBP

4. **Какая зрелость?**
   - Нет процесса → начать с базового
   - Зрелый → добавить продвинутый слой

### 4.2 Главные ошибки при выборе

- **«Toyota делает X — давайте мы тоже»** — игнорирование контекста
- **«У нас Excel — нам ничего больше не надо»** — недооценка инструмента
- **«Купим Anaplan — он всё решит»** — переоценка инструмента
- **«Всё сразу»** — внедрение 5 методологий одновременно

### 4.3 Pragmatic путь

Для большинства компаний:

1. **Year 1:** Базовый S&OP (5-step cycle, monthly)
2. **Year 2:** + Financial integration → IBP
3. **Year 3:** + Hoshin Kanri для strategy
4. **Year 4:** + DDMRP для execution
5. **Year 5+:** Platform (Anaplan / o9) и AI

Это **5-летний путь** к зрелой системе.

**Ключевой вывод 4.** Выбор методологии — **долгосрочное решение**. Менять методологию каждый год = не иметь методологии вообще.

## 5. Будущее планирования

### 5.1 Тренды 2024-2025

- **AI-augmented planning** — ML предсказывает, человек решает
- **Real-time** — заменяет ежемесячные циклы
- **Decentralization** — больше автономии командам
- **Sustainability layer** — ESG-метрики в планах
- **Scenario-based** — несколько сценариев вместо одного

### 5.2 Connected Planning как future

Anaplan / o9 / SAP IBP делают планирование:
- **Continuous** — не monthly batch
- **Cross-functional** — все функции в одной модели
- **What-if** — мгновенная симуляция
- **AI-driven** — машина предлагает, человек выбирает

К 2030-му году большинство Top 100 компаний будут на Connected Planning.

### 5.3 Что остаётся неизменным

- **Хорошая стратегия** — нужна всегда
- **Дисциплина процесса** — нельзя автоматизировать
- **Quality of leadership** — определяет всё
- **Cross-functional collaboration** — без AI не заменишь

**Ключевой вывод 5.** Технология меняется, **дисциплина планирования** — нет. Лучшие методологии работают и через 50 лет; меняется только реализация.

## Применение для руководителя

| Целевая роль | Главные применения |
|--------------|---------------------|
| **CEO** | Стратегический выбор главной методологии |
| **COO** | Гибрид tactical + execution |
| **CFO** | Связь planning с бюджетом |
| **CIO** | Платформенные решения |
| **Стратегический офис** | Архитектура планирования |

## Связь с другими модулями

- [[01-IBP-Connected-Planning|01 IBP]] — главная корпоративная
- [[02-DDMRP-Deep-Dive|02 DDMRP]] — execution layer
- [[03-Hoshin-Kanri-Strategic|03 Hoshin Kanri]] — strategic layer
- [[../SOP/index|S&OP подмодуль]]
- [[../Other-methodologies/index|Other-methodologies]]
- [[../17-Goal-Setting/index|Модуль 17: Goal Setting]] — OKR
- [[../02-Finance/05-Budgeting|Модуль 02.05: Budgeting]] — ZBB

## Источники

### Книги (приоритет чтения)

- Tom Wallace, Bob Stahl, **«Sales & Operations Planning: The How-To Handbook»** (3-е изд. 2010)
- Carol Ptak, Chad Smith, **«Demand Driven Material Requirements Planning»** (Industrial Press, 3-е изд. 2018)
- Yoji Akao, **«Hoshin Kanri»** (Productivity Press, 1991)
- Oliver Wight, **«Class A Standard for Business Excellence»** (Wiley)
- John Doerr, **«Measure What Matters»** (Portfolio, 2018) — OKR классика
- A.G. Lafley, Roger Martin, **«Playing to Win»** (HBR Press, 2013) — OGSM

### Статьи

- HBR: **«The Right Way to Plan Strategy»**
- McKinsey: **«From traditional to integrated business planning»**
- Gartner: **«Magic Quadrant for Supply Chain Planning»**

### Онлайн-ресурсы

- **APICS / ASCM** — стандарты
- **Oliver Wight Institute** — IBP
- **Demand Driven Institute** — DDMRP
- **Lean Enterprise Institute** — Hoshin

### Сертификации

- См. в специфических заметках 01-03

### Кейсы

- См. в специфических заметках 01-03
## Связанные документы

- [[index|Модуль 14: Planning]]
- [[../index|Education Index]]
- [[01-IBP-Connected-Planning|01 IBP]]
- [[02-DDMRP-Deep-Dive|02 DDMRP]]
- [[03-Hoshin-Kanri-Strategic|03 Hoshin Kanri]]
