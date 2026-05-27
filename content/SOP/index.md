---
aliases: 
tags: 
created: YYYY-MM-DD
updated: YYYY-MM-DD
date created: 2026-05-12
date modified: 2026-05-13
---
---
aliases: ["SOP"]
tags: [index, education, sop]
created: 2026-05-07---

# S&OP — Sales & Operations Planning

Раздел программы обучения: горизонтальный процесс ежемесячного согласования планов продаж, операций и финансов на горизонте 18-24 месяцев. Owner процесса — COO/CSCO/GM, executive sponsor — CEO. Цель — единый план («one number plan»), который снимает разрывы между «продали — не привезли», «закупили — не продали», «бюджет — реальность».

> **Зачем руководителю.** Любой, кто управлял снабжением в товарной компании, на своей шкуре чувствовал: без S&OP отдел продаж обещает одно, склад тащит второе, финансы видят третье. S&OP — это рамка, которая раз в месяц «склеивает» все три плана в один и заставляет executive принимать решения по trade-off (сервис vs запасы vs кэш), а не размазывать их по углам.

## Дорожная карта изучения

| Шаг | Заметка | Результат |
|-----|---------|-----------|
| 1 | [[01-What-is-SOP\|Что такое S&OP]] | Понять рамку и историю (Oliver Wight, 1980-е), отличие от MRP/бюджета |
| 2 | [[02-5-step-cycle\|Пятиступенчатый цикл]] | Знать, кто что делает в Product/Demand/Supply/Reconciliation/Executive review |
| 3 | [[03-Best-practices-US\|US best practices]] | APICS/ASCM, Gartner maturity, Oliver Wight Class A, ключевые KPI |
| 4 | [[04-Cases\|Кейсы компаний]] | Цифры: P&G, Cisco, Coca-Cola, Unilever, Pfizer/Lilly |
| 5 | [[05-IBP-evolution\|IBP — следующая ступень]] | Что добавляется поверх S&OP: финансы, стратегия, портфель |
| 6 | [[06-Tools-software\|Платформы]] | Kinaxis, Anaplan, o9, SAP IBP, Oracle, OMP — кому что подходит |
| 7 | [[07-Implementation-checklist\|Чеклист внедрения]] | Пошагово: спонсор → RACI → данные → пилот → масштаб |
| 8 | [[08-Metrics-and-maturity\|Метрики и зрелость]] | Forecast accuracy/MAPE, OTIF, inventory turns, C2C, шкала зрелости |

## Ключевые понятия одной фразой

- **One number plan** — один согласованный набор цифр для продаж, операций и финансов; «не три истины, а одна».
- **Cadence** — ежемесячный ритм. Чаще не успевает дать сигнал, реже — теряется управляемость.
- **Horizon** — 18-24 месяца rolling, с фокусом на 3-18 месяцев (короче — это уже S&OE, execution).
- **Trade-off** — ключевое слово: S&OP не «оптимизирует всё сразу», а заставляет выбрать (сервис vs cash vs cost).
- **Executive sponsor** — без CEO/COO в роли спонсора процесс не выживает дольше 6-12 месяцев.

## Применимость по типу бизнеса

| Тип бизнеса | Где S&OP применим |
|-------------|-------------------|
| Beauty-импорт (SMB 50-200 человек) | Полный цикл S&OP: размер компании позволяет поставить процесс «в чистом виде» как руководитель |
| Продуктовый ритейл | Demand sensing на уровне магазина, replenishment, OTIF поставщиков |
| Автозапчасти / long-tail SKU | Long-tail SKU, ABC/XYZ + S&OP по группам, supply review критичен |

## Связанные разделы

- [[../Other-methodologies/index|Другие методологии]] — DDMRP, ToC, MRP II как альтернативы или дополнения
- [[../OKR-KPI/index|OKR и KPI]] — метрики S&OP — это и есть KPI операционной функции
- [[../Compare/index|Сравнение методов]] — когда S&OP, когда DDMRP, когда обоих
- [[../index|Education]]

## Источники для всего раздела (общие)

- [Oliver Wight Americas — IBP/Advanced S&OP course](https://www.oliverwight-americas.com/public-courses/integrated-business-planning-advanced-sop-course/)
- [APICS/ASCM Certifications](https://www.ascm.org/learning-development/certifications-credentials/)
- [Gartner — Five-Stage S&OP Maturity Model](https://www.gartner.com/en/documents/2587021)
- [SupplyChainBrain — Demand Planning at Coca-Cola](https://www.supplychainbrain.com/blogs/1-think-tank/post/20951-demand-planning-at-coca-cola-whats-the-secret-formula)
- [Kinaxis — What is S&OP](https://www.kinaxis.com/en/sop)
- [Anaplan — S&OP Process Guide](https://www.anaplan.com/blog/sales-operations-planning-sop-guide/)

## Встроенные схемы

В разделе встроена авторская SVG-схема (полностью офлайн, без зависимости от внешних URL):

- **5-step S&OP cycle** — встроена в [[02-5-step-cycle]]: ![[sop-5-step-cycle.png]]

## Дополнительные иллюстрации (опционально)

Внутри заметок остались HTML-комментарии `<!-- IMG: ... | URL -->` — это не видно в рендере Obsidian, это заметки на будущее, если захочешь добавить ещё иллюстраций (Gartner maturity model, Oliver Wight Class A checklist, S&OP vs IBP, MQ 2024, RACI). Скачай нужный файл в `~/tzh/Education/attachments/` и замени соответствующий placeholder на `![[имя_файла.png]]`.
