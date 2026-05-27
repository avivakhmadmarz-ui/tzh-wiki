---
aliases: 
updated: YYYY-MM-DD
tags: [education, other-methodologies, toc]
created: 2026-05-07
date created: 2026-05-07
date modified: 2026-05-13
---

# Theory of Constraints (ToC) — теория ограничений

Теория ограничений — это **управленческая философия**, которую сформулировал израильский физик **Eliyahu M. Goldratt** в 1984 году в романе **«The Goal»** (на русском «Цель»). Главная идея: в любой системе есть **узкое место** (constraint), и пропускная способность всей системы определяется именно им. Управлять системой = управлять узким местом.

> **TL;DR для руководителя.** Самая универсальная управленческая линза, которую дёшево внедрить в голову. Она работает на складе, на производстве, в проектах, в продажах, в HR. Goldratt написал художественный роман, где на 300 страницах объяснил пять шагов — и эти пять шагов до сих пор используют Boeing, US Marines, Mazda, Delta и сотни meaningful компаний.

## Истоки

- **1979** — Goldratt создаёт software OPT (Optimized Production Technology) для расписаний на производстве. Замечает, что классическая логика «загрузить все ресурсы» — ошибочна.
- **1984** — выходит **«The Goal»** (соавтор Jeff Cox). Книга в форме романа: герой Алекс Рого спасает свой завод от закрытия за 3 месяца, применяя принципы ToC. Продано более 10 миллионов копий.
- **1990-е** — Goldratt разворачивает методологию: Drum-Buffer-Rope (DBR), Critical Chain Project Management (CCPM, книга «Critical Chain» 1997), Throughput Accounting.
- **2000-е** — формируется **TOCICO** (Theory of Constraints International Certification Organization) и Goldratt Institute / Goldratt Consulting.
- **2011** — Goldratt умирает в возрасте 64 лет, оставив наследие в виде ~10 книг и 1000+ применений в индустрии.

![[toc-5-focusing-steps.png]]

## Пять focusing steps (POOGI — Process of Ongoing Improvement)

1. **Identify** the constraint — найди узкое место
2. **Exploit** the constraint — выжми максимум из существующих ресурсов
3. **Subordinate** everything else to the constraint — все остальные шаги работают в темпе constraint, не быстрее и не медленнее
4. **Elevate** the constraint — если выжать всё мы уже выжали, нужны инвестиции, новый ресурс
5. **Repeat** (avoid inertia) — после каждого шага constraint меняется, повторить цикл; не позволять inertia

Это самые цитируемые 5 пунктов в управлении операциями. Goldratt подчёркивал: **«inertia is the worst constraint»** — после успеха люди расслабляются, и система теряет фокус.

### Пример (упрощённый)

Производство велосипедов:
1. Identify: сборочный конвейер — bottleneck (5 vs 7 от painting upstream)
2. Exploit: убираем простои на сборке (lunch overlap, без остановок), увеличиваем работу до 6/час
3. Subordinate: painting сбавляет до 6/час (release of upstream WIP в темпе constraint)
4. Elevate: вторая смена на сборке — 12/час
5. Repeat: теперь bottleneck может стать painting, либо рынок (лимит спроса). Повторяем.

## Drum-Buffer-Rope (DBR) — синхронизация с constraint

DBR — практический механизм step 3 (Subordinate):

- **Drum (барабан)** — constraint задаёт ритм, как барабан в марширующей колонне
- **Buffer (буфер)** — запас перед constraint (защита от вариативности upstream), обычно временной (часы/смены)
- **Rope (верёвка)** — сигнал назад к точке release of materials, чтобы upstream не работал быстрее, чем constraint потребляет

<!-- IMG: Drum-Buffer-Rope diagram | https://www.leanproduction.com/wp-content/uploads/dbr-diagram.png -->

DBR противоположен push-MRP-логике: вместо «всех загрузить» — «работать в ритме узкого места».

**Simplified DBR (S-DBR)** — упрощённая версия для make-to-order, где буфер только перед constraint, а release rate привязан к dispatching priorities.

## Throughput Accounting (управленческий учёт от ToC)

Goldratt атаковал классический cost accounting (которому учат в MBA). По ToC, важны три метрики:

| Метрика | Что | Цель |
|---------|-----|------|
| **Throughput (T)** | Выручка − truly variable costs (материал) | Максимизировать |
| **Operating Expense (OE)** | Постоянные расходы на превращение inventory в throughput | Минимизировать |
| **Investment / Inventory (I)** | Деньги, замороженные в системе (запасы, основные средства) | Минимизировать |

Решения принимаются по **Throughput per constraint hour** — приоритет тем продуктам, которые дают больше денег на час работы узкого места.

Это разворот: классический accounting считает себестоимость и продаёт по unit margin. Throughput accounting считает marginal contribution и приоритизирует по constraint utilization.

## Critical Chain Project Management (CCPM)

Goldratt применил ToC к управлению проектами в книге «Critical Chain» (1997).

Ключевые отличия от классической PMI/CPM:
- **Critical Chain** — не «critical path», а критическая цепочка с учётом ограничений ресурсов
- **Resource buffers** — защита ключевых ресурсов от перегрузки
- **Project buffer** в конце проекта (вместо safety в каждой задаче)
- **Feeding buffers** — между некритическими цепочками и critical chain
- **No multi-tasking** — главный «грех» проектного управления, который CCPM запрещает
- **Student syndrome / Parkinson's law** — Goldratt объяснил, почему 50%-safety каждой задачи съедается, не доходя до проекта

