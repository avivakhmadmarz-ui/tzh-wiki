---
title: "01 — Enterprise Risk Management (ERM)"
aliases: ["ERM", "Enterprise Risk Management", "COSO ERM", "ISO 31000", "Risk Appetite", "Risk Tolerance", "Heat Map", "Taleb"]
type: note
status: active
domain: education
module: 22-Risk-BC
tags: [education, risk-management, erm, coso, iso-31000, risk-appetite, heat-map, taleb]
created: 2026-05-26
updated: 2026-05-26
---

# 01 — Enterprise Risk Management (ERM)

> **Enterprise Risk Management (ERM — управление рисками предприятия)** — целостный подход к управлению **всеми** рисками компании. До 2000-х годов компании управляли рисками **изолированно** (финансовый риск отдельно от операционного, кибер от регуляторного). ERM объединяет их в **единую систему**, связанную со стратегией. Главные стандарты — **COSO ERM Framework 2017** и **ISO 31000:2018**. Эта заметка систематизирует обе модели, концепцию **risk appetite vs tolerance**, инструмент **heat map**, и философский противовес — **antifragility** (Nassim Taleb).

## Карта раздела

![](attachments/diagrams/22-module-map.svg)

## 1. Что такое риск-менеджмент

### 1.1 Определения

**Риск** — возможность отклонения от ожидаемого результата. Может быть и **negative** (вероятность убытка), и **positive** (вероятность выгоды).

**Risk Management (управление рисками)** — процесс **выявления, оценки и реагирования** на риски.

**Enterprise Risk Management (ERM)** — **целостный** подход, охватывающий **все категории** рисков и связанный со **стратегией** компании.

### 1.2 Эволюция риск-менеджмента

**Этап 1 — Изолированный (до 1990-х).**

Каждая функция управляет своими рисками:
- Финансовый директор — финансовыми
- Юрист — юридическими
- Операционный — операционными
- Безопасность — физическими

Проблема: **slipovye» зоны** между функциями. Например, кибер-инцидент имеет финансовый, репутационный, операционный, юридический компоненты — но никто не управляет им целостно.

**Этап 2 — Integrated (1990-2000-е).**

Появление концепции ERM. Создание роли **Chief Risk Officer (CRO)**, координирующей риск-функции.

**Этап 3 — Strategic (2010-е и далее).**

ERM **интегрирован со стратегией**. Риск рассматривается не только как угроза, но и как **источник** конкурентного преимущества (компания, принимающая больше осознанного риска, может расти быстрее).

### 1.3 Категории рисков

Стандартная категоризация:

**Strategic Risks** (стратегические):
- Изменение рынка
- Action конкурентов
- Изменение технологий
- Изменение регулирования

**Operational Risks** (операционные):
- Сбой процессов
- Ошибки персонала
- Сбой систем
- Внешние события (катастрофы, кризисы)

**Financial Risks** (финансовые):
- Кредитный риск
- Рыночный (валюта, процент)
- Ликвидности
- Налоговый

**Compliance Risks** (соблюдение):
- Регуляторные нарушения (см. [[../21-Legal/04-Compliance|21.04 Compliance]])
- Юридические споры
- Этические нарушения

**Reputational Risks** (репутационные):
- Скандалы
- Социальные медиа кризисы
- Этические проблемы

**Strategic vs Tactical** — стратегические риски угрожают **самому существованию** компании; тактические — отдельным операциям.

## 2. COSO ERM Framework 2017

### 2.1 История

**COSO (Committee of Sponsoring Organizations of the Treadway Commission)** — частная инициатива, основанная в 1985 году для разработки стандартов внутреннего контроля.

В 2004 году COSO опубликовала первую версию ERM Framework.

В 2017 году — обновлённая версия **«Enterprise Risk Management — Integrating with Strategy and Performance»**. Главное обновление — **интеграция со стратегией**.

### 2.2 5 компонентов COSO ERM 2017

![](attachments/diagrams/22-coso-erm-cube.svg)

**1. Governance & Culture** (Управление и культура).

- Risk oversight (надзор) со стороны Совета Директоров
- Operating structures (структуры)
- Defining desired culture (культура)
- Demonstrated commitment (приверженность)
- Attracting / developing / retaining people

**2. Strategy & Objective-Setting** (Стратегия и постановка целей).

- Risks embedded in strategy
- Risk appetite definition
- Business objectives и связь с риском
- Evaluating alternative strategies

**3. Performance** (Исполнение).

- Identifying risks
- Assessing severity
- Prioritizing risks
- Implementing responses
- Developing portfolio view

