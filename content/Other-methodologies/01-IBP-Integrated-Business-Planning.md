---
aliases: 
updated: 2026-05-13
tags: [education, other-methodologies, ibp]
created: 2026-05-07
date created: 2026-05-07
date modified: 2026-05-13
---

# IBP — Integrated Business Planning

IBP (Integrated Business Planning) — это эволюция S&OP, которая надстраивает поверх классического процесса три слоя: **финансы, стратегические инициативы и портфель продуктов / R&D**. Термин закрепил Oliver Wight в начале 2000-х, и с тех пор IBP стал де-факто стандартом для крупных международных компаний (Cisco, P&G, Coca-Cola Bottling, AB InBev, Unilever).

> **TL;DR для руководителя.** S&OP отвечает на вопрос «как сбалансировать спрос и поставки на 18 месяцев». IBP отвечает на вопрос «как сбалансировать спрос, поставки, **деньги** и **стратегические инициативы** на 24-36 месяцев». Без единого взгляда CEO / CFO / COO на «как мы будем зарабатывать через 2 года» — IBP закрывает этот gap.

> Если базовый [[../SOP/index|S&OP]] уже изучен, основная связь описана в `[[../SOP/05-IBP-evolution|S&OP → IBP evolution]]`.

## История и происхождение

- **1980-е** — Oliver Wight развивает классический S&OP как часть своей Class A maturity model. Класс A = «ты можешь планировать на 18 месяцев и попадать».
- **2000-е** — Oliver Wight Americas (Dick Ling, George Palmatier и др.) пересобирает S&OP как **Integrated Business Planning**. Идея: «S&OP застрял в supply chain, нам нужен executive-level процесс, который видит и P&L».
- **2010-е** — IBP становится стандартом enterprise consulting (Accenture, Deloitte, EY, BCG продают IBP-трансформации). Software vendors (SAP IBP, Kinaxis, Anaplan, o9) делают это своим маркетинговым нарративом.
- **2020-е** — Gartner маркирует IBP как «mature S&OP, stage 4-5» в своей пятиуровневой шкале.

<!-- IMG: IBP horizon vs S&OP — operational 0-3 мес / tactical 3-18 мес / strategic 18-36 мес | https://www.oliverwight-americas.com/wp-content/uploads/ibp-vs-sop-horizons.png -->

## Что IBP добавляет к S&OP

| Слой | Что есть в S&OP | Что добавляет IBP |
|------|-----------------|-------------------|
| **Спрос** | Demand review, baseline + uplift | + market intelligence, портфельный взгляд |
| **Поставки** | Supply review, capacity, MPS | + multi-sourcing strategy, supplier development |
| **Финансы** | Часто факультативно | **Обязательный финансовый слой**: P&L, cash, capex |
| **Продукт / R&D** | Часто отдельный процесс | **Product Management Review** — pipeline, NPI, lifecycle |
| **Стратегия** | Не входит | **Strategic initiatives review** — статус трансформаций |
| **Горизонт** | 18 мес | 24-36 мес rolling, со связью с 5-летним стратпланом |
| **Cadence** | Месячный | Месячный + ежеквартальный «больший» цикл со стратегией |
| **Owner** | COO / CSCO | CEO как спонсор, CFO + COO + CCO + CHRO как core team |

## Шесть процессов IBP (Oliver Wight)

1. **Product Management Review (PMR)** — портфель, NPI, EOL, R&D pipeline
2. **Demand Review (DR)** — прогноз продаж, scenario planning
3. **Supply Review (SR)** — мощности, запасы, поставщики
4. **Integrated Reconciliation Review (IRR)** — финансовый и операционный gap analysis, формирование вариантов решений
5. **Management Business Review (MBR)** — executive принятие решений по trade-off
6. **Финансовый слой** — пронизывает все 5 шагов, держится CFO

Это именно «6 интегрированных процессов», а не «5 шагов S&OP +1». IBP меняет повестку executive-уровня.

## Кейсы

### Cisco Systems (IT/networking)

- Cisco — один из канонических кейсов Oliver Wight Class A IBP.
- Внедрял IBP в 2000-х после знаменитого «inventory write-down 2001» на ~$2.25 млрд (когда dot-com bust обнажил, что Cisco не мог балансировать спрос/поставки).
- Цели: предотвратить повторение, синхронизировать R&D pipeline (огромный для Cisco) с supply chain и финансами.
- Результат (по Oliver Wight cases и публичным выступлениям Cisco supply chain leadership): сокращение forecast error на десятки процентов, прозрачность revenue forecast для CFO/инвесторов, сокращение запасов при росте сервиса.
- Урок: IBP появляется после крупного провала прогнозирования — это типично.

### Coca-Cola Bottling Consolidated (CCBC) и Coca-Cola Beverages Africa (CCBA)

