---
aliases: 
updated: 2026-05-13
tags: [education, glossary, concepts]
created: 2026-05-07
date created: 2026-05-07
date modified: 2026-05-13
---

# Concepts & Laws — принципы, законы и эффекты в менеджменте

«Законы» в менеджменте — это эмпирические наблюдения, объясняющие, почему вещи не работают как ожидалось. Знать их — значит видеть ловушки заранее. Тут собраны те, что встречаются в твоей программе обучения.

## A

### Anchoring effect · якорный эффект
Поведенческая ошибка: первая увиденная цифра «якорит» все последующие оценки. Поэтому в переговорах важно ставить anchor первым. В бюджетировании прошлогодний бюджет — мощный anchor (отсюда сопротивление ZBB).

### Apocalypse Bias / Recency Bias
Склонность переоценивать вероятность недавних событий. После пандемии все строили supply chain «на случай ещё одной пандемии». Через 2 года все забыли.

## B

### Black Swan · чёрный лебедь
Nassim Taleb (книга «Чёрный лебедь», 2007). Редкое непредсказуемое событие с огромными последствиями. Логика: невозможно предсказать конкретный black swan, но можно сделать систему resilient к любому.
**Применение:** S&OP scenario planning должен включать «низкая вероятность × высокий impact» сценарии.

### Brooks's Law · закон Брукса
Frederick Brooks, «Mythical Man-Month» (1975): «Adding manpower to a late software project makes it later».
Прибавление людей к опаздывающему проекту делает его ещё более опоздавшим (из-за onboarding и communication overhead).

## C

### Campbell's Law · закон Кэмпбелла
«The more any quantitative social indicator is used for social decision-making, the more subject it will be to corruption pressures and the more apt it will be to distort and corrupt the social processes it is intended to monitor».

Чем сильнее количественный индикатор используется для принятия решений, тем сильнее его искажают.
**Близкое к Goodhart's law** (см. ниже).
**Где:** [[../OKR-KPI/05-KPI-cases-and-pitfalls]]

### Cargo Cult · карго-культ
Метафора Richard Feynman из антропологии. Племя видит, что у белых людей есть самолёты с грузом → строит копии аэродромов из дерева, веря, что это привлечёт самолёты. Делают **форму без сути**.
**В менеджменте:** компании копируют ритуалы (дейли-стендапы, OKR, gemba walks), но без культуры и понимания. Результат — чарты выполняют, эффекта нет.
**Где:** [[../Lean/07-For-the-manager]]

### Cobra Effect · эффект кобры
Британское правительство в Индии: чтобы снизить популяцию кобр, объявило вознаграждение за каждую сданную голову кобры. Местные начали разводить кобр для сдачи. Когда программу отменили — выпустили всех кобр в природу, популяция выросла.
**Урок:** стимулы создают неожиданное поведение. Любой KPI с бонусом риск получить cobra effect.
**Где:** [[../OKR-KPI/05-KPI-cases-and-pitfalls]]

### Conway's Law · закон Конвея
Melvin Conway (1967): «Organizations design systems that mirror their own communication structure».
Компании выпускают софт/процессы по образу своей оргструктуры. Если у вас 5 отделов — у вас будет 5 несвязных систем. Reverse Conway maneuver: сначала спроектировать целевую архитектуру, потом подстроить оргструктуру.

## D

### Dunning-Kruger effect
Когнитивное искажение: люди с малым опытом переоценивают свою компетентность; эксперты — недооценивают. Топ-менеджер «нарисовал план» за 1 встречу, реализаторы за 6 мес показывают, что план не работал.

## G

### Gemba (現場) · место реальной работы
Японский термин TPS: место, где создаётся ценность (цех, склад, торговый зал). «Gemba walks» — руководитель идёт смотреть процесс на месте, не на дашборде.
**Принцип Genchi Genbutsu** (現地現物) — «иди и смотри сам».
**Где:** [[../Lean/07-For-the-manager]]

### Goldratt's Inertia · инерция Голдратта
Goldratt: после того, как ограничение «снято» (5-step exploit/elevate), компании склонны оставлять старые правила управления. Это самое опасное ограничение — **policy constraint, embedded в культуре**.
**Где:** [[../Other-methodologies/04-Theory-of-Constraints]]

### Goodhart's Law · закон Гудхарта
«When a measure becomes a target, it ceases to be a good measure».
Любой индикатор, превратившийся в KPI с бонусом, начинает gaming. Wells Fargo делал 8 счетов на одного клиента, потому что у банкиров был KPI «cross-selling 8 products per customer» — открывали fake accounts.
**Где:** [[../OKR-KPI/05-KPI-cases-and-pitfalls]] · [[../OKR-KPI/06-OKR-vs-KPI-the-difference]]

## H

### Hawthorne Effect
Эксперимент в Hawthorne Works (1924-1933): рабочие производительнее, когда их наблюдают. Любое изменение условий давало рост — потому что внимание само по себе мотивировало.
**Урок для руководителя:** просто факт, что ты обращаешь внимание на процесс, уже улучшает его. Поэтому gemba walks работают.

### Hofstadter's Law · закон Хофстедера
«It always takes longer than you expect, even when you take into account Hofstadter's Law».
Проекты всегда занимают больше, чем планировали — даже с учётом этого закона. Эмпирическая основа для project buffers в CCPM.

### Hick's Law · закон Хика
Время принятия решения растёт логарифмически с числом опций. Объяснение, почему «10 KPI > 80 KPI» — слишком много метрик парализует решение. Аргумент в пользу 4DX (1-2 WIGs).

## I

