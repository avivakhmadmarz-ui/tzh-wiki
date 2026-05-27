---
title: "03 — Hoshin Kanri и стратегическое развёртывание"
aliases: ["Hoshin Kanri", "Policy Deployment", "X-Matrix", "Catchball"]
type: note
status: active
domain: education
module: 14-Planning
tags: [education, planning, hoshin-kanri, policy-deployment, toyota, akao]
created: 2026-05-19
updated: 2026-05-19
---

# 03 — Hoshin Kanri и стратегическое развёртывание

> Hoshin Kanri (方針管理 — японский метод, дословно «направление-управление» или «policy deployment» — развёртывание политики) — японский подход к **связыванию стратегии с операциями**. Используется в Toyota, Hewlett-Packard, P&G. Главные инструменты — X-Matrix и Catchball-процесс. Альтернатива западному OGSM / OKR для тех, кто строит **Lean-zрелую** компанию.

## Карта раздела

![](attachments/diagrams/14-hoshin-kanri-x-matrix.svg)

## 1. Контекст Hoshin Kanri

### 1.1 История

Hoshin Kanri разработан в **Bridgestone Tire** (Япония, 1965), популяризирован через TQM и распространился через западные компании в 1980-1990-х.

Каноничные книги:
- **Yoji Akao, «Hoshin Kanri: Policy Deployment for Successful TQM»** (Productivity Press, 1991) — классика
- **Pascal Dennis, «Getting the Right Things Done»** (Lean Enterprise Institute, 2006) — современное практическое руководство

### 1.2 Главная идея

В большинстве компаний **разрыв между стратегией и операциями**:
- Стратегия — slide deck CEO, лежит в папке
- Операции — реактивные пожары
- Связи нет

Hoshin Kanri **разворачивает** (deploy) стратегические цели через все уровни организации до конкретных tactical действий.

### 1.3 Hoshin vs OKR

| Аспект | Hoshin Kanri | OKR |
|--------|--------------|-----|
| **Происхождение** | Toyota, японский | Intel, Google |
| **Горизонт** | 3-5 лет + годовой | Квартал |
| **Структура** | X-Matrix | Cascade objectives |
| **Decision-making** | Top-down + catchball | Top-down + alignment |
| **Цикл** | Annual + monthly review | Quarterly |
| **Главная польза** | Strategic deployment | Agile adaptation |

Часто компании используют **гибрид** — Hoshin для long-term, OKR для quarterly.

**Ключевой вывод 1.** Hoshin Kanri — это **строгая дисциплина** связи стратегии с операциями. Альтернатива OKR для Lean-zрелых компаний.

## 2. X-Matrix

### 2.1 Структура

![](attachments/diagrams/14-hoshin-kanri-x-matrix.svg)

X-Matrix — главный артефакт Hoshin Kanri. Один лист, четыре стороны:

- **North (Север)** — Goals (долгосрочные цели 3-5 лет)
- **West (Запад)** — Strategies (стратегии достижения целей)
- **South (Юг)** — Tactics / Initiatives (конкретные действия года)
- **East (Восток)** — Metrics / KPIs (как измеряем)

Центр — точки **связи**: каждая стратегия связана с целями, каждая тактика — со стратегиями, каждый KPI — с тактиками.

### 2.2 Чтение X-Matrix

X-Matrix читается **по часовой стрелке**:
1. North: что хотим достичь за 3-5 лет
2. West: какие стратегии этого достижения
3. South: какие конкретные инициативы в этом году
4. East: чем измерять прогресс

В центре — **корреляции**, показывающие, какая стратегия поддерживает какие цели, какая тактика — какие стратегии.

### 2.3 Каскадирование

X-Matrix создаётся на уровне:
1. **Корпоративный** — для всей компании
2. **Дивизионный** — для бизнес-единиц
3. **Функциональный** — для функций
4. **Командный** — для команд

Каждый нижний уровень **наследует** цели верхнего как свои стратегии. Это создаёт **сквозную линию** от CEO до linе worker.

### 2.4 Шаблон применения

Стандартный шаблон в Excel или Miro:

```
[ N: Goals ]
       ↓
[E: Metrics] ⊗ [Center: correlations] ⊗ [W: Strategies]
       ↑
[ S: Tactics ]
```

**Ключевой вывод 2.** X-Matrix — **визуальная дисциплина**. Одна страница вместо 50-страничной презентации; помещение на лист = принудительная фокусировка.

## 3. Catchball Process

### 3.1 Концепция

**Catchball** (буквально «перебрасывание мяча») — японская техника **двунаправленного согласования** целей между уровнями.

Не «сверху спустили цели — снизу приняли», а:
1. CEO формулирует draft целей
2. Передаёт vice-president
3. VP обсуждает с командой, **корректирует**
4. Возвращает CEO с реалистичными цифрами
5. Итерация повторяется до согласия

Catchball может занимать 4-8 недель, но даёт **commitment** на каждом уровне.

### 3.2 Почему важно

Без catchball — типичный сценарий: цели нереалистичные (top-down) или слишком скромные (bottom-up). С catchball — **stretch but achievable**.

### 3.3 Связь с Lean культурой

Catchball отражает **respect for people** — один из двух столпов Toyota Way. Цели не «приказ», а **результат разговора**.

**Ключевой вывод 3.** Catchball — это не «формальность согласования», а **сердце** Hoshin Kanri. Без catchball цели становятся пустыми.

## 4. Hoshin Kanri в цикле

### 4.1 PDCA на уровне Hoshin

Hoshin Kanri следует циклу **PDCA** (см. модуль 13.01):

- **Plan** — формулировка X-Matrix через catchball
- **Do** — выполнение tactics
- **Check** — monthly / quarterly review против KPIs
- **Act** — корректировка по результатам

