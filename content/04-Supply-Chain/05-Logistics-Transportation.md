---
title: "05 — Logistics & Transportation"
aliases: ["Logistics", "Transportation", "3PL", "4PL", "WMS", "TMS", "Reverse Logistics", "Cold Chain"]
type: note
status: active
domain: education
module: 04-Supply-Chain
tags: [education, supply-chain, logistics, transportation, 3pl, 4pl, wms, tms, reverse, cold-chain]
created: 2026-05-18
updated: 2026-05-18
---

# 05 — Logistics & Transportation

> Логистика — это физическое движение товаров от точки производства до точки потребления. Стратегические решения здесь — выбор видов транспорта (modes: air / sea / rail / road — воздушный / морской / ж/д / автомобильный), модель работы с провайдерами (1PL → 5PL — First-Party to Fifth-Party Logistics), архитектура IT-систем (WMS — Warehouse Management System / TMS — Transportation Management System), обработка возвратов (reverse logistics — обратная логистика) и специальные потоки (Cold Chain — холодовая цепь).

## Карта раздела

![](attachments/diagrams/04-transportation-modes.svg)

## 1. Modes of Transportation

### 1.1 Контекст и легитимность

Транспортная логистика — древнейшая часть управления цепочками. Каноничный учебник — **Donald Bowersox, David Closs, M. Bixby Cooper, «Supply Chain Logistics Management»** (McGraw-Hill, 5-е изд.). Современная аналитика — в отчётах **CSCMP** (Council of Supply Chain Management Professionals) и **MIT CTL**.

### 1.2 Пять основных modes

![](attachments/diagrams/04-transportation-modes.svg)

#### 1.2.1 Air — авиатранспорт

**Использование:** срочные грузы, высокостоимостные (high-value — электроника, фармацевтика), скоропортящиеся (свежая еда, цветы), длинные межконтинентальные расстояния.

**Параметры:**
- Скорость: 1-3 дня от точки до точки
- Стоимость: 8-12 раз дороже морского за тонну
- Объём ограничен (грузовые отсеки самолётов)
- Высокие требования к упаковке и погодным условиям

**Когда выбирать:** высокое отношение стоимости к весу (value-to-weight ratio): электроника, fashion (модная одежда); временной фактор критичен (запуск продукта, праздничные продажи), скоропортящееся.

#### 1.2.2 Sea — морской транспорт

**Использование:** массовые грузы (контейнеры, наливные грузы, сыпучие), международная торговля, низкая стоимость на единицу веса / объёма.

**Параметры:**
- Скорость: 15-45 дней (зависит от маршрута)
- Стоимость: самый дешёвый mode за тонно-километр
- Подходит для контейнерных перевозок (FCL — Full Container Load / LCL — Less than Container Load)
- Зависимость от погодных условий и портовой инфраструктуры

**Когда выбирать:** международные потоки с длинными lead times (CN → RU, CN → EU), массовые товары, низкая стоимость единицы.

#### 1.2.3 Rail — железнодорожный транспорт

**Использование:** контейнерные перевозки внутри страны, наливные / сыпучие грузы на длинные расстояния (уголь, нефть, зерно), trans-Siberian / China-Europe маршруты.

**Параметры:**
- Скорость: 7-20 дней (зависит от расстояния)
- Стоимость: 2-3 раза дороже sea, но в 5-10 раз дешевле air
- Хорошо для среднего сегмента по value
- Требует развитой ж/д инфраструктуры

**Когда выбирать:** длинные внутренние маршруты, China-Europe потоки (как альтернатива sea, более быстро), массовые товары средней стоимости. После 2022 года rail из CN в RU стал основным маршрутом для импорта.

#### 1.2.4 Road — автомобильный транспорт

**Использование:** региональные перевозки, last-mile, гибкие маршруты, доставка из / на склады.

**Параметры:**
- Скорость: часы — несколько дней
- Стоимость: выше rail за тонну, но конкурентоспособен на коротких расстояниях
- Универсальный: подходит для всех типов грузов
- Зависимость от качества дорог, погоды, регулирования

**Когда выбирать:** региональные потоки, last-mile, любые грузы при отсутствии прямых ж/д / морских путей.

#### 1.2.5 Pipeline — трубопровод

**Использование:** жидкости и газы — нефть, газ, нефтепродукты, химические продукты.

**Параметры:**
- Скорость: непрерывный поток
- Стоимость: после инвестиций в инфраструктуру — самый дешёвый
- Огромные капитальные затраты на строительство
- Ограниченная гибкость (фиксированная точка → точка)

