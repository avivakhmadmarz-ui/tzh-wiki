---
aliases: 
updated: 2026-05-13
tags: [education, okr-kpi, kpi, cases, pitfalls]
created: 2026-05-07
date created: 2026-05-07
date modified: 2026-05-13
---

# 05 — Кейсы KPI и ловушки: Walmart, Amazon, GE, Wells Fargo

> «When a measure becomes a target, it ceases to be a good measure.»
> — Goodhart's Law (Marilyn Strathern's reformulation, 1997)

KPI — мощнейший инструмент. Он же — самый опасный. Эта заметка — два полюса: компании, которые **выиграли благодаря KPI**, и компании, которые **разрушили себя через KPI**.

## Часть А — Где KPI работают

### 1. Walmart — KPI-driven supply chain (1962 → сегодня)

**Контекст.** Sam Walton основал Walmart в 1962. С самого начала — **одержимость данными**.

> «People think we got big by putting big stores in small towns. Really, we got big by replacing inventory with information.»
> — Sam Walton

#### Главные KPI Walmart

**1. GMROII** (Gross Margin Return on Inventory Investment) — сколько долларов валовой прибыли Walmart получает с каждого доллара инвентаря по себестоимости.

```
GMROII = Gross Margin $ / Average Inventory at Cost
```

Walmart требует от поставщиков **GMROII > 3.0** для удержания на полке. Это означает: каждый доллар, лежащий на складе, должен зарабатывать $3 валовой прибыли в год.

**2. OTIF** (On-Time In-Full) — % поставок, доставленных вовремя и в полном объёме.

В 2017 Walmart ввёл **OTIF mandate**: поставщики должны достигать **98%+ OTIF**. Каждый процент ниже = штрафы, занесение в supplier performance database. Это форма leading indicator для shelf availability.

**3. SQEP** (Supplier Quality Excellence Program) — качество PO и грузов (правильная маркировка, упаковка, документы).

#### Retail Link

Walmart открыл супер-инструмент: **Retail Link** — доступ поставщика к **realtime sales data** по своим SKU в каждом магазине. Поставщик сам управляет своим запасом (Vendor-Managed Inventory). Это **shifts the cost of forecasting onto the supplier**, при этом обе стороны видят одни данные.

#### Результат

- 1962: 1 магазин, $700K выручки.
- 1985: $8.4B revenue, #1 retailer in USA.
- 2024: **$648B revenue**, #1 in the world. ~10,500 магазинов в 19 странах.

