---
title: "04 — TMS — системы управления транспортом"
aliases: ["TMS", "Transportation Management", "VRP", "Freight Audit"]
type: note
status: active
domain: education
module: 12-ERP-Digital
tags: [education, tms, transportation, vrp, freight, oracle-tm, mercurygate]
created: 2026-05-19
updated: 2026-05-19
---

# 04 — TMS — системы управления транспортом

> TMS (Transportation Management System — система управления транспортом) — это **операционная система транспорта**: планирование маршрутов, тарификация, отправка, отслеживание, аудит счетов. Без TMS транспортная функция работает с потерями 15-25% на неоптимальных маршрутах, переплате тарифов, отсутствии видимости.

## Карта раздела

![](attachments/diagrams/12-wms-tms-flow.svg)

## 1. Что такое TMS

### 1.1 Контекст и легитимность

TMS как класс систем оформился в 2000-х. Каноничные книги — **John Coyle et al., «Transportation: A Supply Chain Perspective»** (Cengage, 10-е изд. 2021). Стандарт обзора — **Gartner Magic Quadrant for TMS** (ежегодно).

Глобальный рынок TMS — ~$15 млрд (2024), растёт 15% годовых. Главный драйвер — рост e-commerce, complex omnichannel networks, давление на стоимость доставки.

### 1.2 Главные функции TMS

- **Planning & Optimization** — построение оптимальных маршрутов (VRP — Vehicle Routing Problem — задача маршрутизации транспорта)
- **Carrier Management** — управление перевозчиками, ставки, контракты
- **Tendering** — выбор перевозчика на конкретный груз (auction, fixed, dynamic)
- **Execution** — отправка, отслеживание, ETA (Estimated Time of Arrival — расчётное время прибытия)
- **Freight Audit & Payment** — сверка фактических счетов с тарифами, оплата
- **Analytics** — отчёты по затратам, performance перевозчиков

**Ключевой вывод 1.** TMS — операционная основа транспортной функции. Без TMS экономия от оптимизации маршрутов и аудита счетов теряется в ручном труде.

## 2. VRP — Vehicle Routing Problem

### 2.1 Сложность задачи

VRP — классическая NP-hard задача оптимизации. Для 20 точек ~10^18 возможных маршрутов; для 100 — астрономическое число. Поэтому используются **эвристические** алгоритмы, дающие near-optimal решения за разумное время.

Каноничный учебник — **Paolo Toth, Daniele Vigo, «Vehicle Routing: Problems, Methods, and Applications»** (SIAM, 2-е изд. 2014).

### 2.2 Варианты VRP

| Тип | Что добавляет | Применение |
|-----|---------------|------------|
| **Basic VRP** | Точки, машины, депо | Базовый случай |
| **CVRP** (Capacitated VRP) | Ограничение по объёму машины | Стандарт |
| **VRPTW** (with Time Windows) | Временные окна доставки | E-commerce, B2B |
| **PDPTW** (Pickup & Delivery) | Загрузка и выгрузка в разных точках | Курьерская доставка |
| **DVRP** (Dynamic) | Новые заказы во время выполнения | Last-mile в реальном времени |

### 2.3 Алгоритмы

- **Heuristics** (эвристики) — Savings, Sweep, Nearest Neighbor
- **Metaheuristics** — Tabu Search, Simulated Annealing, Genetic Algorithms
- **Mathematical Programming** — для малых задач (точное решение)
- **ML-augmented** — нейросети для разогрева классических методов

В современных TMS под капотом — комбинация: ML предсказывает входы, метаэвристика решает.

### 2.4 Экономия от оптимизации

Типичные результаты внедрения VRP-оптимизатора:
- Снижение пробега 10-20%
- Снижение стоимости транспорта 8-15%
- Улучшение OTD (On-Time Delivery) 5-10%

ROI — обычно 6-18 месяцев.

**Ключевой вывод 2.** VRP — математически сложная задача с реальным бизнес-эффектом. Современные TMS делают её доступной без PhD по операционным исследованиям.

## 3. Главные TMS на рынке

