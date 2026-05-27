---
title: "Модуль 11 — Analytics & Business Intelligence"
aliases: ["Module 11", "Analytics", "BI", "Аналитика"]
type: hub
status: active
domain: education
module: 11-Analytics-BI
tags: [index, education, analytics, bi, sql, ml, statistics]
created: 2026-05-18
updated: 2026-05-19
---

# Модуль 11 — Analytics & Business Intelligence (бизнес-аналитика)

> Переход от пользовательского уровня BI-инструментов (Power BI, Tableau) к data-driven C-level навыку: аналитическое мышление по McKinsey-стандарту, SQL для прямой работы с данными, проектирование экспериментов, ML-методы для операций. Это **базовый слой** уровня D — без него остальные модули данных и систем (12-ERP, 13-Operations-Excellence, 14-Planning) превращаются в покупку софта без понимания, какие решения этот софт должен поддерживать.

## Карта раздела

![](attachments/diagrams/11-analytics-bi-module-map.svg)

## Заметки модуля

1. **[[01-Analytical-Thinking|01 Аналитическое мышление]]** — Hypothesis-Driven Analysis (анализ от гипотез, McKinsey), Pyramid Principle (принцип пирамиды, Barbara Minto), Data Storytelling (сторителлинг через данные, Cole Knaflic), когнитивные искажения в аналитике (Kahneman)
2. **[[02-SQL-Databases|02 SQL и базы данных]]** — SELECT / JOIN / GROUP BY / window functions, схема «звезда» vs «снежинка», OLTP vs OLAP (Online Transaction Processing / Analytical Processing — оперативная обработка транзакций / аналитическая обработка), data warehouse
3. **[[03-BI-Tools|03 BI-инструменты]]** — Power BI deep dive (DAX, Power Query), Tableau / Looker / Metabase / Apache Superset, принципы дизайна дашбордов (Stephen Few)
4. **[[04-Statistics-Experimentation|04 Статистика и эксперименты]]** — доверительные интервалы и p-значения, проверка гипотез (t-test, χ², ANOVA), A/B-тесты, причинно-следственный анализ (DiD — Difference-in-Differences, синтетический контроль, инструментальные переменные)
5. **[[05-Machine-Learning-Operations|05 Машинное обучение для операций]]** — прогнозирование спроса (Prophet, XGBoost, LSTM), сегментация клиентов (K-Means, DBSCAN), Predictive Maintenance (предсказательное обслуживание), Anomaly Detection (обнаружение аномалий), LLM / GenAI в операциях

## Зачем модуль руководителю

Современный COO / директор закупок / директор продукта живёт в мире, где **отсутствие данных — это конкурентный риск**. Главные сдвиги последних 10 лет:

- **Решения по интуиции теряют силу** — конкуренты с дисциплиной данных опережают по точности и скорости
- **Power BI / Tableau стали грамотностью** — как раньше Excel; не владеть ими в 2025 = не уметь читать
- **SQL — следующая грамотность** — самостоятельный доступ к данным без зависимости от аналитика
- **A/B-тестирование стало стандартом** — для пересмотра цен, промо, ассортимента, UX (User Experience — пользовательского опыта)
- **ML-методы из R&D вошли в операции** — прогноз спроса, оптимизация запасов, антифрод

Этот модуль превращает руководителя из «потребителя отчётов» в **активного аналитика своих гипотез**, способного самостоятельно проверить идею, доказать рекомендацию и распознать манипуляцию данными.

## Применение для руководителя

| Целевая роль | Что взять из модуля |
|--------------|---------------------|
| **COO** (Chief Operating Officer — главный операционный директор) | Аналитическое мышление как ежедневная практика; чтение дашбордов на «принять решение», а не «получить информацию»; запуск A/B-культуры в операциях |
| **Директор закупок** | SQL для самостоятельной выгрузки из ERP / 1С; статистика для проверки эффекта промо; ML для прогноза спроса |
| **Директор продукта** | A/B-тесты для проверки гипотез по продукту; статистика как защита от cherry-picking; data storytelling для коммуникации со советом |
| **Категорийный менеджер** | Прямой SQL-доступ к данным продаж; сегментация SKU и клиентов через ML; обнаружение аномалий в продажах |
| **CDO / Head of Analytics** | Полный набор: аналитическое мышление, SQL, BI, статистика, ML, governance данных |
| **CFO** | Финансовые дашборды; статистика для финансового моделирования; data quality как часть аудита |

## Дорожная карта чтения