**Когда выбирать:** массовые потоки жидкости / газа между фиксированными точками; для большинства товарных компаний неприменимо.

### 1.3 Multimodal Transportation

**Multimodal** или **intermodal** транспорт — комбинация нескольких modes в одной отгрузке через стандартизированные контейнеры (ISO containers). Канонический пример — импорт из CN:

1. Road от завода в CN до порта Шанхай
2. Sea из Шанхая в Гамбург (~30 дней)
3. Rail из Гамбурга в Восточную Европу
4. Road от рельсового терминала до DC

Преимущества: оптимизация под cost / speed на каждом сегменте; контейнер не разгружается между modes; стандартизация документации.

**Ключевой вывод 1.** Выбор вида транспорта — это компромисс между стоимостью и скоростью, плюс ограничения по типу груза. Для большинства международных потоков ответ — мультимодальный (multimodal). Для российских компаний в 2024-2025 годах rail из КНР стал главной альтернативой sea.

## 2. Контейнерная логистика — FCL и LCL

### 2.1 FCL — Full Container Load

**FCL** (Full Container Load — полная контейнерная партия) — отгрузка, занимающая целый контейнер (20-футовый = 33 м³ или 40-футовый = 67 м³).

Плюсы:

- Дешевле в пересчёте на единицу
- Контейнер не открывается до точки назначения (меньше повреждений и краж)
- Быстрее обработки в портах
- Простая документация

Минусы:

- Требует достаточно большого заказа
- Капитал замораживается в большем количестве товара

### 2.2 LCL — Less than Container Load

**LCL** (Less than Container Load — частичная контейнерная партия) — отгрузка, занимающая часть контейнера, делящегося с грузами других отправителей.

Плюсы:

- Подходит для небольших заказов
- Не требует наполнить целый контейнер

Минусы:

- Дороже за единицу веса / объёма
- Дольше — нужно ждать наполнения контейнера
- Больше риск повреждений (множественная разгрузка / погрузка)
- Сложная документация (consolidation)

### 2.3 Когда что выбирать

Эмпирическое правило: если заказ занимает более 15 м³ — выгоднее FCL. Меньше — LCL.

В практике этот выбор делается на уровне S&OP: «забирать больше за раз и держать запасы» vs «забирать чаще малыми партиями и иметь меньше запасов». Это часть Network Design и Inventory Management решений.

**Ключевой вывод 2.** FCL vs LCL — это микро-решение в большой картине, но оно влияет на стоимость закупки на 20-40%. Зрелые компании оптимизируют заказы под FCL, объединяя несколько SKU от одного поставщика в один контейнер.

## 3. Логистические провайдеры — 1PL → 5PL

### 3.1 Эволюция модели

Логистические провайдеры классифицируются по тому, сколько функций цепочки они принимают на себя.

![](attachments/diagrams/04-3pl-4pl-5pl-hierarchy.svg)

| Уровень | Описание | Примеры |
|---------|----------|---------|
| **1PL** | First-Party — компания везёт сама собственным транспортом | Внутренняя логистика производителя |
| **2PL** | Transporter — перевозчик, владеющий transportation assets | Железная дорога, контейнерная линия (Maersk, MSC) |
| **3PL** | Комплексный провайдер: склад + транспорт + IT | DHL, Kuehne+Nagel, СДЭК, DPD, Boxberry |
| **4PL / LLP** | Lead Logistics Provider — оркестратор, управляющий сетью 3PL | Maersk Logistics, DHL Supply Chain (в режиме 4PL) |
| **5PL** | Комплексный провайдер цепочки + аналитика + AI оптимизация | Развивающаяся концепция |

### 3.2 1PL — Self-managed

**Когда:** малая компания с локальным бизнесом; критичная функция, требующая контроля; нет квалифицированного (qualified) 3PL в регионе.

**Плюсы:** полный контроль, защита IP (Intellectual Property — интеллектуальной собственности), ноу-хау внутри.

**Минусы:** не использует экономию масштаба специализированных провайдеров; ресурсы отвлекаются от ключевого (core) бизнеса.

### 3.3 3PL — самый распространённый уровень

**Когда:** компания хочет освободить ресурсы для ключевого бизнеса; нужны масштаб и экспертиза, которые трудно построить собственными силами (in-house).

**Что включает 3PL:**

- Склад: приёмка, размещение, хранение, комплектация, упаковка, отгрузка
- Транспорт: своя сеть или интеграция с перевозчиками
- IT: WMS, TMS, портал для клиента
- Доп. услуги: возвраты, кросс-докинг, ко-пакинг, кастомизация

**Контрактные модели:**