### 3.1 Top-5 мировых платформ

| Платформа | Сегмент | Сильные стороны |
|-----------|---------|-----------------|
| **Oracle Transportation Management (OTM)** | Enterprise | Глубина функций, лидер Gartner |
| **MercuryGate** | Mid-Enterprise | Cloud-native, цена/качество |
| **Blue Yonder TMS** | Enterprise | Интеграция с SCM-стеком |
| **Trimble (TMW)** | Carriers | Для самих перевозчиков |
| **Manhattan Active Transportation** | Enterprise | Интеграция с WMS Manhattan |

### 3.2 Российский ландшафт

- **Antor** — российский лидер в маршрутизации для FMCG
- **ЛогистАс** — для крупного e-commerce
- **GoodsForecast** — российская TMS-платформа
- **Maxoptra** (с российской поддержкой)
- **Кастомные на open-source** — Optaplanner, jsprit

### 3.3 Last-Mile TMS

Отдельная категория для последней мили:

- **OnFleet** — для on-demand доставки
- **Bringg** — last-mile управление
- **DeliverApp** — оркестрация курьеров
- **Российские:** Yandex.Routing, СберЛогистика

### 3.4 Когда какой TMS

| Сценарий | Рекомендация |
|----------|--------------|
| Грузоотправитель (shipper) с >100 отгрузок/день | Oracle TM / MercuryGate / Antor |
| 3PL / 4PL | Specialized (Manhattan, Blue Yonder) |
| Перевозчик | Trimble TMW / российские |
| Last-mile e-commerce | OnFleet / Bringg / Yandex.Routing |

**Ключевой вывод 3.** TMS-выбор зависит от роли в цепочке (shipper vs carrier vs 3PL) и типа доставки (long-haul vs last-mile).

## 4. KPI транспортной функции

### 4.1 Стоимость

- **Cost per km / mile** — стоимость на единицу пути
- **Cost per stop** — стоимость на остановку (для last-mile)
- **Cost per order** — стоимость на заказ
- **Empty miles %** — процент пробега без груза (целевая <15%)

### 4.2 Сервис

- **OTD** (On-Time Delivery) — доставка вовремя (целевая 95%+)
- **DIFOT** (Delivered In-Full On-Time) — полностью и вовремя (целевая 92%+)
- **Failed deliveries %** — неудачные доставки (целевая <5%)
- **Customer rating** — оценка клиента

### 4.3 Эффективность

- **Fleet utilization** — загрузка флота (целевая 75-85%)
- **Loading factor** — заполнение машины (целевая 80%+)
- **Driver productivity** — заказы / часов работы
- **Fuel efficiency** — литры / 100 км

### 4.4 Качество

- **Damage rate** — повреждения
- **Claims rate** — претензии
- **Documentation accuracy** — точность документов

**Ключевой вывод 4.** Полный дашборд транспортной функции — 12-15 KPI. Зрелые компании отслеживают их еженедельно.

## 5. Современные тренды

### 5.1 Real-time visibility

GPS-трекинг + интеграция с ELD (Electronic Logging Device — электронный регистратор):
- Project44, FourKites, Shippeo — лидеры визибилити-платформ
- Российские: Wialon, GLONASSSoft

Реальное время от заказа до доставки — стандарт 2024-2025.

### 5.2 AI в TMS

- **Predictive ETA** — точный прогноз времени прибытия
- **Dynamic routing** — пересчёт маршрута на ходу
- **Anomaly detection** — выявление проблем
- **Procurement automation** — автоматический выбор перевозчика

### 5.3 Sustainability

- **Углеродный след** каждой отгрузки
- **Trade-off** между cost и emissions
- **Modal shift** — переключение с авто на ж/д, sea
- **EV (Electric Vehicles)** в last-mile

### 5.4 Digital Freight Marketplaces

Платформы типа Uber для груза:
- Convoy (закрыт 2023), Loadsmart, Transfix — США
- Sennder — Европа
- Российские: ATI.SU, Везёт, GroozGo

Меняют ландшафт грузоперевозок.