**4. Review & Revision** (Обзор и пересмотр).

- Substantial change assessment
- Reviewing risk and performance
- Pursuing improvement

**5. Information, Communication & Reporting** (Информация, коммуникация, отчётность).

- Information systems
- Communicating risk information
- Reporting on risk, culture, performance

### 2.3 Главное послание COSO 2017

ERM — **не отдельный процесс**, а **интегральная часть** стратегии и operational management. Главный сдвиг — **от контроля рисков к интеграции с принятием решений**.

**Ключевой вывод 1.** COSO ERM — **управленческий фреймворк**, применимый ко всем индустриям. Главное преимущество — целостный взгляд на все категории рисков через единую модель.

## 3. ISO 31000:2018

### 3.1 Что это

**ISO 31000:2018** — международный стандарт «Risk management — Guidelines» (Управление рисками — Руководящие указания).

В отличие от COSO ERM (американская инициатива), ISO 31000 — **глобальный стандарт**.

### 3.2 Главные принципы (8 принципов)

1. **Integrated** — управление рисками интегрировано во все организационные деятельности
2. **Structured and comprehensive** — структурированный и всеобъемлющий подход
3. **Customized** — подходит под контекст организации
4. **Inclusive** — вовлечение стейкхолдеров
5. **Dynamic** — адаптивный к изменениям
6. **Best available information** — использование лучшей доступной информации
7. **Human and cultural factors** — учёт человеческого и культурного факторов
8. **Continual improvement** — непрерывное улучшение

### 3.3 Process в ISO 31000

Цикличный процесс из 5 шагов:

1. **Communication and consultation** — общение со стейкхолдерами
2. **Scope, context, criteria** — определение масштаба
3. **Risk assessment** — оценка рисков:
   - Risk identification
   - Risk analysis
   - Risk evaluation
4. **Risk treatment** — обработка рисков
5. **Monitoring and review** — мониторинг

### 3.4 COSO vs ISO

| Аспект | COSO ERM 2017 | ISO 31000:2018 |
|---|---|---|
| **Происхождение** | США, частная инициатива | Международный стандарт |
| **Фокус** | Связь со стратегией и performance | Универсальный подход к управлению рисками |
| **Применимость** | Бизнес (особенно публичные компании) | Любая организация |
| **Уровень детализации** | Высокий | Средний (принципы) |
| **Сертификация** | Нет формальной | ISO certification possible |
| **Где доминирует** | США, крупные корпорации | Европа, государственный сектор |

Большинство **зрелых компаний** используют **оба** — COSO для интеграции с финансовой отчётностью (SOX-compliance в США), ISO 31000 для общего подхода.

**Ключевой вывод 2.** COSO и ISO 31000 — **комплементарные**, не конкурирующие фреймворки. Выбор зависит от регуляторного контекста и масштаба компании.

## 4. Risk Appetite vs Risk Tolerance

### 4.1 Определения

**Risk Appetite (риск-аппетит)** — **сколько риска** компания **готова принять** для достижения своих стратегических целей.

**Risk Tolerance (риск-толерантность)** — **допустимые отклонения** от ожидаемых результатов в конкретных областях.

Аналогия: **risk appetite — это "стиль жизни"** (агрессивный / умеренный / консервативный); **risk tolerance — это "конкретные границы"** (могу пройти 10 км в день, не больше).

### 4.2 Примеры

**Risk Appetite — высокого уровня:**

> «Наша компания принимает высокий уровень риска для роста выручки, но низкий уровень риска в области комплаенса и репутации».

**Risk Tolerance — конкретного:**

- Volatility EBITDA: не более ±15% от плана за квартал
- Customer attrition: не более 5% годовых
- Information security incidents: не более 1 в год категории P1
- Compliance violations: 0 нарушений (zero tolerance)

### 4.3 Зачем нужны

- **Стратегические решения** — какие проекты принимать? (high-risk, high-reward vs low-risk, low-reward)
- **Operational decisions** — какие тропические операции допустимы?
- **Compliance decisions** — какие нарушения absolute non-tolerable?
- **Reporting** — когда нужна эскалация? (превышение tolerance)

### 4.4 Как формулировать

**Top-down:**
1. **Совет Директоров** утверждает общий risk appetite (1-2 страницы)
2. **CEO + executive team** переводит в risk tolerances по областям
3. **Operational managers** применяют tolerances в daily decisions

Главное правило: **risk appetite пишется не abstractly, а с конкретными KPI**. «Умеренный риск» ничего не значит, «волатильность EBITDA до 15%» — operational metric.

### 4.5 Российская специфика

