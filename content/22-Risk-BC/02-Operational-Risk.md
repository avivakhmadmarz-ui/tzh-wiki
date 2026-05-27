---
title: "02 — Operational Risk"
aliases: ["Operational Risk", "Risk Register", "KRI", "Key Risk Indicators", "Three Lines of Defense", "IIA", "Internal Controls", "COSO Internal Control"]
type: note
status: active
domain: education
module: 22-Risk-BC
tags: [education, risk-management, operational-risk, risk-register, kri, three-lines-of-defense, internal-controls]
created: 2026-05-26
updated: 2026-05-26
---

# 02 — Operational Risk

> **Operational Risk (операционный риск)** — риск убытков от **неадекватных или сбойных** внутренних процессов, людей, систем или внешних событий. Это **самая широкая** категория рисков, потому что включает всё, что может пойти не так в ежедневной работе. Эта заметка покрывает практические инструменты: Risk Register (реестр рисков) как главный артефакт, KRI (Key Risk Indicators) для мониторинга, Three Lines of Defense (модель IIA — Institute of Internal Auditors) для распределения ответственности, и Internal Controls по COSO Internal Control — Integrated Framework.

## Карта раздела

![](attachments/diagrams/22-risk-register-flow.svg)

## 1. Что такое operational risk

### 1.1 Определение

Классическое определение от Basel Committee (комитет по банковскому надзору):

> «**Операционный риск** — это риск убытков, возникающих из неадекватных или сбойных внутренних процессов, людей и систем, или из внешних событий».

Это **широкая** категория, включающая:
- **Processes (процессы)** — сбои, ошибки, неэффективность
- **People (люди)** — человеческие ошибки, мошенничество, недостаток квалификации
- **Systems (системы)** — отказы IT, кибер-атаки, потеря данных
- **External events (внешние события)** — стихийные бедствия, регуляторные изменения, пандемии

### 1.2 Соотношение с другими типами риска

- **Strategic risk** — выше, более долгосрочный
- **Financial risk** — может быть результатом operational risk (но не наоборот)
- **Compliance risk** — частный случай operational risk
- **Reputational risk** — часто следствие operational risk

Operational risk — **базовый слой**, на котором сидят другие.

### 1.3 Категоризация Basel II / III

Basel выделяет **7 категорий** event types (для банков, но применимо шире):

1. **Internal fraud** — внутреннее мошенничество
2. **External fraud** — внешнее мошенничество
3. **Employment practices and workplace safety** — трудовые практики и безопасность
4. **Clients, products and business practices** — практики работы с клиентами
5. **Damage to physical assets** — повреждение физических активов
6. **Business disruption and system failures** — нарушение бизнеса и сбои систем
7. **Execution, delivery and process management** — исполнение, поставка, управление процессами

## 2. Risk Register — реестр рисков

### 2.1 Что это

**Risk Register (реестр рисков)** — структурированный документ со списком **всех идентифицированных** рисков компании.

Это **главный артефакт** operational risk management — без risk register всё остальное теряет смысл.

### 2.2 Структура Risk Register

Стандартный шаблон:

| Поле | Что заполняется |
|---|---|
| **Risk ID** | Уникальный идентификатор (R-001, R-002...) |
| **Category** | Strategic / Operational / Financial / Compliance / Reputational |
| **Subcategory** | Более детальная (например, IT system failure) |
| **Description** | Подробное описание риска |
| **Cause** | Причины (root causes) |
| **Consequence** | Последствия |
| **Owner** | Кто отвечает за управление этим риском |
| **Inherent Likelihood** | Вероятность без контролей (1-5) |
| **Inherent Impact** | Влияние без контролей (1-5) |
| **Inherent Score** | Likelihood × Impact (1-25) |
| **Existing Controls** | Какие контроли уже есть |
| **Residual Likelihood** | Вероятность с контролями |
| **Residual Impact** | Влияние с контролями |
| **Residual Score** | Likelihood × Impact с контролями |
| **Mitigation Actions** | Что планируется делать |
| **Target Date** | Когда mitigation будет завершён |
| **Status** | Open / In Progress / Closed |
| **Last Review** | Дата последнего обзора |

### 2.3 Risk Register Flow

![](attachments/diagrams/22-risk-register-flow.svg)

**1. Identify (идентификация).**

Источники:
- **Brainstorming sessions** с командой
- **Interviews** с менеджерами разных уровней
- **Historical data** — прошлые инциденты
- **Industry benchmarks** — что происходило у конкурентов
- **Internal audit reports**
- **External signals** — регуляторные изменения, новые угрозы

**2. Assess (оценка).**

Для каждого риска:
- Inherent risk = likelihood × impact (без контролей)
- Residual risk = likelihood × impact (с контролями)

