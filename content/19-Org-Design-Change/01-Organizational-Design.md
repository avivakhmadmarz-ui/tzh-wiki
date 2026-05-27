---
title: "01 — Organizational Design"
aliases: ["Organizational Design", "Star Model", "Galbraith", "McKinsey 7S", "Two-Pizza Teams", "Span of Control", "Holacracy", "Matrix Organization"]
type: note
status: active
domain: education
module: 19-Org-Design-Change
tags: [education, org-design, galbraith, mckinsey-7s, two-pizza-teams, matrix, holacracy]
created: 2026-05-26
updated: 2026-05-26
---

# 01 — Organizational Design

> Organizational Design (организационное проектирование) — практика создания структуры компании, которая **поддерживает её стратегию**. Главный закон — **Conway's Law**: системы повторяют структуру организаций, их создающих. Поэтому неправильная структура — это **архитектурный долг**, который дороже технического. Эта заметка систематизирует: Star Model (Jay Galbraith), McKinsey 7S, основные архетипы (functional / divisional / matrix / network / holacracy), параметры дизайна (span of control, centralization), современные подходы (Two-Pizza Teams от Amazon).

## Карта раздела

![](attachments/diagrams/19-star-model.svg)

## 1. Conway's Law — фундаментальный принцип

### 1.1 Что это

**Conway's Law** (Melvin Conway, 1968):

> «Любая организация, проектирующая систему, неизбежно создаст дизайн, структура которого копирует структуру коммуникаций организации».

Изначально про software systems, но применимо к любым artifacts: продукты, процессы, организации.

Следствие: **изменение системы требует изменения организации**, и наоборот.

### 1.2 Inverse Conway Maneuver

**Inverse Conway** — сознательная **перестройка организации**, чтобы её структура соответствовала **желаемой архитектуре системы**.

Пример: если компания хочет microservices-архитектуру, она должна быть организована как **малые автономные команды**, а не как большой монолитный отдел разработки.

## 2. Star Model — Jay Galbraith

### 2.1 Концепция

**Jay Galbraith** (1939-2014) — профессор Wharton, основатель Center for Effective Organizations. Книга **«Designing Organizations»** (Jossey-Bass, 3-е изд. 2014) — каноничная.

Главная идея: организация — это **сбалансированное взаимодействие 5 элементов** в виде звезды:

![](attachments/diagrams/19-star-model.svg)

1. **Strategy (стратегия)** — куда движемся?
2. **Structure (структура)** — как сгруппированы люди и работа?
3. **Processes (процессы)** — как передаётся информация и решения?
4. **Rewards (награды)** — за что поощряем?
5. **People (люди)** — кого нанимаем и развиваем?

**Главное правило:** все 5 элементов должны быть **согласованы** друг с другом. Несогласованность хотя бы одного → разрушение всей системы.

### 2.2 Strategy → Design

Стратегия задаёт **дизайн-критерии**:
- **Growth strategy** → нужна гибкая структура для масштабирования
- **Cost leadership** → нужна централизованная структура для эффективности
- **Differentiation** → нужна децентрализованная для innovation
- **Customer intimacy** → нужна organization по клиентским сегментам

### 2.3 Структурные выборы

Galbraith выделяет 5 главных структурных выборов:

1. **By function** (маркетинг, продажи, IT) — эффективность через специализацию
2. **By product** (Brand A, Brand B) — фокус на продуктовом результате
3. **By geography** (Europe, Asia) — адаптация к локальным рынкам
4. **By customer segment** (Enterprise, SMB, Consumer) — близость к клиенту
5. **By process** (Procure-to-Pay, Order-to-Cash) — потоковая ориентация

Главное правило: **выбирать по доминирующей бизнес-логике**. Если главное — продуктовая дифференциация — by product. Если эффективность — by function.

**Ключевой вывод 1.** Star Model — **диагностический инструмент**. При проблемах с организацией начинать с проверки: какой элемент звезды не согласован?

## 3. McKinsey 7S

### 3.1 Концепция

**McKinsey 7S** — модель, разработанная **Tom Peters и Robert Waterman** для McKinsey & Company в 1980-х. Книга **«In Search of Excellence»** (Harper & Row, 1982).

![](attachments/diagrams/19-mckinsey-7s.svg)

7 элементов организации:

**Hard S's (структурные):**
1. **Strategy** — куда движемся?
2. **Structure** — как организованы?
3. **Systems** — какие процессы и системы?

**Soft S's (культурные):**
4. **Style** — как мы решаем? (лидерский стиль)
5. **Staff** — кто мы? (команда)
6. **Skills** — что умеем? (компетенции)

**Связующий элемент:**
7. **Shared Values** — что нас связывает? (культура)

### 3.2 Главные принципы

- **Все 7 элементов взаимосвязаны** — изменение одного требует изменения других
- **Shared Values в центре** — без них структурные элементы не работают
- **Soft S's важнее, чем кажется** — culture eats strategy for breakfast (Drucker)

