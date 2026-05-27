---
title: "06 — Автоматизация и AI"
aliases: ["RPA", "Process Mining", "AI Agents", "Digital Twin"]
type: note
status: active
domain: education
module: 12-ERP-Digital
tags: [education, rpa, uipath, process-mining, celonis, ai-agents, digital-twin]
created: 2026-05-19
updated: 2026-05-19
---

# 06 — Автоматизация и AI в операциях

> Автоматизация в 2024-2025 годах прошла три волны: **RPA** (Robotic Process Automation — роботизация процессов) для рутинных задач (2015+), **Process Mining** для выявления узких мест (2018+), **AI-агенты на базе LLM** для сложных задач (2023+). Этот раздел — про каждый из этих слоёв, когда что применять, и про **Digital Twin** как следующий уровень.

## Карта раздела

![](attachments/diagrams/12-rpa-process-mining.svg)

## 1. RPA — Robotic Process Automation

### 1.1 Контекст и легитимность

RPA как класс систем оформилась в 2010-х. Каноничная книга — **Mary Lacity, Leslie Willcocks, «Service Automation: Robots and the Future of Work»** (Steve Brookes Publishing, 2016). Современный анализ — **Forrester Wave for RPA** (ежегодно).

Глобальный рынок RPA — ~$5 млрд в 2024, растёт 25% годовых.

### 1.2 Что такое RPA

RPA — программные «боты», эмулирующие действия пользователя в UI существующих систем:
- Открывают ERP, копируют данные, переводят в Excel
- Парсят email, извлекают вложения, обрабатывают
- Заполняют формы на сайтах
- Сверяют данные между системами

В отличие от классической интеграции (через API), RPA работает **с UI**, поэтому подходит к **legacy systems без API**.

### 1.3 Когда применять RPA

| Критерий | Подходит для RPA |
|----------|-------------------|
| **Объём** | Высокая частота (сотни-тысячи в день) |
| **Структура** | Rule-based, предсказуемые шаги |
| **Качество данных** | Стандартизированный input |
| **Стабильность** | UI системы не меняется часто |
| **ROI** | Часы человеческого труда в неделю |

Типичные применения:
- Финансовая сверка (bank reconciliation)
- Сверка данных между системами
- Обработка инвойсов
- Onboarding сотрудников (заведение в 10 системах)
- HR transactions

### 1.4 Главные платформы

| Платформа | Сильные стороны |
|-----------|-----------------|
| **UiPath** | Лидер Gartner, широкая экосистема, marketplace |
| **Blue Prism** | Enterprise, сильное governance |
| **Automation Anywhere** | Облачная архитектура |
| **Microsoft Power Automate** | Интеграция с Microsoft 365 |
| **Российские** | PIX RPA, Sherpa RPA, Robin |

### 1.5 ROI RPA

Типичные результаты:
- 30-70% экономии FTE (Full-Time Equivalent — эквивалента полной занятости) на автоматизированных процессах
- Окупаемость 6-18 месяцев
- Точность 99.9% (нет человеческих ошибок)
- 24/7 работа

### 1.6 Главные риски

- **Bot fragility** — изменение UI ломает бота
- **Maintenance burden** — боты требуют постоянной поддержки
- **Wrong process** — автоматизация плохого процесса делает его быстрее, но не лучше
- **Governance** — без CoE (Center of Excellence — центра компетенций) RPA превращается в хаос

**Ключевой вывод 1.** RPA — мощный инструмент для рутинной работы, но требует **правильного выбора процессов** (см. Process Mining) и **governance**. Без этого 50% ботов умирают в первый год.

## 2. Process Mining

### 2.1 Контекст

Process Mining — техника **анализа реальных процессов по логам систем**. Вместо рисования процессов «как они должны быть», Process Mining показывает «как они реально работают» — через тысячи реальных кейсов.

Каноничная книга — **Wil van der Aalst, «Process Mining: Data Science in Action»** (Springer, 2-е изд. 2016). Pioneering tool — **Celonis** (немецкая компания, основана 2011).

### 2.2 Как работает Process Mining

1. **Сбор event logs** — каждое действие в ERP / CRM / другой системе с timestamp
2. **Process discovery** — алгоритм восстанавливает диаграмму процесса
3. **Analysis** — узкие места, отклонения от стандарта, длительность шагов
4. **Conformance checking** — соответствие фактического процесса целевому
5. **Recommendations** — где автоматизировать, где упростить

### 2.3 Главные применения

- **Process improvement** — найти узкие места
- **Compliance** — проверить, что процесс соответствует регламенту
- **RPA opportunity assessment** — какие процессы стоит автоматизировать
- **Audit** — отслеживание изменений и нарушений
- **M&A integration** — сравнение процессов двух компаний

### 2.4 Главные платформы

- **Celonis** — лидер, $13B оценка
- **UiPath Process Mining** (бывшая ProcessGold)
- **Software AG ARIS**
- **Microsoft Process Mining** (часть Power Platform)
- **Disco** — для аналитиков, меньше для enterprise

