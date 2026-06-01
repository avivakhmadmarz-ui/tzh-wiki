---
title: "06 — Supply Chain Risk Management"
aliases: ["Supply Chain Risk", "Resilience", "BCP", "Risk Mitigation"]
type: note
status: active
domain: education
module: 04-Supply-Chain
tags: [education, supply-chain, risk, resilience, bcp, nearshoring, geopolitical]
created: 2026-05-18
updated: 2026-05-18
---

# 06 — Supply Chain Risk Management

> 2020-2025 годы стали серией шоков — COVID-19, блокировка Суэцкого канала, дефицит полупроводников (semiconductor shortage), война в Украине, санкции против РФ. Эпоха «оптимизированной до минимума» цепочки закончилась — теперь требуется баланс между эффективностью (efficiency) и устойчивостью (resilience). Управление рисками превратилось из периферийной функции в центральную стратегическую задачу.

## Карта раздела

![](attachments/diagrams/04-supply-chain-risks-matrix.svg)

## 1. Эволюция мышления о рисках цепочки

### 1.1 Контекст и легитимность

Каноничные работы по resilience — у **Yossi Sheffi** (MIT), профессора и исследователя цепочек поставок. Книги **«The Resilient Enterprise»** (MIT Press, 2005, после теракта 9/11) и **«The Power of Resilience»** (2015, после Тохоку и Тайфуна Хайянь) — основа дисциплины. Третья книга **«The New (Ab)Normal»** (2020) — реакция на COVID.

Sheffi показал, что компании, инвестировавшие в resilience до шока, восстанавливались в разы быстрее и теряли меньше выручки. Это превратило resilience из «затрат» в инвестиции с измеримым ROI.

### 1.2 От efficiency-first к balanced approach

В 1990-2010-х доминировала философия «эффективность прежде всего» (efficiency-first):

- **JIT** (Just-in-Time — «точно в срок») — минимальные запасы
- **Single sourcing** (закупка у единственного поставщика) — один поставщик на категорию, чтобы получить максимальную скидку
- **Global sourcing** (глобальный сорсинг) — производство в самой дешёвой юрисдикции
- **Lean operations** (бережливые операции) — минимизация всего «лишнего»

Этот подход максимизировал ROIC и операционную маржу, но создавал уязвимость:

- COVID-19 (2020) — сбои у единственных поставщиков в Ухане остановили глобальные цепочки
- Блокировка Суэцкого канала (март 2021) — корабль Ever Given застрял на 6 дней, остановив 15% глобального флота
- Дефицит полупроводников (2020-2023) — автопром потерял миллиарды от остановки производства из-за нехватки чипов
- Война в Украине (2022) — сбои поставок зерна, удобрений, металлов
- Санкции против РФ (2022-2024) — резкая перестройка сорсинга для российских компаний

К 2024 году консенсус: цепочка должна быть **сбалансированной (balanced)** — достаточно эффективная для конкурентоспособной цены и достаточно устойчивая для выживания при шоках.

**Ключевой вывод 1.** Эпоха чистой эффективности закончилась с COVID-19. Зрелое управление цепочкой требует структурного баланса между эффективностью и устойчивостью. Это не «или-или», а вопрос правильного соотношения для конкретной индустрии и стратегии.

## 2. Шесть категорий рисков

### 2.1 Классификация

![](attachments/diagrams/04-supply-chain-risks-matrix.svg)

Supply chain risks обычно классифицируются по шести категориям по источнику:

| Категория | Описание | Примеры |
|-----------|----------|---------|
| **Geopolitical** (геополитические) | Санкции, войны, торговые барьеры, национализация | Санкции против РФ, торговая война США-КНР, Brexit |
| **Natural** (природные) | Стихийные бедствия, пандемии, экологические катастрофы | COVID-19, землетрясение в Тохоку, блокировка Суэцкого канала |
| **Financial** (финансовые) | Дефолт поставщика, курсовые колебания, кредитный риск | Дефолт ключевого поставщика, девальвация |
| **Operational** (операционные) | Срыв качества, кибератака, кадровый кризис | Атака программ-вымогателей (ransomware) на 3PL-партнёра, отзыв (recall) продукции |
| **Regulatory** (регуляторные) | Изменение законов, сертификации, соответствие | GDPR (General Data Protection Regulation — Общий регламент защиты данных ЕС), Carbon Border Adjustment (углеродная корректировка на границе), валютный контроль |
| **Demand** (спрос) | Резкое падение или рост спроса, изменение предпочтений | Эффект кнута в COVID, отказ от пластика |

### 2.2 Geopolitical risks

