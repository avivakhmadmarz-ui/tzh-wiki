---
title: "03 — Business Continuity"
aliases: ["BCM", "Business Continuity Management", "ISO 22301", "BIA", "Business Impact Analysis", "RTO", "RPO", "Disaster Recovery", "DR"]
type: note
status: active
domain: education
module: 22-Risk-BC
tags: [education, business-continuity, bcm, iso-22301, bia, rto, rpo, disaster-recovery]
created: 2026-05-26
updated: 2026-05-26
---

# 03 — Business Continuity

> **Business Continuity Management (BCM — управление непрерывностью бизнеса)** — дисциплина обеспечения **продолжения критических операций** компании в условиях нарушений: стихийных бедствий, кибер-атак, пандемий, кадровых катастроф. После COVID-2020 BCM стал **обязательной** компетенцией для executive — те компании, которые имели **планы непрерывности**, выжили; те, кто не имел — потеряли долю рынка или закрылись. Эта заметка систематизирует: международный стандарт ISO 22301, инструмент BIA (Business Impact Analysis), концепции RTO и RPO, различие между Business Continuity и Disaster Recovery.

## Карта раздела

![](attachments/diagrams/22-bcm-bia-rto-rpo.svg)

## 1. Что такое Business Continuity

### 1.1 Определение

**Business Continuity (непрерывность бизнеса)** — способность организации **продолжать предоставлять продукты и услуги** в условиях нарушений на **приемлемом уровне**.

**Business Continuity Management (BCM)** — формальный процесс **планирования, внедрения и поддержания** этой способности.

### 1.2 Зачем нужно

Без BCM компания **уязвима** к:
- **Стихийные бедствия** — землетрясения, пожары, наводнения
- **Технологические сбои** — отказ ЦОДов, кибер-атаки
- **Эпидемии** — COVID-19 показал, насколько компании были не готовы
- **Кадровые катастрофы** — ключевой человек уходит / умирает
- **Сбои в цепи поставок** — критический поставщик закрывается
- **Регуляторные изменения** — внезапные запреты или ограничения
- **Терроризм / военные действия**

Статистика: **40-60% компаний**, перенёсших крупные нарушения **без BCM**, закрываются в течение 5 лет.

### 1.3 Эволюция BCM

**1980-1990-е** — BCM как **disaster recovery** (восстановление после катастрофы). Фокус на IT.

**2000-е** — расширение на бизнес-процессы, не только IT.

**2010-е** — ISO 22301 (2012), формализация международного стандарта.

**2020+** — COVID-19 как **wake-up call**. BCM стал стратегической компетенцией.

## 2. ISO 22301 — международный стандарт

### 2.1 Что это

**ISO 22301:2019** — стандарт **Security and resilience — Business continuity management systems — Requirements**. Главный международный документ для BCM.

Применим к любым организациям независимо от размера и индустрии.

Возможна **сертификация** по ISO 22301 — внешняя проверка, что компания соответствует стандарту.

### 2.2 Структура стандарта

ISO 22301 базируется на **PDCA-цикле** (Plan-Do-Check-Act):

**Plan:**
- Понимание организации и её контекста
- Лидерство и приверженность
- Планирование (включая BIA — см. ниже)
- Поддержка (ресурсы, компетенции, awareness)

**Do:**
- Operation — реализация процедур
- BCP (Business Continuity Plans)
- Тренинги и тесты

**Check:**
- Performance evaluation
- Internal audits
- Management reviews

**Act:**
- Improvement
- Корректирующие действия

### 2.3 Главные требования

1. **Top management commitment** — приверженность высшего руководства
2. **BCM policy** — формальная политика
3. **BCM team** — назначение ответственных
4. **Business Impact Analysis (BIA)** — обязательно
5. **Risk assessment** — оценка рисков для критических процессов
6. **Business Continuity strategies** — стратегии для каждого критического процесса
7. **Business Continuity Plans (BCP)** — план действий
8. **Training and awareness** — тренинги
9. **Testing** — регулярные тесты планов (минимум раз в год)
10. **Reviews** — постоянное улучшение

### 2.4 Сертификация vs соответствие

**Сертификация** ISO 22301:
- Требует внешней аудиторской проверки
- Стоит $20-100K в год (зависит от размера компании)
- Обновляется каждые 3 года
- Полезна для крупных компаний с международными клиентами

**Соответствие без сертификации:**
- Использовать ISO 22301 как **гайд**, не получать сертификат
- Большинство компаний идут этим путём

**Ключевой вывод 1.** ISO 22301 — **золотой стандарт** BCM. Даже без формальной сертификации стоит использовать его структуру для построения внутренних BCM-процессов.

