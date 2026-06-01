---
title: "Forecasting — прогнозирование спроса"
aliases: ["Forecasting", "Прогнозирование спроса", "Demand Forecasting", "Demand Planning"]
type: hub
status: active
domain: education
module: Forecasting
tags: [index, education, forecasting, demand-planning, m-competitions, ml]
created: 2026-06-01
updated: 2026-06-01
---

# Forecasting — прогнозирование спроса

> Прогноз спроса — вход для почти всех решений в цепочке поставок: запасов, закупок, мощностей, S&OP. Этот раздел отвечает на вопрос «как делают форкаст в мире по лучшим практикам»: какие методы существуют (от наивных до нейросетей), какие из них реально выигрывают по данным мировых соревнований (M-competitions), как измерять точность честно, как настраивать модели под тренд / сезонность / праздники / промо, и какие системы это автоматизируют. Раздел кросс-модульный — связан с [[../14-Planning/SOP/index|S&OP]], [[../14-Planning/02-DDMRP-Deep-Dive|DDMRP]], [[../04-Supply-Chain/03-Demand-Planning-SOP|демпленнингом в цепочке]] и [[../11-Analytics-BI/index|аналитикой]].

## Карта раздела

![](attachments/diagrams/forecasting-module-map.svg)

## Заметки раздела

1. **[[01-Classical-Methods|01 Классические методы]]** — naïve и seasonal naïve как бенчмарки; скользящее среднее; экспоненциальное сглаживание (SES, Holt, Holt-Winters); ETS; ARIMA / SARIMA / SARIMAX; STL-декомпозиция; Croston для прерывистого спроса. Дерево выбора метода под характер ряда.
2. **[[02-ML-and-Competitions|02 ML-методы и уроки M-competitions]]** — Prophet, LightGBM, N-BEATS, DeepAR, Temporal Fusion Transformer; **статистика соревнований M3 / M4 / M5** (что реально выигрывает: гибриды и комбинации на одиночных рядах vs LightGBM на больших иерархиях); почему чистый ML провалился в M4 и победил в M5.
3. **[[03-Accuracy-and-Hierarchy|03 Точность и иерархия]]** — метрики (MAPE, WMAPE, MASE, RMSSE, Bias, Forecast Value Added) и их ловушки; бенчмарки точности по индустриям; иерархическое прогнозирование (bottom-up / top-down / middle-out) и оптимальная реконсиляция MinT.
4. **[[04-Tunable-and-Systems|04 Настройка моделей и системы]]** — настраиваемые коэффициенты (декомпозиция Prophet: тренд / сезонность / праздники / регрессоры; параметры Holt-Winters α / β / γ); системы и вендоры (Gartner MQ, Amazon Forecast, Blue Yonder, o9, ToolsGroup, RELEX, Kinaxis); demand sensing против demand planning.

## Зачем раздел руководителю

Качество прогноза напрямую конвертируется в деньги: точнее форкаст → меньше страхового запаса при том же сервисе, меньше списаний, выше доступность. Но «улучшать прогноз» без понимания методов и метрик бессмысленно — можно тратить ресурсы на сложную модель, которая по данным соревнований проигрывает простой. Раздел даёт руководителю **диагностический язык**: какой метод уместен для каких данных, как честно мерить точность (и не обмануться красивым MAPE), когда нужен ML, а когда хватает статистики, и какие коэффициенты реально настраиваются под бизнес (сезонность, тренд, промо).

## Применение для руководителя

| Целевая роль | Что взять из раздела |
|---|---|
| **COO / директор по цепочке поставок** | Связь точности прогноза с запасами и сервисом; что требовать от демпленнинга |
| **Директор по планированию** | Выбор метода под данные; метрики (WMAPE + Bias + FVA); иерархическая реконсиляция |
| **Директор закупок** | Прогноз как вход в закупочные решения и буферы DDMRP |
| **Аналитик / data scientist** | Уроки M4/M5; когда LightGBM/ансамбли, когда ETS/ARIMA; настройка коэффициентов |
| **Директор по цифровизации** | Выбор системы прогнозирования (вендоры, движки, demand sensing) |

## Дорожная карта чтения

1. **[[01-Classical-Methods|01 Классические методы]]** — фундамент, начать здесь
2. **[[02-ML-and-Competitions|02 ML и M-competitions]]** — что реально работает по данным соревнований
3. **[[03-Accuracy-and-Hierarchy|03 Точность и иерархия]]** — как честно мерить и согласовывать
4. **[[04-Tunable-and-Systems|04 Настройка и системы]]** — практическая реализация

## Источники (свод)

- **Rob Hyndman, George Athanasopoulos — «Forecasting: Principles and Practice» (FPP3)**, otexts.com/fpp3 (бесплатно) — основной учебник
- **M-competitions** (Makridakis, Spiliotis, Assimakopoulos) — M3 (2000), M4 (2018), M5 (2020, данные Walmart)
- **«Learnings from Kaggle's Forecasting Competitions»** (arXiv 2009.07701)
- N-BEATS (Oreshkin et al., arXiv 1905.10437); Temporal Fusion Transformer (Google)
- Prophet (Taylor & Letham, «Forecasting at scale», Meta)
- SAS — Forecast Value Added analysis (Mike Gilliland); IBF — глоссарий метрик
- Gartner — Magic Quadrant for Supply Chain Planning Solutions (2024)
- Amazon Forecast developer guide

## Связь с другими модулями

- [[../14-Planning/SOP/index|S&OP]] — прогноз как вход в Demand Review
- [[../14-Planning/02-DDMRP-Deep-Dive|DDMRP]] — pull-альтернатива, снижающая зависимость от точности прогноза
- [[../04-Supply-Chain/03-Demand-Planning-SOP|04.03 Demand Planning & S&OP]] — демпленнинг в цепочке поставок
- [[../04-Supply-Chain/04-Inventory-Management|04.04 Inventory Management]] — прогноз → страховой запас
- [[../11-Analytics-BI/05-Machine-Learning-Operations|11.05 ML Operations]] — инфраструктура ML-моделей
## Связанные документы

- [[../index|Education Index]]
- [[../14-Planning/index|Модуль 14: Planning]]
- [[../04-Supply-Chain/index|Модуль 04: Supply Chain]]