**Источник:** [Walmart KPI 101 PDF](https://cdn.corporate.walmart.com/41/75/674f6f8e43cdac0b10b16e1e66fe/walmart-index-tsc-kpis-101.pdf); [SupplierWiki — Walmart OTIF](https://supplierwiki.supplypike.com/articles/walmart-otif-metrics); [Vector — Walmart supply chain](https://www.withvector.com/blog/walmarts-supply-chain-a-detailed-look-at-how-they-manage-it/).

### 2. Amazon — Two-Pizza teams + Input metrics + WBR (1995 → сегодня)

Amazon имеет наиболее чистую и развитую KPI-философию из всех публично известных компаний. Описана в **Working Backwards** (Colin Bryar & Bill Carr, 2021).

#### Концепции

**Two-Pizza Teams.** Команда не больше, чем можно накормить двумя пиццами (~6-10 человек). Owns конкретный сервис end-to-end. Команда сама определяет свои KPI.

**Single-Threaded Leader (STL).** Один человек 100% посвящён одной инициативе. Не COO, у которого 5 направлений. Не CTO с 10 командами. STL = single accountable person, у которого нет другой работы. Сегодня в Amazon вся новая инициатива должна иметь STL.

**Input vs Output metrics.** Краеугольная идея.

| Output (lagging) | Input (leading, controllable) |
|------------------|-------------------------------|
| Revenue | Selection (# SKUs available) |
| Profit | Price competitiveness |
| Customer satisfaction | In-stock rate |
| Net Promoter Score | Time-to-deliver |

Принцип Bezos: «**Don't manage outputs. Manage inputs.**» Outputs — следствие. Inputs — то, чем можно управлять.

**Working Backwards.** Прежде чем строить продукт, пишут **PR/FAQ** — пресс-релиз и FAQ от лица будущего клиента, как если бы продукт уже запустили. Сначала определяют **исход для клиента**, потом строят к нему. Это и есть «working backwards from the customer».

**Weekly Business Review (WBR).** Каждый понедельник, обычно 3 часа. Все top-level метрики на стенах. Команда разбирает аномалии, не презентации. **«Are we still on track?»**

#### Известный KPI-фреймворк Amazon

Под пирамидой:
1. **North Star metric**: long-term customer value (revenue, retention).
2. **Top output metrics**: revenue, profit, customer satisfaction.
3. **Critical input metrics**: 5-10 leading indicators, controllable.
4. **Operational metrics**: десятки tactical metrics.

Команда mainly работает на уровне **3** (input metrics). Они **знают**, что если двигают input, output двинется через предсказуемое время.

#### Результат

Amazon с 1995 по 2024: $0 → $638B revenue. Без OKR (Bezos исторически их не любил), исключительно на input metrics + Working Backwards + STL.

**Это альтернатива OKR, доказывающая, что KPI-only подход тоже работает — при правильной культуре.**

**Источник:** [AWS Two-Pizza Teams](https://aws.amazon.com/executive-insights/content/amazon-two-pizza-team/); [AWS Day 1 Culture](https://aws.amazon.com/executive-insights/content/how-amazon-defines-and-operationalizes-a-day-1-culture/); [Working Backwards Single-Threaded Teams](https://workingbackwards.com/concepts/amazon-single-threaded-teams/); Bryar & Carr, *Working Backwards* (St Martin's, 2021).

### 3. GE под Jack Welch — Six Sigma + Vitality Curve (1981-2001)

**Контекст.** Jack Welch стал CEO General Electric в 1981. За 20 лет market cap GE вырос с **$14B до $410B** — рост в **29 раз**.

#### Двойной KPI-подход Welch

**Six Sigma** — методология качества от Motorola (Bill Smith, 1986), которую Welch внедрил во всём GE с 1995.
- Цель: **3.4 defects per million opportunities** (6σ).
- Все менеджеры обязаны были получить **Green Belt** или выше.
- Главный KPI на каждом производственном участке: **DPMO (Defects Per Million Opportunities)**.
- К 2000-м: GE заявлял экономию **$10-12B/год** благодаря Six Sigma.

**Vitality Curve («Rank and Yank», «20-70-10»).**
- Каждый год менеджер ранжировал команду:
  - **Top 20%** — A-players, лучшая оплата, повышение, опционы.
  - **Middle 70%** — B-players, развитие, удержание.
  - **Bottom 10%** — C-players, **увольняли**.
- Welch требовал жёсткого соблюдения: даже в высокоэффективной команде увольнять 10%.

#### Результат и крах

**С 1981 по 2001:** market cap $14B → $410B. GE — самая дорогая компания мира.

**С 2001 по 2018:** под Jeff Immelt и Larry Culp GE столкнулся с накопленными проблемами. Stack ranking стало токсичным — менеджеры боролись друг с другом за «20%», люди прятали ошибки, чтобы не попасть в «10%».

**В 2015 GE официально отказался от Vitality Curve** (Microsoft сделал то же в 2013, Adobe — в 2012, см. [[03-OKR-cases|03]]).

**Урок:** даже выдающийся KPI-подход (Six Sigma) комбинированный с **разрушительной HR-практикой** (forced ranking) даёт краткосрочный результат и долгосрочный коллапс. См. дальше — Wells Fargo.

**Источник:** [Vitality Curve — Wikipedia](https://en.wikipedia.org/wiki/Vitality_curve); [Quartz — GE killed annual reviews](https://qz.com/428813/ge-performance-review-strategy-shift); [Performyard — Welch management style](https://www.performyard.com/articles/jack-welch-management-style).

## Часть Б — Где KPI разрушили компанию

### 4. Wells Fargo cross-selling scandal (2002-2016)

**Самый каноничный пример того, как KPI убил компанию.**

#### Контекст

Wells Fargo с 1990-х строил стратегию **«cross-selling»** — продавать одному клиенту много продуктов (чек, сберегательный счёт, кредитка, ипотека, страховка). Цель: **8 products per household** (внутренний слоган: *«Eight is great»*).

#### Как KPI стал токсичным

В каждом отделении установили **жёсткие KPI продаж**:
- Минимум 8 проданных продуктов в день на teller.
- Невыполнение → выговор, потом увольнение.
- Перевыполнение → бонус, повышение.

Менеджеры избивали teller'ов цифрами **ежедневно**. Многие квоты были **физически недостижимы** в районах, где клиентов мало.

#### Что произошло

Сотрудники начали **открывать фейковые счета без ведома клиентов**. Просто брали данные настоящего клиента, открывали ему ещё один сберегательный счёт, кредитку, иногда переводили мизерные суммы, чтобы счёт «работал». Цифры в KPI росли.

**К 2016 году:**
- **3.5+ миллиона фейковых счетов** (по данным CFPB и Harvard Business School).
- ~5,300 сотрудников уволено за участие.
- Fines: **$3B+ от регуляторов** (CFPB, OCC, DOJ, SEC).
- CEO John Stumpf вынужден уйти в отставку.
- Бывший COO Carrie Tolstedt — обвинения, $17M штраф.
- Stock dropped, brand damage **на десятилетие** вперёд.

#### Урок

KPI **«8 products per household»** работал как стратегия — пока не стал **жёстким targets с наказанием за непопадание**. Это **классический Goodhart's law**.

> «The cross-sell metric was the bank's target. Once management placed pressure to hit the target, cross-selling became not just a bad target — it corrupted the entire retail side of the business.»
> — Truth on the Market

**Источник:** [Wells Fargo cross-selling scandal — Wikipedia](https://en.wikipedia.org/wiki/Wells_Fargo_cross-selling_scandal); [Harvard Law — corpgov on the scandal](https://corpgov.law.harvard.edu/2019/02/06/the-wells-fargo-cross-selling-scandal-2/); [Truth on the Market — Goodhart](https://truthonthemarket.com/2020/03/18/goodhart-and-bad-policy/).

## Часть В — Законы измерения

### Goodhart's Law (1975)

Британский экономист **Charles Goodhart** в 1975 году в статье про монетарную политику Bank of England сформулировал:

> «Any observed statistical regularity will tend to collapse once pressure is placed upon it for control purposes.»

Антрополог Marilyn Strathern в 1997 переформулировала это в более запоминающуюся форму, ставшую **canonical**:

> **«When a measure becomes a target, it ceases to be a good measure.»**

Логика. Метрика хорошо отражает реальность, **пока никто не пытается на неё влиять**. Как только она становится целью с наказанием/наградой — люди начинают **оптимизировать саму метрику**, а не реальность за ней.

**Примеры:**
- **Wells Fargo:** «8 products per household» → фейковые счета.
- **NHS UK (2000-е):** KPI «4 hours max waiting in A&E» → пациентов держали в скорых на парковке, не пуская в приёмный покой, чтобы 4-часовой счётчик не запустился.
- **Soviet truck factories:** план на «количество гвоздей» → делали микроскопические гвозди. План на «тоннаж гвоздей» → делали один огромный гвоздь.
- **Uber drivers:** KPI «accept rate» → водители принимают заказ, потом отменяют.

### Campbell's Law (1976)

Социолог **Donald Campbell** в 1976 году сформулировал близкое:

> «The more any quantitative social indicator is used for social decision-making, the more subject it will be to corruption pressures and the more apt it will be to distort and corrupt the social processes it is intended to monitor.»

В переводе: чем сильнее метрика влияет на решения, тем больше люди её портят (намеренно или нет).

**Примеры:**
- **No Child Left Behind (USA, 2001-2015):** standardized test scores как KPI школ → teachers «teach to the test», некоторые подделывают результаты (Atlanta Public Schools scandal, 2009: 178 учителей и админов уволены).
- **Hospital readmission rates:** KPI «readmissions <X%» → больницы отказываются принимать пациентов с высоким риском, или маркируют визиты как «observation» вместо «admission».
- **Police clearance rates:** KPI «закрытых дел» → давление закрывать дела без расследования.

### Cobra effect (perverse incentive)

Историческая байка (правдивость спорная, но иллюстрация работает): британская колониальная администрация в Индии хотела сократить популяцию кобр в Дели. Объявили **bounty за каждую сданную кобру**.

Локальные предприниматели начали **разводить кобр** для сдачи. Когда правительство узнало и отменило программу, заводчики **выпустили всех кобр на волю** — популяция выросла больше прежней.

**Современные cobra effects:**
- KPI «закрытые тикеты» в support → агенты закрывают без решения, клиент открывает новый тикет.
- KPI «время в Zoom» в remote-командах → люди ставят Zoom фоном.
- KPI «количество строк кода» → разработчики пишут многословный код.

## Топ-10 anti-pattern'ов KPI

1. **KPI без owner.** Никто не отвечает = никто не действует.
2. **Только lagging indicators.** Управляешь по зеркалу заднего вида.
3. **Слишком много KPI.** >25 на executive dashboard = никто не смотрит.
4. **Vanity metrics.** Followers, downloads, page views без связи с бизнесом.
5. **KPI с привязкой к зарплате 100%.** → Wells Fargo, gaming, sandbagging.
6. **KPI без threshold.** «Revenue $50M» — а $48M это плохо? Нужны зелёный/жёлтый/красный.
7. **Невозможные KPI.** Если люди никогда не достигают, они либо ломают цифры, либо игнорируют.
8. **KPI без cadence review.** Проверяем раз в год = не управляем.
9. **KPI противоречащие друг другу.** Sales хочет «больше клиентов», support хочет «меньше тикетов» → drama.
10. **KPI замораживается на 5 лет.** Бизнес меняется, KPI должен меняться. Если не пересматриваем — мониторим вчерашнюю реальность.

## Защита от Goodhart's law

| Принцип | Что делать |
|---------|------------|
| **Множественность** | Не один KPI, а 3-5 на одну стратегическую цель. Сложно «обмануть» все одновременно. |
| **Triangulation** | Lagging + leading + qualitative (фокус-группы, support tickets). |
| **Ротация KPI** | Раз в год пересматривайте, заменяйте устаревшие. |
| **Decouple from comp** | Бонус привязывайте к **общему результату**, не к одной метрике. |
| **Audit trail** | Кто-то независимый периодически перепроверяет цифры. |
| **Red-team** | Спрашивайте: «Как я мог бы взломать этот KPI, не достигая реальной цели?» |
| **OKR-слой** | OKR двигает на новые горизонты, KPI следит за здоровьем — не путать роли. |

## Что читать дальше

- [[06-OKR-vs-KPI-the-difference|06 — OKR vs KPI]] — главный синтез.
- [[07-Implementation-for-leader|07 — Внедрение]] — как избежать всех ошибок.
- [[index|OKR-KPI Index]]

## Источники

- [Wells Fargo cross-selling scandal — Wikipedia](https://en.wikipedia.org/wiki/Wells_Fargo_cross-selling_scandal)
- [The Wells Fargo Cross-Selling Scandal — Harvard Law](https://corpgov.law.harvard.edu/2019/02/06/the-wells-fargo-cross-selling-scandal-2/)
- [Goodhart's law — Wikipedia](https://en.wikipedia.org/wiki/Goodhart's_law)
- [Campbell's law — Wikipedia](https://en.wikipedia.org/wiki/Campbell's_law)
- [NN/G — Campbell's Law and Metric Fixation](https://www.nngroup.com/articles/campbells-law/)
- [Vitality curve — Wikipedia](https://en.wikipedia.org/wiki/Vitality_curve)
- [Quartz — Why GE killed annual reviews](https://qz.com/428813/ge-performance-review-strategy-shift)
- [AWS Two-Pizza Teams](https://aws.amazon.com/executive-insights/content/amazon-two-pizza-team/)
- [Walmart KPI 101 PDF](https://cdn.corporate.walmart.com/41/75/674f6f8e43cdac0b10b16e1e66fe/walmart-index-tsc-kpis-101.pdf)
- [SupplierWiki — Walmart OTIF metrics](https://supplierwiki.supplypike.com/articles/walmart-otif-metrics)
- Bryar & Carr, *Working Backwards* (St Martin's, 2021)
- Charles Goodhart, "Problems of Monetary Management: The U.K. Experience" (1975)
- Donald T. Campbell, "Assessing the Impact of Planned Social Change" (1976)