Самая обсуждаемая категория с 2022 года. Включает:

- **Санкции** — запрет торговли с определёнными странами / компаниями / лицами
- **Tariffs** — повышение пошлин, торговая война
- **Sanctions secondary effects** — риск вторичных санкций для третьих сторон, торгующих с подсанкционными
- **Currency controls** — ограничения на валютные операции
- **Nationalization** — экспроприация иностранного бизнеса
- **War / conflict** — прямое влияние конфликтов на цепочки

Для российской компании эта категория после 2022 года стала доминирующей: перестройка sourcing с EU/US на CN/IN/TR, поиск платёжных маршрутов через third countries, работа с параллельным импортом.

### 2.3 Natural risks

Естественные риски — наименее предсказуемые:

- Землетрясения, наводнения, ураганы
- Пандемии (COVID-19, MERS, SARS)
- Лесные пожары, экстремальные температуры
- Climate change как long-term тренд (увеличение частоты экстремальных событий)

Sheffi показывает, что катастрофические natural events случаются примерно раз в 5-10 лет в каждой крупной географической зоне. Это не «black swan», а обычная статистика — компании должны планировать наличие подобных событий.

### 2.4 Financial risks

Финансовые риски на стороне партнёров:

- Bankruptcy ключевого поставщика
- Currency fluctuation (девальвация рубля в 2014, 2022)
- Interest rate changes (влияет на стоимость capital)
- Credit risk клиентов

Управление через credit-monitoring поставщиков и клиентов, hedging (currency, interest rate), multi-supplier strategy.

### 2.5 Operational risks

Внутренние и партнёрские операционные сбои:

- Quality failures (recall продукции)
- Cyber attacks (ransomware, data breach)
- Labor disputes (страйки, забастовки)
- Equipment failures (поломка ключевого оборудования)
- Loss of key personnel (уход критичного эксперта)

Кибератаки стали особенно частыми в 2020-х. Примеры: NotPetya (2017, $10 млрд глобальных потерь, включая Maersk), Colonial Pipeline (2021), различные ransomware на 3PL-провайдерах.

### 2.6 Regulatory risks

Изменение регуляторики может радикально изменить экономику цепочки:

- Tariff changes (Trade Wars 2018-2019)
- Carbon taxes (CBAM в ЕС с 2026)
- GDPR / data localization
- Industry-specific regulations (food safety, pharmaceutical, automotive)
- Trade compliance (export controls)

### 2.7 Demand risks

Резкие изменения спроса:

- Pandemics (всплеск спроса на отдельные категории + резкое падение на другие)
- Trend shifts (отказ от пластика, тренд на eco-products)
- Bullwhip effect — усиление колебаний вверх по цепочке
- Cyclical industries (automotive, capital goods)

**Ключевой вывод 2.** Six categories дают структурированный обзор рисков. Компания должна оценивать каждую категорию для своей конкретной ситуации — не игнорируя ни одну. Particularly geopolitical risks для российских компаний после 2022 — приоритет №1.

## 3. Стратегии митигации рисков

### 3.1 Buffer strategies — буферизация

Самая простая стратегия — buffer'ы, увеличенные запасы / capacity:

- **Strategic inventory buffer** — повышенные safety stocks на критичные SKU
- **Capacity buffer** — недозагруженные мощности для absorbing demand spikes
- **Time buffer** — увеличенные lead times в контрактах для absorbing delays

Стоимость: рост запасов / упущенная маржа от unused capacity. Подходит для несфокусированной защиты (когда не знаешь, какой именно риск сработает).

### 3.2 Multi-sourcing — диверсификация поставщиков

Иметь несколько поставщиков для каждой критичной категории:

- **Geographic diversification** — поставщики в разных регионах / странах
- **Multi-supplier strategy** — 2-3 поставщика на один компонент с заранее согласованным split (например, 50/30/20)
- **Backup supplier** — qualified backup, готовый увеличить долю при необходимости

Стоимость: меньший discount от каждого поставщика, рост сложности управления, разные lead times. Подходит для критичных категорий.

### 3.3 Nearshoring / Friendshoring

Перенос производства / sourcing ближе к рынку или в дружественные страны:

- **Nearshoring** — географически ближе (например, из CN в Мексику для US-рынка)
- **Friendshoring** — политически дружественные страны
- **Reshoring** — возврат в свою страну

Стоимость: типично 10-30% выше цены продукта. Подходит для критичных категорий, особенно после torrent disruptions последних лет.

### 3.4 Vertical Integration

Покупка ключевых поставщиков или внутреннее производство critical components:

- Apple verticalнее integrate chip design (M-series)
- Tesla — собственная gigafactory
- Sportswear брендов — покупка fabric suppliers

Стоимость: огромные капитальные затраты, потеря фокуса. Подходит для очень критичных компонентов.

### 3.5 Flexible contracts

Контракты, дающие гибкость в кризисе:

- **Take-or-pay clauses** с гибкостью
- **Volume flexibility** — поставщик готов принять колебания заказа ±30%
- **Force majeure clauses** — четкое определение, что является непреодолимой силой
- **Termination clauses** — возможность смены поставщика при определённых условиях

Стоимость: меньший discount за гибкость. Подходит для среднеуровневых рисков.

### 3.6 Insurance

Страхование рисков:

- **Cargo insurance** — для грузов в пути
- **Trade credit insurance** — защита от дефолта клиента
- **Political risk insurance** — для инвестиций в развивающиеся страны
- **Sinosure** — для торговли с CN (см. модуль 06 ВЭД)

Стоимость: страховая премия 0.5-3% от стоимости застрахованного. Подходит для конкретных, измеримых рисков.

### 3.7 Visibility и Early Warning

Невозможно митигировать риск, если о нём узнаёшь поздно. Современные инструменты:

- **Supply chain visibility platforms** (Project44, FourKites, riskmethods, Resilinc)
- **Geopolitical monitoring** (PolitDecks, Maplecroft)
- **Weather monitoring** (для weather-sensitive грузов)
- **Supplier financial monitoring** (Dun & Bradstreet, Bureau van Dijk)

Раннее предупреждение позволяет активировать митигацию до того, как риск материализуется.

**Ключевой вывод 3.** Стратегии митигации — это набор инструментов, не «one-size-fits-all». Зрелая компания применяет разные стратегии для разных категорий рисков и продуктов, опираясь на cost-benefit анализ.

## 4. Resilience vs Efficiency — главный trade-off

### 4.1 Спектр выбора

![](attachments/diagrams/04-resilience-vs-efficiency.svg)

Каждая компания выбирает положение на спектре:

- **Efficiency-first:** JIT, single sourcing, минимум запасов, lean operations. Низкая стоимость, высокий ROIC, но уязвимость к шокам
- **Resilience-first:** многопоставщиковость, страховые запасы, регионализация, гибкие контракты. Устойчивость к шокам, но рост стоимости

Полная efficiency или полная resilience — крайности; реальный выбор — где-то посередине.

### 4.2 Финансовые последствия

| Метрика | Efficiency-first | Resilience-first |
|---------|------------------|-------------------|
| Стоимость запасов | Низкая | Выше на 10-25% |
| ROIC | Высокий | Ниже на 2-5 п.п. |
| Operating margin | Высокая | Ниже на 1-3 п.п. |
| Время восстановления после disruption | 6-18 месяцев | 2-6 месяцев |
| Потеря выручки во время disruption | 15-30% | 3-8% |

Sheffi показал, что resilience-first компании теряют меньше в кризисе, но это компенсируется только через долгое время и при условии, что disruption случается.

### 4.3 Дифференцированный подход

Зрелое решение — дифференцированный подход:

- **Critical products** (high impact на бизнес, IP-зависимые) — resilience-first
- **Strategic products** (важные, но не критичные) — balanced
- **Commodity products** (легко заменяемые) — efficiency-first

Это не «или-или» для всей цепочки, а отдельные решения для каждой категории.

### 4.4 Стратегический вопрос

Главный стратегический вопрос для CEO / Board: **какова толерантность компании к risk?**

- High-tolerance компании (фондовые, с быстрым доступом к капиталу) могут позволить себе efficiency-first
- Low-tolerance компании (с высоким уровнем debt, в кризисных индустриях) должны инвестировать в resilience
- Этот выбор должен быть осознанным, формально документированным, регулярно пересматриваемым

**Ключевой вывод 4.** Resilience vs efficiency — главный стратегический trade-off в supply chain. Это не операционный вопрос, а C-level / Board level. Выбор должен быть осознанным и дифференцированным по категориям продуктов.

## 5. Business Continuity Planning (BCP)

### 5.1 Что такое BCP

**BCP** (Business Continuity Planning — планирование непрерывности бизнеса) — формальная методология подготовки к disruptions и плана действий при их наступлении.

Стандарт — **ISO 22301** (Business Continuity Management Systems), от ISO. Многие крупные компании сертифицированы по этому стандарту.

### 5.2 Структура BCP

Полный BCP включает:

