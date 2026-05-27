---
title: "Модуль 12 — ERP & Digitalization"
aliases: ["Module 12", "ERP", "Digital", "Цифровизация"]
type: hub
status: active
domain: education
module: 12-ERP-Digital
tags: [index, education, erp, digital, wms, tms, mdm, rpa, process-mining]
created: 2026-05-18
updated: 2026-05-19
---

# Модуль 12 — ERP & Digitalization (ERP-системы и цифровизация)

> ERP (Enterprise Resource Planning — планирование ресурсов предприятия) и связанная цифровая инфраструктура (WMS, TMS, MDM, RPA) — это **операционный фундамент** современной компании. Без понимания этого стека руководитель не может вести проект внедрения, оценить инвестицию в IT, понять, почему компании-конкуренты эффективнее. Российский стек (1С) — это одна часть мирового ландшафта, в которой COO / директор закупок часто выступает владельцем проектов внедрения и развития.

## Карта раздела

![](attachments/diagrams/12-erp-digital-module-map.svg)

## Заметки модуля

1. **[[01-ERP-Systems|01 ERP-системы]]** — обзор мирового и российского ландшафта: SAP S/4HANA, Oracle, Microsoft Dynamics 365, Odoo, 1С: ERP. Архитектура модулей, жизненный цикл внедрения, почему 70% проектов проваливаются (Standish CHAOS Report)
2. **[[02-SCM-Planning-Systems|02 SCM Planning-системы]]** — Kinaxis RapidResponse, Blue Yonder, o9 Solutions, SAP IBP (Integrated Business Planning — интегрированное бизнес-планирование), APS (Advanced Planning & Scheduling — продвинутое планирование и расписание). Связь с S&OP-циклом
3. **[[03-WMS-Warehouse-Systems|03 WMS — системы управления складом]]** — функции (приёмка, размещение, отбор, упаковка, инвентаризация), архитектура, голосовое управление (voice picking), pick-by-light, RFID (Radio-Frequency Identification — радиочастотная идентификация), решения (Manhattan Associates, Blue Yonder, SAP EWM, 1С: WMS), KPI склада
4. **[[04-TMS-Transportation-Systems|04 TMS — системы управления транспортом]]** — функции (планирование маршрутов, тарификация, freight audit), VRP-алгоритмы, интеграция с WMS и e-com, решения (Oracle Transportation Management, MercuryGate, Trimble, Antor), KPI транспорта
5. **[[05-MDM-PIM-DAM|05 MDM, PIM, DAM]]** — Master Data Management (управление мастер-данными) для справочников, PIM (Product Information Management — управление информацией о продукте: Akeneo, inRiver), DAM (Digital Asset Management — управление цифровыми активами)
6. **[[06-Automation-AI|06 Автоматизация и AI]]** — RPA (Robotic Process Automation — роботизированная автоматизация процессов: UiPath, Blue Prism), Process Mining (Celonis, Disco), AI-агенты в операциях, Digital Twin (цифровой двойник)
7. **[[07-IT-Strategy-Non-IT|07 IT-стратегия для нон-IT-руководителя]]** — Build vs Buy vs Configure, TCO (Total Cost of Ownership — полная стоимость владения) IT-системы, Data Governance, выбор интеграторов

## Зачем модуль руководителю

Большинство современных операций «живут внутри ERP»: каждая закупка, отгрузка, продажа, начисление — это запись в ERP. Решения о внедрении / развитии ERP — **самые дорогие IT-инвестиции** (5-50 млн рублей для среднего бизнеса, миллиарды для крупного) с самым высоким риском провала (Standish CHAOS Report: 70% IT-проектов провалены или просрочены).

После 2022 года российский ERP-ландшафт радикально перестроен:
- Уход SAP, Oracle, Microsoft из РФ → миграция на 1С: ERP / отечественные платформы
- Параллельный импорт лицензий — серая зона
- Российские решения для WMS / TMS (СКЛАД 3PL, Antor, ЛогистАс) активно растут
- AI-агенты и LLM в корпоративных операциях — новый стандарт

Этот модуль даёт руководителю **функциональный язык** для разговора с IT-директором, интегратором, вендором — и снижает риск провального внедрения.

## Применение для руководителя