## 3. BIA — Business Impact Analysis

### 3.1 Концепция

![](attachments/diagrams/22-bcm-bia-rto-rpo.svg)

**Business Impact Analysis (BIA — анализ воздействия на бизнес)** — фундаментальный инструмент BCM. Это **анализ**, который отвечает на вопрос:

> «**Что произойдёт с бизнесом, если процесс X остановится** на 1 час / 1 день / 1 неделю / 1 месяц?»

Без BIA невозможно построить осмысленную BCM-программу.

### 3.2 Структура BIA

Для каждого бизнес-процесса:

**1. Описание процесса.**

Кто делает, что делает, для кого, какие inputs и outputs.

**2. Зависимости.**

- **People** — какие сотрудники
- **Systems** — какие IT-системы
- **Suppliers** — какие поставщики
- **Facilities** — какие физические помещения
- **Other processes** — какие другие процессы

**3. Time-criticality.**

- Может ли процесс остановиться на 1 час без последствий?
- На 1 день?
- На 1 неделю?
- На 1 месяц?

**4. Impact analysis.**

При остановке процесса на различные сроки:
- **Financial impact** — потеря выручки
- **Operational impact** — нарушение других процессов
- **Reputational impact** — ущерб бренду
- **Regulatory impact** — нарушение требований
- **Legal impact** — судебные последствия

**5. Recovery requirements.**

- **RTO** (Recovery Time Objective) — см. раздел 4
- **RPO** (Recovery Point Objective) — см. раздел 4
- **MTPD** (Maximum Tolerable Period of Disruption) — макс. допустимый период нарушения

### 3.3 Результат BIA

После BIA каждый бизнес-процесс получает приоритет:

- **Critical** — нельзя остановиться больше чем на несколько часов
- **Important** — может остановиться на 1-2 дня
- **Non-critical** — может остановиться на неделю+

Дальнейшая работа фокусируется на **critical** и **important** процессах.

### 3.4 Пример BIA

**Процесс:** Розничные онлайн-продажи (e-commerce платформа).

- **Зависимости:** платформа Magento + CRM Bitrix + платёжный шлюз + WMS + 3PL логистика
- **Time-criticality:** > 4 часов простой = серьёзные убытки
- **Financial impact (1 час):** $50K потери выручки
- **Financial impact (1 день):** $1.2M
- **Reputational impact:** социальные медиа, негативные отзывы
- **RTO:** 2 часа
- **RPO:** 15 минут

### 3.5 Главные ошибки BIA

- **«Все процессы critical»** — попытка защитить всё одинаково = не защищаешь ничего хорошо
- **Subjective оценки** — без формальной шкалы impact
- **Опрос только IT** — операционные процессы упускаются
- **Не обновляется** — BIA устаревает за 6-12 месяцев

**Ключевой вывод 2.** BIA — **самая важная** часть BCM. Без BIA Business Continuity Plans пишутся **на основе интуиции**, а не данных.

## 4. RTO и RPO — две главные метрики

### 4.1 Recovery Time Objective (RTO)

**RTO** — **максимально допустимое время** восстановления процесса после нарушения.

Примеры RTO:
- Mission-critical: 1-4 часа
- Critical: 4-24 часа
- Important: 1-3 дня
- Non-critical: 3+ дней

RTO определяется бизнесом, не IT. IT обеспечивает технические возможности для достижения RTO.

### 4.2 Recovery Point Objective (RPO)

**RPO** — **максимально допустимая потеря данных** при нарушении, выраженная во времени.

Пример: RPO = 1 час → допустимо потерять данные за последний час.

Зависит от частоты backup'ов:
- **Real-time replication** — RPO ~0 (нет потерь)
- **Incremental backup каждый час** — RPO ~1 час
- **Daily backup** — RPO ~24 часа
- **Weekly backup** — RPO ~1 неделя

### 4.3 Цена снижения RTO / RPO

Снижение RTO / RPO стоит **денег**. Экспоненциальная зависимость:

- **RTO 24 часов** — стандартный backup, restore from tape: дёшево
- **RTO 4 часа** — geographical replication, hot standby: дороже в 5-10 раз
- **RTO 30 минут** — active-active configuration: дороже в 20-50 раз
- **RTO 0** (no downtime) — fully redundant system: очень дорого

Поэтому: устанавливать RTO / RPO нужно **с учётом стоимости** альтернатив. RTO = 30 минут для non-critical процесса — расточительство.

### 4.4 MTPD — Maximum Tolerable Period of Disruption

