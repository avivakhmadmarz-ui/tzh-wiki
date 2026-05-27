---
aliases: 
updated: YYYY-MM-DD
tags: [education, lean, six-sigma, lss]
created: 2026-05-07
date created: 2026-05-07
date modified: 2026-05-13
---

# 06 — Lean Six Sigma: слияние потока и вариативности

> Lean борется с **потерями** (waste) и оптимизирует **поток**. Six Sigma борется с **вариативностью** и оптимизирует **качество**. По отдельности — каждое работает только частично. Lean Six Sigma (LSS) объединяет их в единую методологию, которая закрывает оба измерения.

> **Запоминающаяся формула:** Lean делает процесс **быстрее**, Six Sigma делает его **точнее**. LSS делает и то, и другое.

## Lean vs Six Sigma — фундаментальная разница

| Аспект | Lean | Six Sigma |
|--------|------|-----------|
| **Что атакует** | Потери (8 видов Muda + Mura + Muri) | Вариативность (отклонения от стандарта) |
| **Цель** | Поток без перерывов; устранение non-value-added | DPMO ≤ 3,4 (defects per million opportunities) |
| **Ключевая метрика** | Cycle time, Lead time, PCE, OEE | Cp/Cpk, sigma level, DPMO |
| **Метод** | Kaizen, VSM, 5S, Kanban, Poka-Yoke | DMAIC, статистические инструменты, DOE |
| **Происхождение** | Toyota, 1948–1975 | Motorola, 1986; популяризация GE, 1995+ |
| **Стиль работы** | Быстрые kaizen-циклы (часы/дни) | Углублённые DMAIC-проекты (недели/месяцы) |
| **Главный инструмент анализа** | 5 Why, Spaghetti, VSM | Statistical analysis, hypothesis testing, regression |
| **Кто внедряет** | Все сотрудники, культура | Сертифицированные Belts |

### Когда что нужно

| Симптом проблемы | Что лечим |
|------------------|-----------|
| Долгий цикл, много waiting, большие запасы | **Lean** |
| Высокая дефектность, разные результаты разных операторов/смен/линий | **Six Sigma** |
| И то, и другое | **Lean Six Sigma** |
| Нечёткое целеполагание, политика | **Не Lean / не SS** — это менеджерская проблема |

## История Six Sigma

### Motorola, 1986

**Bill Smith**, инженер Motorola, заметил, что **field failure rate** (отказы в эксплуатации) гораздо хуже, чем **factory yield rate**. Углубился в статистику и предложил: чтобы field failures были приемлемы, factory должен идти на **6 sigma уровне** (отсюда название) = 3,4 дефекта на миллион возможностей.

В 1988-м Motorola первой выиграла Malcolm Baldrige National Quality Award (MBNQA). Six Sigma стал известен.

### General Electric, 1995

