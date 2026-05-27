---
title: "02 — Reliability Engineering"
aliases: ["Reliability", "TPM", "OEE", "FMEA", "RCM"]
type: note
status: active
domain: education
module: 13-Operations-Excellence
tags: [education, reliability, tpm, oee, fmea, rcm, mtbf]
created: 2026-05-19
updated: 2026-05-19
---

# 02 — Reliability Engineering

> Reliability (надёжность) — это **способность системы работать без отказа** в заданных условиях за заданное время. Для производства / логистики / IT — это центральная метрика. TPM (Total Productive Maintenance — всеобщее производительное обслуживание), OEE (Overall Equipment Effectiveness — общая эффективность оборудования), FMEA (Failure Mode and Effects Analysis — анализ режимов и последствий отказов) — главные инструменты управления надёжностью.

## Карта раздела

![](attachments/diagrams/13-oee-components.svg)

## 1. OEE — Overall Equipment Effectiveness

### 1.1 Контекст

OEE предложил **Seiichi Nakajima** (Япония) в 1960-х как часть TPM. Каноничная книга — **«Introduction to TPM»** (Productivity Press, 1988).

OEE — стандарт мирового производства. Зрелые компании отслеживают OEE по каждому критичному оборудованию.

### 1.2 Формула OEE

![](attachments/diagrams/13-oee-components.svg)

```
OEE = Availability × Performance × Quality
```

**Availability (доступность)** = фактическое время работы / плановое время
- Учитывает: breakdowns, setup/changeover
- Целевая: 90%+

**Performance (производительность)** = фактическая скорость / плановая скорость
- Учитывает: micro-stops, reduced speed
- Целевая: 95%+

**Quality (качество)** = годные единицы / всего произведено
- Учитывает: rejects, rework
- Целевая: 99%+

### 1.3 Бенчмарки

| Уровень | OEE |
|---------|-----|
| **World class** | 85%+ |
| **Good** | 70-85% |
| **Average** | 50-70% |
| **Poor** | <50% |

Большинство компаний думают, что у них 80-90%, а после реального измерения — 40-60%.

### 1.4 Шесть больших потерь (Six Big Losses)

1. **Breakdowns** — поломки
2. **Setup and Adjustments** — переналадки
3. **Small Stops** — мелкие остановки
4. **Reduced Speed** — пониженная скорость
5. **Startup Rejects** — брак на старте
6. **Production Rejects** — брак в процессе

Каждая категория относится к одной из A/P/Q компонент.

**Ключевой вывод 1.** OEE — главная метрика производственной надёжности. Без её измерения улучшения «по ощущениям» дают иллюзорные результаты.

## 2. TPM — Total Productive Maintenance

### 2.1 Контекст

TPM разработан в **Nippondenso** (Япония, 1969). Распространился через JIPM (Japan Institute of Plant Maintenance). Каноничная книга — **Nakajima «Introduction to TPM»**.

### 2.2 Восемь столпов TPM

![](attachments/diagrams/13-tpm-pillars.svg)

1. **Autonomous Maintenance** — операторы сами обслуживают свои станки
2. **Focused Improvement** (kobetsu kaizen) — целевые улучшения узких мест
3. **Planned Maintenance** — плановое обслуживание по графику
4. **Quality Maintenance** — качество встроено в оборудование
5. **Early Equipment Management** — качество дизайна при закупке
6. **Training** — обучение операторов и техников
7. **Safety / Health / Environment** — безопасность как приоритет
8. **Office TPM** — TPM в офисных функциях

### 2.3 Autonomous Maintenance — главный сдвиг

Традиционная модель: операторы работают, техники чинят. Проблема — операторы не знают своё оборудование, техники приходят только при поломке.

TPM: **операторы выполняют базовое обслуживание сами** (чистка, смазка, проверка, мелкие настройки). Это:
- Снижает число поломок 30-50%
- Повышает OEE 10-30%
- Делает операторов компетентными
- Освобождает техников для серьёзных задач

### 2.4 Внедрение TPM

Стандартный roadmap (Nakajima):
- Phase 1 — Decision (executive commitment)
- Phase 2 — Education & promotion
- Phase 3 — Master plan (3-5 years)
- Phase 4 — Kick-off
- Phase 5 — Implementation
- Phase 6 — Excellence (TPM Award)

Полная TPM-трансформация — 3-5 лет.

**Ключевой вывод 2.** TPM — не «программа обслуживания», а **культурная трансформация**. Превращает операторов в владельцев своего оборудования.

## 3. FMEA — Failure Mode and Effects Analysis

### 3.1 Контекст

FMEA разработана в военной промышленности США (1949), массово распространилась через автопром (Ford, Toyota). Каноничный стандарт — **AIAG-VDA FMEA Handbook** (2019).

### 3.2 Процесс FMEA

![](attachments/diagrams/13-fmea-process.svg)

**Шаг 1 — Identify failure modes** — все возможные режимы отказа

**Шаг 2 — Effect** — последствия отказа, **Severity** (1-10)

**Шаг 3 — Cause** — причины, **Occurrence** (1-10)

**Шаг 4 — Detection** — как обнаружим, **Detection** (1-10)

**Шаг 5 — RPN (Risk Priority Number)** = S × O × D
- RPN 100+ — обязательное действие
- RPN 50-100 — действие желательно
- RPN <50 — мониторинг