- Bottlers в Coca-Cola system — независимые компании, со своей структурой издержек, поставками и местными SKU.
- Запустили IBP в середине 2010-х для синхронизации между маркетингом, поставками, финансами на горизонте 24 мес.
- Coca-Cola Beverages Africa также внедряла DDMRP под IBP-зонтиком (см. `[[03-DDMRP-Demand-Driven|DDMRP]]`) — это пример «IBP сверху + DDMRP внутри для исполнения».

### AB InBev

- Крупнейший пивовар мира.
- Использует комбинацию IBP + Zero-Based Budgeting (см. `[[06-ZBB-Zero-Based-Budgeting|ZBB]]`) — это часть «3G-стайла» Jorge Paulo Lemann.
- IBP даёт планирование, ZBB даёт финансовую дисциплину. Связка работает в зрелых FMCG, где есть жёсткий cost-out фокус.

### P&G, Unilever, Pfizer/Lilly

- P&G — пионер internal S&OP/IBP с 1990-х, классически упоминается как лучший практик демон-сенсинга и портфельного IBP.
- Unilever и Pfizer/Lilly — реализовали IBP как часть programs «one supply chain» (Unilever) и «commercial / supply integration» (Pharma).

## Когда IBP оправдан, а когда избыточен

| Ситуация | IBP оправдан? |
|----------|---------------|
| Enterprise (>$1B revenue), public company | Да — нужен финансовый слой для investor relations |
| Multi-BU, многоуровневая иерархия | Да — IBP integrate'ит BU |
| Мощный R&D pipeline (pharma, tech, FMCG) | Да — Product Management Review критичен |
| SMB 50-300 человек | Нет — избыточно. Достаточно S&OP + EOS (см. `[[07-EOS-and-other\|EOS]]`) |
| Стартап / scale-up | Нет — слишком тяжёлая надстройка. Используй OKR + базовый supply review |
| Производственная компания со стабильным портфелем | S&OP достаточно |

## Стек технологий

- **SAP IBP** — лидер enterprise (особенно для компаний на S/4HANA)
- **Kinaxis RapidResponse** — лидер по «what-if» и concurrent planning, используется Cisco, Ford
- **Anaplan** — гибкий моделирующий слой для финансов + supply chain (Coca-Cola, P&G частично)
- **o9 Solutions** — современный AI-driven IBP (Walmart, Pepsi)
- **OMP, Logility** — нишевые игроки

## Чеклист готовности к IBP (для руководителя)

- [ ] У вас уже работает S&OP cadence минимум 12 месяцев (Class B по Oliver Wight)
- [ ] CFO активно участвует в supply review, не только в бюджетировании
- [ ] CEO готов спонсировать процесс (не делегировать)
- [ ] Есть единый продуктовый roadmap на 24+ месяца
- [ ] Стратегические инициативы измеряются количественно
- [ ] Есть IT-платформа или готовность инвестировать (SAP IBP / Anaplan / Kinaxis)
- [ ] Зрелый Master Data Management (без чистых данных IBP не работает)

Если ставишь меньше 5 галочек — рано. Иди сначала «класс B» по S&OP, потом надстраивай.

## Связь с другими методологиями

- **IBP надстраивается над S&OP** — это эволюция, не замена (см. `[[../SOP/index|S&OP]]`)
- **IBP + DDMRP** — IBP даёт тактический план, DDMRP исполняет pull (см. `[[03-DDMRP-Demand-Driven\|DDMRP]]`)
- **IBP + Hoshin Kanri** — Hoshin даёт breakthrough objectives для strategic review (см. `[[05-Hoshin-Kanri\|Hoshin Kanri]]`)
- **IBP + ZBB** — финансовый слой может опираться на ZBB-методику (3G-style — см. `[[06-ZBB-Zero-Based-Budgeting\|ZBB]]`)

## Источники

- [Oliver Wight Americas — IBP Course](https://www.oliverwight-americas.com/public-courses/integrated-business-planning-advanced-sop-course/)
- [Oliver Wight Class A Standard, 7th Edition (Wiley/O'Reilly)](https://www.oreilly.com/library/view/the-oliver-wight/9781119404477/c04.xhtml) — Chapter 4 explicitly on IBP
- [Oliver Wight EAME — IBP Practice Hub](https://oliverwight-eame.com/integrated-business-planning)
- [Establish Inc — What is Integrated Business Planning](https://www.establishinc.com/what-is-integrated-business-planning)
- [George Palmatier — White papers on S&OP/IBP](http://georgepalmatier.com/white-papers-sop-ibp.html)
- [Gartner — S&OP Maturity Model](https://www.gartner.com/en/documents/2587021)
- Goodfellow, Christian (2017). _Integrated Business Planning Workbook_, Oliver Wight series.

См. также `[[../SOP/05-IBP-evolution|S&OP → IBP evolution]]` (планируемая заметка в разделе SOP).