### 2.5 Целевые процессы

Process Mining лучше всего работает на **транзакционных процессах** с цифровым следом:
- Order-to-Cash (от заказа до оплаты)
- Procure-to-Pay (от закупки до оплаты)
- IT Service Management
- Customer Service tickets
- Claims processing (insurance, warranty)

**Ключевой вывод 2.** Process Mining — следующий уровень после визуального картирования процессов. Даёт **объективную картину** на основе данных, не интервью.

## 3. AI-агенты на базе LLM

### 3.1 Контекст 2024-2025

После прорыва GPT-4 (2023) и появления AI-агентов (агенты, выполняющие multi-step задачи) в 2024-2025 началась **новая волна автоматизации**: LLM-агенты, способные обрабатывать неструктурированные задачи, в отличие от rule-based RPA.

Каноничные исследования — OpenAI, Anthropic Claude, Google DeepMind. Практические применения активно появляются в Bain, McKinsey, BCG отчётах.

### 3.2 Чем AI-агенты отличаются от RPA

| Аспект | RPA | AI-агент |
|--------|-----|----------|
| **Тип задач** | Rule-based, structured | Open-ended, judgement |
| **Input** | Structured (поля формы) | Unstructured (текст, изображение, голос) |
| **Маршрут** | Фиксированный workflow | Динамический выбор шагов |
| **Адаптация** | Не адаптируется | Адаптируется через context |
| **Зрелость** | Production-ready | Ранняя зрелость, 2024-2025 |

### 3.3 Главные применения AI-агентов

- **Customer support tier 1** — обработка типичных запросов (70-80% покрытие)
- **Document processing** — извлечение данных из контрактов, счетов
- **Code copilots** — GitHub Copilot, Cursor для разработки
- **Knowledge work** — резюме, drafting emails, аналитические записки
- **Sales agents** — квалификация лидов, follow-up emails
- **Data analysis** — натуральный язык в SQL и BI

### 3.4 RAG — Retrieval-Augmented Generation

Главный паттерн enterprise LLM — **RAG**:
1. Корпоративные документы → vector database (Pinecone, Weaviate)
2. По запросу пользователя — semantic search релевантных документов
3. LLM генерирует ответ на основе **извлечённых** документов

Это решает проблему **галлюцинаций** LLM и работы с private data.

### 3.5 Главные платформы для AI-агентов

- **OpenAI ChatGPT Enterprise / Microsoft Copilot Studio**
- **Anthropic Claude (для длинного контекста, безопасности)**
- **Google Gemini for Workspace**
- **LangChain / LangGraph** — фреймворк построения агентов
- **Российские:** GigaChat (Сбер), YandexGPT

### 3.6 Риски AI-агентов

- **Галлюцинации** — уверенно неверная информация
- **Privacy** — данные могут утечь через облачные модели
- **Prompt injection** — атаки через вредоносные промпты
- **Costs** — высокие расходы на API при массовом использовании
- **Безопасность action-агентов** — реальные действия (отправка email, платежи)

**Ключевой вывод 3.** AI-агенты — следующая волна автоматизации после RPA. RPA для structured, AI для unstructured. К 2026-2027 годам зрелость для критичных бизнес-процессов.

## 4. Гибридный стек автоматизации

### 4.1 Три слоя

Зрелая компания комбинирует три инструмента:

1. **Process Mining (Celonis)** — выявление кандидатов на автоматизацию
2. **RPA (UiPath)** — для structured rule-based задач
3. **AI-агенты (LLM)** — для unstructured judgment задач

### 4.2 Принятие решения «что чем автоматизировать»

| Тип задачи | Инструмент |
|------------|-----------|
| Structured, rule-based, high-volume | **RPA** |
| Structured + некоторое judgment | **RPA + AI augmentation** |
| Unstructured, judgment, low-volume | **AI-agent** |
| Repetitive с UI старых систем | **RPA** |
| Document processing с разными форматами | **AI-agent (LLM + OCR)** |

### 4.3 Center of Excellence (CoE)

Зрелые компании создают **Automation CoE**:
- Standards разработки ботов / агентов
- Process selection criteria
- Шаблоны и компоненты
- Мониторинг и метрики
- Обучение бизнес-пользователей (citizen developers)

Без CoE — автоматизация превращается в shadow IT.

**Ключевой вывод 4.** Зрелая автоматизация — **гибрид RPA + AI + governance**. Лидеры (Walmart, Bank of America, Сбер) внедряют все три слоя одновременно.

## 5. Digital Twin

### 5.1 Что это

**Digital Twin** (цифровой двойник) — математическая модель физического актива / процесса / целой компании, **синхронизированная с реальностью в реальном времени**.

![](attachments/diagrams/12-digital-twin-concept.svg)

Цикл:
1. Сенсоры / системы → данные
2. Данные → digital twin (модель)
3. Twin → симуляции «что если»
4. Решения → действия в реальном мире

