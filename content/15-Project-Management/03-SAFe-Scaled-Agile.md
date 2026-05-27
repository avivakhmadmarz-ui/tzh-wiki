---
title: "03 — SAFe и масштабирование Agile"
aliases: ["SAFe", "Scaled Agile", "LeSS", "Spotify Model"]
type: note
status: active
domain: education
module: 15-Project-Management
tags: [education, project-management, safe, scaled-agile, less, spotify]
created: 2026-05-19
updated: 2026-05-19
---

# 03 — SAFe и масштабирование Agile

> Agile отлично работает в командах 5-10 человек. Но как **масштабировать на 50, 500, 5000 разработчиков**? Это вопрос, который решают **SAFe** (Scaled Agile Framework), **LeSS** (Large-Scale Scrum), Spotify Model и другие подходы. Этот раздел — про современный ландшафт scaled agile.

## Карта раздела

![](attachments/diagrams/15-pm-module-map.svg)

## 1. Проблема масштабирования

### 1.1 Почему Agile не масштабируется автоматически

Scrum рассчитан на **одну команду 3-9 человек**. При 10 командах появляются:

- **Coordination overhead** — кто что делает
- **Dependencies** — команда A блокирует команду B
- **Vision alignment** — куда мы все идём
- **Architecture** — кто решает технические стандарты
- **Release management** — синхронизация выпусков

### 1.2 Главные подходы масштабирования

| Подход | Размер | Сложность | Адопция |
|--------|--------|-----------|---------|
| **SAFe** | 50-1000+ | Высокая | Самый популярный в enterprise |
| **LeSS** | 8-2000 | Средняя | Меньшая, но растёт |
| **Nexus** | До 9 команд | Низкая | Простое расширение Scrum |
| **Spotify Model** | Любой | Гибкая | Часто copied wrong |
| **Scrum@Scale** | Любой | Средняя | От Jeff Sutherland |
| **DAD (Disciplined Agile)** | Любой | Высокая | Менее популярна, PMI поддерживает |

**Ключевой вывод 1.** Scale Agile — отдельная дисциплина. Чистый Scrum не работает выше 10 команд.

## 2. SAFe — Scaled Agile Framework

### 2.1 Контекст

**SAFe** разработан **Dean Leffingwell** (бывший Rally), коммерциализирован Scaled Agile Inc. Последняя версия — SAFe 6.0 (2023).

Доминирует в enterprise: Ericsson, Cisco, Lockheed Martin, многие банки.

### 2.2 Четыре уровня конфигурации

- **Essential SAFe** — базовый, 50-125 человек, один Agile Release Train (ART)
- **Large Solution SAFe** — для очень крупных продуктов
- **Portfolio SAFe** — корпоративный уровень
- **Full SAFe** — все вместе

### 2.3 Главные концепции

- **ART** (Agile Release Train — гибкий релизный поезд) — 5-12 команд (50-125 человек), один продукт
- **PI** (Program Increment — приращение программы) — 8-12 недель, состоит из sprints
- **PI Planning** — главное событие, 2-дневное планирование всего ART
- **Lean Portfolio Management** — управление портфелем по принципам Lean

### 2.4 Главные роли

- **RTE** (Release Train Engineer — инженер релизного поезда) — Scrum Master для ART
- **Product Management** — Product Owners на уровне ART
- **System Architect**
- **Business Owners**

### 2.5 Преимущества SAFe

- **Comprehensive** — всё прописано
- **Сертификации** — массово доступны
- **Tools support** — Jira, Azure DevOps поддерживают
- **Predictable** — PI Planning даёт visibility на квартал

### 2.6 Критика SAFe

- **Heavy** — много ритуалов
- **«Water-SAFe»** — превращается в Waterfall с Agile-ярлыками
- **Less individual autonomy** — больше уровней
- **Expensive** — обучение и сертификация дорогие

**Ключевой вывод 2.** SAFe — стандарт для крупных корпораций, но требует disciplinы. «Cargo cult SAFe» — главный риск.

## 3. LeSS — Large-Scale Scrum

### 3.1 Концепция

**LeSS** (Bas Vodde, Craig Larman) — «Scrum для масштаба без добавления ролей». Главная идея: **не добавлять**, а **делать Scrum шире**.

LeSS Basic — до 8 команд (50 человек). LeSS Huge — до 100+ команд.

