---
aliases: 
tags: 
created: YYYY-MM-DD
updated: YYYY-MM-DD
date created: 2026-05-12
date modified: 2026-05-13
---
---
aliases: ["Compare methodologies"]
tags: [index, education, compare]
created: 2026-05-07---

# Сравнение методов и применимость

Самый практический раздел программы обучения. Здесь — не теория, а **навигатор по выбору**: «у меня такая ситуация — какую методологию применять?» Раздел рассчитан на то, что ты уже прошёл S&OP, Other-methodologies, Lean, OKR/KPI, и теперь нужно собрать всё в практический инструмент.

> **Главная заметка раздела — `[[02-Decision-matrix|Decision matrix]]`**. Если читать только одну — читай её. Это decision tree для руководителя: размер компании, тип бизнеса, стадия, цель → конкретные рекомендации.

## Структура раздела

| Заметка | О чём | Когда читать |
|---------|-------|--------------|
| [[01-Methodology-landscape\|01 — Карта ландшафта методологий]] | Полная картина: что планируют, на каком горизонте, какая зрелость требуется | Сначала, чтобы видеть лес |
| [[02-Decision-matrix\|02 — Матрица выбора]] (главная) | Декомпозированный совет «если у вас X — начните с Y» | Когда нужно решение для **своей** ситуации |
| [[03-Combinations-that-work\|03 — Рабочие комбинации]] | Какие методологии хорошо работают в связке | Когда базовый метод выбран и думаешь о расширении |
| [[04-Cases-by-situation\|04 — Кейсы по ситуациям]] | Реальные сценарии (закупки, импорт, beauty, ритейл, SMB) | Когда хочешь увидеть «как это в жизни» |

## Ключевые вопросы, на которые отвечает раздел

1. **«У меня компания на 80 человек, beauty-импорт, что внедрять — S&OP, OKR или EOS?»** → `[[02-Decision-matrix\|02]]` + `[[04-Cases-by-situation\|04]]` кейс 4
2. **«Я внедрил OKR, теперь что — KPI? BSC?»** → `[[03-Combinations-that-work\|03]]` + `[[../OKR-KPI/index|OKR/KPI]]`
3. **«Что выбрать между S&OP и DDMRP для импорта?»** → `[[02-Decision-matrix\|02]]` + `[[../Other-methodologies/03-DDMRP-Demand-Driven|DDMRP]]`
4. **«Стартап → IBP — нужно ли?»** → `[[01-Methodology-landscape\|01]]` (нет, не нужно)
5. **«Кризис в компании — что делать?»** → `[[02-Decision-matrix\|02]]` секция «по стадии»

## Связанные разделы

- [[../SOP/index|S&OP]] — операционное планирование
- [[../Other-methodologies/index|Другие методологии]] — IBP, MRP, DDMRP, ToC, Hoshin, ZBB, EOS
- [[../Lean/index|Lean]] — операционное совершенство
- [[../OKR-KPI/index|OKR / KPI / BSC]] — целеполагание и метрики
- [[../index|Education главная]]

## Источники для всего раздела (общие)

- [HBR — Strategy Execution archive](https://hbr.org/topic/strategy-execution)
- [McKinsey — Operations practice](https://www.mckinsey.com/capabilities/operations/our-insights)
- [BCG — Operations](https://www.bcg.com/capabilities/operations/overview)
- [Bain — Operations](https://www.bain.com/consulting-services/performance-improvement/operations/)
- [Gartner — Supply Chain Top 25](https://www.gartner.com/en/supply-chain/research/supply-chain-top-25)
- [Deloitte Insights — Operations](https://www2.deloitte.com/us/en/insights/topics/operations.html)

## Встроенная схема (офлайн)

В разделе встроена авторская SVG-схема:

- **Methodology Landscape** (домен × горизонт — где живёт каждая методология) — в [[01-Methodology-landscape]]. Файл: `attachments/methodology-landscape.svg`

## Дополнительные иллюстрации (опционально)

В заметках остались HTML-комментарии с URL — на будущее: decision tree, OKR+KPI dashboard, Hoshin+Lean stack, ABC/XYZ matrix, категорийный менеджер дашборд. Скачай в `~/tzh/Education/attachments/` и замени placeholder на `![[имя_файла.png]]`.