**MTPD** — максимально допустимый период нарушения, после которого бизнес не сможет восстановиться.

Это **upper bound** для RTO. RTO должен быть **меньше** MTPD.

Пример: e-commerce платформа.
- MTPD: 1 неделя (потом массовый отток клиентов, банкротство)
- RTO: 4 часа (значительно меньше MTPD — большой запас прочности)

## 5. Business Continuity Plans (BCP)

### 5.1 Что это

**Business Continuity Plan (BCP — план непрерывности бизнеса)** — формальный документ, описывающий, **как продолжать критические операции** в условиях нарушения.

### 5.2 Структура BCP

**1. Activation triggers** — когда BCP активируется.

**2. Crisis management team** — кто руководит реагированием.

**3. Communication plan** — кому, что, когда сообщается:
- Employees
- Customers
- Suppliers
- Regulators
- Media

**4. Continuity strategies** — конкретные действия для каждого critical процесса.

**5. Resource requirements** — что нужно (люди, оборудование, помещения).

**6. Recovery procedures** — детальные шаги восстановления.

**7. Roles and responsibilities** — кто что делает.

**8. Contact lists** — телефоны, emails ключевых людей.

**9. Testing schedule** — когда тестируется план.

### 5.3 Типы стратегий BCP

**1. Redundancy (резервирование).**

Дублирование критических ресурсов:
- Резервные ЦОДы
- Несколько поставщиков
- Резервные сотрудники с cross-training

**2. Alternative arrangements (альтернативы).**

Заранее подготовленные альтернативные варианты:
- Альтернативные офисы (для work-from-home или другой локации)
- Альтернативные supplier'ы
- Альтернативные технологические стеки

**3. Manual workarounds (ручные обходы).**

Если автоматизированная система упала — есть ручные процедуры.

**4. Outsourcing (аутсорсинг).**

Передача функций третьим лицам в кризисной ситуации.

### 5.4 Testing BCP

ISO 22301 требует **минимум** раз в год тестировать BCP.

**Типы тестов:**

- **Tabletop exercise** — обсуждение «что если?», без реальных действий. Дешёвый, низкие риски.
- **Walkthrough** — пошаговое следование плану без реального восстановления.
- **Simulation** — имитация события с реальной координацией команд.
- **Full-scale test** — реальный «выключение» с переключением на резерв. Дорого, но даёт реальные данные.

Главное правило: BCP, **не протестированный**, — **не работает**. Тесты выявляют:
- Устаревшие контакты
- Неработающие резервные системы
- Непонятные шаги в плане
- Недостающие ресурсы

**Ключевой вывод 3.** BCP — **живой документ**, требующий постоянной актуализации. Тестирование — **обязательно** минимум раз в год. После каждого реального инцидента — обзор и обновление BCP.

## 6. Disaster Recovery vs Business Continuity

### 6.1 Различие

Часто путают, но это **разные** концепции.

**Disaster Recovery (DR — восстановление после катастрофы)** — **технический** аспект: восстановление **IT-инфраструктуры**.

**Business Continuity (BC)** — **бизнес-аспект**: продолжение **operational процессов**.

DR — **подмножество** BC.

### 6.2 Сравнение

| Аспект | Disaster Recovery | Business Continuity |
|---|---|---|
| **Фокус** | IT systems | Все бизнес-процессы |
| **Главный owner** | CTO / CIO | CEO / COO |
| **Метрики** | RTO, RPO (для IT) | RTO, RPO + financial impact, customer impact |
| **План** | DR Plan | BCP (включает DR) |
| **Тренинги** | IT staff | All employees |

### 6.3 Их сочетание

**Грамотный подход:**
1. **BIA** — определяет critical процессы и их RTO/RPO
2. **BCP** — общая стратегия непрерывности
3. **DR Plan** — техническая часть BCP, посвящённая IT

DR без BC — **наивно** (восстановили IT, но процессы остановились по другим причинам).

BC без DR — **нереалистично** (большинство процессов сегодня зависят от IT).

## 7. BCM — практические аспекты

### 7.1 Crisis Management Team

Кто входит в crisis management team:
- **CEO или COO** — overall leadership
- **CFO** — financial decisions, cash management
- **CIO / CTO** — IT recovery
- **CHRO** — employee management, communications
- **General Counsel** — legal aspects, regulatory
- **CMO / Head of Comms** — external communications
- **Head of Security** — physical security, cyber
- **Operations Heads** — критические процессы

### 7.2 Communication during crisis

