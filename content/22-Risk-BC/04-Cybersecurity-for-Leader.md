---
title: "04 — Cybersecurity для руководителя"
aliases: ["Cybersecurity", "NIST CSF", "NIST Cybersecurity Framework", "Ransomware", "Supply Chain Attacks", "Phishing", "Cyber Risk"]
type: note
status: active
domain: education
module: 22-Risk-BC
tags: [education, cybersecurity, nist-csf, ransomware, supply-chain-attacks, phishing, cyber-risk]
created: 2026-05-26
updated: 2026-05-26
---

# 04 — Cybersecurity для руководителя

> Кибербезопасность перестала быть **технической дисциплиной IT** — сегодня это **стратегический риск executive-уровня**. Ransomware-атаки парализуют крупные компании на недели (Colonial Pipeline 2021), supply chain атаки компрометируют тысячи организаций сразу (SolarWinds 2020), штрафы за утечки достигают сотен миллионов (Meta €1.2B в 2023). Эта заметка — для руководителя, не для IT-специалиста: что должен знать CEO / COO / CFO про **NIST Cybersecurity Framework** как стандартную модель, главные угрозы (ransomware, supply chain attacks, phishing, DDoS), и как организовать кибербезопасность на executive-уровне.

## Карта раздела

![](attachments/diagrams/22-nist-csf.svg)

## 1. Зачем executive должен понимать cybersecurity

### 1.1 Эволюция угрозы

**До 2010-х:** кибератаки — нечастые, в основном теоретические для большинства компаний. Cybersecurity — внутренняя функция IT.

**2010-2020:** растущая частота и серьёзность атак. Крупные взломы (Target 2013, Equifax 2017, Yahoo 2014). Cybersecurity начинает выходить на executive level.

**2020+:** массовые ransomware-атаки на критическую инфраструктуру (Colonial Pipeline, JBS Foods, Kaseya). Cybersecurity — **обязательная** компетенция CEO. Регуляторы (SEC, EU, Россия) требуют raportировать инциденты.

### 1.2 Главные drivers

- **Профессионализация атакующих** — кибератака стала отдельной индустрией с разделением труда (initial access brokers, ransomware-as-a-service)
- **Геополитика** — спонсируемые государствами группы (Россия, Китай, КНДР, Иран)
- **Криптовалюты** — позволили монетизировать ransomware (анонимные выплаты)
- **Cloud / Remote work** — увеличили attack surface (поверхность атаки)
- **Supply chain complexity** — компании зависят от тысяч поставщиков, каждый — потенциальный вектор атаки

### 1.3 Финансовый impact

По IBM Cost of a Data Breach Report 2023:

- **Средняя стоимость утечки** — $4.45M
- **Healthcare** — самая дорогая индустрия ($10.93M)
- **Time to identify and contain** — 277 дней (в среднем)
- **Mega breaches** (>50M записей) — $332M в среднем

Это **прямые** затраты. С учётом репутации, потери клиентов, регуляторных штрафов — реальная цена в **2-3 раза** выше.

### 1.4 Регуляторный контекст

Растущие требования:

- **GDPR (ЕС)** — обязательное уведомление об утечках в 72 часа
- **152-ФЗ (РФ)** — требования к защите персональных данных
- **187-ФЗ (РФ)** — «О безопасности критической информационной инфраструктуры» (2017)
- **ФСТЭК, ФСБ требования** для отдельных категорий компаний
- **SEC Cybersecurity Disclosure Rules (США, 2023)** — обязательное раскрытие инцидентов

**Ключевой вывод 1.** Cybersecurity — не «IT-проблема», а **executive-уровень риск**. CEO, не понимающий cyber risk, делает свою компанию **уязвимой** в условиях растущих угроз.

## 2. NIST Cybersecurity Framework (NIST CSF)

### 2.1 Что это

**NIST CSF (National Institute of Standards and Technology Cybersecurity Framework)** — **самый распространённый** в мире фреймворк cybersecurity. Разработан американским институтом NIST в 2014 году (версия 1.0), обновлён в 2018 (1.1) и 2024 (2.0).

Главное преимущество — **доступность для не-технических руководителей**. Структурирует кибербезопасность через **функции**, понятные executive.