### 5.2 Уровни Digital Twin

- **Asset twin** — двойник одного актива (станок, машина)
- **Process twin** — двойник процесса (склад, логистическая цепочка)
- **System twin** — двойник системы (вся производственная линия)
- **Enterprise twin** — двойник всей компании

### 5.3 Применения

- **Predictive Maintenance** — когда сломается оборудование
- **Production optimization** — оптимизация загрузки в реальном времени
- **Supply chain simulation** — what-if по всей цепочке
- **Smart cities** — управление инфраструктурой
- **Healthcare** — персональные модели пациентов

### 5.4 Главные платформы

- **Siemens Digital Industries Software** (Teamcenter, MindSphere)
- **PTC ThingWorx** — IoT + Digital Twin
- **Microsoft Azure Digital Twins**
- **AWS IoT TwinMaker**
- **Российские:** Цифровая модель промышленности (Минпромторг)

### 5.5 Уровень зрелости

В 2024-2025 годах Digital Twin — **early adopter phase**. Применяется в:
- Авиа (Rolls-Royce — каждый двигатель имеет twin)
- Промышленности (Siemens Amberg factory)
- Энергетике (electricity grids)
- Городах (Singapore Virtual Twin)

Mass adoption в Mid-market ожидается 2027-2030.

**Ключевой вывод 5.** Digital Twin — стратегическая инвестиция на 5-10 лет. Лидеры закладывают сейчас; большинство компаний не готовы.

## Сводный практический протокол

Внедрение автоматизации в компании:

| Этап | Срок | Артефакт |
|------|------|----------|
| 1. Process Mining audit | 2-3 месяца | Карта процессов с узкими местами |
| 2. Pipeline кандидатов | 1-2 месяца | Список 20-50 процессов для авто |
| 3. Pilot 5 ботов | 3-6 месяцев | Первые работающие боты |
| 4. CoE setup | 6 месяцев | Стандарты, обучение, governance |
| 5. Scale to 50+ ботов | 12-24 месяца | Полная программа |
| 6. AI-агенты слой | 12-24 месяца | LLM для unstructured |
| 7. Digital Twin | 24-60 месяцев | Стратегическая инвестиция |

## Применение для руководителя

| Целевая роль | Главные применения |
|--------------|---------------------|
| **COO** | Стратегия автоматизации; CoE; ROI инвестиций |
| **CIO / CDO** | Архитектура стека; выбор платформ; governance |
| **HR-директор** | Влияние автоматизации на роли; reskilling |
| **CFO** | RPA для финансовых процессов; ROI |
| **Директор закупок** | Автоматизация P2P процесса |

## Связь с другими модулями

- [[01-ERP-Systems|01 ERP-системы]] — RPA автоматизирует ERP-процессы
- [[../03-Management-Accounting/03-Operational-Decisions|Модуль 03: Operational Decisions]] — process mining для процессных решений
- [[../11-Analytics-BI/05-Machine-Learning-Operations|Модуль 11.05: ML]] — AI применения в операциях
- [[../18-HR-Management/index|Модуль 18: HR Management]] — автоматизация и работа

## Источники

### Книги (приоритет чтения)

- Mary Lacity, Leslie Willcocks, **«Service Automation: Robots and the Future of Work»** (Steve Brookes, 2016) — стандарт RPA
- Wil van der Aalst, **«Process Mining: Data Science in Action»** (Springer, 2-е изд. 2016) — academic standard
- Tom Davenport, Steven Miller, **«Working with AI»** (MIT Press, 2022) — практика AI в работе
- Mike Walker et al., **«Digital Twin: Things, Threads, and Threats»** (Springer, 2020)

### Статьи

- Gartner Magic Quadrant for RPA, Process Mining (ежегодно)
- Forrester Wave for RPA / AI Agents
- HBR: «Robots Are Coming for Your Job»
- McKinsey: «The State of AI in 2024»

### Онлайн-ресурсы

- **UiPath Academy** — бесплатные курсы по RPA
- **Celonis Academy** — для Process Mining
- **DeepLearning.AI courses** — Andrew Ng
- **Российские:** Sherpa, PIX обучающие материалы

### Сертификации

- **UiPath Certified RPA Developer / Architect**
- **Celonis Process Mining Practitioner**
- **Microsoft Certified: Power Automate**
- **AWS / Azure / Google ML certifications**

### Кейсы

- **Bank of America — Erica chatbot** — публичные доклады
- **Klarna — ChatGPT** — замена 700 customer service agents
- **Siemens Amberg factory** — каноничный Digital Twin
- **Rolls-Royce engine twins** — каждый двигатель имеет цифрового двойника
- **Российские:** Сбер AI-агенты, Газпром цифровые двойники
## Связанные документы

- [[index|Модуль 12: ERP & Digital]]
- [[../index|Education Index]]
- [[../11-Analytics-BI/05-Machine-Learning-Operations|Модуль 11.05: ML]]