Оценка обычно **subjective** (на основе экспертного мнения), но должна следовать **формальной шкале**.

**3. Mitigate (mitigation).**

4 стратегии:
- **Avoid** — избежать (выйти из деятельности)
- **Reduce** — снизить через контроли
- **Transfer** — передать (страхование, аутсорсинг)
- **Accept** — принять (если в рамках risk appetite)

**4. Control (контроль).**

Дизайн контролей:
- **Preventive** — предотвращают событие (например, KYC процедуры)
- **Detective** — обнаруживают событие (например, мониторинг)
- **Corrective** — устраняют последствия (например, business continuity plan)

**5. Monitor (мониторинг).**

- Periodic review (минимум раз в квартал)
- Incident reports (когда событие случилось)
- KRI tracking (см. ниже)
- Update register

### 2.4 Размер Risk Register

| Размер компании | Кол-во рисков в register |
|---|---|
| Small business | 20-50 |
| Mid-size | 50-150 |
| Large enterprise | 150-500 |
| Financial institution | 500+ (часто 1000+) |

Главное правило — **не перегружать** register. Лучше иметь **50 хорошо отслеживаемых** рисков, чем 500 формально записанных, но никогда не пересматриваемых.

**Ключевой вывод 1.** Risk Register — **базовый артефакт**. Без него все ERM-инициативы становятся academic. Hardest часть — **поддержание актуальности**, не первичное создание.

## 3. KRI — Key Risk Indicators

### 3.1 Что это

**KRI (Key Risk Indicators — ключевые индикаторы рисков)** — **метрики**, отслеживающие изменение уровня риска во времени. Аналог KPI, но для рисков.

Если KPI отвечает на «**как мы движемся к цели?**», KRI отвечает на «**какие риски накапливаются**?»

### 3.2 Примеры KRI по категориям

**HR / People risks:**
- Текучесть кадров (turnover rate)
- Average tenure
- % vacancies
- Employee engagement score
- # дисциплинарных взысканий за квартал

**IT / System risks:**
- System availability (uptime %)
- # incidents per month (по уровню severity)
- Mean time to recovery (MTTR)
- # security alerts

**Process / Operations risks:**
- Defect rate
- Customer complaints volume
- # process exceptions
- Inventory accuracy

**Financial risks:**
- Current ratio
- Days sales outstanding (DSO)
- Cash conversion cycle
- Debt-to-equity ratio

**Compliance risks:**
- # regulatory inquiries
- # compliance training non-completions
- # whistleblowing reports
- Audit findings count

### 3.3 Хороший KRI

Признаки хорошего KRI:

- **Predictive** — предсказывает будущий риск (не только фиксирует прошлый)
- **Measurable** — количественно измеряем
- **Trackable** — можно отслеживать во времени
- **Actionable** — на основе KRI можно принять решение
- **Cost-effective** — стоимость сбора оправдана ценностью

### 3.4 Thresholds — пороговые значения

Каждый KRI должен иметь **пороги** для реагирования:

- **Green** — норма, нет действий
- **Yellow / Amber** — повышенный риск, attention
- **Red** — высокий риск, эскалация и действия

Пример (для customer churn):
- Green: <5% годовых
- Yellow: 5-8%
- Red: >8%

### 3.5 Связь с risk register

KRI — это **продолжение** risk register. Для каждого высокоприоритетного риска должны быть **1-3 KRI**, отслеживающих его уровень.

**Ключевой вывод 2.** KRI — **проактивный** инструмент. В отличие от incident reports (фиксирующих **что произошло**), KRI показывают **что будет происходить**, если не вмешаться.

## 4. Three Lines of Defense Model

### 4.1 Концепция

![](attachments/diagrams/22-three-lines-of-defense.svg)

**Three Lines of Defense (Три линии защиты)** — модель распределения ответственности за управление рисками. Разработана **IIA (Institute of Internal Auditors)** в 2013 году.

Обновлена в 2020 году как **«Three Lines Model»** (с убранным словом «defense», чтобы подчеркнуть positive aspect).

### 4.2 Три линии

**1-я линия — Operational Management (операционный менеджмент).**

**Кто:** прямые менеджеры, владельцы процессов.

**Что делает:**
- **Owners рисков** в своей области
- Реализует контроли каждый день
- Identifies риски на местах
- Reports проблемы наверх

**Пример:** Sales Director управляет рисками потери клиентов через CRM, KAM-программы, контроль ценообразования.

**2-я линия — Risk Management & Compliance.**

**Кто:** Risk Function, Compliance Function, Quality Function, Security Function.

**Что делает:**
- **Develop methodologies** для управления рисками
- **Monitor** outcomes 1-й линии
- **Challenge** 1-ю линию (где недостаточно контролей)
- **Provide expertise** в специализированных областях

