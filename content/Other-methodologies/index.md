---
aliases: 
tags: 
created: YYYY-MM-DD
updated: YYYY-MM-DD
date created: 2026-05-12
date modified: 2026-05-13
---
---
aliases: ["Other methodologies"]
tags: [index, education, other-methodologies]
created: 2026-05-07---

# Другие методологии планирования и операционного управления

Раздел программы обучения, который расширяет картину за пределы S&OP и Lean. Здесь — те фреймворки, которые либо появились раньше (MRP), либо параллельно (ToC, Hoshin Kanri), либо позже как реакция на ограничения предыдущих (DDMRP, IBP, Beyond Budgeting), плюс «модные» системы для SMB (EOS) и крайности (Holacracy).

> **Зачем руководителю.** S&OP и Lean — рабочие лошадки. Но реальность шире: длинный lead time из Китая (это уже DDMRP-ландшафт), бюджетные конфликты (ZBB vs Beyond Budgeting), long-tail SKU (требует ABC/XYZ + MRP II), SMB-команда, где может зайти EOS вместо «полного S&OP». Эта папка — про то, что ещё бывает. А [[../Compare/index|раздел Compare]] — про то, что когда применять.

## Карта методологий раздела

| Класс | Метод | Где применим | Чем отличается |
|-------|-------|--------------|----------------|
| Эволюция S&OP | [[01-IBP-Integrated-Business-Planning\|IBP]] | Enterprise, multi-BU, public companies | Добавляет финансы + стратегию + multi-horizon |
| Push-планирование | [[02-MRP-MRPII-ERP\|MRP / MRP II / ERP]] | Производство со стабильным BOM | Push, базируется на forecast, root системы SAP/Oracle |
| Pull-планирование | [[03-DDMRP-Demand-Driven\|DDMRP]] | Высокая variability, длинный lead time, импорт | Pull, buffers вместо safety stock, decoupling points |
| Управление узкими местами | [[04-Theory-of-Constraints\|Theory of Constraints]] | Любая система с bottleneck | 5 focusing steps, throughput accounting, DBR, CCPM |
| Стратегия → ежедневное управление | [[05-Hoshin-Kanri\|Hoshin Kanri]] | Lean-зрелые компании, 3-5 летняя стратегия | X-matrix, catchball, breakthrough objectives |
| Бюджетирование | [[06-ZBB-Zero-Based-Budgeting\|Zero-Based Budgeting]] | Cost-out трансформации, M&A | Бюджет с нуля, не incremental |
| Компактные системы для SMB | [[07-EOS-and-other\|EOS, 4DX, Holacracy, Beyond Budgeting, Agile Strategy]] | SMB, scale-ups, эксперименты | Книжно-консалтинговые системы |

## Дорожная карта изучения

| Шаг | Заметка | Зачем |
|-----|---------|-------|
| 1 | [[01-IBP-Integrated-Business-Planning\|IBP]] | Понять, что после S&OP идёт IBP — естественная эволюция в больших компаниях |
| 2 | [[02-MRP-MRPII-ERP\|MRP/MRP II/ERP]] | Понять корни современных ERP-систем (SAP, 1C) и ограничения push-логики |
| 3 | [[03-DDMRP-Demand-Driven\|DDMRP]] | Pull-альтернатива MRP — критично для импорта и волатильного спроса |
| 4 | [[04-Theory-of-Constraints\|Theory of Constraints]] | Универсальная линза «найди bottleneck», работает в проектах, на складе, в продажах |
| 5 | [[05-Hoshin-Kanri\|Hoshin Kanri]] | Связка стратегии и daily management — то, чего не делает S&OP |
| 6 | [[06-ZBB-Zero-Based-Budgeting\|ZBB]] | Понять «3G-стайл» — токсичный, но мощный инструмент |
| 7 | [[07-EOS-and-other\|EOS и компания]] | Что выбирать для SMB 50-200 человек, когда «полный S&OP» избыточен |

## Связанные разделы

- [[../SOP/index|S&OP]] — базовая рамка, на которую IBP надстраивается
- [[../Lean/index|Lean Production]] — операционный движок, в который встраивается Hoshin Kanri
- [[../OKR-KPI/index|OKR / KPI / BSC]] — методики целеполагания, родственные Hoshin
- [[../Compare/index|Сравнение и применимость]] — практическая матрица «когда что использовать»
- [[../index|Education]]

## Источники для всего раздела (общие)

- [Oliver Wight — Integrated Business Planning](https://oliverwight-eame.com/integrated-business-planning) — IBP Class A standard
- [Demand Driven Institute](https://www.demanddriveninstitute.com/) — DDMRP origin (Carol Ptak, Chad Smith)
- [Theory of Constraints Institute](https://www.tocinstitute.org/) — Goldratt's institute
- [Goldratt Marketing — Five Focusing Steps](https://www.toc-goldratt.com/en/toc-application/five-focusing-steps)
- [EOS Worldwide](https://www.eosworldwide.com/) — Entrepreneurial Operating System
- [FranklinCovey — 4DX](https://www.franklincovey.com/create-breakthrough-results/the-4-disciplines-of-execution-4dx-system/)
- [Bogsnes Advisory — Beyond Budgeting](https://bogsnesadvisory.com/)
- [HBR archive — поиск по методологиям](https://hbr.org/)
- [McKinsey Insights — Operations](https://www.mckinsey.com/capabilities/operations/our-insights)

## Встроенные схемы (офлайн)

В разделе встроены 3 авторские SVG-схемы:

- **DDMRP Buffer Profile** (red/yellow/green zones) — в [[03-DDMRP-Demand-Driven]]. Файл: `attachments/ddmrp-buffer.svg`
- **ToC 5 Focusing Steps** (Identify-Exploit-Subordinate-Elevate-Repeat) — в [[04-Theory-of-Constraints]]. Файл: `attachments/toc-5-focusing-steps.svg`
- **Hoshin X-Matrix** — в [[05-Hoshin-Kanri]]. Файл: `attachments/hoshin-x-matrix.svg`

## Дополнительные иллюстрации (опционально)

В заметках остались HTML-комментарии с URL — на будущее: IBP horizon, Net Flow Equation, Drum-Buffer-Rope, Catchball, EOS V/TO, EOS Six Components, 4DX Scoreboard, MRP II closed-loop. Скачай в `~/tzh/Education/attachments/` и замени соответствующий placeholder.
