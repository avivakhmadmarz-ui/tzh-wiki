---
title: "Hoshin Kanri — стратегическое разворачивание (Policy Deployment)"
type: note
status: active
domain: education
module: Other-methodologies
aliases: 
updated: 2026-05-13
tags: [education, other-methodologies, hoshin-kanri]
created: 2026-05-07
date created: 2026-05-07
date modified: 2026-05-13
---

# Hoshin Kanri — стратегическое разворачивание (Policy Deployment)

Hoshin Kanri (方針管理) — японская методология **связывания стратегии и ежедневного управления**. «Hoshin» — компас / направление, «Kanri» — управление. На английском часто переводят как **Policy Deployment** или **Strategy Deployment**. Это часть Lean management system (родом из TPS-экосистемы).

> **TL;DR для руководителя.** Hoshin Kanri отвечает на самый болезненный вопрос: «как сделать, чтобы стратегия из документа на 50 страниц превратилась в действия каждого менеджера в понедельник утром?» Через **breakthrough objectives** (3-5 лет) → **annual hoshin** → **catchball-каскад** → **daily management**. Это рамка для зрелых организаций, обычно с Lean-практикой. Плохо приживается в иерархичных культурах без культуры дискуссии.

## Истоки

- **1950-е** — Lean-движение в Японии (Deming PDCA, Juran на quality, TPS Toyota)
- **1965** — методология формализована в **Bridgestone Tire**, и оттуда расходится по японским компаниям (Toyota, Honda, Komatsu)
- **1980-е** — приходит в США через consulting и benchmarking. **HP** (Hewlett-Packard) — один из первых крупных US-внедрителей. Также Xerox.
- **2000-е** — становится стандартом в Lean-зрелых компаниях: Danaher, Ingersoll Rand, Toyota North America, Bridgestone, Bajaj, M&M, Honda, Ford
- **2010-е+** — software vendors (i-nexus, KaiNexus, Hoshin Online) делают X-matrix цифровым

![](attachments/diagrams/14-hoshin-kanri-x-matrix.svg)

## Ключевые элементы

### 1. Breakthrough objectives (3-5 лет)

Это не годовые цели, а **breakthrough** — амбициозные стратегические скачки. Обычно 2-3 максимум. Примеры: «удвоить долю рынка», «сократить time-to-market на 50%», «выйти из 3 регионов».

### 2. Annual hoshin (1 год)

Декомпозиция breakthrough на год. 3-5 годовых hoshin максимум. Каждый — measurable.

### 3. Improvement priorities / Strategies

Конкретные подходы как достичь annual hoshin: «trim продуктовый портфель», «redesign процесса закупок», «развернуть Kanban в 5 цехах».

### 4. Targets to improve (KPI)

Метрики, по которым измеряется прогресс. Не обязательно те же, что входят в breakthrough — могут быть leading indicators.

### 5. Owners / Resources

Кто отвечает за каждый strategy и target. Один владелец на одну линию.

### 6. Business fundamentals (BAU)

Параллельно с breakthrough идёт обычная операционная деятельность. Hoshin не отменяет BAU, но breakthrough приоритизируется при конфликте ресурсов.

## X-Matrix — визуальный инструмент

X-Matrix — одностраничный документ, на котором всё это связывается. Структура:

```
              [Annual hoshin]
[Improvement     ┌────────┐    [Targets to
 priorities]  ←──┤   X    ├──→ improve]
              └────────┘
              [Breakthrough
               objectives 3-5 yr]
       [Owners and resources на полях]
```

Связи отмечаются точками или цветами на пересечениях квадрантов. Это позволяет видеть **причинно-следственные** цепочки на одной странице.

## Catchball — ключевой социальный процесс

Catchball — back-and-forth переговоры между уровнями организации.

### Как работает

1. Top management формулирует draft breakthrough + annual hoshin
2. **Бросает «мяч»** вниз — middle management
3. Middle management не просто принимает, а возвращает: «вот наша интерпретация, вот ресурсы, вот реалистичный target — мы можем не +50%, а +35%»
4. Top рассматривает, договаривается. Возможно, корректируют ресурсы или цель
5. Когда «мяч пойман» с обеих сторон — есть commitment
6. Теперь middle бросает мяч team leads — повторение
7. Цикл вниз до individual contributors

<!-- IMG: Catchball process (top-down + bottom-up negotiation) | https://blog.i-nexus.com/hubfs/catchball-illustration.png -->

**Почему это важно**: без catchball сверху приходят нереалистичные цели, и organization тихо саботирует. Catchball заменяет «голоса» на договор.

## Hoshin Kanri vs Strategy Map (Kaplan-Norton BSC)

Часто сравнивают и часто путают. Это разные вещи:

| Параметр | Hoshin Kanri | Balanced Scorecard / Strategy Map |
|----------|--------------|------------------------------------|
| Происхождение | Toyota, Bridgestone (1965) | Harvard, Kaplan & Norton (1992-2000) |
| Фокус | Breakthrough + daily management | Балансировка 4 перспектив (Financial / Customer / Internal / Learning) |
| Инструмент | X-Matrix, Catchball | Strategy Map, Scorecard |
| Драйвер | PDCA на каждом уровне | Cause-and-effect chain |
| Культура | Lean / continuous improvement | Performance management |
| Сильная сторона | Каскадирование и execution | Visualisation стратегии |
| Слабая сторона | Не учит измерять value chain | Слабо связан с daily ops |