### 2.2 6 функций NIST CSF 2.0

![](attachments/diagrams/22-nist-csf.svg)

В версии 2.0 (2024 год) добавлена функция Govern. Теперь 6 функций:

**1. Govern (NEW в 2.0).**

Стратегия, рисковый менеджмент, roles & responsibilities на уровне всей компании.

- Organizational context
- Risk management strategy
- Roles, responsibilities, authorities
- Policy
- Oversight
- Supply chain risk management

**2. Identify.**

Понимание **что у нас есть** и **что нужно защитить**:
- Asset management
- Business environment
- Governance (теперь в Govern)
- Risk assessment
- Risk management strategy
- Supply chain risk management

**3. Protect.**

Принятие мер защиты:
- Identity management & access control
- Awareness & training
- Data security
- Information protection processes
- Maintenance
- Protective technology

**4. Detect.**

Обнаружение событий безопасности:
- Anomalies & events
- Continuous monitoring
- Detection processes

**5. Respond.**

Реагирование на инциденты:
- Response planning
- Communications
- Analysis
- Mitigation
- Improvements

**6. Recover.**

Восстановление после инцидента:
- Recovery planning
- Improvements
- Communications

### 2.3 Tiers — уровни зрелости

NIST CSF также определяет **4 уровня зрелости**:

1. **Partial** — кибербезопасность ad hoc, реактивная
2. **Risk Informed** — есть процессы, но не систематические
3. **Repeatable** — формальные процессы, регулярно применяемые
4. **Adaptive** — continuous improvement, integration with business

Большинство средних компаний — Tier 1-2. Зрелые — Tier 3-4.

### 2.4 Profiles — целевое состояние

**Current Profile** — где мы сейчас.

**Target Profile** — где хотим быть.

**Gap analysis** — что нужно сделать для перехода.

Это даёт **roadmap** для cybersecurity-программы.

### 2.5 Применение NIST CSF в РФ

Хотя NIST — американский институт, фреймворк **универсально применим**:

- Российские компании с международными операциями
- Дочки иностранных компаний
- Российские компании, ищущие международные стандарты

Альтернативные стандарты:
- **ISO/IEC 27001** — европейский / международный
- **CIS Controls** — практический набор контролей
- **MITRE ATT&CK** — knowledge base атак

В российском государственном секторе действуют **собственные** требования ФСТЭК и ФСБ.

**Ключевой вывод 2.** NIST CSF — **лучшая стартовая точка** для executive. Структурирует cybersecurity через понятные функции (Govern, Identify, Protect, Detect, Respond, Recover) и даёт roadmap maturity.

## 3. Главные угрозы для retail / e-commerce

### 3.1 Ransomware

![](attachments/diagrams/22-cyber-threats.svg)

**Ransomware** — вредоносный программ, **шифрующий данные** и требующий выкуп за расшифровку.

**Типичный сценарий:**
1. Initial access — обычно через phishing email или уязвимость VPN
2. Lateral movement — атакующий распространяется по сети
3. Privilege escalation — получает admin-доступ
4. Data exfiltration — копирует данные
5. Encryption — шифрует системы
6. Ransom demand — обычно $1M-$50M

**Double extortion (двойной шантаж)** — современная техника:
- Если не платите за расшифровку — публикуем украденные данные

**Triple extortion (тройной шантаж)** — продолжение:
- Атакуем клиентов / поставщиков жертвы

### 3.2 Кейсы крупного ransomware

- **Colonial Pipeline (2021)** — US oil pipeline shut down for 6 days, $4.4M ransom paid
- **JBS Foods (2021)** — крупнейший producer мяса, $11M ransom
- **Kaseya (2021)** — supply chain атака, поразила 1000+ компаний-клиентов
- **MOVEit (2023)** — file transfer software, ~2000 компаний скомпрометированы

### 3.3 Защита от ransomware

**Базовая гигиена:**
- **Patching** — регулярное обновление систем
- **Email filtering** — блокировка phishing
- **Endpoint detection** — обнаружение malware на компьютерах
- **Network segmentation** — изоляция критических систем
- **Privileged access management** — ограничение admin-прав