**Ключевой вывод 5.** TMS-индустрия в активной трансформации: real-time visibility, AI, sustainability, digital marketplaces. Лидеры (DHL, Maersk, FedEx) уже там.

## 6. Внедрение TMS

### 6.1 Стандартный roadmap

| Фаза | Срок |
|------|------|
| Selection | 2-3 месяца |
| Design | 2-3 месяца |
| Configure | 4-6 месяцев |
| Test | 1-2 месяца |
| Go-Live | 1-2 месяца |
| Stabilization | 3 месяца |

Итого 12-18 месяцев для среднего проекта.

### 6.2 Главные риски

- **Качество данных перевозчиков** — нужны актуальные тарифы и контракты
- **Интеграция с ERP / WMS** — потенциальные конфликты
- **Сопротивление перевозчиков** — особенно при tendering
- **Master data адресов** — геокодирование, нормализация

### 6.3 Best practices

- Pilot на одном регионе перед rollout
- Mandatory carrier onboarding (обязательная интеграция)
- Continuous improvement через KPI-дашборд

**Ключевой вывод 6.** TMS-внедрение менее рискованно, чем ERP, но требует чистых master data и change management.

## Применение для руководителя

| Целевая роль | Главные применения |
|--------------|---------------------|
| **COO** | Стратегия транспортного стека; интеграция TMS+WMS |
| **Директор логистики** | Daily управление; KPI; контракты с перевозчиками |
| **Директор закупок транспорта** | Tendering, freight audit, carrier scorecards |
| **CFO** | Cost per order; freight audit savings |
| **Категорийный менеджер** | Влияние транспорта на маржу категории |

## Связь с другими модулями

- [[01-ERP-Systems|01 ERP-системы]] — данные заказов из ERP
- [[03-WMS-Warehouse-Systems|03 WMS]] — пара WMS + TMS
- [[../04-Supply-Chain/05-Logistics-Transportation|Модуль 04: Logistics]] — общая логистика
- [[../04-Supply-Chain/07-Last-Mile-Delivery|Модуль 04: Last-Mile]] — специфика последней мили
- [[../06-Foreign-Trade/05-Customs-and-Logistics|Модуль 06: Customs]] — международная логистика

## Источники

### Книги (приоритет чтения)

- John Coyle, John Langley, Brian Gibson, **«Transportation: A Supply Chain Perspective»** (Cengage, 10-е изд. 2021) — стандартный учебник
- Paolo Toth, Daniele Vigo, **«Vehicle Routing: Problems, Methods, and Applications»** (SIAM, 2-е изд. 2014) — академический стандарт VRP
- Donald Bowersox et al., **«Supply Chain Logistics Management»** (McGraw-Hill) — детальный учебник
- Joseph Walden, **«The Definitive Guide to Transportation»** (Pearson, 2014) — практический справочник

### Статьи

- Gartner Magic Quadrant for TMS (ежегодно)
- Inbound Logistics — практические кейсы
- Journal of Business Logistics — академические исследования
- HBR: «The Future of Logistics»

### Онлайн-ресурсы

- **Oracle Transportation Management Learning** — официальные курсы
- **MercuryGate Academy** — для MercuryGate
- **ASCM CLTD** — стандарт по транспорту
- **CSCMP** (Council of Supply Chain Management Professionals) — публикации
- **Российские:** Российская логистическая ассоциация, конференции «Транспорт и логистика»

### Сертификации

- **ASCM CLTD** — главная сертификация по логистике
- **CITT (Canadian Institute of Traffic and Transportation)**
- **APICS CSCP** — общая supply chain включает транспорт

### Кейсы

- **DHL Resilience360** — публичные доклады по visibility
- **Maersk integrated logistics** — преобразование 4PL
- **Российские:** СДЭК, DPD автоматизация маршрутизации
- **Wildberries / Ozon** — собственные TMS для last-mile
## Связанные документы

- [[index|Модуль 12: ERP & Digital]]
- [[../index|Education Index]]
- [[03-WMS-Warehouse-Systems|03 WMS]]