### 3.2 Главные принципы

- **One Product Backlog** для всех команд
- **One Product Owner**
- **Один Sprint** для всех команд параллельно
- **Минимум новых ролей** (нет RTE, нет coaches как отдельной роли)
- **Component teams**

### 3.3 LeSS vs SAFe

| Аспект | LeSS | SAFe |
|--------|------|------|
| Сложность | Простой | Сложный |
| Ритуалы | Минимум | Много |
| Bureaucracy | Низкая | Высокая |
| Доступность курсов | Меньше | Очень много |
| Подходит | Tech компании | Enterprise |

**Ключевой вывод 3.** LeSS — «честный Scrum для масштаба». Меньшая популярность, но больше дисциплины.

## 4. Spotify Model

### 4.1 Концепция

В 2012 году Spotify опубликовал статью **«Scaling Agile at Spotify»** (Henrik Kniberg). Описал свою организационную модель:

- **Squads** — автономные команды 6-12 человек
- **Tribes** — группы squads (40-150 человек)
- **Chapters** — кросс-squad сообщества по специальности (frontend, QA)
- **Guilds** — interest groups

### 4.2 Почему стало популярно

Простая, наглядная модель. Adopted сотнями компаний.

### 4.3 Главная проблема

Spotify сам не считает это «model» — это **снимок** их культуры в 2012 году. Сейчас Spotify работает по-другому.

Многие компании copy без понимания контекста — получают organizational chaos.

**Ключевой вывод 4.** Spotify Model — **источник идей, не методология**. Copy without context = anti-pattern.

## 5. Выбор подхода

### 5.1 Decision matrix

| Сценарий | Рекомендация |
|----------|--------------|
| **2-3 команды** | Чистый Scrum + lightweight coordination |
| **5-10 команд** | Nexus или LeSS |
| **10-50 команд** | SAFe Essential или LeSS Huge |
| **50+ команд, регулируемая индустрия** | Full SAFe |
| **Tech-компания, культура** | LeSS / Spotify-inspired |
| **Корпорация, traditional** | SAFe |

### 5.2 Главные ошибки

- **Не масштабировать вообще** — играем в Scrum в 100-человечной команде
- **SAFe by default** — без анализа подходит ли
- **Spotify Model copy** — без understanding context
- **«Scaled Agile» как имя на старом waterfall**

**Ключевой вывод 5.** Выбор подхода масштабирования = стратегическое решение. Менять каждый год = разрушать команду.

## Применение для руководителя

| Целевая роль | Главные применения |
|--------------|---------------------|
| **CIO** | Выбор подхода масштабирования; SAFe vs LeSS |
| **CTO** | Architecture в масштабе; technical excellence |
| **Head of Product** | Product strategy across teams |
| **PMO** | SAFe vs hybrid PM standards |
| **CEO** | Decision о Agile transformation |

## Связь с другими модулями

- [[02-Agile-Scrum-Kanban|02 Agile]] — фундамент
- [[04-Portfolio-PMO|04 Portfolio]] — связь с portfolio
- [[../19-Org-Design-Change/index|Модуль 19: Org Design]] — связь с организацией

## Источники

### Книги (приоритет чтения)

- Dean Leffingwell, **«SAFe 6.0 Reference Guide»** (Addison-Wesley) — SAFe стандарт
- Craig Larman, Bas Vodde, **«Large-Scale Scrum: More with LeSS»** (Addison-Wesley, 2016) — LeSS
- Henrik Kniberg, **«Scaling Agile at Spotify»** — оригинальная статья
- Scaled Agile Inc, **«SAFe 6.0 Reference Guide»** (regularly updated)

### Сертификации

- **SAFe Agilist (SA)**, **SAFe Program Consultant (SPC)** — SAFe sertификации
- **Certified LeSS Practitioner / Coach** — LeSS
- **Certified Scrum Professional (CSP)** — для опытных

### Кейсы

- **Spotify** — оригинальный, но evolved
- **Ericsson, Cisco** — каноничные SAFe внедрения
- **Российские:** Сбер Agile@scale, Альфа-Банк, Тинькофф
## Связанные документы

- [[index|Модуль 15: PM]]
- [[../index|Education Index]]
- [[02-Agile-Scrum-Kanban|02 Agile]]