**Backup strategy:**
- **3-2-1 rule** — 3 копии данных, 2 разных носителя, 1 offsite
- **Immutable backups** — backups, которые нельзя изменить
- **Test restores** — регулярные тесты восстановления

**Incident response:**
- Подготовленный план
- Отдельные коммуникационные каналы (не email, который может быть скомпрометирован)
- Контакты с правоохранительными органами
- Контакты с страховщиком (cyber insurance)

### 3.4 Платить ли выкуп?

**Аргументы против:**
- Стимулирует следующие атаки
- Нет гарантии получения decryption key
- Регуляторные риски (платежи могут быть санкционными)
- Reputational damage

**Аргументы за:**
- Если без выкупа — банкротство
- Decryption быстрее, чем восстановление из backups

В целом — **не платить** при наличии хороших backups. Это решение **executive-уровня**, не IT.

### 3.5 Supply Chain Attacks

**Supply chain attack** — атака **через поставщика** для доступа к жертве. Очень опасны, потому что:
- Компания не контролирует security партнёров
- Может затронуть **тысячи компаний** одновременно

**Знаковые кейсы:**
- **SolarWinds (2020)** — backdoor в legitimate software update, ~18000 компаний скомпрометировано (включая US правительство)
- **Kaseya (2021)** — managed services provider, ransomware распространился через update
- **MOVEit (2023)** — file transfer software

**Защита:**
- **Vendor risk assessment** — оценка cybersecurity поставщиков перед onboarding
- **Continuous monitoring** — отслеживание изменений у ключевых поставщиков
- **Contract clauses** — security requirements в договорах
- **Limit access** — минимум прав для поставщиков

### 3.6 Phishing и BEC

**Phishing** — фейковые emails / сообщения, чтобы получить credentials.

**BEC (Business Email Compromise)** — фейковые emails якобы от руководства / поставщиков для:
- Перевода денег на счета атакующих
- Получения чувствительной информации

По FBI данным, BEC — **№1 по убыткам** среди cyber crimes ($2.7B в 2022 году).

**Защита:**
- **Awareness training** — регулярные тренинги
- **Email authentication** — DKIM, SPF, DMARC
- **Multi-factor authentication** — на всех критических системах
- **Out-of-band verification** — для финансовых операций (звонок руководителю, не только email)

### 3.7 Другие критические угрозы

**DDoS (Distributed Denial of Service)** — отказ в обслуживании из-за переполнения трафика. Угроза для e-commerce в высокие сезоны.

**Account Takeover (ATO)** — компрометация клиентских или admin-аккаунтов через украденные credentials. Особенно опасно для retail.

**API Abuse** — атаки на web API. Современные приложения зависят от API, любая слабость — вектор.

**Insider Threat** — атаки **изнутри**, от сотрудников. Намеренные (саботаж) или случайные (mishandling).

**Zero-day exploits** — атаки на уязвимости **до их обнаружения**. Защита почти невозможна, кроме defense-in-depth.

**Ключевой вывод 3.** Top-3 угрозы для большинства бизнесов: **ransomware, supply chain attacks, phishing/BEC**. Совокупно они отвечают за 70-80% серьёзных инцидентов.

## 4. Cybersecurity organisation

### 4.1 CISO — Chief Information Security Officer

**CISO** — топ-руководитель, ответственный за cybersecurity. В крупных компаниях — отдельная позиция, в небольших — может совмещаться с CIO / IT Director.

**Обязанности:**
- Стратегия cybersecurity
- Соответствие регуляторным требованиям
- Управление командой security
- Reporting в Совет Директоров

**Reporting line — спорный вопрос:**
- **CIO** — традиционно, но создаёт конфликт интересов (security vs. delivery)
- **CEO** — лучше для независимости
- **CRO** — security как часть risk management
- **General Counsel** — для регулируемых индустрий

### 4.2 Security team structure

В зрелой компании:

**Strategic level:**
- CISO + Deputy CISO
- Security Architects
- Risk & Compliance Lead