### Iceberg Principle · принцип айсберга
В качестве: 1 видимый дефект (выше воды) = 30 hidden defects (под водой). Аналогично: 1 customer complaint = 25 silent unhappy customers (TARP study).

## J

### Just-in-Time vs Just-in-Case
Две философии запасов:
- **JIT** (Toyota): минимум запасов, поток
- **JIC**: «на всякий случай», большие safety stocks

После COVID и Suez Canal blockage маятник качнулся к JIC. Реальность: между ними нужен баланс — DDMRP buffer profiles предлагают «Just-Right».

## L

### Law of Diminishing Returns · закон убывающей отдачи
Каждая следующая единица ресурса даёт меньший прирост результата. После определённой точки — нулевой или отрицательный. Применяется к budget allocations: первые $1M рекламы дают $5M revenue, следующий $1M даёт $2M, etc.

## M

### Murphy's Law · закон Мёрфи
«Anything that can go wrong, will go wrong».
Эмпирическая основа для риск-менеджмента: вместо «надеяться на лучшее» — «планировать худшее».

## P

### Pareto Principle · принцип Парето · 80/20
Vilfredo Pareto (1906): 80% последствий приходят от 20% причин.
**Применение:** ABC analysis, key accounts, top defects, top complaints, top SKUs. Концентрация усилий на 20% даёт 80% результата.

### Parkinson's Law · закон Паркинсона
«Work expands so as to fill the time available for its completion».
Если задача может занять 1 день, но дано 5 — она займёт 5. Объяснение, почему CCPM убирает safety из каждой задачи (никто не сдаёт раньше) и собирает в project buffer.

### Peter Principle · принцип Питера
Laurence Peter (1969): «In a hierarchy, every employee tends to rise to his level of incompetence».
Хорошего разработчика делают тимлидом — он плохой тимлид. Хорошего тимлида — head of engineering — он плохой head. Каждый растёт до уровня, на котором перестаёт быть эффективным.
**Lean-противодействие:** Toyota не повышает на менеджмент тех, кто не может научить других. Менеджер = учитель.

## R

### Reverse Conway Maneuver
См. Conway's Law. Сознательно проектируем оргструктуру под желаемую архитектуру системы, а не наоборот.

### Risk Compensation · компенсация риска
Когда люди чувствуют себя безопаснее, они принимают больше рисков. Введение ABS на машинах не снижает аварии (водители едут быстрее). Введение safety stock не снижает out-of-stock (планировщики становятся менее аккуратными).

## S

### Student Syndrome · синдром студента
Goldratt в CCPM: люди начинают серьёзно работать только перед самым дедлайном (как студенты перед экзаменом). Если task имеет 50% safety, это съедается.
**Где:** [[../Other-methodologies/04-Theory-of-Constraints]]

### Sunk Cost Fallacy · ошибка невозвратных издержек
«Мы уже потратили $1M на этот проект, нельзя его закрыть». Невозвратные издержки иррациональны для решений — их уже нет. Решение принимается по marginal cost / marginal benefit будущего.
**Применение:** ZBB прямо борется с sunk cost fallacy в бюджетировании.

## T

### Theory X / Theory Y · теория X/Y МакГрегора
Douglas McGregor (1960):
- **Theory X**: люди ленивы, нужно контролировать → командно-контрольный стиль, KPI с штрафами
- **Theory Y**: люди мотивированы, нужна автономия → OKR, EOS, Holacracy, beyond budgeting

Большинство компаний живут в Theory X, проповедуя Theory Y.

## V

### VUCA — Volatility, Uncertainty, Complexity, Ambiguity
Военный термин (US Army War College, 1990s) → корпоративный мир. Описывает современную бизнес-среду:
- **Volatility** — высокая изменчивость (цены, спрос)
- **Uncertainty** — низкая предсказуемость
- **Complexity** — много взаимосвязанных переменных
- **Ambiguity** — неоднозначность сигналов

**Реакция:** scenario planning (S&OP), DDMRP вместо forecast-driven MRP, Beyond Budgeting вместо AOP.

## W

### Watermelon KPI · «арбузный» KPI
Зелёный снаружи (для отчёта), красный внутри (на самом деле). KPI, который выглядит хорошо в дашборде, но реальность плохая. Часто результат gaming или плохой формулы.
**Лекарство:** проверять KPI «на месте» (gemba), кросс-проверять метрики между собой (Goodhart-resistance).

## Z

### Zero-Sum Thinking · мышление с нулевой суммой
Убеждение, что чужой выигрыш = мой проигрыш. В operations часто проявляется: продавцы не говорят с операциями, потому что «нам нужно больше продаж, а им нужно меньше дёрганий». S&OP-цикл лечит zero-sum thinking через консенсус-процесс.

## Связанные документы

- [[index|Glossary Index]]
- [[01-Operations-metrics|Operations & Supply Chain]]
- [[02-Financial-metrics|Financial]]
- [[04-Methodology-acronyms|Methodology Acronyms]]
- [[../OKR-KPI/05-KPI-cases-and-pitfalls|KPI ловушки]] — много из этих законов там используется

## Источники / рекомендуемые книги

- **«Thinking, Fast and Slow»** — Daniel Kahneman (2011) — поведенческие искажения
- **«The Black Swan»** — Nassim Taleb (2007) — black swans, fragility
- **«Antifragile»** — Nassim Taleb (2012) — что делать с unpredictability
- **«Mythical Man-Month»** — Frederick Brooks (1975) — software / project management classics
- **«The Goal»** — Eliyahu Goldratt (1984) — ToC, inertia, student syndrome
- **«Range»** — David Epstein (2019) — против узкой специализации
- **«Atomic Habits»** — James Clear (2018) — про привычки и систематические improvements