- Open book (открытая книга) — клиент видит реальные затраты провайдера + согласованную маржу
- Closed book (закрытая книга) — фиксированные тарифы за услугу

**Ключевые KPI и SLA:**

- OTIF (On-Time In-Full — поставка вовремя и в полном объёме), точность (accuracy), доля повреждений (damage rate)
- Точность учёта запасов (inventory accuracy)
- Стоимость за единицу / за паллету / за заказ

### 3.4 4PL — оркестратор

**Когда:** глобальная компания с многими 3PL-партнёрами; нужна единая точка управления.

**Что делает 4PL:**

- Управляет несколькими 3PL от имени клиента
- Оптимизирует сеть в целом
- Внедряет IT-платформу для единого view
- Управляет supplier relationships

Пример: производитель электроники с production в CN, складами в RU и регионалкой через 3PL партнёров может нанять 4PL Maersk Logistics или DHL Supply Chain для оркестрации всей цепочки.

### 3.5 5PL — концепция будущего

**5PL** — пока концепция, без чёткого стандарта. Идея: 5PL это AI-driven supply chain orchestrator, который не только управляет цепочкой, но и оптимизирует её в реальном времени через ML, прогнозирует disruption, автоматизирует решения.

Признаки 5PL появляются в практиках Top 25 (Apple, Amazon), но как самостоятельная коммерческая категория провайдеров — пока редкость.

**Ключевой вывод 3.** Выбор уровня логистического партнёра — стратегическое решение. Для большинства средних компаний 3PL — оптимальный выбор; для крупных мультинациональных групп — переход к 4PL даёт значительные эффекты. 5PL — это будущее, и тренд движется туда.

## 4. WMS и TMS — IT-инфраструктура

### 4.1 WMS — Warehouse Management System

**WMS** (Warehouse Management System — система управления складом) — программный продукт, управляющий всеми операциями склада.

**Функции:**

- Приёмка: receiving, putaway directing
- Хранение: bin / location management, ABC zoning
- Комплектация: pick lists, pick paths, wave picking
- Упаковка: pack station automation, shipping label
- Отгрузка: load planning, carrier integration
- Инвентаризация: cycle counting, reconciliation

**Топ-вендоры:**

- Manhattan Associates (лидер enterprise)
- Blue Yonder (бывший JDA)
- SAP EWM (Extended Warehouse Management)
- Oracle WMS
- HighJump (для SMB)
- Российские: 1C Логистика, FirstBIT, Логос

### 4.2 TMS — Transportation Management System

**TMS** (Transportation Management System — система управления транспортом) — программный продукт, управляющий планированием и исполнением транспортировки.

**Функции:**

- Планирование маршрутов (route optimization)
- Выбор перевозчика (rate management, carrier selection)
- Отслеживание (tracking, ETA prediction)
- Документооборот (waybill, manifesto)
- Audit & payment (freight bill audit)

**Топ-вендоры:**

- Oracle TMS
- SAP TM
- Blue Yonder
- Manhattan Active TM
- Project44 (visibility)
- Российские: 1C TMS, Гарант-TMS, AntorLogistics

### 4.3 Интеграция WMS / TMS / ERP

Зрелая компания имеет интегрированный стек:

- **ERP** (SAP, Oracle, 1C) — финансы, BOM, master data, order management
- **WMS** — операции склада
- **TMS** — операции транспорта
- **OMS** (Order Management System) — управление заказами
- **CRM** — клиентский опыт

Интеграция обеспечивает end-to-end visibility и сквозные процессы. Без интеграции возникают разрывы данных, ручная работа, ошибки.

**Ключевой вывод 4.** WMS и TMS — фундамент операционной excellence. Внедрение полноценных систем — это многомиллионный проект на 12-24 месяцев, но без них масштабирование операций невозможно. Для маркетплейсов и крупного e-commerce WMS / TMS — must-have.

## 5. Reverse Logistics — обработка возвратов

### 5.1 Зачем reverse logistics

**Reverse Logistics** — это управление обратным потоком: возвраты от клиентов, возвраты поставщикам, утилизация / переработка. В современной цепочке reverse logistics может составлять 5-30% от объёма forward flow — особенно в e-commerce (категории fashion 30-40% return rate).

Reverse logistics — самый дорогой и сложный сегмент цепочки:

- Стоимость обработки возврата в 2-3 раза выше стоимости отгрузки
- Качество возвращённого товара неопределённое
- Часть товара не подлежит возврату в продажу
- Сложности с документооборотом и compliance

### 5.2 Типы возвратов