Как было разобрано в [[04-Cases#7 GE под Welch|кейсе GE]], Jack Welch сделал Six Sigma главной операционной программой компании. **$12 млрд savings** за 5 лет — и весь корпоративный мир посмотрел.

К 2000-му Six Sigma стал **must-have** для Fortune 500.

### Объединение в Lean Six Sigma, 2000-е

К 2002-му стало ясно, что:
- Six Sigma в одиночку **слишком медленный** (один Black Belt project = 3–6 месяцев).
- Six Sigma не атакует все 8 видов потерь, только Defects (и часть Variation, что близко к Mura).
- Lean без статистики не может справиться с complex variability problems (например, в полупроводниках).

**Michael George** (книги «Lean Six Sigma» 2002, «Lean Six Sigma for Service» 2003) формализовал объединение. С тех пор LSS — стандартный термин.

## Что такое sigma level

Sigma (σ) — стандартное отклонение в нормальном распределении. Six Sigma означает, что **между средним и ближайшей спецификационной границей помещается 6σ** — а это 3,4 дефекта на миллион.

| Sigma уровень | Дефектов на миллион (DPMO) | Yield (% годных) | Comment |
|---------------|----------------------------|------------------|---------|
| 1σ | 691 462 | 31% | Хаос |
| 2σ | 308 537 | 69% | Слабая компания |
| 3σ | 66 807 | 93,3% | Средняя западная компания |
| 4σ | 6 210 | 99,38% | Очень хорошая |
| 5σ | 233 | 99,977% | Лучшие в классе |
| **6σ** | **3,4** | **99,99966%** | Цель Six Sigma |

**Контекст:** 99% звучит хорошо, но это 10 000 дефектов на миллион. На скорости 1000 операций в день — это 10 дефектов **в день**. Six Sigma добивается того, что дефект — это раз в год.

**Пример из жизни:** аэропортовый багаж работает на ~3.5 sigma (≈30 000 потерянных багажей на миллион). 6σ означал бы 3 потерянных багажа в год.

## DMAIC — главный цикл Six Sigma

**Define → Measure → Analyze → Improve → Control**.

В отличие от PDCA (быстрый, итеративный, гибкий), DMAIC — **структурированный проект**, обычно 3–6 месяцев, с tollgate-ревью на каждом этапе.

<!-- IMG: DMAIC cycle diagram | https://www.6sigma.us/six-sigma-articles/dmaic/ -->

### D — Define (1–2 нед)

Артефакты:
- **Project Charter** — проблема, цель, scope, команда, сроки, business case ($).
- **SIPOC** — Suppliers, Inputs, Process, Outputs, Customers (1-страничный обзор).
- **Voice of Customer (VoC)** — что клиент реально считает «качеством».
- **CTQ tree (Critical to Quality)** — каскад от VoC к измеримым параметрам.

### M — Measure (2–4 нед)

- **Operational definitions** — что именно мы считаем дефектом, в каких единицах.
- **Data collection plan** — какие данные собираем, как часто, кто.
- **MSA (Measurement System Analysis)** — наша **система измерения** надёжна? (Gage R&R)
- **Baseline metrics** — текущий sigma level, Cp/Cpk, DPMO.

Это самый недооценённый этап. Часто оказывается, что 50% «вариации процесса» — это вариация системы измерения, а не реальный процесс.

### A — Analyze (3–6 нед)

- **Process analysis** — VSM, swim lanes, value-add анализ.
- **Cause analysis** — Ishikawa, 5 Why, FMEA, Pareto.
- **Statistical analysis** — hypothesis testing, ANOVA, regression — для выявления **значимых** причин из подозреваемых.

Цель: получить **few critical X's** (главные причины), которые объясняют большую часть Y (variance).

### I — Improve (3–6 нед)

- **Generate solutions** — brainstorm + benchmarking.
- **DOE (Design of Experiments)** — оптимизировать настройки X, чтобы Y вышел в target.
- **Pilot test** — проверить в малом масштабе.
- **Implement** — раскатить на full scale.

### C — Control (4+ нед)

- **Control plan** — кто, что, как часто измеряет.
- **SPC (Statistical Process Control)** — control charts (Shewhart), out-of-control rules.
- **Standardize** — обновить SOP, обучение операторов.
- **Handoff to process owner** — проект закрыт, владелец процесса ведёт control.

**Без Control — типовая ловушка:** улучшение «работало 6 мес, потом всё откатилось». Control plan — самая важная часть DMAIC.

### DMAIC vs PDCA

| Аспект | DMAIC | PDCA |
|--------|-------|------|
| Длительность | 3–6 мес | Часы–недели |
| Формализм | Высокий | Низкий |
| Команда | 5–10 человек, dedicated time | Любая, в потоке работы |
| Артефакты | Charter, SIPOC, A3, control plan | A3 |
| Когда | Сложная проблема с вариативностью | Любое улучшение |
| Использование статистики | Обязательно | Опционально |

В правильно организованной LSS-системе DMAIC и PDCA **сосуществуют**: DMAIC для «лоси», PDCA для «зайцев».

## DMADV / DFSS — для design новых процессов

Когда DMAIC не хватает — например, нужно **спроектировать** новый процесс/продукт. Тогда:

**Define → Measure → Analyze → Design → Verify** — DFSS (Design for Six Sigma).

Используется для R&D и нового продукта/услуги.

## Belt-структура

LSS заимствовал из боевых искусств градацию по поясам. Это и роль, и сертификация.

| Belt | Время обучения | Роль | Что делает |
|------|----------------|------|------------|
| **White** | ~4 ч | Awareness | Знает базовую терминологию, понимает зачем; может участвовать в командах |
| **Yellow** | 2–3 дня | Team member | Понимает DMAIC, ведёт **части** проекта, помогает Green/Black Belts |
| **Green** | 1–2 нед | Project leader (part-time) | Ведёт DMAIC-проект параллельно основной работе; ~5–10 проектов в год |
| **Black** | 4–6 нед обучения + проекты | Project leader (full-time) | Лидер сложных кросс-функциональных проектов; mentor Green Belts |
| **Master Black** | Опыт + дополнительное | Coach + strategist | Тренер Black Belts, стратегия LSS-программы, селекция проектов |
| **Champion** | По мере необходимости | Sponsor (executive) | Топ-менеджер, спонсор и patron LSS-программы |

### Типичная структура программы

| Уровень | % сотрудников |
|---------|---------------|
| Awareness (White Belt) | 100% |
| Yellow Belt | 20–30% |
| Green Belt | 5–10% |
| Black Belt | 1% |
| Master Black Belt | 0,1% |

GE при Welch имела ~5000 Black Belts на 300 000 сотрудников.

### Стоимость и ROI

- Black Belt должен принести **$500K–1M savings в год** (типичный target).
- Green Belt project — $50–100K savings.
- LSS программа окупается за 12–18 мес при правильном внедрении.

## Кейс — GE: $12 млрд за 5 лет (детально)

Контекст и базовые цифры — в [[04-Cases#7 GE под Welch|04]]. Дополнительные детали:

### Что сделал Welch

1. **Personal commitment** — лично участвовал в monthly reviews, делал shop floor visits.
2. **Bonus alignment** — 40% топового бонуса = от Six Sigma результатов.
3. **Mandatory training** — все executives 13 дней / 100 ч обучения.
4. **Mandatory project completion** — все executives закрыли минимум 1 project до конца 1998.
5. **Cross-divisional** — Six Sigma внедрили во все 14 divisions GE (от двигателей до Capital).

### Ключевые ошибки, которые потом признал GE

- **Слишком много Six Sigma, слишком мало Lean.** К 2005-му стало ясно, что многие проекты были «академическими» с большой статистикой, но не атаковали поток. Это и подтолкнуло GE к LSS.
- **Бумажная отчётность.** Иногда savings считались «креативно», и реальный P&L impact был меньше отчётного.
- **«Мания сертификации»** — люди шли за поясом, не за результатом.

### Главный урок

При внедрении LSS — **ставить project savings в P&L и проверять финансами**, а не в отдельной отчётности «качество».

## Когда нужен только Lean, без Six Sigma

| Симптом | Подход |
|---------|--------|
| Долгий процесс с большим waiting | **Lean (VSM + Kanban)** |
| Большие запасы, overproduction | **Lean (pull system, heijunka)** |
| Хаос на рабочем месте | **5S** |
| Низкое engagement сотрудников | **Kaizen culture** |
| Поломки оборудования | **TPM** |

В этих случаях **Six Sigma overhead не оправдан** — статистика тут не нужна.

## Когда нужен Six Sigma (или LSS)

| Симптом | Подход |
|---------|--------|
| Высокая дефектность (>1%) | **Six Sigma DMAIC** |
| Разные результаты у разных смен/операторов/линий | **Six Sigma** (analyze variation) |
| Сложный процесс с многими X | **Six Sigma DOE** |
| Регулируемая отрасль (медицина, фарма, авиа) | **LSS обязательно** |
| Качество — главный KPI клиента | **LSS** |

## LSS vs чистый Lean — практический выбор

В контексте закупок / ритейла / категорийного менеджмента:

| Сценарий | Рекомендация |
|----------|--------------|
| Хочешь сократить cycle time закупочного процесса | **Lean (VSM, kaizen)** — Six Sigma тут overkill |
| Хочешь снизить overstock | **Lean (pull, heijunka)** |
| Хочешь снизить пересортицу/брак на приёмке | **LSS** — нужен DMAIC + статистический анализ причин |
| Хочешь стандартизовать процесс работы поставщиков | **Lean** |
| Хочешь стабилизировать прогноз продаж | **Six Sigma** (анализ вариации) |
| Хочешь выстроить культуру улучшений в команде | **Lean** (kaizen) |

**Общий принцип:** **начни с Lean (быстрее результат, проще)**. К Six Sigma добавляй, **когда упрёшься в проблемы вариативности**, которые kaizen-инструменты не решают.

## Что забрать руководителю

1. **Lean ≠ Six Sigma.** Lean — поток, Six Sigma — точность. Не путай и не смешивай задачи.
2. **DMAIC — структурный, медленный, мощный.** Используй для сложных вариативных проблем. Не используй для микро-улучшений.
3. **PDCA — быстрый, итеративный.** Используй для рутинного kaizen.
4. **Belt-структура — это роль, не диплом.** Без живых проектов с финансовым impact'ом сертификат бесполезен.
5. **Контроль (Control plan) — самая важная фаза DMAIC.** Без неё все улучшения откатываются.
6. **Если ты только начинаешь — начни с Lean.** Six Sigma добавляй, когда нужно лечить именно variability.

## Источники

- [Six Sigma — Wikipedia](https://en.wikipedia.org/wiki/Six_Sigma)
- [Six Sigma Belts — 6sigmacertificationonline](https://www.6sigmacertificationonline.com/six-sigma-belts/)
- [Lean Six Sigma Belt System — DMAIC.com](https://www.dmaic.com/faq/belt-system-in-lean-and-six-sigma/)
- [Six Sigma Case Study GE — SixSigma.us](https://www.6sigma.us/ge/six-sigma-case-study-general-electric/)
- [Jack Welch and Six Sigma — SixSigma Daily](https://www.sixsigmadaily.com/remembering-jack-welch-and-his-relation-to-six-sigma/)
- [DMAIC Process — SixSigma.us](https://www.6sigma.us/six-sigma-articles/dmaic/)
- [Lean Six Sigma Explained — UTSA](https://www.utsa.edu/pace/news/lean-six-sigma-explained-which-belt-level-right-for-you.html)
- [Understanding Six Sigma Ranks — Air Academy](https://airacad.com/what-are-six-sigma-ranks/)

## Связанные заметки

- [[index|Lean Index]]
- [[02-8-wastes-Muda-Mura-Muri|02 — 8 потерь]] (LSS атакует Defects + Mura)
- [[03-Lean-tools|03 — Lean tools]] (PDCA vs DMAIC)
- [[04-Cases#7 GE под Welch — Six Sigma at scale|04 — кейс GE]]
- [[05-Lean-in-services-and-office|05 — Lean в банках]] (LSS особенно популярен в фининдустрии)
- [[07-For-the-manager|07 — Для руководителя]]