В крупных российских компаниях (Сбер, Газпром, Роснефть) risk appetite формализован. В среднем бизнесе — часто отсутствует, заменяется «интуицией» CEO.

Это **зона роста** для российского риск-менеджмента.

## 5. Heat Map — главный визуальный инструмент

### 5.1 Что это

![](attachments/diagrams/22-risk-heat-map.svg)

**Heat Map (тепловая карта)** — матрица **likelihood × impact**:

- **Likelihood (вероятность)** — насколько вероятно событие? (low / medium / high)
- **Impact (влияние)** — насколько серьёзны последствия? (low / medium / high)

Каждый риск помещается в одну из 9 ячеек.

### 5.2 Стратегии по ячейкам

| | Low Impact | Medium Impact | High Impact |
|---|---|---|---|
| **High Likelihood** | Accept / Monitor | Mitigate / Insure | Avoid / Mitigate urgent |
| **Medium Likelihood** | Accept | Mitigate / Monitor | Mitigate / Transfer |
| **Low Likelihood** | Accept | Accept / Monitor | Transfer / Contingency plan |

4 стратегии реагирования на риск (4 T's):
1. **Treat / Mitigate** — снизить риск
2. **Transfer** — передать (insurance, hedging)
3. **Tolerate / Accept** — принять
4. **Terminate / Avoid** — избежать

### 5.3 Размерность heat map

Обычная heat map — 3×3 или 5×5. Для крупных компаний — 5×5 (более детальная).

Для каждого риска оценивается:
- **Inherent risk** — внутренний риск (без контролей)
- **Residual risk** — остаточный риск (после контролей)

Цель — снизить residual risk до приемлемого уровня.

### 5.4 Главные ошибки

- **Subjective ratings** — оценки likelihood / impact без чёткой шкалы. Лечение: формальные критерии (например, impact: low <$100K, medium $100K-$1M, high >$1M)
- **Только negative risks** — heat map обычно для downside risks. Upside risks (opportunities) часто упускаются
- **Не обновляется** — heat map made one quarter, used for years
- **Не связана с действиями** — heat map есть, но что с ней делать?

**Ключевой вывод 3.** Heat map — **базовый** visual инструмент ERM. Прост в применении, но требует **дисциплины обновления** (минимум раз в квартал) и **формальных критериев** likelihood / impact.

## 6. Antifragility — Nassim Taleb

### 6.1 Концепция

**Nassim Nicholas Taleb** — статистик, автор книг **«The Black Swan»** (2007), **«Antifragile»** (2012). Его подход — **философский противовес** классическому ERM.

Главная идея: классический риск-менеджмент **управляет известными рисками**. Но самые большие потери происходят от **неизвестных рисков** (Black Swans — чёрные лебеди) — событий, которые мы **не могли предсказать**.

### 6.2 Fragility — Robustness — Antifragility

Taleb разделяет три состояния:

**Fragile (хрупкое)** — ломается при стрессе. Пример: банк с высоким leverage в кризисе.

**Robust (прочное)** — выдерживает стресс. Пример: компания с большой денежной подушкой.

**Antifragile (антихрупкое)** — **усиливается** от стресса. Пример: венчурный фонд, инвестирующий в стартапы, — большинство fails, но единичные exits обеспечивают огромную доходность.

### 6.3 Свойства antifragile systems

- **Optionality** — наличие опций для разных сценариев
- **Skin in the game** — те, кто принимают решения, несут последствия
- **Distributed risk** — много малых ставок вместо одной крупной
- **Convex payoffs** — потенциальный upside больше потенциального downside
- **Stoicism** — готовность переживать стрессы

### 6.4 Применение в бизнесе

Antifragile-стратегии:

- **Barbell strategy** — комбинация консервативных (80-90%) и **очень рискованных** (10-20%) элементов
- **Optionality** — поддержка нескольких возможных направлений развития
- **Distributed manufacturing** — несколько производственных площадок вместо одной крупной
- **Multiple suppliers** — diversification вместо single source
- **Cash reserves** — возможность купить активы во время кризиса

### 6.5 Критика и применение

Taleb критикует классический ERM:
- **VaR (Value at Risk)** — не работает для редких событий
- **Normal distribution** — недооценка хвостовых рисков
- **Historical data** — будущее не похоже на прошлое

Современный консенсус — **гибрид**: COSO/ISO для daily управления + Taleb mindset для **strategic resilience**.

**Ключевой вывод 4.** Antifragility — **не методология**, а **способ мышления** о рисках. Дополняет, не заменяет ERM. Особо ценен в условиях высокой неопределённости (2020 COVID, 2022 санкции).

## 7. ERM Framework — практическое внедрение

### 7.1 Этапы построения ERM

**Этап 1 — Foundation (3-6 месяцев).**
- Назначить CRO (Chief Risk Officer) или ответственного
- Сформулировать risk appetite на высоком уровне
- Создать risk register (см. [[02-Operational-Risk|02 Operational Risk]])
- Базовая heat map

**Этап 2 — Integration (6-12 месяцев).**
- Интеграция риск-оценки в стратегическое планирование
- Risk-based audit planning
- Включение риск-метрик в operational reports

**Этап 3 — Maturity (12-24 месяцев).**
- ERM как часть всех major decisions
- Continuous monitoring через KRI (key risk indicators)
- Risk-adjusted performance metrics (RAROC и т.п.)

**Этап 4 — Excellence (24+ месяцев).**
- Predictive risk analytics
- Scenario planning
- Antifragility-стратегии

### 7.2 Размер ERM-функции

| Размер компании | ERM команда |
|---|---|
| <500 чел. | Совмещение с финансами / compliance |
| 500-2000 чел. | 1-3 risk специалистов + CRO |
| 2000-10000 чел. | 5-15 человек, CRO + категориальные специалисты |
| 10000+ чел. | 20-100+ человек, full risk function |
| Финансовый сектор (банки, страховщики) | 5-15% штата (regulatory requirement) |

### 7.3 Российский контекст

В России формальный ERM активно развивается с 2010-х. Лидеры:
- Банки (под регулированием ЦБ РФ)
- Крупные публичные компании (Газпром, Роснефть)
- Иностранные дочки (под требованиями материнской компании)

Средний российский бизнес часто без формального ERM, заменяет интуицией CEO.

## Применение для руководителя

| Целевая роль | Главные применения |
|---|---|
| **CEO** | Risk appetite на высоком уровне; интеграция с стратегией |
| **CFO** | Финансовые риски; investment decisions с учётом риска |
| **CRO (Chief Risk Officer)** | Полная ответственность за ERM |
| **COO** | Operational risks; daily управление через KRI |
| **Совет Директоров** | Risk oversight; approval risk appetite |
| **Internal Auditor** | Аудит эффективности ERM |

## Связь с другими модулями

- [[index|Модуль 22: Risk & BC]]
- [[02-Operational-Risk|02 Operational Risk]] — следующий уровень детализации
- [[03-Business-Continuity|03 Business Continuity]] — реакция на материализованные риски
- [[04-Cybersecurity-for-Leader|04 Cybersecurity]] — киберриски как часть ERM
- [[../21-Legal/04-Compliance|21.04 Compliance]] — compliance как часть risk management
- [[../17-Goal-Setting/index|Модуль 17: Goal Setting]] — risk в постановке целей
- [[../04-Supply-Chain/06-Supply-Chain-Risk|04.06 Supply Chain Risk]] — отраслевой пример

## Источники

### Книги

- COSO, **«Enterprise Risk Management — Integrating with Strategy and Performance»** (2017) — обязательная
- ISO, **ISO 31000:2018 «Risk management — Guidelines»**
- Nassim Nicholas Taleb, **«Antifragile: Things That Gain from Disorder»** («Антихрупкость», Random House, 2012)
- Nassim Nicholas Taleb, **«The Black Swan»** («Чёрный лебедь», Random House, 2007)
- John Fraser, Betty Simkins, **«Enterprise Risk Management»** (Wiley, 2010) — практическое руководство
- James Lam, **«Enterprise Risk Management: From Incentives to Controls»** (Wiley, 2-е изд., 2014)
- Douglas Hubbard, **«The Failure of Risk Management»** (Wiley, 2009) — критика классического подхода

### Регулирующие документы

- COSO ERM Framework 2017
- ISO 31000:2018
- Basel III (для банков)
- Solvency II (для страховщиков)
- Положение ЦБ РФ о risk management в банках

### Онлайн-ресурсы

- **coso.org** — COSO Committee
- **iso.org** — ISO standards
- **rims.org** — Risk and Insurance Management Society
- **theirm.org** — Institute of Risk Management

### Сертификации

- **CRMA** (Certification in Risk Management Assurance, IIA)
- **PRM** (Professional Risk Manager, PRMIA)
- **FRM** (Financial Risk Manager, GARP)
- **CRMP** (Certified Risk Management Professional)
## Связанные документы

- [[index|Модуль 22: Risk & BC]]
- [[../index|Education Index]]
- [[02-Operational-Risk|02 Operational Risk]]
- [[../21-Legal/04-Compliance|21.04 Compliance]]