Кейсы CCPM: NASA, Boeing, Israeli Air Force, US Air Force, Lucent Technologies, ABB.

## Известные кейсы ToC

### Boeing

Goldratt был консультантом Boeing. Применение ToC и CCPM в авиастроении: значительное сокращение lead time производства самолётов и проектов разработки. Boeing использовал DBR и CCPM в 787 program (хотя там было много drama по другим причинам).

### Delta Air Lines

ToC применялся в maintenance / overhaul operations (TechOps). Идея: bottleneck — это availability of specific maintenance bays и certified technicians. После ToC-внедрения — сокращение time-to-return-to-service на десятки процентов (по open publications consultancy companies).

### US Marines

Goldratt и его команда работали с Marine Corps Logistics Command. Применение ToC в обслуживании и поставках в полевые подразделения — публично известный кейс, описан в работе TOCICO.

### Mazda

Японский автопроизводитель применял ToC во время восстановления после Asian financial crisis. Сокращение lead time, рост ROI.

### General Motors, Procter & Gamble, AT&T, Philips, ABB

Goldratt был консультантом для всех — публично подтверждено в его биографии и материалах TOC Institute.

### Nationwide Insurance, Avraham Y. Goldratt Institute

Применение ToC в финансовых услугах (claim processing) — неочевидная, но успешная реализация.

## Связь ToC с Lean и Six Sigma

Часто противопоставляют, но это не конкуренты, а **дополнения**:

| Аспект | Lean | Six Sigma | ToC |
|--------|------|-----------|-----|
| Фокус | Поток, муда | Variability, defects | Constraints |
| Цель | Устранить waste | Сократить вариативность | Максимизировать throughput |
| Метод | Kaizen, Kanban | DMAIC | 5 focusing steps, DBR, CCPM |
| Где сильнее | High-volume, repetitive | Process control | System-level optimization |

В практике используется **TLS** (ToC + Lean + Six Sigma) — комбинированный подход, где ToC даёт фокус, Lean — поток, Six Sigma — статистический контроль.

## Применение к твоему опыту (закупки/ритейл)

ToC применима не только к производству:

- **Bottleneck в закупках**: ограниченное количество категорийных менеджеров → 5 focusing steps на повышении производительности процесса согласования заказов
- **Bottleneck на складе**: receiving / putaway / picking. Drum = picking (если он медленнее всего)
- **Bottleneck в ритейле**: касса в час пик, выкладка в магазине, частота поставок
- **Bottleneck в продажах B2B**: время первого ответа лида, согласование коммерческого

Линза ToC — «где сейчас bottleneck в моей системе?» — должна стать постоянной привычкой руководителя.

## Книги Goldratt'а (рекомендуется)

| Книга | Год | О чём |
|-------|-----|-------|
| **The Goal** | 1984 | Производство, 5 focusing steps. Обязательно прочитать |
| **It's Not Luck** | 1994 | Применение в маркетинге, продажах, supply chain. Thinking processes |
| **Critical Chain** | 1997 | Project management |
| **Necessary But Not Sufficient** | 2000 | ERP и ToC, как технология не решает проблему сама |
| **The Choice** | 2008 | Философия thinking processes |
| **Isn't It Obvious?** | 2009 | Применение к ритейлу — особенно близко тебе |

## Связь с другими методологиями

- **ToC vs MRP**: ToC отказывается от detailed scheduling везде, кроме constraint (см. `[[02-MRP-MRPII-ERP|MRP]]`)
- **ToC vs DDMRP**: оба pull-ориентированные, оба используют буферы; ToC + DDMRP = decoupling в bottleneck (см. `[[03-DDMRP-Demand-Driven|DDMRP]]`)
- **ToC vs Lean**: дополняют друг друга, см. TLS (см. `[[../Lean/index|Lean]]`)
- **ToC + S&OP**: throughput accounting помогает в supply review (см. `[[../SOP/index|S&OP]]`)
- **ToC vs OKR**: 5 focusing steps как фильтр для приоритизации OKR (см. `[[../OKR-KPI/index|OKR/KPI]]`)

## Источники

- [Theory of Constraints Institute](https://www.tocinstitute.org/theory-of-constraints.html)
- [Eliyahu Goldratt biography — TOC Institute](https://www.tocinstitute.org/eliyahu-goldratt.html)
- [Five Focusing Steps — Goldratt Marketing](https://www.toc-goldratt.com/en/toc-application/five-focusing-steps)
- [Theory of Constraints — Lean Production](https://www.leanproduction.com/theory-of-constraints/)
- [PMI — DBR and Critical Chain Buffering Techniques](https://www.pmi.org/learning/library/drum-buffer-rope-critical-chain-buffering-8526)
- [Drum-Buffer-Rope critique — AllAboutLean](https://www.allaboutlean.com/drum-buffer-rope/)
- [TOC impact study (TOC Institute PDF)](https://www.tocinstitute.org/uploads/1/2/7/9/12796657/toc_impact_study.pdf)
- Goldratt, E. M. & Cox, J. (1984). _The Goal_. North River Press.
- Goldratt, E. M. (1997). _Critical Chain_. North River Press.
- Cox, J. F. & Schleier, J. (2010). _Theory of Constraints Handbook_. McGraw-Hill.