**Operational level:**
- **SOC (Security Operations Center)** — мониторинг 24/7
- **Incident Response Team** — реагирование на инциденты
- **Vulnerability Management** — patches and scans
- **Identity & Access Management** — управление доступом
- **Application Security** — secure coding, code review
- **Data Protection** — privacy, encryption
- **Awareness & Training** — обучение

### 4.3 Размер team

| Размер компании | Security team |
|---|---|
| <100 чел. | 0-1 (часто outsource) |
| 100-500 | 2-5 |
| 500-2000 | 5-15 |
| 2000-10000 | 15-50 |
| 10000+ | 50-500+ |

Финансовые компании и критическая инфраструктура — обычно **в 2-3 раза больше** норм.

### 4.4 Cybersecurity budget

Эмпирическое правило:
- **5-10% от IT budget** — норма для большинства индустрий
- **15-25% от IT budget** — для финансовых, healthcare, регулируемых
- **<5% от IT budget** — недостаточно для современных угроз

### 4.5 Внешние партнёры

Зрелая security-функция использует внешних партнёров:
- **MSSP (Managed Security Service Providers)** — outsourced SOC
- **Pen testers** — проникающее тестирование
- **Incident response retainers** — premium support при инцидентах
- **Threat intelligence vendors** — данные о текущих угрозах
- **Cyber insurance** — финансовая защита

## 5. Cyber Insurance

### 5.1 Что это

**Cyber Insurance** — страхование от cybersecurity-инцидентов.

Покрытие может включать:
- **First-party coverage** — собственные убытки компании (data restoration, business interruption, ransom payments)
- **Third-party coverage** — иски от affected сторон
- **Forensic services** — расследование инцидента
- **PR / communication** — стоимость crisis management
- **Regulatory fines** — штрафы (где разрешено покрытие)
- **Legal defense** — стоимость юридической защиты

### 5.2 Рынок и тренды

С 2020-2023 годов рынок cyber insurance:
- **Стоимость премий выросла** в 2-5 раз
- **Ограничения покрытия** — многие исключения (war exclusions, ransomware sublimits)
- **Жёсткие требования** — для получения insurance нужно соответствовать минимальным security standards
- **Российский рынок** — ограничен из-за санкций; крупные международные insurers ушли

### 5.3 Что нужно для получения

Современные insurance carriers требуют:
- **Multi-factor authentication** — везде
- **Endpoint detection & response (EDR)** — на всех endpoints
- **Backup strategy** — с immutable copies
- **Incident response plan** — задокументированный
- **Awareness training** — регулярный
- **Patching cadence** — критические patches в течение 30 дней

Без этих контролей **получить insurance крайне сложно**.

## 6. Executive responsibilities

### 6.1 CEO responsibilities

- **Tone at the top** — публичная поддержка cybersecurity
- **Risk appetite** — определение, сколько cyber risk принимаем
- **Resource allocation** — budget и people для cybersecurity
- **Crisis management leadership** — лично руководит во время крупных инцидентов
- **Stakeholder communication** — Совет, регуляторы, медиа

### 6.2 CFO responsibilities

- **Cyber insurance** decisions
- **Investment in security** — обоснованный budget
- **Financial impact assessment** — что мы потеряем при разных сценариях
- **Reporting** — финансовые последствия инцидентов

### 6.3 General Counsel responsibilities

- **Regulatory compliance** — соответствие GDPR, 152-ФЗ, и т.п.
- **Incident notification** — кому, когда, что сообщать
- **Legal privilege** — защита communications во время investigations
- **Vendor contracts** — security clauses

### 6.4 Board responsibilities

- **Oversight** — регулярные обзоры cybersecurity (минимум раз в квартал)
- **Approval** — стратегии, budgets, major changes
- **Director and Officer (D&O) liability** — растущая ответственность за cyber

### 6.5 Личная ответственность руководителей

Растёт регуляторно:
- **SEC (США)** — обязательное disclosure инцидентов
- **EU NIS2 Directive** — личная ответственность executives для критических индустрий
- **Russia** — ответственность по 187-ФЗ для критической информационной инфраструктуры

**Ключевой вывод 4.** Cybersecurity — **обязательная** executive-компетенция. CEO, который не понимает basics, **личнo** уязвим к ответственности при крупном инциденте.

