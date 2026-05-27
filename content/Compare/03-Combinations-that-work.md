---
aliases: 
updated: YYYY-MM-DD
tags: [education, compare, combinations]
created: 2026-05-07
date created: 2026-05-07
date modified: 2026-05-13
---

# Комбинации методологий, которые реально работают

Ни одна методология не покрывает всё. Зрелая управленческая система — это **стек из 2-4 методологий** в комбинации. Эта заметка — каталог проверенных, не выдуманных, комбинаций. Каждая — с примером компании, которая её использует, и логикой, почему они дополняют друг друга.

> **Принцип сборки.** Стек обычно состоит из трёх слоёв: **стратегия → execution → operations**. На каждом слое — одна методология. Сверху — финансовый «зонтик» (бюджет / IBP финансовый слой).

## 1. S&OP + Lean (Toyota, Boeing, Pfizer)

### Логика

- **S&OP** даёт тактическое планирование на 18 мес: что сколько произвести/продать/закупить.
- **Lean** обеспечивает операционное исполнение: устранение муда, kanban, TPS daily management.
- Без S&OP Lean «летает в темноте» — не знает спроса.
- Без Lean S&OP — это план без discipline исполнения.

### Кейсы

- **Toyota** — родина TPS, S&OP интегрирован в Hoshin Kanri и Daily Management.
- **Boeing** — Lean внедрён в production system, S&OP для авиапрограмм (787, 737-MAX).
- **Pfizer / Lilly** — S&OP в pharma + Lean Manufacturing.

<!-- IMG: S&OP + Lean stack — Toyota Way visualization | https://example.com/sop-lean-toyota.png -->

### Когда применять

Mid-large производственная компания. Mature operations, физический продукт. Готов к 12-24-мес culture journey.

### Связанные заметки

- `[[../SOP/index|S&OP]]`, `[[../Lean/index|Lean]]`

## 2. OKR + KPI (Google, LinkedIn, Spotify)

### Логика

- **OKR** — стретчевые квартальные цели для трансформации (3-5 на квартал, ~70% completion = success)
- **KPI** — стационарные операционные индикаторы для контроля «здоровья» (есть всегда, всегда зелёные)
- Это два **разных** инструмента: OKR — про change, KPI — про health.
- Ошибка №1: путать их (превращать KPI в OKR или наоборот).

### Структура

```
Strategic OKR (annual)
  ↓
Quarterly OKR (cascade by team)
  ↓
Weekly check-in: KR progress + KPI scoreboard
  ↓
Action items
```

### Кейсы

- **Google** — формат OKR из Intel (Andy Grove), внедрён John Doerr-ом. Quarterly cycle с публичной видимостью.
- **LinkedIn** — описано в *Measure What Matters* (Doerr).
- **Twitter / X**, **Adobe**, **Anheuser-Busch** — публичные OKR-практики.

### Когда применять

Tech / product / scale-up. Tech-friendly culture. Когда нужно сочетать «трансформацию» (OKR) и «стационар» (KPI).

### Связанные заметки

- `[[../OKR-KPI/index|OKR/KPI]]`

## 3. Hoshin Kanri + Lean (Toyota original, Danaher, Bridgestone)

### Логика

- **Hoshin Kanri** — стратегический слой: breakthrough objectives (3-5 лет), annual hoshin, X-matrix, catchball
- **Lean** — daily management: visual board, leader standard work, gemba walks, kaizen
- Hoshin задаёт направление, Lean делает «компас в каждой команде»
- Без Lean Hoshin — это план в Excel. Без Hoshin Lean — kaizen без direction.

### Структура

```
Breakthrough (3-5 yr)
  ↓ catchball
Annual Hoshin (X-Matrix)
  ↓ catchball
Department/Team Hoshin
  ↓
Daily Management Board (Lean)
  ↓
Standard work + Kaizen
```

### Кейсы

- **Toyota** — original implementation; до сих пор Hoshin + TPS — backbone их менеджмента
- **Danaher** — Danaher Business System (DBS), worldwide-known operational excellence machine. Hoshin centerpiece. CEOs из Danaher (Larry Culp в GE) разносят DBS дальше.
- **Bridgestone** — origin of Hoshin Kanri (1965); комбинация Hoshin + Lean
- **Ingersoll Rand** — IR Operating System, аналог DBS

<!-- IMG: Hoshin + Lean stack (стратегия → daily management) | https://example.com/hoshin-lean-stack.png -->

### Когда применять

