---
aliases: 
updated: YYYY-MM-DD
tags: [education, lean, cases]
created: 2026-05-07
date created: 2026-05-07
date modified: 2026-05-13
---

# 04 — Кейсы Lean: цифры, результаты, источники

> Lean без цифр — религия. Ниже — 7 кейсов с конкретными метриками: cycle time, defects, inventory, $ savings. Все цифры со ссылками на источники.

## Сводная таблица

| Компания | Период | Cycle Time | Defects / Quality | Inventory / WIP | $ Savings |
|----------|--------|------------|-------------------|------------------|-----------|
| Toyota (TPS origin) | 1948–наст. | Hours/car: 16.8 (JP) vs 25.1 (US) | 60 vs 82 defects/100 cars | 2 ч буфер vs 2 нед в US | Прибыльна в кризис 1973 |
| Boeing (737 moving line) | 1999–2004 | Final Assembly: 22 → 11 дней (-50%) | — | WIP −55%, stores −59% | Footprint −21% |
| Intel (configuration ctrl) | 2010-е | Manufacturing time 3 мес → <10 дней | Качество ↑ | — | Idle time −60% (target 40%) |
| Nike (lean supply chain) | 2008–12 | New style ramp-up −30% | Defects −50% | — | Productivity +10–20%, +$50M margins |
| Amazon (Kaizen + 2-pizza) | 2000-е–наст. | Cycle time on millions of process | Correction of Errors docs | — | Embedded culture |
| Tesla (lean+kaizen) | 2017–наст. | Part every 6 sec | Model 3 ramp resolved | Pre-order = pull | (mixed results) |
| GE (Six Sigma) | 1995–2000 | — | DPMO sharp drop | — | **$12 млрд за 5 лет** |
| ThedaCare (healthcare) | 2003–10 | Door-to-balloon: 90→37 мин | Cut medical errors | — | $27 млн savings |

## 1. Toyota — origin story

**Контекст:** Послевоенная Япония, 1945–1973. Toyota — маленькая компания, ресурсов мало, рынок мал, копировать Ford нельзя.

**Проблема:** Как делать машины разных моделей мелкими сериями (массовое производство а-ля Ford не подходит) с конкурентным качеством и стоимостью.

**Что применили:**
- 30 лет постепенной разработки TPS Тайити Оно (см. [[01-Toyota-Production-System|01]])
- Pull-система Kanban (с 1956 г., после визита в супермаркет)
- Jidoka, Andon, Poka-Yoke
- Kaizen как культура
- SMED (Сигео Синго довёл переналадку штампа с 4 ч до 3 мин)

**Результаты (по данным MIT IMVP, 1990, *The Machine That Changed the World*):**

| Метрика | Японский завод | Американский завод |
|---------|----------------|--------------------|
| Часов сборки на машину | 16,8 | 25,1 |
| Дефектов на 100 машин | 60 | 82 |
| Запас деталей | 2 часа | 2 недели |
| Площадь / квадратный фут | 4,8 | 8,1 |

**Ключевой урок:** Toyota была **единственной японской автокомпанией, которая остаётся прибыльной в нефтяной кризис 1973**. Это и заставило MITI приказать всем перенять TPS, а потом и весь мир обратил внимание.