### 3.3 Применение

McKinsey 7S используется для:
- **Диагностики** — где в организации misalignment?
- **Слияний и поглощений** — оценка culture fit
- **Трансформаций** — какие элементы нужно изменить?

## 4. Organizational Archetypes

### 4.1 Functional (по функциям)

![](attachments/diagrams/19-org-archetypes.svg)

Группировка по специализации: Marketing, Sales, Engineering, Finance, HR.

**Плюсы:**
- Глубокая экспертиза в функции
- Эффективность через специализацию
- Карьерный рост ясен

**Минусы:**
- Silos (изоляция функций друг от друга)
- Медленная координация между функциями
- Конфликты функциональных приоритетов

**Когда применяется:** молодые компании, стабильные индустрии, единый продукт.

### 4.2 Divisional (по дивизионам)

Группировка по продукту, географии, клиентскому сегменту.

**Плюсы:**
- Автономия дивизионов
- Фокус на продуктовом / клиентском результате
- Ясная P&L по дивизиону

**Минусы:**
- Дублирование функций (HR в каждом дивизионе)
- Конкуренция между дивизионами за ресурсы
- Сложно делиться knowledge

**Когда применяется:** крупные диверсифицированные корпорации (GE, P&G, Coca-Cola).

### 4.3 Matrix (матричная)

Сотрудник имеет **двух руководителей**: функционального (например, Engineering Manager) и проектного (Product Manager).

**Плюсы:**
- Гибкость — ресурсы перераспределяются между проектами
- Двойная экспертиза (функциональная + проектная)
- Эффективное использование специалистов

**Минусы:**
- Конфликты между двумя руководителями
- Сложность отчётности
- Подчинённые часто перегружены

**Когда применяется:** консалтинг, R&D, проектные организации.

### 4.4 Network

Компания как **платформа узлов**, без чёткой иерархии. Узлы — autonomous teams, partnerships, agencies.

**Плюсы:**
- Высокая гибкость
- Низкие фиксированные costs
- Доступ к специализированным навыкам

**Минусы:**
- Сложная координация
- Knowledge management
- Контроль качества

**Когда применяется:** entertainment, fashion, software (open source).

### 4.5 Holacracy / Sociocracy

**Holacracy** — система без формальной иерархии, разработанная Brian Robertson (HolacracyOne) в 2007. Используется в Zappos (внедрено в 2013, частично откатано в 2020) и других.

Главные принципы:
- Решения принимают **circles** (круги команд)
- **Lead Links** — координаторы кругов, не «менеджеры»
- **Tactical meetings** — еженедельные оперативные синки
- **Governance meetings** — изменение структуры

**Плюсы:**
- Высокая вовлечённость
- Гибкость структуры
- Чёткие правила принятия решений

**Минусы:**
- Сложно масштабировать (>100-200 чел.)
- Долгое обучение
- Может ощущаться как «бюрократия наоборот»

### 4.6 Two-Pizza Teams (Amazon)

**Two-Pizza Teams** — принцип Amazon (Jeff Bezos, начало 2000-х): команда должна быть **не больше**, чем можно накормить **двумя пиццами** (6-10 человек).

**Single-Threaded Leader** — один человек, **полностью** фокусирующийся на одной задаче / продукте. Не делит внимание между несколькими.

**Плюсы:**
- Высокая автономия
- Быстрые решения
- Чёткая ответственность

**Минусы:**
- Координация между командами требует усилий
- Не подходит для очень крупных проектов

**Когда применяется:** tech-компании, scale-up, R&D.

## 5. Параметры дизайна

### 5.1 Span of Control (норма управляемости)

**Span of Control** — сколько прямых подчинённых у одного руководителя.

| Span | Описание | Применение |
|---|---|---|
| **3-5** | Tight (тесный) | Военные, регулируемые, сложные адаптивные задачи |
| **5-9** | Medium (средний) | Большинство компаний; «оптимальная» норма по психологическим исследованиям |
| **10-15** | Wide (широкий) | Современные tech-компании, IC-роли, низкая координация |
| **15-30+** | Very wide (очень широкий) | Только для administrative или delegated работ |

Правило: чем **сложнее задачи** и чем **больше координации** нужно, тем **уже** span должен быть.

### 5.2 Centralization vs Decentralization

**Centralization (централизация)** — решения принимаются на верху, тиражируются вниз.

Плюсы: единообразие, экономия масштаба, контроль.
Минусы: медленность, не учитывает local context.

**Decentralization (децентрализация)** — решения принимаются на местах.

Плюсы: скорость, адаптивность, ownership.
Минусы: дублирование, фрагментация стандартов.

**Reality:** большинство компаний имеют **смешанную** модель — что-то централизовано (бренд, финансы), что-то децентрализовано (операции, продажи).

### 5.3 Layers — количество уровней иерархии

**Flat organization** — 3-4 уровня от CEO до individual contributor.

