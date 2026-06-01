---
title: "07 — Last-Mile Delivery"
aliases: ["Last Mile", "Доставка последней мили", "VRP", "Dark Store", "Click and Collect"]
type: note
status: active
domain: education
module: 04-Supply-Chain
tags: [education, supply-chain, last-mile, delivery, vrp, dark-store, fulfillment, ecommerce]
created: 2026-05-18
updated: 2026-05-18
---

# 07 — Last-Mile Delivery

> Последняя миля — самый дорогой сегмент цепочки поставок, на который приходится 30-50% общей стоимости доставки. От её организации зависит юнит-экономика всего e-commerce, удовлетворённость клиентов и конкурентоспособность. В 2020-х last-mile превратилась в стратегическое поле боя — gig-модели (модели с самозанятыми курьерами), «тёмные» микросклады (dark stores), доставка дронами (drone delivery), автономные транспортные средства (autonomous vehicles) меняют картину каждые несколько лет.

## Карта раздела

![](attachments/diagrams/04-last-mile-options.svg)

## 1. Зачем last-mile отдельная дисциплина

### 1.1 Контекст и легитимность

Last-mile delivery как самостоятельный фокус оформился с ростом e-commerce в 2010-х. Каноничный обзор — **Lyle Ginsburg, «Last Mile Logistics: A New Era of Distribution»** (2021). Современная аналитика — в ежегодных отчётах McKinsey **«The future of last-mile delivery»** (2021-2025).

### 1.2 Экономика последней мили

Стоимость последней мили составляет 30-50% от полной стоимости транспорта. Причины:

- **Низкая плотность доставки:** курьер делает 15-25 остановок в день, а в магистральной перевозке (long-haul truck) — 1 остановка на тысячи единиц груза
- **Маленькие партии:** одна или несколько единиц на остановку
- **Сложная навигация:** городские заторы, ограничения движения, парковка
- **Высокая стоимость рабочей силы:** курьер на остановку = 5-10 минут реального времени
- **Неудачные доставки (failed deliveries):** клиента нет дома, требуется повторная попытка

Эта структура затрат принципиально отличает last-mile от других сегментов цепочки и делает её главным объектом оптимизации в e-commerce.

### 1.3 Стратегическая значимость

Помимо стоимости, last-mile определяет:

- **Customer experience** — финальный touchpoint, где клиент видит сервис воочию
- **Сроки доставки** — главный конкурентный фактор для e-commerce
- **Возвраты** — last-mile часто содержит reverse logistics (если клиент отказывается)
- **Brand perception** — курьер часто единственный «живой человек» от бренда

**Ключевой вывод 1.** Last-mile — это не операционный задний план, а стратегическое поле боя. Компании, выигравшие на последней миле (Amazon, Wildberries, Самокат), получают долгосрочное конкурентное преимущество. Компании, упустившие её, теряют клиентов в пользу более быстрых.

## 2. Модели доставки

### 2.1 Спектр решений

![](attachments/diagrams/04-last-mile-options.svg)

Существует семь основных моделей:

| Модель | Описание | Лучше всего для |
|--------|----------|------------------|
| **Own Fleet** (собственный парк) | Собственный курьерский штат и парк | Высокая плотность, премиум-опыт |
| **3PL / Courier** (3PL / курьерская служба) | Внешние курьерские службы | Стартап, средние объёмы, гибкость |
| **ПВЗ / Locker** (пункт выдачи / почтомат) | Пункты выдачи и почтоматы | Удобство клиента, низкая стоимость |
| **Marketplace FBO** | Маркетплейс делает всё | Маркетплейс — основной канал продаж |
| **Gig-модель** | Самозанятые (self-employed) курьеры | Экономика по запросу (on-demand) |
| **Dark Store** («тёмный» микросклад) | Микросклад в городе | 15-30 мин доставка |
| **Click-and-Collect** (заказ онлайн — самовывоз офлайн) | Самовывоз из магазина | Омниканальная розница |

### 2.2 Own Fleet — собственный курьерский штат

**Когда:** высокая density доставок (concentrated area), премиум-бренд требует контроля experience, объёмы оправдывают capital investment.

**Структура:**