Lean-зрелая mid-large компания. Multi-year transformation готовность.

### Связанные заметки

- `[[../Other-methodologies/05-Hoshin-Kanri|Hoshin Kanri]]`, `[[../Lean/index|Lean]]`

## 4. BSC + KPI (P&G, Mobil USM&R, Bank of America)

### Логика

- **Balanced Scorecard** — strategic frame через 4 perspectives: Financial / Customer / Internal Process / Learning & Growth
- **KPI cascade** — конкретные индикаторы внутри каждого perspective, разложенные по подразделениям
- BSC даёт **причинно-следственную логику**: «инвестиции в обучение → лучше процессы → клиент доволен → деньги»
- KPI без BSC превращается в дашборд без логики; BSC без KPI — слайд без действия

### Структура (Strategy Map → Scorecard → KPI)

```
Strategy Map (visual, 4 perspectives, cause-effect)
  ↓
Strategic Themes (3-5)
  ↓
Strategic Objectives (15-25)
  ↓
KPI per objective (1-2 each = 30-50 KPI)
  ↓
Initiatives / projects to move KPI
```

### Кейсы

- **Mobil North American Marketing & Refining** — каноничный BSC-кейс Kaplan-Norton, 1995-1998, перешли с #6 на #1 в industry profitability.
- **P&G** — BSC интегрирован с annual planning.
- **Bank of America, Hilton, FedEx, US Army** — все имеют BSC implementations
- Kaplan-Norton основали Palladium Group (теперь часть Accenture) на этой методологии.

### Когда применять

Mid-large. Хочется страт. логики, видимой для всех. BSC — это «communication tool of strategy».

### Связанные заметки

- `[[../OKR-KPI/index|OKR/KPI/BSC]]` (BSC раздел)

## 5. IBP + DDMRP (Coca-Cola Beverages Africa, Michelin)

### Логика

- **IBP** — тактический план на 24-36 мес, executive-уровень, всех функций
- **DDMRP** — pull-исполнение: buffer-based replenishment в decoupling points
- IBP видит «где мы должны быть через 12 мес»; DDMRP даёт «что мы делаем сегодня в каждой точке цепочки»
- Эта связка особенно сильна в **высокой variability**: длинный lead time, сезонность, импорт, промо

### Структура

```
IBP MBR (executive monthly)
  ↓ tactical demand & supply plan
S&OP (operational monthly)
  ↓ family-level plan
DDMRP buffers in decoupling points
  ↓ daily Net Flow Equation
Replenishment orders
```

### Кейсы

- **Coca-Cola Beverages Africa** — IBP сверху + DDMRP в supply (через Intuiflow). Live с 2019.
- **Michelin** — комбинация IBP + DDMRP, public DDI cases.
- **Kraft Heinz, Schneider Electric, Unilever** — частичные внедрения.

### Когда применять

Mid-large с complex supply chain. Длинный lead time. Variability в спросе. Важно: внедрять последовательно — сначала S&OP/IBP, потом DDMRP.

### Связанные заметки

- `[[../Other-methodologies/01-IBP-Integrated-Business-Planning|IBP]]`, `[[../Other-methodologies/03-DDMRP-Demand-Driven|DDMRP]]`

## 6. OKR + Agile/Scrum (Google, Atlassian, Twitter)

### Логика

- **OKR** — квартальный strategic frame: что мы хотим достичь и как измерим
- **Agile/Scrum** — двухнедельные sprints исполнения: что делаем сейчас
- OKR даёт «зачем»; Agile — «как и сегодня»
- Без OKR sprints превращаются в backlog grooming без направления; без Agile OKR — это roadmap, который не движется

### Структура

```
Quarterly OKR
  ↓
Roadmap (12 weeks)
  ↓
Sprint planning (2 weeks)
  ↓
Daily standup
  ↓
Sprint review → KR progress check
```

### Кейсы

- **Google** — OKR + Agile в product / engineering teams
- **Atlassian** — public о своей OKR practice + Scrum
- **Twitter / X**, **Slack**, **Stripe** — типичный SaaS-stack
- **Spotify model** — squads с OKR + Scrum внутри (хотя сам Spotify публично сказал, что их «model» не работал в чистом виде)

### Когда применять

Tech / product / digital. Software / SaaS. Scale-up до mid-market.

### Связанные заметки

- `[[../OKR-KPI/index|OKR/KPI]]`

## 7. EOS + KPI (SMB)

### Логика