| Целевая роль | Что взять из модуля |
|--------------|---------------------|
| **COO** (Chief Operating Officer — главный операционный директор) | Стратегия ERP-стека; владелец проектов внедрения; build/buy/configure решения; governance |
| **CIO / CDO** (Chief Information / Data Officer) | Полный набор: ERP, SCM-планирование, MDM, RPA, AI, governance |
| **Директор закупок** | Закупочные модули ERP; интеграция с поставщиками (EDI — Electronic Data Interchange); WMS для склада |
| **Директор логистики** | WMS / TMS — главные системы; VRP для маршрутизации; интеграция с 3PL |
| **Категорийный менеджер** | PIM для управления контентом SKU; MDM для справочника продуктов; интеграция с маркетплейсами |
| **CFO** | TCO IT-инвестиций; бюджетирование ERP; ROI цифровизации |

## Дорожная карта чтения

1. **01 ERP-системы** (читать первым) — фундамент: что такое ERP, как устроены
2. **02 SCM Planning** — следующий слой над ERP для планирования
3. **03 WMS + 04 TMS** — операционные системы склада и транспорта
4. **05 MDM, PIM, DAM** — мастер-данные как фундамент всего
5. **06 Автоматизация и AI** — современный слой над всем стеком
6. **07 IT-стратегия** — каркас принятия решений

## Источники модуля (свод)

### Книги (обязательные)

- Carl Olofson, **«Inside SAP S/4HANA»** (SAP Press, 2023) — стандарт по SAP
- Karl Wiegers, **«Software Requirements»** (Microsoft Press, 3-е изд. 2013) — для всех IT-проектов
- Gwynne Richards, **«Warehouse Management»** (Kogan Page, 4-е изд. 2017) — стандарт по WMS
- John Coyle et al., **«Transportation: A Supply Chain Perspective»** (10-е изд.) — TMS-стандарт
- Marco Wirthlin, **«Process Mining in Action»** (Springer, 2020) — про Celonis и Process Mining
- Thomas Wailgum, **«Why ERP Projects Fail»** (CIO.com, серия статей)
- Eric Kimberling, **«Lessons from 1000+ ERP Implementations»** (Third Stage Consulting, серия)
- Российские: **«1С: ERP — управление предприятием»** методология от 1С (официальная документация)

### Журналы и онлайн-ресурсы

- **Gartner Magic Quadrant** — ERP, SCM Planning, WMS, TMS, MDM (ежегодные обзоры)
- **Forrester Wave** — параллельные обзоры
- **CIO.com** — практические статьи по IT-стратегии
- **MIT Sloan Management Review** — Digital Transformation insights
- **Российские:** TAdviser (российский Gartner), CRN/RE, Computerworld Russia

### Сертификации

- **SAP Certified Application Associate** (S/4HANA-треки) — для SAP-специалистов
- **Microsoft Dynamics 365 Certifications**
- **Oracle Cloud ERP Specialist**
- **1С: Специалист / Эксперт** — российский стандарт
- **UiPath RPA Developer / Solution Architect** — для RPA
- **Celonis Process Mining Practitioner** — для Process Mining
- **ITIL Foundation** — для IT Service Management
- **TOGAF** — для enterprise architecture

## Связь с другими модулями

- [[../02-Finance/index|Модуль 02: Corporate Finance]] — ERP финансовые модули; TCO IT-инвестиций
- [[../03-Management-Accounting/04-Reporting-Standards|Модуль 03: Reporting Standards]] — параллельный учёт через ERP-функционал
- [[../04-Supply-Chain/index|Модуль 04: Supply Chain]] — ERP, WMS, TMS как операционная основа
- [[../05-Procurement/06-eProcurement-and-Digital|Модуль 05: eProcurement]] — закупочные модули и платформы
- [[../11-Analytics-BI/index|Модуль 11: Analytics & BI]] — ERP как источник данных для аналитики
- [[../14-Planning/index|Модуль 14: Planning]] — SCM Planning-системы как реализация S&OP / IBP
## Связанные документы

- [[../index|Education Index]]
- [[../11-Analytics-BI/index|Модуль 11: Analytics & BI]]
- [[../14-Planning/index|Модуль 14: Planning]]
- Методология Education