**Шаг 6 — Action** — меры по предотвращению или детектированию

### 3.3 Виды FMEA

- **Design FMEA (DFMEA)** — на стадии проектирования продукта
- **Process FMEA (PFMEA)** — для производственных процессов
- **System FMEA** — для систем целиком
- **Service FMEA** — для услуг

### 3.4 Применение

FMEA — обязательный инструмент:
- Запуск новых продуктов (особенно auto, medical)
- Запуск новых процессов
- После серьёзных incidents
- Регулярный пересмотр критичного оборудования

**Ключевой вывод 3.** FMEA — структурированный способ **предотвращения отказов до того, как они случатся**. Замена реактивного подхода («сломалось — починим») на проактивный.

## 4. RCM и MTBF / MTTR

### 4.1 RCM — Reliability-Centered Maintenance

**RCM** (Reliability-Centered Maintenance — обслуживание на основе надёжности) — методология выбора оптимальной стратегии обслуживания для каждой части оборудования.

Каноничная книга — **John Moubray, «Reliability-Centered Maintenance»** (Industrial Press, 1997).

Семь вопросов RCM:
1. Каковы функции актива?
2. Как актив может перестать выполнять функции?
3. Что вызывает каждый отказ?
4. Что происходит при отказе?
5. Каковы последствия отказа?
6. Что можно сделать для предотвращения?
7. Если предотвращение невозможно — что делать?

### 4.2 Стратегии обслуживания

| Стратегия | Когда применять |
|-----------|------------------|
| **Run-to-Failure** | Дешёвые компоненты, дублированные |
| **Time-Based** | По графику (масло раз в год) |
| **Condition-Based** | По состоянию (вибрация, температура) |
| **Predictive (ML)** | Предсказание поломки за дни / часы |
| **Proactive (FMEA-driven)** | Устранение причин до отказа |

### 4.3 MTBF и MTTR

**MTBF** (Mean Time Between Failures — среднее время между отказами) — мера надёжности. Чем выше, тем надёжнее.

**MTTR** (Mean Time To Repair — среднее время восстановления) — мера ремонтопригодности. Чем меньше, тем лучше.

**Availability** = MTBF / (MTBF + MTTR)

Пример: MTBF = 100 часов, MTTR = 4 часа → Availability = 100 / 104 = 96.2%

### 4.4 Современные тренды

- **Predictive Maintenance с AI** — нейросети по сенсорным данным
- **Digital Twin** оборудования — модель в реальном времени
- **IoT-сенсоры** — постоянный мониторинг
- **AR (Augmented Reality)** — навигация для техника

**Ключевой вывод 4.** Современная надёжность — это **переход от reactive к proactive и predictive**. Лидеры производства (Siemens, GE, Rolls-Royce) уже работают на predictive уровне.

## Применение для руководителя

| Целевая роль | Главные применения |
|--------------|---------------------|
| **COO** | OEE как стратегический KPI; TPM-трансформация |
| **Директор производства** | Daily владение OEE, TPM, FMEA |
| **Директор техобслуживания** | RCM-стратегии; predictive maintenance |
| **CFO** | ROI инвестиций в надёжность; экономия от downtime reduction |
| **CIO** | IT-инфраструктура для predictive maintenance |

## Связь с другими модулями

- [[01-Quality-Management|01 Quality Management]] — quality + reliability
- [[../Lean/03-Lean-tools|Lean tools]] — TPM как часть Lean
- [[../11-Analytics-BI/05-Machine-Learning-Operations|Модуль 11.05: ML]] — predictive maintenance
- [[../12-ERP-Digital/06-Automation-AI|Модуль 12.06: Digital Twin]] — twin оборудования
- [[../22-Risk-BC/index|Модуль 22: Risk]] — reliability риски

## Источники

### Книги (приоритет чтения)

- Seiichi Nakajima, **«Introduction to TPM»** (Productivity Press, 1988) — каноничный TPM
- John Moubray, **«Reliability-Centered Maintenance»** (Industrial Press, 1997) — стандарт RCM
- AIAG-VDA, **«FMEA Handbook»** (AIAG, 2019) — стандарт FMEA
- Robert Hansen, **«Overall Equipment Effectiveness»** (Industrial Press, 2002)
- Patrick O'Connor, **«Practical Reliability Engineering»** (Wiley, 5-е изд.)

### Стандарты

- ISO 55000 — Asset Management
- IEC 60300 — Dependability Management
- SAE JA1011/1012 — RCM standards

### Онлайн-ресурсы

- **JIPM (Japan Institute of Plant Maintenance)** — TPM Awards
- **SMRP (Society for Maintenance & Reliability Professionals)**
- **IISE Industrial Engineering** — research
- **Российские:** конференции «Надёжность производственного оборудования»

### Сертификации

- **CMRP (Certified Maintenance & Reliability Professional)** — SMRP
- **TPM Excellence Award (JIPM)** — для компаний
- **CRE (Certified Reliability Engineer)** — ASQ

### Кейсы

- **Toyota TPM** — каноничный кейс
- **Siemens Amberg factory** — predictive maintenance с Digital Twin
- **Rolls-Royce engines** — каждый двигатель имеет digital twin
- **Российские:** Северсталь, ММК TPM-программы
## Связанные документы

- [[index|Модуль 13: Operations Excellence]]
- [[../index|Education Index]]
- [[01-Quality-Management|01 Quality Management]]
