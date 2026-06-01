---
title: "Glossary — словарь терминов, метрик и аббревиатур"
aliases: ["Glossary", "Словарь", "Глоссарий"]
type: hub
status: active
domain: education
module: Glossary
tags: [index, education, glossary]
created: 2026-05-07
updated: 2026-06-01
---

# Glossary — словарь терминов, метрик и аббревиатур

Справочник по всему, что встречается в программе обучения. Англоязычные термины и аббревиатуры с переводом, расшифровкой, формулами и примерами. Используй как:

- **Lookup** — встретил незнакомое сокращение в заметке → нашёл здесь, что это
- **Шпаргалка** — перед совещанием с CFO/COO/инвестором быстро освежить, что значит ROIC vs ROE или OTIF vs Fill Rate
- **Контекст** — где этот термин ещё используется в твоей программе обучения (через wikilinks)

## Структура словаря

| # | Раздел | Что внутри | Пример терминов |
|---|--------|------------|-----------------|
| 01 | [[01-Operations-metrics\|Operations & Supply Chain]] | Метрики операций и цепочки поставок | MAPE, OTIF, OEE, C2C, DIO, takt time, ABC/XYZ |
| 02 | [[02-Financial-metrics\|Financial]] | Финансовые метрики и термины | EBITDA, ROIC, ROCE, EPS, GMV, NWC, OCF |
| 03 | [[03-Customer-metrics\|Customer & Growth]] | Клиентские и продуктовые метрики | NPS, CSAT, CES, MAU/DAU, ARPU, churn, retention |
| 04 | [[04-Methodology-acronyms\|Methodology Acronyms]] | Аббревиатуры методологий и систем | S&OP, IBP, MRP II, DDMRP, ToC, TPS, JIT, BSC, EOS, RACI |
| 05 | [[05-Concepts-and-laws\|Concepts & Laws]] | Принципы и «законы» из менеджмента | Goodhart's law, Pareto, Black Swan, Cargo Cult, Parkinson, Conway |

## Как читать запись словаря

```
**EBITDA** (Earnings Before Interest, Taxes, Depreciation, and Amortization)
Прибыль до вычета процентов, налогов и амортизации
↳ Определение: показатель операционной прибыли без учёта структуры капитала и налоговой среды
↳ Формула: EBITDA = Net Income + Interest + Taxes + D&A
↳ Зачем: сравнивать компании из разных стран / с разной долговой нагрузкой
↳ Где упоминается: [[../OKR-KPI/04-KPI-and-Balanced-Scorecard]] · [[../SOP/04-Cases]]
```

Если у термина есть синоним или вариант — указывается через `=`, с источником/контекстом.

## Принципы оформления словаря

1. **Английская аббревиатура → русское название → расшифровка** (англ.) — все три уровня, чтобы можно было найти и по аббревиатуре, и по русскому переводу
2. **Формула** — где применимо, в виде `LHS = RHS` без LaTeX
3. **«Зачем»** — короткий ответ «зачем эту метрику считают», не просто определение
4. **Wikilinks** — на заметки программы, где термин используется в контексте
5. **Источники** — где смотреть авторитетную интерпретацию (Investopedia, ASCM glossary, HBR, Damodaran, etc.)

## Полезные внешние словари

- [Investopedia](https://www.investopedia.com/) — финансовые термины с примерами
- [ASCM Supply Chain Dictionary](https://www.ascm.org/learning-development/ascm-publications/) (бывший APICS Dictionary) — стандарт supply chain
- [Lean Lexicon — LEI](https://www.lean.org/lexicon-terms/) — Lean-термины
- [Aswath Damodaran's Glossary](https://pages.stern.nyu.edu/~adamodar/) — корпоративные финансы
- [Reforge / First Round](https://review.firstround.com/) — продуктовые/growth метрики

## Связанные документы

- [[../index|Education]]
- [[../Compare/index|Compare]] — сравнение методологий
- [[../SOP/08-Metrics-and-maturity|S&OP метрики]] — где KPI операционных функций раскрыты глубже
- [[../OKR-KPI/04-KPI-and-Balanced-Scorecard|KPI и BSC]] — методические основы метрик