1. **Risk assessment** — идентификация рисков и оценка их вероятности / impact
2. **Business Impact Analysis (BIA)** — какие процессы критичны, сколько компания может работать без них
3. **Recovery strategies** — конкретные стратегии восстановления для каждого критичного процесса
4. **Recovery Time Objectives (RTO)** — целевое время восстановления каждого процесса
5. **Recovery Point Objectives (RPO)** — максимально допустимая потеря данных при восстановлении
6. **Continuity procedures** — пошаговые инструкции
7. **Training and testing** — регулярные exercises для проверки готовности
8. **Communication plan** — кто кому что сообщает в кризисе

### 5.3 Tabletop exercises

Один из самых мощных инструментов BCP — **tabletop exercises**: симуляция кризисного сценария с участием всей C-level и ключевых функций.

Типичный сценарий: «Сегодня утром произошла ransomware-атака на WMS вашего ключевого DC. Что вы делаете?» Команда проходит через все шаги — от первого часа до полного восстановления — и выявляет gaps в готовности.

Sheffi рекомендует tabletop exercises каждый квартал, с разными сценариями.

### 5.4 Lessons from COVID

COVID-19 стал крупнейшим тестом BCP в истории. Lessons:

- **Single-point-of-failure** анализ обязателен: где ваш бизнес зависит от одного поставщика, одной локации, одной системы
- **Cross-training** team members — критичные навыки должны быть у нескольких людей
- **Remote work readiness** — оказалось, что часть операций можно делать удалённо, что раньше казалось невозможным
- **Communication** в кризисе — кризисный центр с чёткими ролями и регулярными updates
- **Government engagement** — отношения с регуляторами критичны в кризисе

**Ключевой вывод 5.** BCP — формальная дисциплина, требующая регулярных tabletop exercises и постоянного обновления. Зрелые компании выделяют отдельную позицию Business Continuity Manager и сертифицированы по ISO 22301.

## 6. Российская специфика после 2022 года

### 6.1 Природа изменений

После февраля 2022 года российские supply chains столкнулись с экстраординарными изменениями:

- **Уход или ограничения** западных поставщиков (Apple, Adobe, Microsoft, SAP, Oracle, McDonald's, Starbucks и сотни других)
- **Санкции** на импорт технологий (chips, dual-use goods)
- **Платёжные ограничения** — отключение от SWIFT крупных российских банков
- **Логистические сбои** — закрытие воздушного пространства, ограничения на ж/д перевозки через ЕС
- **Параллельный импорт** — новая регуляторная категория, разрешившая ввоз без согласия правообладателя

### 6.2 Стратегические сдвиги

Российские компании перестраивают цепочки по нескольким направлениям:

1. **Sourcing shift to CN / IN / TR** — переход с EU/US поставщиков на азиатских / турецких
2. **Payment maps** — использование платёжных коридоров через third countries (ОАЭ, Гонконг, Кыргызстан, Армения)
3. **Параллельный импорт** — для электроники, авто, brands с уникальной продукцией
4. **Локализация** — производство внутри РФ для критичных категорий
5. **Substitution** — переход на российские / БРИКС-альтернативы (software, оборудование)

### 6.3 Управление новыми рисками

Специфические российские риски 2024-2025:

- **Вторичные санкции** на партнёров в third countries — постоянный мониторинг
- **Валютный контроль 173-ФЗ** — сложности с платежами поставщикам
- **Курсовая волатильность** — резкие колебания рубля влияют на экономику импорта
- **Транспортные ограничения** — длинные маршруты через Каспий, Турцию, KZ
- **Дефицит специалистов** — отток части кадров после 2022

### 6.4 Best practices для российских компаний

- **Multi-supplier для критичных категорий** — диверсификация по 3+ странам
- **Inventory buffer** — повышенные safety stocks для импортных категорий
- **Currency hedging** — фиксация курса хотя бы на часть платежей
- **Compliance officer** — отдельная функция для отслеживания изменений в санкциях
- **Сценарное планирование** — регулярное upgрейд сценариев

**Ключевой вывод 6.** Российские supply chains после 2022 года находятся в режиме постоянной адаптации. Управление рисками — приоритет №1, и компании, успешно перестроившиеся, получили конкурентное преимущество над теми, кто отставал. Это live exam для всех тех методологий, описанных в этой заметке.

## Сводный практический протокол

Построение supply chain risk management в компании среднего размера:

| Месяц | Шаг | Артефакт |
|-------|-----|----------|
| 1 | Identification рисков по 6 категориям | Risk register |
| 2 | Business Impact Analysis для критичных процессов | BIA report |
| 3 | Расчёт RTO / RPO, выбор стратегий митигации | Risk mitigation plan |
| 4 | Внедрение visibility tools и early warning | Risk dashboard |
| 5 | First tabletop exercise — простой сценарий | Lessons learned |
| 6-12 | Регулярные tabletop quarterly, обновление register | Mature BCP |

После 12 месяцев — постоянная работа: ежеквартальные exercises, обновление register, мониторинг geopolitical environment.

## Применение для руководителя

| Целевая роль | Что взять из заметки |
|--------------|---------------------|
| **CEO / Board** | Resilience vs efficiency как стратегический выбор; tolerance to risk; регулярные ревью BCP |
| **COO** | Запуск supply chain risk management; tabletop exercises; quarterly risk review |
| **Директор закупок** | Multi-supplier strategy для критичных категорий; nearshoring / friendshoring; supplier financial monitoring |
| **Финансовый директор** | Currency hedging; trade credit insurance; financial impact disruptions |
| **CIO / CISO** | Cybersecurity как часть supply chain risk; ransomware preparedness |
| **Compliance officer** | Sanctions monitoring; regulatory changes; export controls |

## Связь с другими модулями

- [[01-SCOR-Maturity|01 SCOR & Maturity]] — Enable-процесс SCOR включает risk
- [[02-Network-Design|02 Network Design]] — resilient network как часть стратегии
- [[05-Logistics-Transportation|05 Logistics & Transportation]] — operational risks логистики
- [[../05-Procurement/index|Модуль 05: Procurement]] — supplier risk management
- [[../06-Foreign-Trade/index|Модуль 06: Foreign Trade]] — sanctions, валютный контроль
- [[../21-Legal/index|Модуль 21: Legal & Compliance]] — regulatory risks
- [[../22-Risk-BC/index|Модуль 22: Risk Management]] — общая методология risk

## Источники

### Книги (приоритет чтения)

- Yossi Sheffi, **«The Resilient Enterprise»** (MIT Press, 2005) — каноничная книга, начало дисциплины
- Yossi Sheffi, **«The Power of Resilience»** (MIT Press, 2015) — продолжение, кейсы 2010-х
- Yossi Sheffi, **«The New (Ab)Normal»** (MIT Press, 2020) — COVID-19 reflections
- David Simchi-Levi, **«Operations Rules: Delivering Customer Value through Flexible Operations»** (MIT Press, 2010)
- Donna Marshall, **«Supply Chain Risk Management»** (Routledge, 2-е изд.)
- Andreas Wieland, Carl Marcus Wallenburg, **«Supply Chain Risk Management»** (Springer)
- ISO 22301:2019 — Business continuity management systems

### Статьи

- HBR, **«Resilience-Focused Risk Management»** (различные годы)
- HBR, **«From Just-in-Time to Just-in-Case Supply Chains»** (2021)
- McKinsey, **«How COVID-19 has changed supply chains»** (2020-2021)
- McKinsey, **«Risk and resilience in 2024»** (ежегодные отчёты)
- BCG, **«The Imperative for Supply Chain Resilience»**
- Deloitte, **«Future of Supply Chain Risk Management»**

### Онлайн-ресурсы

- MIT CTL Supply Chain Risk Center (ctl.mit.edu)
- Resilinc (resilinc.com) — supply chain risk platform с research
- Project44 — visibility platform with risk insights
- riskmethods — risk management tools
- DRJ (Disaster Recovery Journal) — отраслевые ресурсы по BCP
- DRI International (drii.org) — сертификации по Business Continuity

### Сертификации

- **CBCP** (Certified Business Continuity Professional, DRI International)
- **CBCI** (Certificate of the BCI, Business Continuity Institute)
- **ISO 22301 Lead Implementer / Auditor**

### Кейсы

- **Toyota** после 2011 Tohoku earthquake — каноничный кейс resilient supply chain
- **Apple** во время COVID — диверсификация sourcing из CN в VN, IN
- **P&G** во время COVID — успешная адаптация production / distribution
- **Cisco** — постоянная инвестиция в resilience с 2000-х (после dot-com crash)
- **Honda** vs **Toyota** после 2011 — Honda восстанавливалась дольше, отсутствовала тщательность Toyota в supplier mapping
- **Maersk и NotPetya** (2017) — кейс кибератаки и восстановления
- **Российские компании после 2022** — массовая адаптация sourcing strategy
- **Boeing 787** — комбинация рисков аутсорсинга
## Связанные документы

- [[index|Модуль 04: Supply Chain Management]]
- [[../index|Education Index]]
- [[01-SCOR-Maturity|01 SCOR & Maturity]]
- [[02-Network-Design|02 Network Design]]
- Методология Education