Принципы:
- **Speed** — первые часы критичны
- **Accuracy** — не давать неподтверждённую информацию
- **Single source of truth** — один человек / канал отвечает на запросы
- **Layered messages** — внутренние, клиенты, регуляторы, медиа — разные сообщения
- **Update frequency** — регулярные обновления, даже если «нет изменений»

### 7.3 Когда BCP активируется

Критерии активации (определяются в BCP):
- Production downtime > X часов
- Office building inaccessible
- Key system unavailable
- Critical supplier failure
- Pandemic-level event
- Cyber attack with significant impact

### 7.4 После кризиса — Hot Wash / Post-mortem

После закрытия кризиса:
- **Hot wash** — встреча команды в течение 24-48 часов, capturing immediate observations
- **Post-mortem** — формальный анализ через 1-4 недели
- **Lessons learned** — обновление BCP
- **Communication** — отчёт стейкхолдерам

## 8. COVID-19 как кейс BCM

### 8.1 Что показал COVID

COVID-19 был **первым глобальным** BCM-тестом для всех компаний одновременно. Главные уроки:

**Что работало:**
- Готовые планы для пандемии (биотех, healthcare)
- Гибкая IT-инфраструктура (cloud-based)
- Tech-savvy культура (привычка к remote work)
- Diversified supply chains

**Что не работало:**
- BCPs «на бумаге» без реального тестирования
- Один офис, один поставщик, один ЦОД
- Слабая remote work infrastructure
- Отсутствие cash reserves

### 8.2 Главные изменения после COVID

- **Pandemic planning** теперь обязательный сценарий в BCP
- **Remote work capability** — must have, не nice to have
- **Supply chain diversification** — приоритет
- **Cash reserves** — увеличены (90-180 дней vs предыдущие 30-60)
- **Insurance** — большое внимание к business interruption insurance

### 8.3 Российская специфика 2022+

Санкции 2022 года стали **второй wave** BCM-стрессом:
- Уход иностранных вендоров (Cisco, Oracle, SAP)
- Блокировка платёжных систем (Visa, Mastercard)
- Запрет на импорт критических компонентов
- Уход consultancies (McKinsey, BCG, Bain)

Компании, у которых были BCP-планы с санкционным сценарием, **легче перенесли** транзицию.

## Применение для руководителя

| Целевая роль | Главные применения |
|---|---|
| **CEO** | Стратегические решения по BCM; финансирование программы |
| **COO** | Daily ownership BCM; coordination crisis management team |
| **CIO / CTO** | DR portion of BCP; RTO/RPO для IT |
| **CFO** | BIA financial impact; cash reserves; business interruption insurance |
| **CHRO** | Employee communication; pandemic planning; remote work |
| **General Counsel** | Legal aspects of crisis communication; regulatory reporting |

## Связь с другими модулями

- [[index|Модуль 22: Risk & BC]]
- [[01-ERM-Framework|01 ERM Framework]] — BC как часть ERM
- [[02-Operational-Risk|02 Operational Risk]] — predisruption risks
- [[04-Cybersecurity-for-Leader|04 Cybersecurity]] — кибер-инциденты как BCM trigger
- [[../04-Supply-Chain/06-Supply-Chain-Risk|04.06 Supply Chain Risk]] — supply chain continuity

## Источники

### Книги

- ISO 22301:2019 — главный стандарт
- Christopher Lawrence, **«Business Continuity Management»** (Routledge, 2017)
- David Snedaker, **«Business Continuity & Disaster Recovery Planning for IT Professionals»** (Syngress, 2-е изд., 2013)
- Nassim Taleb, **«Antifragile»** (Random House, 2012) — философский контекст

### Стандарты

- **ISO 22301:2019** — Business Continuity Management Systems
- **ISO 22313:2020** — Guidance on the use of ISO 22301
- **NIST SP 800-34** — Contingency Planning Guide (для IT-focused BC)

### Онлайн-ресурсы

- **drii.org** — Disaster Recovery Institute International
- **thebci.org** — Business Continuity Institute
- **drj.com** — Disaster Recovery Journal
- **ready.gov/business** — US government business continuity resources

### Сертификации

- **CBCP** (Certified Business Continuity Professional, DRII)
- **MBCI** (Member of the Business Continuity Institute)
- **CISM** (Certified Information Security Manager, ISACA) — с BC компонентом
- **CISSP** (Certified Information Systems Security Professional) — с BC компонентом
## Связанные документы

- [[index|Модуль 22: Risk & BC]]
- [[../index|Education Index]]
- [[01-ERM-Framework|01 ERM Framework]]
- [[04-Cybersecurity-for-Leader|04 Cybersecurity]]