**Источники:**
- [The Machine That Changed the World — Womack/Jones/Roos](https://www.amazon.com/Machine-That-Changed-World-Revolutionizing/dp/0743299795)
- [TPS — Toyota Global](https://global.toyota/en/company/vision-and-philosophy/production-system/)

## 2. Boeing — 737 moving line transformation

**Контекст:** Boeing 737 — самый продаваемый коммерческий самолёт. К концу 1990-х производство велось в **статических доках**: самолёт стоял, бригады приходили к нему. Цикл — недели простоев между этапами.

**Проблема:** Растущий спрос (после 11 сентября), но завод не масштабировался. Long lead time, высокая стоимость единицы.

**Что применили (с 1999 г.):**
- Перешли на **moving line** по образу автомобильного конвейера. Самолёт буквально движется через цех со скоростью **5 см/мин**.
- Реализовали через RV-лебёдку, прикрученную к полу: «потянули медленно — если что-то не так, остановили, записали, починили на следующем цикле». Это пример Andon в действии.
- 9 тактик flow Boeing для финальной сборки.
- Redesign рабочих мест по принципам 5S и стандартной работы.

**Результаты (1999 → 2004):**

| Метрика | Изменение |
|---------|-----------|
| Factory cycle time | **−46%** |
| Final Assembly flow time | 22 дня → **11 дней** (цель: 8) |
| Stores inventory | **−59%** |
| Work-in-progress (WIP) | **−55%** |
| Factory footprint | **−21%** |
| Время сборки фюзеляжа | **сокращено вдвое** |

**Боковой урок:** Boeing 737 MAX (2018-19) — печальный пример того, что бывает, **когда Lean остаётся, а Jidoka теряется**: в погоне за скоростью и снижением стоимости были обойдены процедуры качества/безопасности (MCAS-system flaw). Подробнее у Marcus Chao в [The Lean Thinker](https://theleanthinker.com/2024/07/02/boeing-the-turning-points/).

**Источники:**
- [The Lean Journey at the Boeing Company — John Black](http://johnblackandassociates.com/uploads/2/0/7/8/20782048/the-lean-journey-at-boeing.pdf)
- [Lean enterprise Boeing 737 — Cengage case study](http://cws.cengage.co.uk/colekelly7/students/Video%20Cases/Chapter%2038%20-%20Video%20Case%20Study%2065.pdf)
- [Boeing's Lean Manufacturing Strategies — OrcaLean](https://www.orcalean.com/article/how-boeing's-lean-manufacturing-strategies-reduce-production-costs-and-improve-efficiency)
- [Lean Manufacturing — On the Move (Flightglobal, 2001)](https://www.flightglobal.com/strategy/2001/03/lean-manufacturing-on-the-move/)

## 3. Intel — Lean Six Sigma в полупроводниках

**Контекст:** Intel — производство микрочипов = высочайшая сложность процессов, ультранизкая допустимая дефектность (3,4 на миллион — Six Sigma уровень). Каждый миллиметр пластины (wafer) измеряется тысячами параметров.

**Проблема (R&D configuration control):** Слишком много идле-времени и потерь в процессе контроля конфигурации между R&D и production ramp-up.

**Что применили:** Lean Six Sigma (DMAIC) — сочетание Lean (поток) и Six Sigma (вариация). Один из ключевых элементов — Intel'овская методика **«Copy Exactly!»** (копировать процесс производства один-в-один из R&D-факта в массовое производство — без «творческой адаптации» на местах).

**Результаты:**

| Метрика | Результат |
|---------|-----------|
| Idle time / non-value-added | **−60%** (target был −40%) |
| Manufacturing time микрочипа | **>3 мес → <10 дней** |
| Качество | ↑, customer satisfaction ↑ |
| Costs | ↓ |
| Stakeholder satisfaction | ↑ без потери технической строгости |

**Что особенно ценно:** Intel показал, что Lean **работает в высокотехнологичной отрасли с экстремальными требованиями** — а не только в простой штамповке.

**Источники:**
- [The application of Lean Six Sigma to configuration control in Intel — Emerald Insight](https://www.emerald.com/insight/content/doi/10.1108/ijlss-02-2014-0004/full/html)
- [Inside Intel's Lean Manufacturing — OrcaLean](https://www.orcalean.com/article/inside-intel's-lean-manufacturing:-how-the-semiconductor-giant-stays-ahead-of-the-competition)

## 4. Nike — Lean Supplier Capability Program

**Контекст:** Nike — не производитель, а brand+design+marketing. Производство — на сотнях фабрик контрактных подрядчиков по всему миру (Вьетнам, Индонезия, Китай). Старая модель: «купить дешёво у любого, кто согласен».

**Проблема (середина 2000-х):** Скандалы вокруг условий труда в фабриках-партнёрах, высокий уровень дефектов, медленные ramp-up'ы новых моделей, долгие сроки поставки.

**Что применили (2008–2012):**
- Запустили **Nike Lean Supplier Capability Program**: помогали фабрикам-партнёрам внедрять TPS-практики (5S, kaizen, standard work, Andon).
- Привязали ранг поставщика (% бизнеса, который Nike даёт) к уровню Lean-зрелости.
- Это одновременно повысило качество **и** условия труда — связь, документированная в академических исследованиях.

**Результаты (по 2012 г.):**

| Метрика | Изменение |
|---------|-----------|
| Defects | **−50%** |
| Скорость поставки | **+40%** |
| Productivity | **+10–20%** |
| Время ramp-up новой модели | **−30%** |
| Margin uplift (от sustainable+lean) | **+$50 млн** |
| Стоимость единицы (savings) | **−$0,15** |
| Серьёзные нарушения трудового законодательства | **−15%** (Stanford GSB study) |

**Adoption:** К FY2011 — 80% единиц обуви, 57% одежды, 11% оборудования производились на Lean-сертифицированных линиях.

**Ключевой урок:** **Lean можно внедрять в supply chain, не владея производством.** Nike не покупает фабрики — он развивает поставщиков. Это прямой аналог того, что должен делать руководитель закупок: не «выжать поставщика по цене», а растить его lean-зрелость как актив.

**Источники:**
- [Nike Strikes Gold with Lean Manufacturing — PEX Network](https://www.processexcellencenetwork.com/lean-six-sigma-business-performance/articles/nike-strikes-gold-with-lean-manufacturin)
- [How Nike's Lean Manufacturing Transformed Its Supply Chain — Supply Chain Nuggets](https://supplychainnuggets.com/how-nikes-lean-manufacturing-transformed-its-supply-chain/)
- [Does Lean Improve Labor Standards? Management Science (Stanford GSB)](https://www.gsb.stanford.edu/faculty-research/publications/nikes-strategy-improve-conditions-its-global-supply-chain-case-study)
- [Nike Lean Supplier Capability Program — ILO](https://www.ilo.org/media/285046/download)

## 5. Amazon — Kaizen + Two-Pizza Teams

**Контекст:** Amazon — не классическая Lean-компания, но многие принципы операционной эффективности, которые Безос привнёс с ранних дней, **прямо параллельны Lean**.

**Проблема (середина 2000-х):** Big-bureaucracy slowdown — большие команды, бесконечные согласования, медленная итерация.

**Что применили:**

### Two-Pizza Teams
Команды должны быть такими маленькими, чтобы их **могли накормить две пиццы** (т.е. ~6–10 человек). Каждая команда — autonomous, full-stack, owns its outcome end-to-end.

**Связь с Lean:** прямая аналогия с **autonomous teams в TPS** + минимизация передач (handoffs = transport waste).

### Kaizen at Amazon
- Front-line Kaizen approach: каждый член топ-менеджмента **минимум 1 рабочий день в год работает на фронтлайне** (склад, оператор).
- **Dream Kaizen Team** — кросс-функциональная команда (frontline + engineers + executives) решает реальные операционные проблемы.
- **Correction of Errors (COE)** документы — после любой проблемы команда пишет document «5 Why + что мы изменили в процессе»; они хранятся в searchable database.

### Operational excellence
- Working backwards (от пресс-релиза к продукту) = customer-pull mindset.
- Single-threaded leaders = ownership.
- Ruthless metrics-driven culture (Bezos: "Good intentions don't work, mechanisms work").

**Результаты:** Сложно дать прямые цифры (Amazon не публикует savings), но эмерджентный результат — компания, которая **на масштабе сотен тысяч сотрудников и миллиардов транзакций сохраняет startup-скорость итерации**. Это и есть зрелый Lean.

**Источники:**
- [Amazon's Two Pizza Teams — AWS Executive Insights](https://aws.amazon.com/executive-insights/content/amazon-two-pizza-team/)
- [Amazon Lean Management — Henry Harvin](https://www.henryharvin.com/blog/amazon-lean-management/)
- [The Amazon Way: How Technology Company is Changing Market through Lean — Pipefy](https://www.pipefy.com/blog/the-amazon-lean-way/)
- [Powering Innovation with Two-Pizza Teams — AWS eBook](https://d1.awsstatic.com/executive-insights/en_US/two_pizza_teams_eBook.pdf)

## 6. Tesla — попытка «out-Toyota Toyota»

**Контекст:** Tesla основана в 2003-м, в 2010-м купила Toyota'вский завод **NUMMI** во Фримонте — тот самый завод, где TPS впервые столкнулся с американскими рабочими.

**Проблема (2017–18, Model 3 ramp):** Знаменитый «production hell» — Tesla не могла выйти на план производства Model 3. Музск пытался **гипер-автоматизировать** конвейер; результат — палатка с ручной сборкой за периметром завода.

**Что применили:**
- Изначально партнёрились с Toyota (взяли советы по TPS).
- Pull system: каждая Tesla **pre-ordered** (нет накопленных запасов).
- Kaizen-команды по решению bottleneck'ов в Model 3 ramp-up.
- Часть (например, конвейеры) сначала пытались убрать (Musk: «лишняя автоматизация — потеря»), потом частично вернули.
- Вертикальная интеграция: батарея, чипы, ПО — всё своё (нет supply chain Mura).

**Результаты — смешанные:**

| Что получилось | Что не получилось |
|----------------|-------------------|
| Model 3 в итоге вышла на массовое производство | Production hell стоил Tesla миллиарды и почти банкротство |
| Pull-модель прямых продаж клиенту | Чрезмерная автоматизация, потом откат |
| Скорость инноваций (1 деталь каждые 6 сек) | Качество сборки в первые годы Model 3 — критика |
| Vertical integration | Многократный пере-design процессов |

**Урок:** Tesla показала, что **Lean — это не просто скорость**. Без Jidoka (встроенного качества) и без баланса human/machine скорость разрушает себя. Boeing 737 MAX — другой пример той же ловушки.

[LEI Lean Lessons from Tesla](https://www.lean.org/the-lean-post/articles/lean-lessons-from-tesla/) специально подчёркивает: Tesla **«начала с Lean, потом отбросила уроки»**.

**Источники:**
- [Lean Lessons from Tesla — Lean Enterprise Institute](https://www.lean.org/the-lean-post/articles/lean-lessons-from-tesla/)
- [The Lean Transformation of Tesla and Elon Musk — Lean Factories](https://leanfactories.com/the-lean-transformation-of-tesla-and-elon-musk/)
- [Tesla is Lean Six Sigma at Its Finest — SixSigma.us](https://www.6sigma.us/kaizen/tesla-is-lean-six-sigma-at-its-finest/)

## 7. GE под Welch — Six Sigma at scale

**Контекст:** General Electric, конец 1990-х. Конгломерат с десятками divisions от авиадвигателей до бытовой техники до финансов.

**Проблема:** Уровень дефектов и вариативности процессов разный по дивизионам, нет единой методологии непрерывного улучшения, на которую завязано senior management.

**Что применили (1995–2000):**
- Jack Welch (CEO) как-то прочитал кейс Motorola (Six Sigma) и решил: GE будет крупнейшим Six Sigma-чемпионом в мире.
- **Все** топ-руководители прошли 13-дневное / 100-часовое обучение DMAIC.
- Все должны были закрыть **минимум один Six Sigma project** к концу 1998.
- В 1997 — **бонусы topa привязаны к Six Sigma результатам**.
- **40% топ-менеджмента бонуса** = от Six Sigma.
- Полная Belt-структура (Yellow / Green / Black / Master Black) на всех уровнях.

**Результаты:**

| Год | Инвестиции в Six Sigma | Возврат |
|-----|------------------------|---------|
| 1996 | ~$200M | $170M |
| 1997 | $400M | $700M |
| 1998 | — | $1,2B |
| 1999 | — | $2,0B |
| 2000 | — | $2,5B+ |
| **5-летний total** | — | **~$12 млрд savings** |

**Ключевой урок №1 — leadership commitment.** Welch не «делегировал» Six Sigma в отдел качества, он сам участвовал, делал surprise visits на shop floor, требовал monthly reports. Это и сработало.

**Ключевой урок №2 — Six Sigma не равно Lean.** GE-программа была чистый Six Sigma (фокус на вариативности и DPMO). Только в 2000-е GE добавил Lean-составляющую и появился Lean Six Sigma. Подробно — в [[06-Lean-Six-Sigma|06]].

**Источники:**
- [Six Sigma Case Study: General Electric — SixSigma.us](https://www.6sigma.us/ge/six-sigma-case-study-general-electric/)
- [Jack Welch and Six Sigma — SixSigma Daily](https://www.sixsigmadaily.com/remembering-jack-welch-and-his-relation-to-six-sigma/)
- [GE and Six Sigma: The Beginning — 6sigma.com](https://6sigma.com/ge-and-six-sigma-the-beginning-of-a-beautiful-relationship/)
- [How GE Saved Billions Using Six Sigma — LinkedIn / Musyoka](https://www.linkedin.com/pulse/how-general-electric-saved-billions-using-six-sigma-john-musyoka)

## 8. ThedaCare — Lean в здравоохранении (бонусный кейс)

**Контекст:** ThedaCare — система здравоохранения в Висконсине. 3 больницы, 27 клиник, 5000 сотрудников. До 2003-го — типичный американский провайдер: высокие costs, медицинские ошибки, неудовлетворённые пациенты.

**Что применили (с 2003 г.):**
- John Toussaint (CEO) после визита в Toyota и в Virginia Mason запустил Lean-трансформацию.
- Value Stream Mapping всех клинических процессов.
- Rapid Improvement Events (kaizen blitz) — недельные команды на конкретных процессах.
- One-piece flow для пациентов.
- Daily huddles, andon, A3-thinking on every process.

**Результаты (за 7 лет):**

| Метрика | Изменение |
|---------|-----------|
| Total savings | **$27 млн** (без сокращений!) |
| Door-to-balloon time для инфаркта | **90 → 37 мин** (50% быстрее = жизни спасены) |
| Wait time для радиохирургии | **26 → 6 дней** |
| % stroke patients с CT scan за <25 мин | **51% → 89%** |
| Medical errors | значительное снижение |
| Staff morale | значительное улучшение |

**Ключевой урок:** **Lean переносится в любую отрасль, где есть процесс**, при условии адаптации (см. [[05-Lean-in-services-and-office|05]]).

**Источники:**
- [Going Lean in Health Care — IHI white paper](https://www.entnet.org/wp-content/uploads/files/GoingLeaninHealthCareWhitePaper-3.pdf)
- [On The Mend — Toussaint, Gerard (book)](https://createvalue.org/product/on-the-mend/)
- [Innovation and Lean Thinking — PSNet AHRQ](https://psnet.ahrq.gov/perspective/innovation-and-lean-thinking-mutually-supportive-partners-transformation-health-care)

## Кросс-кейс выводы для руководителя

### 1. Lean работает везде, но требует адаптации

Toyota / Boeing / Intel / Nike / Tesla — производство. Amazon / ThedaCare — услуги. GE — конгломерат. Все получили эффект, но **никто не «копировал Toyota буквально»**. Каждый адаптировал.

### 2. Топ-leadership commitment — необходимое условие

Без CEO-уровня (Toyoda, Welch, Toussaint, Bezos) — Lean не приживается. Нельзя «делегировать Lean в отдел качества».

### 3. Цифры повторяются

Типовые результаты Lean-трансформации (по совокупности кейсов):
- Cycle time / Lead time: **−40 до −60%**
- Inventory / WIP: **−40 до −60%**
- Defects: **−50% до −90%**
- Footprint: **−20%**
- Productivity: **+10 до +30%**

Если инициатива даёт менее 20% улучшения — либо копают не там, либо Lean-инструменты применяются формально.

### 4. Опасность gone wrong: Boeing 737 MAX, Tesla production hell

Lean в погоне за скоростью без Jidoka и без respect for people = катастрофа. Это **самый важный урок** для руководителя — Lean не про экономию любой ценой.

### 5. Поставщики — твой Lean-fronter

Кейс Nike показывает: лучшие закупочные результаты — не от давления на цену, а от развития Lean-зрелости поставщика. Прямая параллель с твоим контекстом в закупках.

## Связанные заметки

- [[index|Lean Index]]
- [[01-Toyota-Production-System|01 — TPS]]
- [[02-8-wastes-Muda-Mura-Muri|02 — 8 потерь]]
- [[03-Lean-tools|03 — Инструменты]]
- [[05-Lean-in-services-and-office|05 — Lean вне производства]] (ThedaCare детальнее)
- [[06-Lean-Six-Sigma|06 — Lean Six Sigma]] (GE детальнее)