**Best practice** — комбинировать: Strategy Map визуализирует логику, Hoshin даёт execution mechanics. См. подробно в `[[../Compare/03-Combinations-that-work|Combinations that work]]`.

## Кейсы

### Toyota

Использует Hoshin Kanri с 1960-х. Это часть Toyota Production System (TPS). Знаменитая дисциплина: каждый менеджер каждое утро может объяснить, **как его задача сегодня связана с annual hoshin**. Это и есть истинное разворачивание.

### Hewlett-Packard (и HP Enterprise)

Один из первых US-имплементаторов в 1980-х. Внутренний термин **«HP Way»** включал Hoshin как часть управленческой системы. После split HP / HPE / HPI методология поддерживается в HPE.

### Danaher

Машиностроительный конгломерат, известный как один из лучших операторов Lean в мире (Danaher Business System, DBS). Hoshin Kanri — central component of DBS. CEO Larry Culp (потом ушёл в GE) использовал Hoshin как механизм M&A integration: каждое купленное подразделение садят в Hoshin-цикл.

### Ingersoll Rand

Использовал Hoshin для трансформации в IR Operating System.

### Xerox UK

Один из первых британских implementers. Использовали Hoshin для quality program.

### Bridgestone

Originator. До сих пор использует Hoshin как backbone планирования.

### Intel

Andy Grove и команда — известны как создатели OKR (см. `[[../../17-Goal-Setting/OKR-KPI/index|OKR]]`), но в Intel также жил Hoshin Kanri в производственных подразделениях. OKR можно видеть как «Hoshin Kanri для tech-компаний» (хотя они отличаются по культуре).

## Когда Hoshin Kanri оправдан

- Lean-зрелая организация (есть TPM, Kaizen, daily management)
- Сложная, multi-level организация (>500 человек)
- Стратегия не «фокус» (focus = OKR), а «разворачивание» (deployment = Hoshin)
- Долгосрочные breakthrough objectives (не 3-месячные)

## Когда Hoshin Kanri не подходит

- Стартап / scale-up с быстрой адаптацией — слишком тяжёлая надстройка, бери OKR
- Организация без culture of negotiation — catchball не приживётся
- Если у менеджеров нет навыков ведения KPI в daily management

## Чеклист внедрения

- [ ] CEO sponsors process and **personally** facilitates first cycle
- [ ] 2-3 breakthrough objectives sketched (не 10!)
- [ ] X-Matrix template настроен (можно в Excel или i-nexus)
- [ ] Catchball — workshops запланированы с middle managers
- [ ] Daily management board уже есть в командах (без него Hoshin висит в воздухе)
- [ ] Quarterly review cadence (не годовой!)
- [ ] Связь с annual budget — синхронизировано

## Связь с другими методологиями

- **Hoshin + Lean**: исторически связаны (см. `[[../../13-Operations-Excellence/Lean/index|Lean]]`). Hoshin — стратегический слой над Kaizen / TPS.
- **Hoshin vs OKR**: похожи на каскадирование, но Hoshin — про breakthrough на 3-5 лет, OKR — про квартал и более динамику. См. `[[../Compare/01-Methodology-landscape|Methodology landscape]]`.
- **Hoshin + S&OP**: Hoshin даёт долгосрочные breakthrough, S&OP — тактический ops planning (см. `[[../SOP/index|S&OP]]`).
- **Hoshin + IBP**: в IBP strategic review есть место для Hoshin (см. `[[01-IBP-Integrated-Business-Planning|IBP]]`).
- **Hoshin vs BSC**: дополняют, см. сравнение выше.

## Источники

- [i-nexus — What is Hoshin Kanri](https://blog.i-nexus.com/what-is-hoshin-kanri)
- [i-nexus — Danaher, Ingersoll Rand, Xerox case studies](https://blog.i-nexus.com/policy-deployment-in-practice-danaher-ingersoll-rand-xerox)
- [i-nexus — X-matrix explained](https://blog.i-nexus.com/hoshin-kanri-x-matrix-explained)
- [Asana — Hoshin Kanri 7-step planning guide](https://asana.com/resources/hoshin-kanri)
- [Businessmap — Hoshin Kanri X-Matrix](https://businessmap.io/lean-management/hoshin-kanri/what-is-hoshin-kanri-x-matrix)
- [BSC Designer — Hoshin Kanri vs Balanced Scorecard](https://bscdesigner.com/hoshin-kanri.htm)
- [Toyota Way to Effective Strategy Deployment (Sage journal)](https://journals.sagepub.com/doi/abs/10.1177/2516600X20946542)
- [MoreSteam — Implementing Hoshin Kanri](https://www.moresteam.com/resources/blogs/implementing-hoshin-kanri)
- Akao, Y. (1991). _Hoshin Kanri: Policy Deployment for Successful TQM_. Productivity Press.
- Jackson, T. L. (2006). _Hoshin Kanri for the Lean Enterprise_. Productivity Press.
- Kaplan, R. & Norton, D. (2004). _Strategy Maps_. HBR Press.