**Пример:** Compliance Officer проверяет, что Sales-команда соблюдает 381-ФЗ при работе с розничными сетями.

**3-я линия — Internal Audit (внутренний аудит).**

**Кто:** Internal Audit Function, отчитывающаяся **прямо Совету Директоров** (для независимости).

**Что делает:**
- **Independent assurance** — независимая оценка работы 1-й и 2-й линий
- **Audit** policies, processes, controls
- **Report** в Совет / Audit Committee

**Пример:** Internal Audit проверяет, действительно ли compliance-программа работает, или это «бумажная процедура».

**Внешние элементы:**
- **External Audit** (PwC, KPMG, EY, Deloitte) — независимая внешняя оценка
- **Regulators** (ЦБ, ФАС, и т.п.) — государственный надзор

### 4.3 Главные принципы

1. **Independence** — каждая линия имеет свою независимую функцию
2. **Reporting lines** — 3-я линия отчитывается прямо Совету, не CEO (чтобы избежать конфликта интересов)
3. **Coordination** — линии должны сотрудничать, не конкурировать
4. **Maturity** — модель применима к крупным компаниям; в малых компании линии часто **смешиваются**

### 4.4 Когда применяется

- **Банки и страховщики** — обязательно (регуляторное требование)
- **Публичные компании (>500 чел.)** — стандарт corporate governance
- **Крупные private companies** — best practice
- **Small business** — обычно одна функция (например, CFO + compliance)

### 4.5 Главные проблемы внедрения

- **Слабая 1-я линия** — operations не видит себя owners рисков, делегирует «risk people»
- **Перегруженная 2-я линия** — пытается делать работу 1-й линии
- **Зависимая 3-я линия** — internal audit отчитывается CEO, теряет независимость

**Ключевой вывод 3.** Three Lines of Defense — **structural foundation** ERM. Без правильного распределения ответственности компания либо концентрирует риск в одной функции (overload), либо размазывает (никто не отвечает).

## 5. Internal Controls — COSO Internal Control Framework

### 5.1 Что это

**COSO Internal Control — Integrated Framework** — стандарт **внутреннего контроля**, первая версия 1992, обновление 2013. Главный реference document for SOX-compliance в США.

### 5.2 5 компонентов internal controls

1. **Control Environment** — общее «отношение» организации к контролю (tone at the top)
2. **Risk Assessment** — выявление и оценка рисков для целей
3. **Control Activities** — конкретные политики и процедуры
4. **Information and Communication** — информационные системы для контроля
5. **Monitoring Activities** — постоянное наблюдение за эффективностью

### 5.3 Типы control activities

**Preventive Controls (превентивные):**
- Segregation of duties (разделение обязанностей) — например, тот, кто принимает заявки на покупку, не подписывает счета
- Authorization controls — лимиты подписи
- Pre-employment checks — проверка персонала перед наймом

**Detective Controls (детективные):**
- Reconciliations — сверки
- Reviews — обзоры
- Audits — аудиты

**Corrective Controls (корректирующие):**
- Backup procedures
- Disaster recovery plans
- Incident response procedures

### 5.4 Главные принципы

- **Segregation of duties** — критические задачи разделены между разными людьми (предотвращение fraud)
- **Authorization levels** — лимиты подписи на разных уровнях
- **Documentation** — все важные процессы документированы
- **Reconciliations** — регулярные сверки (между системами, между внутренним и внешним учётом)
- **Periodic reviews** — регулярные обзоры эффективности контролей

### 5.5 SOX-compliance (для контекста)

**Sarbanes-Oxley Act (2002)** — американский закон, регулирующий публичные компании после Enron / WorldCom scandals. Требует:
- CEO и CFO **лично подписывают** финансовую отчётность
- Independent audit of internal controls (Section 404)
- Whistleblowing protection
- **Книги и записи** must be accurate (отголосок FCPA)

Применимо к публичным компаниям США, российским дочкам американских публичных компаний, российским компаниям с ADR/GDR в США.

**Ключевой вывод 4.** Internal controls — **detail level** ERM. COSO Internal Control Framework — **самый детальный** стандарт, применяемый как для финансовой отчётности (SOX), так и для общего управления рисками.

## 6. Operational Risk Management — практическое внедрение

### 6.1 Roadmap

**Этап 1 — Foundation (3-6 месяцев).**
- Назначить risk owner на каждое подразделение
- Создать risk register (первая версия)
- Базовая heat map
- Identify топ-10 рисков

**Этап 2 — Operationalization (6-12 месяцев).**
- Внедрить KRI для топ-10 рисков
- Quarterly risk reviews с risk owners
- Incident management process
- Audit of key controls