## 7. Что должен знать каждый сотрудник

### 7.1 Basic hygiene

- **Не кликать** на подозрительные ссылки в email
- **Не открывать** вложения из unknown sources
- **Сообщать** о подозрительных emails в security team
- **Использовать** strong passwords + MFA
- **Не оставлять** компьютер unlocked
- **Не подключать** USB sticks из неизвестных источников
- **Соблюдать** clean desk policy

### 7.2 Awareness training

Лучшие практики:
- **Минимум раз в год** — обязательный тренинг для всех
- **Phishing simulations** — регулярные имитации
- **Specific training** для high-risk roles (finance, HR, executives)
- **Onboarding** — security как часть orientation

### 7.3 Reporting culture

Главное — **создать культуру**, где сотрудники **не боятся** сообщать об инцидентах:
- **Анонимные каналы** для сообщений
- **No-blame culture** для случайных ошибок
- **Quick response** на сообщения

Если сотрудник кликнул на phishing и сразу сообщил — **incident contained**. Если боится сообщить — **ransomware распространяется**.

## Применение для руководителя

| Целевая роль | Главные применения |
|---|---|
| **CEO** | Cyber risk на executive level; resource allocation; crisis leadership |
| **CFO** | Cyber insurance decisions; financial impact assessment; budget |
| **CIO / CTO** | Технические аспекты NIST CSF; IT security |
| **CISO** | Полная ownership cybersecurity function |
| **CHRO** | Awareness training programs; culture of security |
| **General Counsel** | Regulatory compliance; incident notification |
| **Совет Директоров** | Oversight; quarterly reviews; D&O liability |

## Связь с другими модулями

- [[index|Модуль 22: Risk & BC]]
- [[01-ERM-Framework|01 ERM Framework]] — cyber как часть ERM
- [[02-Operational-Risk|02 Operational Risk]] — cyber как тип operational risk
- [[03-Business-Continuity|03 Business Continuity]] — cyber incidents trigger BCM
- [[../21-Legal/04-Compliance|21.04 Compliance]] — GDPR, 152-ФЗ, 187-ФЗ
- [[../12-ERP-Digital/index|Модуль 12: ERP & Digital]] — security в digital transformation

## Источники

### Книги

- **NIST CSF 2.0** (2024) — главный фреймворк
- Bruce Schneier, **«Click Here to Kill Everybody»** (Norton, 2018) — общий контекст
- Andy Greenberg, **«Sandworm»** (Doubleday, 2019) — государственные кибератаки
- Nicole Perlroth, **«This Is How They Tell Me the World Ends»** (Bloomsbury, 2021) — zero-day market

### Стандарты

- **NIST Cybersecurity Framework 2.0**
- **ISO/IEC 27001:2022** — Information Security Management
- **CIS Critical Security Controls** — практический набор контролей
- **MITRE ATT&CK Framework** — knowledge base атакующих техник

### Регулирование

- **GDPR (ЕС)** — Privacy
- **NIS2 Directive (ЕС)** — критическая инфраструктура
- **152-ФЗ (РФ)** — персональные данные
- **187-ФЗ (РФ)** — критическая информационная инфраструктура
- **SEC Cybersecurity Disclosure Rules (США, 2023)**

### Онлайн-ресурсы

- **nist.gov/cyberframework** — NIST CSF documentation
- **sans.org** — SANS Institute — обучение, исследования
- **csa.gov.sg/threat-feed** — Threat feeds
- **kb.cert.org** — vulnerability database

### Сертификации

- **CISSP** (Certified Information Systems Security Professional) — самая известная
- **CISM** (Certified Information Security Manager, ISACA)
- **CISA** (Certified Information Systems Auditor)
- **CRISC** (Certified in Risk and Information Systems Control)
- **CEH** (Certified Ethical Hacker)
- **OSCP** (Offensive Security Certified Professional)
- **Российские:** профессиональные программы по 187-ФЗ, ФСТЭК
## Связанные документы

- [[index|Модуль 22: Risk & BC]]
- [[../index|Education Index]]
- [[03-Business-Continuity|03 Business Continuity]]
- [[../12-ERP-Digital/index|Модуль 12: ERP & Digital]]