- **EOS** даёт operating system: V/TO, Rocks, L10, scorecard, IDS
- **KPI scoreboard** в EOS — это «Data» компонент, 5-15 weekly metrics
- Этой комбинации обычно достаточно для SMB 30-200 человек
- НЕ нужно добавлять S&OP / IBP / Hoshin сверху, пока не вырастешь

### Структура

```
V/TO (Vision)
  ↓
Annual goals (1-Year Plan)
  ↓
Quarterly Rocks (3-7 priorities)
  ↓
Weekly L10 + Scorecard (5-15 KPI)
  ↓
IDS for issues
```

### Кейсы

- 250 000+ компаний в США (EOS Worldwide network)
- Типичный портрет — services / contracting / distribution / SMB manufacturing 50-200 человек

### Когда применять

SMB 30-250 человек. Founder / family-business. Готовность к ритуалам (L10 еженедельно).

### Связанные заметки

- `[[../Other-methodologies/07-EOS-and-other|EOS]]`

## 8. ToC (5 focusing steps) как cross-cutting линза

### Логика

- ToC не «отдельная методология» — это **линза**, которую можно наложить на S&OP, Lean, OKR, IBP
- Принцип «найти bottleneck → выжать → подчинить → инвестировать» работает на любом масштабе
- Может быть постоянной привычкой руководителя

### Где применить ToC поверх

| Где | Как |
|-----|-----|
| Поверх S&OP supply review | Bottleneck = constraint resource (capacity / supplier / cash) |
| Поверх OKR | 5 steps как фильтр приоритизации Objectives |
| Поверх Lean | DBR заменяет наивный «push pull everything» |
| Поверх проектов | CCPM (Critical Chain) |
| Поверх financial decisions | Throughput accounting вместо unit margin |

### Связанные заметки

- `[[../Other-methodologies/04-Theory-of-Constraints|ToC]]`

## Антикомбинации (что НЕ работает)

### OKR + Hoshin Kanri одновременно

Оба — про стратегическое разворачивание целей. Дублируют друг друга, конфликтуют по cadence (квартал vs год). Выбери одно.

### Holacracy + S&OP

Holacracy distributed roles конфликтует с S&OP, который требует cross-functional executive review. Не работает.

### ZBB + Beyond Budgeting

Противоположности. Невозможно делать одновременно.

### EOS + IBP

EOS — для SMB; IBP — для enterprise. Если ты уже dorab IBP — переросли EOS. Не нужны вместе.

### Lean + Six Sigma «вместо» друг друга

Это часто не комбинация, а ОДНА методология (Lean Six Sigma). Не «или», а «и» в одной системе.

### Полный «зоопарк» (5+ методологий одновременно)

Симптом overconsulting'а. Менеджеры тонут в meetings. Принцип: 1 strategy + 1 execution + 1 operations + опционально financial = 3-4 методологии максимум.

## Дорожная карта стека (для разной зрелости)

### Стартап stack
```
OKR + KPI + Agile/Scrum
```

### SMB stack
```
EOS + KPI + базовый S&OP
ИЛИ
OKR + KPI + Lean basics + базовый S&OP
```

### Mid-market stack
```
S&OP + Lean + OKR/KPI + BSC + DDMRP (опционально)
```

### Enterprise stack
```
IBP + S&OP + Lean Six Sigma + Hoshin Kanri + BSC + KPI + DDMRP + ToC linза
```

## Связь с другими заметками

- Карта ландшафта — `[[01-Methodology-landscape|Methodology landscape]]`
- Decision matrix — `[[02-Decision-matrix|Decision matrix]]`
- Реальные кейсы — `[[04-Cases-by-situation|Cases by situation]]`

## Источники

- Kaplan, R. & Norton, D. (2004). _Strategy Maps_. HBR Press.
- Kaplan, R. & Norton, D. (2008). _The Execution Premium_. HBR Press.
- Doerr, J. (2018). _Measure What Matters_. Portfolio.
- Wickman, G. (2011). _Traction_. BenBella.
- Smith, C. & Ptak, C. (2018). _DDMRP, Version 2_. Industrial Press.
- Liker, J. (2004). _The Toyota Way_. McGraw-Hill.
- [Danaher Business System (DBS) overview](https://www.danaher.com/how-we-work/danaher-business-system)
- [HBR — How to Combine Lean and Six Sigma](https://hbr.org/2002/01/six-sigma-and-the-lean-enterprise)
- [Demand Driven Tech — CCBA case](https://demanddriventech.com/case-studies/coca-cola-beverages-africa-ccba/)