1. **Customer returns** — возвраты от клиентов (отказ от заказа, defective, не подошло)
2. **Supplier returns** — возвраты поставщикам (defective, excess, end-of-life)
3. **Distribution returns** — возвраты между уровнями сети (между DC, между магазинами)
4. **Reverse from retail** — возвраты из магазинов на DC

### 5.3 Процесс обработки возврата

1. **Authorization** — клиент уведомляет о возврате (RMA — Return Merchandise Authorization)
2. **Pickup** — забор товара (курьер, ПВЗ, самовывоз клиентом)
3. **Receipt** — приёмка обратно на склад
4. **Inspection** — проверка состояния и комплектности
5. **Disposition** — решение: возврат в продажу, уценка, возврат поставщику, утилизация
6. **Reconciliation** — возврат денег клиенту, обновление учёта

### 5.4 Disposition decisions

- **Restock as new** — товар в идеальном состоянии, возврат в продажу по обычной цене
- **Restock with discount** — небольшие дефекты, продажа со скидкой
- **Refurbishment** — восстановление и продажа как refurbished (обычно skincare, electronics)
- **Liquidation** — продажа через специализированный канал (outlet, B2B liquidators)
- **Donation** — благотворительность с налоговым вычетом
- **Recycling / Disposal** — утилизация, переработка

### 5.5 Circular Economy и Sustainability

Современные тенденции — встраивание reverse logistics в core-стратегию через **Circular Economy**:

- Take-back программы (производитель забирает старый продукт обратно для переработки)
- Refurbishment как самостоятельный бизнес (Apple Certified Refurbished)
- Material recovery (extraction ценных материалов из утилизируемого товара)
- Product-as-a-Service (аренда вместо продажи, владение остаётся у производителя)

**Ключевой вывод 5.** Reverse logistics — самый сложный и часто недооценённый сегмент цепочки. Для e-commerce с 30-40% return rate он определяет половину операционной экономики. Зрелые компании инвестируют в reverse logistics так же серьёзно, как в forward.

## 6. Cold Chain — холодовая цепь

### 6.1 Что это и зачем

**Cold Chain** (холодовая цепь) — это специальный режим логистики с контролем температуры на всём пути от производителя до потребителя. Применяется для:

- Замороженные продукты (-18°C и ниже)
- Охлаждённые продукты (+2 до +8°C)
- Фармацевтика, вакцины (специальные диапазоны)
- Цветы, биологические образцы

### 6.2 Сложности cold chain

- **Специальная инфраструктура:** рефрижераторные склады, refrigerated trucks, температурные мониторы
- **Высокие операционные затраты:** энергия, обслуживание оборудования
- **Compliance:** регуляторные требования (GDP — Good Distribution Practice для pharma)
- **Риски:** даже короткий выход за температурный диапазон может испортить весь груз
- **Last-mile сложности:** доставка в режиме холодовой цепи дороже и медленнее

### 6.3 Технологии cold chain

- IoT-датчики температуры с реал-тайм мониторингом
- Blockchain для иммутабельной записи температурной истории
- Specialty packaging (gel packs, dry ice, vacuum-insulated panels)
- Predictive analytics для prevention disruptions

### 6.4 Российская специфика

В РФ cold chain критична для:

- Северного завоза в Арктику
- Доставки в truднодоступные регионы Сибири / ДВ
- Pharma logistics (COVID vaccines)
- E-grocery (Самокат, Лавка, Magnit Online, СберМаркет)

**Ключевой вывод 6.** Cold chain — специализированный сегмент логистики с высокими операционными требованиями и compliance. Для продуктовых, фармацевтических и biotech-компаний — обязательный элемент стратегии. Для остальных — узкая ниша.

## Сводный практический протокол

Постановка зрелой логистики в компании среднего размера:

| Шаг | Действие | Артефакт |
|-----|----------|----------|
| 1 | Аудит текущего стека (WMS / TMS / Carrier mix) | Baseline assessment |
| 2 | Анализ modes transportation по категориям | Mode allocation strategy |
| 3 | Решение о 3PL vs 1PL для разных категорий | Outsourcing decision matrix |
| 4 | Выбор 3PL-партнёров (RFP, evaluation, contracts) | Carrier list with SLAs |
| 5 | Внедрение WMS / TMS | Working integrated stack |
| 6 | Постановка reverse logistics процесса | RMA process |
| 7 | Постоянный мониторинг KPI (OTIF, fill rate, damage) | Logistics dashboard |

## Применение для руководителя