### 4.2 Annual cycle

Стандартный годовой цикл:

| Период | Событие |
|--------|---------|
| **Q4 предыдущего года** | Strategy review, draft X-Matrix |
| **Январь** | Catchball, финальный X-Matrix |
| **Месячно** | Mid-month review status |
| **Квартально** | Deep review, корректировки |
| **Q3** | Mid-year assessment |
| **Q4** | Hoshin retrospective + новый цикл |

### 4.3 3-5 letniй cycle

Параллельно с годовым — **3-5-летние стратегические цели** (North в X-Matrix). Каждый год — корректировка плана движения к ним.

**Ключевой вывод 4.** Hoshin Kanri — это **ритм организации**, не одноразовое упражнение. Сила в дисциплине ритуала.

## 5. Hoshin Kanri в Toyota

### 5.1 Roots в Toyota

Hoshin Kanri — обязательный процесс в Toyota:
- 5-летние «Vision» цели
- Годовые Hoshin плана
- Monthly reviews
- Catchball на всех уровнях

Связан с другими элементами Toyota Way:
- **Genchi Genbutsu** (go and see — иди и смотри) — review происходит на месте
- **Hansei** (reflection — рефлексия) — постоянный self-critique
- **Kaizen** — постоянное улучшение

### 5.2 Применение за пределами Toyota

Hoshin Kanri внедрили:
- **Hewlett-Packard** (с 1980-х)
- **Procter & Gamble**
- **Intel**
- **Boeing**
- **Lockheed Martin**
- **Российские:** некоторые автозаводы (КАМАЗ), отдельные операционные компании

### 5.3 Главные кейсы успеха

- **HP TQC era 1980-1990-х** — Hoshin как ключевой инструмент роста
- **Toyota TPS** — Hoshin как часть полной системы
- **Boeing Quality** — Hoshin в quality transformation

**Ключевой вывод 5.** Hoshin Kanri работает там, где есть **Lean culture**. В компаниях с командно-контрольной культурой Hoshin становится «ещё одной отчётностью».

## 6. Сравнение с OGSM и OKR

### 6.1 Hoshin Kanri vs OGSM

| Аспект | Hoshin | OGSM |
|--------|--------|------|
| Происхождение | Toyota | P&G |
| Структура | X-Matrix | OGSM (Objective-Goal-Strategy-Measure) |
| Catchball | Обязателен | Опционален |
| Lean ties | Сильные | Нет |
| Сложность | Средняя | Низкая |

### 6.2 Hoshin Kanri vs OKR

OKR (см. модуль 17 Goal Setting):
- Quarterly cycle vs Hoshin annual
- Bottom-up vs top-down through catchball
- Tech companies vs manufacturing
- Agile vs Lean

Многие компании комбинируют: **Hoshin для долгосрочного, OKR для квартального**.

### 6.3 Когда что выбирать

- **Manufacturing, Lean culture** → Hoshin
- **Tech / scale-ups, agile** → OKR
- **FMCG, стандартный корпорат** → OGSM
- **Гибрид** → Hoshin + OKR

**Ключевой вывод 6.** Hoshin — один из трёх главных подходов к strategic deployment. Выбор зависит от культуры и индустрии.

## Применение для руководителя

| Целевая роль | Главные применения |
|--------------|---------------------|
| **CEO** | Owner Hoshin Kanri; X-Matrix корпоративная |
| **COO** | Каскадирование операционных целей; review |
| **Стратегический офис** | Facilitation catchball, X-Matrix templates |
| **HR** | Связь Hoshin с performance management |
| **Lean leaders** | Hoshin как часть Lean transformation |

## Связь с другими модулями

- [[01-IBP-Connected-Planning|01 IBP]] — operational planning
- [[02-DDMRP-Deep-Dive|02 DDMRP]] — execution layer
- [[../Other-methodologies/05-Hoshin-Kanri|Other-meth: Hoshin базовый]]
- [[../17-Goal-Setting/index|Модуль 17: Goal Setting]] — OKR альтернатива
- [[../01-Strategy/03-Scenario-planning|Модуль 01.03: OGSM]] — третий подход
- [[../Lean/index|Lean]] — Hoshin как часть Lean

## Источники

### Книги (приоритет чтения)

- Yoji Akao, **«Hoshin Kanri: Policy Deployment for Successful TQM»** (Productivity Press, 1991) — каноничная книга
- Pascal Dennis, **«Getting the Right Things Done»** (Lean Enterprise Institute, 2006) — современная практика
- Thomas Jackson, **«Hoshin Kanri for the Lean Enterprise»** (Productivity Press, 2006)
- Mike Rother, **«Toyota Kata»** (McGraw-Hill, 2009) — связана концепция

### Статьи

- Boeing Hoshin case studies — публичные
- HBR: **«Hoshin Planning»** — серия статей

### Онлайн-ресурсы

- **Lean Enterprise Institute** — Hoshin resources
- **Shingo Institute** — Hoshin как часть Shingo Model
- **TPS Lean Toyota Production System** — глубокое погружение

### Сертификации

- **Shingo Prize** — для компаний с Hoshin maturity
- **Lean Six Sigma Black Belt** — включает Hoshin
- **Hoshin Kanri Master Belt** (некоторые провайдеры)

### Кейсы

- **Toyota TPS Hoshin** — публичные доклады
- **HP TQC** — каноничный западный кейс
- **Boeing Quality Transformation**
- **Российские:** КАМАЗ, отдельные кейсы Lean-зрелых компаний
## Связанные документы

- [[index|Модуль 14: Planning]]
- [[../index|Education Index]]
- [[../Other-methodologies/05-Hoshin-Kanri|Hoshin базовый]]
- [[../17-Goal-Setting/index|Модуль 17: Goal Setting]]