**Tall organization** — 7-10+ уровней.

Современный тренд — **flattening** (уплощение). Причины:
- Тech enables: communication tools, transparency
- Speed: меньше уровней = быстрее решения
- Cost: меньше middle managers
- Talent: senior IC ценятся как leaders

Кейс: Google имеет 5-6 уровней для 150K+ сотрудников. Microsoft под Балмером имел 12+ уровней; Наделла сократил до 7-8.

## 6. Tradeoffs дизайна

### 6.1 Efficiency vs Agility

**Efficiency** — оптимизация процессов, scale, repeatability.
**Agility** — скорость адаптации к изменениям.

Старая модель — efficiency через стандартизацию (Ford, McDonald's).
Современная — agility через автономные команды (Spotify, Amazon).

В реальности — **разные часть компании требуют разного**:
- Core operations (supply chain, finance) — efficiency
- Customer-facing / product — agility

### 6.2 Specialization vs Generalization

**Specialization:** глубокая экспертиза, но silos.
**Generalization:** широкая компетенция, но поверхностная.

Большинство компаний нуждается в **обоих** — T-shaped people (deep + broad).

### 6.3 Standardization vs Customization

Чем более стандартизованы процессы, тем эффективнее, но менее customised под local context. Glob ↔ local trade-off.

## 7. Реальные кейсы

### 7.1 GE — Welch era

Под Уэлчем (1981-2001) — **decentralized matrix** с сильной central HR. Каждый дивизион имеет автономию, но 7-S и forced ranking — обязательны.

### 7.2 Amazon — Two-Pizza Teams + Single-Threaded Leaders

С начала 2000-х. Структура — fundamentally decentralized, с тысячами автономных команд. Coordinations через **standard interfaces** (APIs, written documents).

### 7.3 Spotify — Squad / Tribe / Chapter / Guild

Подробно в [[../15-Project-Management/02-Agile-Scrum-Kanban#3.2|15.02.3.2]]. Эталон для tech-organization.

### 7.4 Holacracy в Zappos

Tony Hsieh внедрил holacracy в 2013-2014. 14% сотрудников ушло (предложен «buyout» — компенсация за уход). К 2020 году Zappos частично откатил holacracy, но многие принципы остались.

### 7.5 Российские примеры

- **Тинькофф** — изначально flat, по мере роста (до 35K чел.) формализовали структуру
- **Сбер** — крупная иерархическая структура, с 2018 движение к Agile (squad/tribe)
- **Яндекс** — относительно flat для размера (15K+), сильная inженерская культура

## Применение для руководителя

| Целевая роль | Главные применения |
|---|---|
| **CEO** | Strategy → Structure alignment; периодический org redesign |
| **COO** | Operational structure; centralization decisions |
| **CHRO** | Внедрение and поддержка структурных изменений |
| **Менеджер дивизиона** | Понимание архетипа своей структуры; внутренняя организация |
| **C-suite candidate** | Conway's Law; Star Model для cross-functional thinking |

## Связь с другими модулями

- [[index|Модуль 19: Org Design & Change]]
- [[02-Change-Management|02 Change Management]] — структурные изменения требуют change management
- [[../16-Leadership/02-Team-Management|16.02 Team Management]] — Team Topologies (Skelton, Pais)
- [[../15-Project-Management/02-Agile-Scrum-Kanban|15.02 Agile/Scrum]] — Spotify model
- [[../18-HR-Management/04-Engagement-Culture|18.04 Engagement & Culture]] — структура и культура
- [[../01-Strategy/01-Corporate-strategy|01.01 Corporate Strategy]] — strategy → structure

## Источники

### Книги

- Jay Galbraith, **«Designing Organizations»** (Jossey-Bass, 3-е изд. 2014) — каноничная по Star Model
- Tom Peters, Robert Waterman, **«In Search of Excellence»** (Harper & Row, 1982) — McKinsey 7S
- Brian Robertson, **«Holacracy»** (Henry Holt, 2015)
- Matthew Skelton, Manuel Pais, **«Team Topologies»** (IT Revolution, 2019)
- Jeffrey Liker, David Meier, **«The Toyota Way Fieldbook»** (McGraw-Hill, 2006)
- Henry Mintzberg, **«The Structuring of Organizations»** (Prentice Hall, 1979) — академический фундамент

### Онлайн-ресурсы

- **mckinsey.com/quarterly** — статьи по org design
- **bcg.com/perspectives** — BCG insights
- **holacracy.org** — официальный сайт Holacracy
- **gitlab.com/handbook** — открытая структура GitLab

### Сертификации

- **HCI Strategic HR Business Partner** (Human Capital Institute)
- **Organization Design Forum** (ODF) certifications
## Связанные документы

- [[index|Модуль 19: Org Design & Change]]
- [[../index|Education Index]]
- [[02-Change-Management|02 Change Management]]
- [[../16-Leadership/02-Team-Management|16.02 Team Management]]