1. **01 Аналитическое мышление** (читать первым) — фундамент: как формулировать вопросы, как структурировать ответы
2. **02 SQL и базы данных** — техническая грамотность работы с данными
3. **03 BI-инструменты** — практическая визуализация
4. **04 Статистика и эксперименты** — как отличить сигнал от шума
5. **05 Машинное обучение** — следующий уровень после статистики, для зрелых компаний

## Источники модуля (свод)

### Книги (обязательные)

- Cole Nussbaumer Knaflic, **«Storytelling with Data»** («Сторителлинг через данные», Wiley, 2015) — стандарт для презентации данных руководителю
- Barbara Minto, **«The Pyramid Principle»** («Принцип пирамиды», Pearson, 3-е изд. 2010) — каноничная книга по структурированию выводов
- Stephen Few, **«Information Dashboard Design»** («Дизайн информационных дашбордов», Analytics Press, 2-е изд. 2013) — стандарт дизайна дашбордов
- Daniel Kahneman, **«Thinking, Fast and Slow»** («Думай медленно, решай быстро», FSG, 2011) — когнитивные искажения, обязательное чтение
- Andrew Gelman, John Carlin, Hal Stern et al., **«Bayesian Data Analysis»** («Байесовский анализ данных», CRC Press, 3-е изд. 2013) — серьёзная статистика
- Rob Hyndman, George Athanasopoulos, **«Forecasting: Principles and Practice»** («Прогнозирование: принципы и практика», OTexts, 3-е изд., бесплатно онлайн) — современный стандарт
- Joel Grus, **«Data Science from Scratch»** («Data Science с нуля», O'Reilly, 2-е изд. 2019) — практика ML на Python
- Joshua Angrist, Jörn-Steffen Pischke, **«Mostly Harmless Econometrics»** («В основном безвредная эконометрика», Princeton, 2009) — причинно-следственный анализ для бизнеса
- Aurélien Géron, **«Hands-On Machine Learning with Scikit-Learn, Keras, TensorFlow»** (O'Reilly, 3-е изд. 2022) — практическое ML
- Alberto Cairo, **«The Truthful Art»** («Правдивое искусство», New Riders, 2016) — визуализация без манипуляций

### Журналы и онлайн-ресурсы

- **Harvard Business Review** — раздел Analytics & Data Science
- **MIT Sloan Management Review** — Data & AI Insights
- **Towards Data Science (Medium)** — практические разборы методов
- **Stack Overflow / Stack Exchange** — Cross Validated для статистики
- **Kaggle** — соревнования по ML, открытые датасеты
- **Российские:** Хабр (раздел Data Mining / Big Data), DataScientist.club

### Сертификации (для карьерного развития)

- **Microsoft Certified: Data Analyst Associate (Power BI)** — практический стандарт для BI в РФ и Европе
- **Tableau Desktop Specialist / Tableau Certified Data Analyst** — для Tableau-экосистемы
- **DataCamp / Coursera tracks по Data Science** — структурированное обучение
- **Google Data Analytics Professional Certificate** (Coursera) — для перехода в аналитику
- **Российские:** «Аналитик данных» от Yandex Praktikum, ВШЭ магистратура «Анализ данных и бизнес-аналитика»

## Связь с другими модулями

- [[../02-Finance/index|Модуль 02: Corporate Finance]] — финансовые дашборды, причинно-следственный анализ инвестиций
- [[../03-Management-Accounting/02-Cost-to-Serve|Модуль 03: Cost-to-Serve]] — аналитика для CTS требует SQL и BI
- [[../04-Supply-Chain/03-Demand-Planning-SOP|Модуль 04: Demand Planning]] — ML-прогнозирование как часть аналитики
- [[../07-Category-Management/06-Customer-Insights-Analytics|Модуль 07: Customer Insights]] — практическое применение аналитики
- [[../09-Ecom-Marketplaces/index|Модуль 09: E-commerce]] — A/B-тесты, аналитика конверсии
- [[../10-Marketing/03-Performance-Marketing|Модуль 10: Performance Marketing]] — атрибуция, MMM, A/B
- [[../12-ERP-Digital/index|Модуль 12: ERP & Digital]] — источники данных для аналитики
- [[../14-Planning/index|Модуль 14: Planning]] — данные как вход в S&OP / IBP
## Связанные документы

- [[../index|Education Index]]
- [[../12-ERP-Digital/index|Модуль 12: ERP & Digital]]
- [[../04-Supply-Chain/index|Модуль 04: Supply Chain]] — Demand Planning пересекается с ML
- Методология Education