**Этап 3 — Integration (12-24 месяца).**
- ERM integrated в operational reporting
- Risk-based budgeting
- Cross-functional risk committees
- Reporting на executive level

**Этап 4 — Maturity (24+ месяцев).**
- Predictive analytics
- Dynamic risk register (real-time updates)
- Risk culture across organization
- Continuous improvement

### 6.2 Главные роли

| Роль | Что делает |
|---|---|
| **CRO (Chief Risk Officer)** | Стратегия, координация всех функций риск-менеджмента |
| **Risk Manager** | Оperational ownership risk register, KRI tracking |
| **Risk Owners** (по подразделениям) | Operational responsibility за конкретные риски |
| **Internal Audit** | Independent assurance |
| **Audit Committee** | Oversight на уровне Совета |
| **CEO + executive team** | Strategic decisions, risk appetite |

### 6.3 Российский контекст

В России формальный operational risk management хорошо развит в:
- **Банках** — обязательно по регулированию ЦБ РФ (Положение № 716-П)
- **Крупных публичных компаниях** — Газпром, Сбер, Ростех
- **Иностранных дочках** — под требованиями материнской

В среднем бизнесе часто отсутствует formal framework. Это **зона роста**.

## 7. Главные ошибки

### 7.1 Risk Register «for compliance»

Создан, но не используется. Заполняется раз в год для аудитора, затем игнорируется. Решение — **ритм** обновления (минимум раз в квартал) + использование в operational decisions.

### 7.2 Слишком много KRI

«У нас 100 KRI». Никто не смотрит. Лучше — 10-20 ключевых, обновляемых регулярно.

### 7.3 Three Lines of Defense только на бумаге

Структура есть, но 1-я линия не воспринимает себя owners рисков. Лечение — **тренинги** для operational managers + **измерение** их вклада в ERM.

### 7.4 Внутренний аудит подчинён CEO

Теряет независимость. Должен подчиняться **Audit Committee** Совета Директоров.

### 7.5 Игнорирование «slow boil» рисков

Большие риски (например, постепенное накопление technical debt) трудно оценить, потому что они не «срабатывают» сразу. Лечение — внимание к **trends**, не только к incidents.

## Применение для руководителя

| Целевая роль | Главные применения |
|---|---|
| **CEO** | Risk appetite; tone at the top; quarterly risk reviews |
| **COO** | Daily ownership операционных рисков; KRI monitoring |
| **CRO** | Полная ответственность за ERM-функцию |
| **CFO** | Financial controls; SOX-compliance (если применимо) |
| **Internal Auditor** | Independent assurance; Three Lines coordination |
| **Любой руководитель** | Risk ownership в своей области; KRI для своих процессов |

## Связь с другими модулями

- [[index|Модуль 22: Risk & BC]]
- [[01-ERM-Framework|01 ERM Framework]] — стратегический контекст
- [[03-Business-Continuity|03 Business Continuity]] — реакция на материализованные риски
- [[04-Cybersecurity-for-Leader|04 Cybersecurity]] — кибер как тип operational risk
- [[../21-Legal/04-Compliance|21.04 Compliance]] — compliance risks
- [[../04-Supply-Chain/06-Supply-Chain-Risk|04.06 Supply Chain Risk]] — отраслевой пример

## Источники

### Книги

- COSO, **«Internal Control — Integrated Framework»** (2013) — обязательная для SOX-environments
- IIA, **«The IIA's Three Lines Model»** (2020 update)
- Basel Committee, **«Principles for the Sound Management of Operational Risk»** (2011)
- Lam James, **«Implementing Enterprise Risk Management»** (Wiley, 2014)
- Douglas Hubbard, **«How to Measure Anything»** (Wiley, 3-е изд., 2014) — про количественную оценку рисков

### Регулирующие документы

- Basel III Operational Risk
- COSO Internal Control 2013
- SOX 404 (для американских публичных компаний)
- Положение ЦБ РФ № 716-П (для российских банков)

### Онлайн-ресурсы

- **theiia.org** — Institute of Internal Auditors
- **garp.org** — Global Association of Risk Professionals
- **prmia.org** — Professional Risk Managers' International Association
- **isaca.org** — для IT-related operational risks

### Сертификации

- **CIA** (Certified Internal Auditor, IIA)
- **CRMA** (Certification in Risk Management Assurance, IIA)
- **FRM** (Financial Risk Manager, GARP)
- **PRM** (Professional Risk Manager, PRMIA)
- **CISA** (Certified Information Systems Auditor)
## Связанные документы

- [[index|Модуль 22: Risk & BC]]
- [[../index|Education Index]]
- [[01-ERM-Framework|01 ERM Framework]]
- [[03-Business-Continuity|03 Business Continuity]]