- Курьеры в штате или работающие через ИП
- Собственный автопарк (или арендованный с долгосрочными контрактами)
- Routing software (TMS, route optimization)
- Униформа, training, customer service

**Плюсы:** контроль качества, brand experience, IP в процессах.

**Минусы:** высокий fixed cost, риск underutilization вне peak season, сложный HR.

**Примеры:** Amazon Logistics (часть последней мили), Wildberries (часть собственной сети), Ozon Express в плотных городах.

### 2.3 3PL / Courier — внешние курьерские службы

**Когда:** объёмы недостаточны для own fleet, потребности in flexibility, географические зоны вне own coverage.

**Структура:**

- Контракт с одним или несколькими курьерскими провайдерами
- API-интеграция для passing заказов
- SLA: time of delivery, success rate, damage rate
- Pricing — per shipment или volume-based

**Российские провайдеры:** СДЭК, Boxberry, DPD Россия, Почта России, Pony Express, Деловые Линии (для крупногабаритного).

**Плюсы:** низкий entry barrier, гибкость, экспертиза провайдера.

**Минусы:** меньше контроля над experience, маржа провайдера, риск capacity constraints в peak.

### 2.4 ПВЗ и Locker — самовывоз

**ПВЗ** (Пункт Выдачи Заказов) — физическая точка с consultant, где клиент забирает заказ. **Locker** (почтомат) — автоматизированный шкаф для self-pickup.

**Когда:** клиент готов к самовывозу за скидку или удобство, density клиентской базы вокруг точек.

**Российские провайдеры:** Ozon ПВЗ, Wildberries ПВЗ, PickPoint (lockers), 5Post, СДЭК ПВЗ.

**Плюсы:** значительно дешевле дoor-to-door доставки (в 2-3 раза), отсутствие failed deliveries, удобство клиента.

**Минусы:** клиент должен сам добраться, ограничение по габаритам, для крупного — невозможно.

В РФ ПВЗ — это revolution: к 2024 году более 50% заказов на Ozon / Wildberries выдаётся через ПВЗ, что радикально снижает стоимость доставки.

### 2.5 Marketplace FBO (Fulfillment by Operator)

**FBO** — модель, при которой маркетплейс полностью отвечает за fulfillment: хранение, комплектацию, отгрузку, доставку. Селлер только присылает товар на склад маркетплейса.

**Когда:** маркетплейс — основной (или единственный) канал продаж, нет собственной fulfillment-инфраструктуры.

**Примеры:** Wildberries FBO, Ozon FBO, Amazon FBA, AliExpress 4PX.

**Плюсы:** zero infrastructure investment, скорость доставки оператора, integrated experience.

**Минусы:** комиссия маркетплейса (5-25%), стоимость хранения (растёт с возрастом запасов), зависимость от платформы.

### 2.6 Gig-модель — self-employed курьеры

**Gig-модель** — курьеры работают как self-employed, получают заказы через app, оплачиваются per task.

**Когда:** ультра-короткая доставка (15-60 мин), peak demand с резкими колебаниями, не критично формальное HR-управление.

**Примеры:** Яндекс.Доставка, Самокат-курьеры, Delivery Club (ныне СберМаркет), Uber Eats, Gett Delivery.

**Плюсы:** scalability, низкая стоимость, не fixed costs.

**Минусы:** контроль качества, regulatory вопросы (классификация work), отсутствие brand uniformity.

### 2.7 Dark Store — городской микрохаб

**Dark Store** — это retail store, не работающий с покупателями, а служащий микро-fulfillment-центром для ультра-быстрой доставки. Товар хранится в формате, оптимизированном для pick & pack курьером.

**Когда:** ультра-быстрая доставка (15-30 минут) — продукты, готовая еда, FMCG, экспресс-доставка.

**Примеры:** Самокат, Яндекс.Лавка, СберМаркет (для некоторых категорий), Magnit Online.

**Плюсы:** скорость недостижимая для централизованных DC, fresh inventory для food, локальный опыт.

**Минусы:** capital intensive (нужно много dark stores в каждом городе), высокая стоимость площадей в центрах, сложности с ассортиментом (нельзя держать full SKU range).

### 2.8 Click-and-Collect