| Целевая роль | Что взять из заметки |
|--------------|---------------------|
| **COO** | Стратегические решения по modes и 3PL/4PL; ROI от WMS / TMS; reverse logistics как стратегический сегмент |
| **Директор логистики** | Глубокое погружение в WMS / TMS внедрение; контрактные модели 3PL; route optimization |
| **Директор закупок** | Inbound logistics стратегия (FCL vs LCL, modes choice); negotiations с перевозчиками |
| **Финансовый директор** | Capex / Opex логистики; ROI digital investments; экономия от 3PL vs internal |
| **Категорийный менеджер** | Logistics cost как часть Cost-to-Serve по SKU; reverse logistics для категорий с высоким return rate |

## Связь с другими модулями

- [[01-SCOR-Maturity|01 SCOR & Maturity]] — Source / Deliver / Return процессы
- [[02-Network-Design|02 Network Design]] — определяет архитектуру логистики
- [[03-Demand-Planning-SOP|03 S&OP & Demand Planning]] — драйверы для transportation planning
- [[04-Inventory-Management|04 Inventory Management]] — связь с FCL / LCL и lead times
- [[07-Last-Mile-Delivery|07 Last-Mile Delivery]] — фокусированно на финальном сегменте
- [[../03-Management-Accounting/02-Cost-to-Serve|03-Management-Accounting: Cost-to-Serve]] — логистика как ключевые buckets CTS
- [[../06-Foreign-Trade/index|Модуль 06: Foreign Trade]] — международная логистика
- [[../12-ERP-Digitalization/index|Модуль 12: ERP & Digitalization]] — IT-стек WMS / TMS / OMS

## Источники

### Книги (приоритет чтения)

- Donald Bowersox, David Closs, M. Bixby Cooper, **«Supply Chain Logistics Management»** (McGraw-Hill, 5-е изд.) — основной учебник по логистике
- Edward Frazelle, **«World-Class Warehousing and Material Handling»** (McGraw-Hill, 2-е изд., 2016) — фокусированно на warehouse operations
- John Manners-Bell, **«Introduction to Global Logistics»** (Kogan Page, 3-е изд.) — стратегический уровень
- Vinod Singhal, Kevin Hendricks, **«Supply Chain Disruptions and Performance»** — академический анализ
- Yossi Sheffi, **«Logistics Clusters»** (MIT Press, 2012)
- Reverse Logistics Executive Council, **«Reverse Logistics Trends and Practices»** — отраслевой обзор
- Lalwani, Mangan, **«Global Logistics and Supply Chain Management»** (Wiley, 4-е изд.)

### Статьи

- HBR, **«Building a More Intelligent Supply Chain»** — серия
- McKinsey, **«The Future of Logistics: 2030 vision»**
- Gartner, **«Magic Quadrant for Transportation Management Systems»** — ежегодно
- Gartner, **«Magic Quadrant for Warehouse Management Systems»** — ежегодно
- DHL Trend Research, **«Logistics Trend Radar»** — обновляется ежегодно

### Онлайн-ресурсы

- CSCMP (cscmp.org) — отраслевые исследования, метрики, мероприятия
- ASCM (ascm.org) — CLTD certification, материалы
- DHL Resilience360 — visibility platform, blog
- Project44 — visibility insights
- FreightWaves (freightwaves.com) — индустриальные новости
- Российская логистическая ассоциация
- ИНКОТЕРМС 2020 (ICC) — официальные правила
- LogisticsViewpoints (logisticsviewpoints.com) — отраслевая аналитика

### Сертификации

- **CLTD** (Certified in Logistics, Transportation and Distribution, ASCM) — основная логистическая сертификация
- **CSCP** (ASCM) — широкая
- **CILT** (Chartered Institute of Logistics and Transport, UK) — британская / международная
- **APICS / ASCM Warehouse Specialist**

### Кейсы

- **Maersk** — крупнейший контейнерный перевозчик, переход в 4PL Maersk Logistics
- **DHL Supply Chain** — крупнейший 3PL/4PL провайдер мира
- **FedEx / UPS** — интегрированные логистические сети
- **Amazon Logistics** — стремительный рост own fleet, конкурент UPS/FedEx
- **Wildberries / Ozon** — fulfillment networks в РФ
- **СДЭК / Boxberry / Почта России** — российские курьерские службы
- **Foxconn** — реверс-логистика комплектующих Apple
- **Patagonia** — каноничный пример reverse logistics для sustainability (Worn Wear program)
## Связанные документы

- [[index|Модуль 04: Supply Chain Management]]
- [[../index|Education Index]]
- [[01-SCOR-Maturity|01 SCOR & Maturity]]
- [[02-Network-Design|02 Network Design]]
- [[07-Last-Mile-Delivery|07 Last-Mile Delivery]]
- Методология Education