**Click-and-Collect** — клиент заказывает онлайн, забирает в физическом магазине retailer. Гибрид e-commerce и offline retail.

**Когда:** компания имеет физическую retail сеть, хочет омни-канальный опыт.

**Примеры:** Лента / Ашан (для FMCG), большинство fashion retailers (Uniqlo, Zara), DIY (Леруа Мерлен).

**Плюсы:** дешевле home delivery, opportunity для upsell в магазине, использует existing infrastructure.

**Минусы:** клиент должен прийти в магазин, нужна синхронизация online и offline inventory.

**Ключевой вывод 2.** Семь моделей последней мили — это не «либо одно, либо другое». Зрелые компании комбинируют их: own fleet для VIP-клиентов в Москве / СПб, 3PL для регионов, ПВЗ для cost-conscious клиентов, dark stores для grocery, click-and-collect для омни-канала. Hybrid-подход — норма для крупного e-commerce.

## 3. Drop Density — главная экономическая переменная

### 3.1 Что такое drop density

**Drop Density** (плотность доставок) — количество доставок на квадратный километр в день. Это главная переменная экономики last-mile.

Чем выше density:

- Меньше километров между остановками
- Меньше времени на навигацию
- Больше доставок на курьера в день
- Ниже стоимость на доставку

Чем ниже density:

- Курьер тратит больше времени на дорогу между остановками
- Меньше эффективность
- Выше стоимость на доставку

### 3.2 Зависимость стоимости от density

Эмпирическое правило: при удвоении density стоимость на доставку снижается на 25-40%. И наоборот — снижение density вдвое почти удваивает стоимость.

Это объясняет, почему e-commerce развивается **сначала в столицах** (Москва, СПб), потом расширяется в города-миллионники, затем — в регионы. Density определяет, где экономически возможна определённая модель доставки.

### 3.3 Стратегии увеличения density

- **Geographic concentration** — фокус на ограниченной зоне до достижения определённой density
- **Time windows** — отказ от ультра-узких окон (15-минутный slot) в пользу 1-2 часовых, что позволяет combining маршруты
- **Group buying / planning** — стимулировать совместные покупки в одной зоне
- **Partnership** — multiple e-commerce платформ используют общую last-mile сеть
- **Click-and-Collect** — концентрация клиентов в фиксированных точках

### 3.4 Влияние на стратегию

Решения по последней миле в малой стране vs большой стране радикально различаются. Для России (огромная территория, низкая средняя density) типична hybrid-стратегия:

- Москва / СПб: own fleet + 3PL для VIP, dark stores для grocery
- Города-миллионники: 3PL для основной массы заказов
- Малые города: ПВЗ как доминирующая модель
- Удалённые регионы: Почта России

**Ключевой вывод 3.** Drop density — фундаментальная переменная экономики last-mile. Все стратегические решения должны учитывать density целевого региона. Игнорирование density — главная причина провалов экспансии e-commerce в новые регионы.

## 4. VRP — Vehicle Routing Problem

### 4.1 Контекст и легитимность

**VRP** (Vehicle Routing Problem — задача маршрутизации транспорта) — фундаментальная оптимизационная задача в логистике. Сформулирована **George Dantzig и John Ramser** в 1959 году. Каноничная книга — **Paolo Toth, Daniele Vigo, «Vehicle Routing: Problems, Methods, and Applications»** (SIAM, 2014).

VRP — NP-hard задача, точное решение для больших instances невозможно. На практике применяются heuristics и metaheuristics — clarke-Wright savings, tabu search, genetic algorithms, simulated annealing.

### 4.2 Постановка задачи

Базовая VRP:

- Есть DC (depot) с грузами
- Есть N клиентов с известными адресами и заказами
- Есть K курьеров / транспортных средств с известной capacity
- Найти маршруты для всех курьеров, минимизирующие общую стоимость (расстояние, время) при условии:
  - Каждый клиент посещён ровно один раз
  - Каждый маршрут начинается и заканчивается в depot
  - Capacity constraints соблюдены

### 4.3 Варианты VRP

В реальности применяются модификации:

- **CVRP** (Capacitated VRP) — с ограничением по capacity
- **VRPTW** (VRP with Time Windows) — клиенты имеют time slots
- **MDVRP** (Multi-Depot VRP) — несколько depot
- **PDPTW** (Pickup and Delivery Problem with Time Windows) — pickup + delivery
- **VRPSPD** — VRP with Simultaneous Pickup and Delivery — для reverse logistics
- **Dynamic VRP** — заказы поступают в течение дня (real-time routing)

### 4.4 Tools для VRP

В практике VRP решают через:

- Commercial software: Routyn, OptimoRoute, Routific, Locus, AntorLogistics (в РФ)
- Open-source: VROOM, OR-Tools (Google)
- Cloud services: Mapbox Optimization, HERE Routing, Yandex Routing
- Custom ML-driven solutions (особенно для dynamic VRP)

Современные подходы используют ML для прогнозирования traffic patterns и улучшения routing решений в реальном времени.

### 4.5 Влияние на экономику

Качественный VRP-solver даёт улучшение 10-25% по сравнению с manual routing. Для крупного e-commerce с тысячами доставок в день это миллионы рублей экономии месячно.

**Ключевой вывод 4.** VRP — это академическая задача с большим практическим эффектом. Любой серьёзный e-commerce должен использовать VRP-solver, не manual routing. Современные tools доступны и в РФ, причём встроены в большинство TMS.

## 5. Возвраты на последней миле

### 5.1 Значимость возвратов

Возвраты в e-commerce — массовое явление:

- **Fashion / одежда:** 30-40% return rate
- **Электроника:** 5-15%
- **Косметика:** 5-10%
- **Книги:** 5-8%
- **Грocery:** менее 5%

Каждый возврат стоит компании 1.5-2x стоимости первоначальной доставки (потому что requires курьер обратно + приёмка + reprocessing).

### 5.2 Стратегии управления возвратами

- **Easy returns** для повышения CSAT (как Zappos, Amazon) — клиент возвращает бесплатно. Стоит дорого, но drive больший loyalty
- **Paid returns** — клиент платит за возврат. Снижает return rate, но рискует unhappy customers
- **Restocking fees** — за возврат удерживается часть стоимости. Промежуточный вариант
- **Return through ПВЗ / Locker** — клиент сам приносит возврат, экономия на курьере
- **Try-before-buy** — try в магазине / dark store, чтобы избежать заказа неподходящего

### 5.3 Reverse last-mile

Когда возврат идёт через курьера, это **reverse last-mile** — сложный обратный процесс:

1. Клиент уведомляет о возврате
2. Назначается курьер для pickup
3. Курьер забирает, проверяет на месте основные дефекты
4. Доставка на склад
5. Reception, более глубокая inspection
6. Disposition (см. модуль 05)

Стоимость reverse last-mile в 1.5-2x выше forward, потому что:

- Невозможно объединить с forward маршрутами (другая логика)
- Меньшая density (возвраты разбросаны)
- Дополнительная работа на месте у курьера

**Ключевой вывод 5.** Возвраты — критический компонент last-mile экономики, особенно для fashion и electronics. Зрелое управление возвратами — это баланс easy returns (для CSAT) и friction (для управления costs). Игнорирование возвратов недопустимо для серьёзного e-commerce.

## 6. B2B vs B2C — разные логики

### 6.1 Различия в требованиях

| Параметр | B2C | B2B |
|----------|-----|-----|
| **Размер партии** | 1 единица | Десятки — тысячи единиц |
| **Время доставки** | Same-day / next-day | Часто 2-5 дней OK |
| **Время window** | Узкое (часовой слот) | Широкое (рабочий день) |
| **Получатель** | Частное лицо | Сотрудник на receiving dock |
| **Документооборот** | Минимальный (электронный чек) | Серьёзный (накладная, акт, счёт) |
| **Стоимость на доставку** | Высокая (low density per stop) | Низкая (large drop) |
| **Возвраты** | Часто | Редко, но крупные |

### 6.2 B2B специфика

B2B last-mile имеет свои особенности:

- **Loading dock requirements** — у клиента должна быть рампа / погрузчик
- **Appointment scheduling** — поставка по предварительной записи
- **Driver Assist** — driver часто помогает разгружать
- **Returnable packaging** — паллеты, контейнеры, которые нужно вернуть поставщику
- **Quality checks at receipt** — клиент проверяет качество при приёмке

### 6.3 B2C специфика

B2C last-mile имеет другие сложности:

- **Failed deliveries** — клиента нет дома, частая проблема
- **Address accuracy** — клиент часто даёт неточный адрес
- **Door-to-door access** — лифт, домофон, дверь
- **Verification** — иногда нужна подпись / документ при доставке dorogix items
- **Customer experience** — поведение курьера влияет на бренд

### 6.4 Hybrid (B2B2C)

Многие маркетплейсы работают в формате **B2B2C** — селлеры продают через платформу конечным клиентам, при этом платформа управляет последней милей. Это требует hybrid-подхода к процессам.

**Ключевой вывод 6.** B2C и B2B last-mile — это две разные дисциплины с разными процессами, метриками и техническими требованиями. Компании, работающие в обоих сегментах (как маркетплейсы), должны держать параллельные процессы или строить чёткие маршруты переключения.

## 7. Тренды и будущее

### 7.1 Drone delivery

Беспилотная доставка дронами — perspective, но пока узкая ниша. Применяется в:

- Удалённые / сложно-доступные регионы (Сибирь, Аляска)
- Медицинская доставка (Zipline в Африке, Matternet)
- Эксперименты Amazon Prime Air, Wing (Alphabet)

Ограничения: regulatory restrictions, ограничения по weight, weather sensitivity, мощность инфраструктуры (battery), регуляторика air space.

### 7.2 Autonomous vehicles

Автономные машины для доставки — активно тестируются:

- **Sidewalk robots** — Starship, Nuro, Yandex Rover в РФ
- **Autonomous delivery vans** — больше R&D, чем коммерчески
- **Autonomous trucks** — для линейной transportation, не last-mile

Драйверы: рост стоимости labor, нехватка курьеров, sustainability.

### 7.3 Electric vehicles

Electric vans, scooters, bicycles для last-mile — массовый тренд. Драйверы:

- Снижение operating cost
- Sustainability commitment
- City restrictions on combustion vehicles (LEZ — Low Emission Zones)
- Заметность бренда (брендированные EVs)

### 7.4 Hyperlocal fulfillment

Тренд на ультра-локализованную fulfillment-инфраструктуру:

- Dark stores в каждом районе крупного города
- Micro-fulfillment centers (MFCs) с автоматизированными системами
- Pop-up хабы для seasonal peaks
- Pickup points / автоматы во дворах

### 7.5 ML и AI

Современные AI решения в last-mile:

- **Demand prediction** для dynamic staffing
- **Real-time routing** с учётом traffic
- **Predictive failed delivery** — заранее предупредить риск provala
- **Personalized delivery time** — оптимальное окно под привычки клиента
- **Customer service automation** — chatbots для tracking, change of address

**Ключевой вывод 7.** Last-mile активно трансформируется через автоматизацию, electrification, hyperlocal infrastructure и AI. Компании, инвестирующие в эти тренды сейчас, получат конкурентное преимущество в 2026-2030. Те, кто остаётся в традиционной модели, рискуют отстать.

## Сводный практический протокол

Запуск зрелой last-mile операции в e-commerce:

| Шаг | Действие | Артефакт |
|-----|----------|----------|
| 1 | Анализ географии клиентской базы, расчёт density по зонам | Map of density |
| 2 | Выбор моделей доставки по зонам (own / 3PL / ПВЗ / FBO) | Delivery model matrix |
| 3 | Подбор и контракты с 3PL партнёрами (RFP, evaluation) | Carrier list with SLA |
| 4 | Внедрение VRP-solver для routing | Working routing system |
| 5 | Постановка возвратов: процесс, SLA, инструменты | RMA process |
| 6 | Метрики: OTIF, on-time delivery rate, cost per drop, NPS | Last-mile dashboard |
| 7 | Постоянное улучшение: A/B-тесты, новые модели, оптимизация | Continuous improvement |

## Применение для руководителя

| Целевая роль | Что взять из заметки |
|--------------|---------------------|
| **CEO / Board** | Last-mile как стратегическое поле боя в e-commerce; ROI от инвестиций в delivery network |
| **COO** | Архитектура last-mile операций; balance цены и сервиса; resilience к peak season |
| **Директор логистики** | Глубокое погружение во все 7 моделей; VRP внедрение; reverse last-mile |
| **Директор клиентского опыта** | Связь delivery experience с NPS и LTV; ratings курьеров; feedback loops |
| **Финансовый директор** | Cost per drop как ключевая метрика; ROI инвестиций в own fleet vs 3PL |
| **Категорийный менеджер** | Влияние last-mile cost на category economics; категории с разными моделями доставки |

## Связь с другими модулями

- [[01-SCOR-Maturity|01 SCOR & Maturity]] — Deliver-процесс SCOR
- [[02-Network-Design|02 Network Design]] — расположение DC влияет на last-mile
- [[03-Demand-Planning-SOP|03 S&OP & Demand Planning]] — прогноз для capacity planning
- [[05-Logistics-Transportation|05 Logistics & Transportation]] — общая логистика
- [[../03-Management-Accounting/02-Cost-to-Serve|03-Management-Accounting: Cost-to-Serve]] — last-mile как ключевой bucket CTS
- [[../09-Ecom-Marketplaces/index|Модуль 09: E-commerce]] — связь с маркетплейсной экономикой
- [[../10-Marketing/index|Модуль 10: Marketing]] — delivery как часть customer journey

## Источники

### Книги (приоритет чтения)

- Lyle Ginsburg, **«Last Mile Logistics: A New Era of Distribution»** (Routledge, 2021) — самая современная книга про last-mile
- Paolo Toth, Daniele Vigo, **«Vehicle Routing: Problems, Methods, and Applications»** (SIAM, 2014, 2-е изд.) — академический стандарт VRP
- Edward Frazelle, **«Logistics Management»** (McGraw-Hill) — главы по last-mile
- Sunil Chopra, Peter Meindl, **«Supply Chain Management»** (Pearson) — раздел по transportation
- Yossi Sheffi, **«The New (Ab)Normal»** (MIT Press, 2020) — last-mile в COVID
- Andreas Holzapfel et al., **«Last Mile Distribution in E-Commerce»** (Springer) — академический обзор

### Статьи

- McKinsey, **«The future of last-mile delivery»** (ежегодные отчёты 2021-2025)
- McKinsey, **«Parcel delivery: The future of last mile»** (2016) — классическая статья
- HBR, **«How Amazon Manages Its Logistics»**
- BCG, **«Same-Day Delivery: A Profitable Reality»**
- Bain, **«Last Mile Delivery Economics»**
- Russian E-commerce reports (Data Insight, ассоциация Akit)

### Онлайн-ресурсы

- Statista E-commerce Reports — данные по последней миле в РФ и мире
- AKIT (Ассоциация компаний интернет-торговли) — российская статистика
- Data Insight — российские данные e-commerce
- LogisticsViewpoints — индустриальные новости
- DHL Trend Research — Logistics Trend Radar
- McKinsey Last-Mile insights
- Wildberries / Ozon / СДЭК / Boxberry — публичные операционные отчёты
- Yandex Routing API documentation
- Google OR-Tools (open-source VRP)

### Кейсы

- **Amazon Logistics** — построение последней мили с нуля до конкурента UPS/FedEx
- **Wildberries** — крупнейшая ПВЗ-сеть в РФ
- **Ozon** — fulfillment + last-mile эволюция
- **Самокат** — dark store модель в РФ, 15-минутная доставка
- **Яндекс.Лавка** — конкурент Самоката, gig-курьеры
- **Доставка от СДЭК** — крупнейший courier в РФ
- **Почта России** — государственный provider с tightest coverage
- **5Post** — locker сеть для маркетплейсов
- **Domino's Pizza** — pioneer в quick last-mile, ~30-минутная доставка
- **Glovo** — pan-European on-demand delivery
- **Last Mile глобальные стартапы** — Stuart, Postmates, Instacart, Gopuff
## Связанные документы

- [[index|Модуль 04: Supply Chain Management]]
- [[../index|Education Index]]
- [[05-Logistics-Transportation|05 Logistics & Transportation]]
- Методология Education
