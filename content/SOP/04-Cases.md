---
aliases: 
updated: YYYY-MM-DD
tags: [education, sop, cases]
created: 2026-05-07
date created: 2026-05-07
date modified: 2026-05-13
---

# Кейсы внедрения S&OP / IBP с цифрами

> **TL;DR.** Лидеры (P&G, Cisco, Coca-Cola, Unilever, Lilly) демонстрируют типовой профиль возврата от S&OP/IBP: forecast accuracy с 60-70% растёт до 80-90%, inventory режется на 15-50%, working capital освобождается на десятки-сотни миллионов $. Внедрение занимает 12-36 месяцев и требует executive sponsor.

## 1. Procter & Gamble — эталон demand sensing + S&OP

**Контекст.** $80B+ выручки, ~5000 SKU в 180+ странах. Сложнейший supply chain в FMCG: миллионы потребителей, тысячи розничных партнёров (Walmart, Costco, Target).

**Проблема (середина 2000-х → 2010-е).**
- Высокая сложность: новые продукты, фрагментация каналов, e-commerce.
- Forecast accuracy на коротких горизонтах (1-3 недели) была проблемой.
- Inventory связывал значительный кэш.

**Что внедрили.**
1. **Multi-Enterprise Demand Sensing (MDS)** — Terra Technology (теперь часть ToolsGroup), глобальный roll-out с США/Западной Европы, далее по миру.
2. **Online S&OP-платформа для дистрибьюторов** — collaborative forecasting с retail партнёрами.
3. **Predictive analytics + AI** на short-term forecast (1-3 недели).
4. **Network simulation** — цифровая модель supply chain для оптимизации.
5. **Integrated Business Planning** интегрирован с финансами и стратегией.

**Результаты (по разным источникам).**
- **Forecast error reduction: ~50%** в ряде категорий на 3-недельном горизонте (Terra/ToolsGroup case).
- **Forecast accuracy improvement: +2-4 п.п. год к году**, по комментариям earnings calls — даже в макроэкономической турбулентности.
- **Network simulation выявила потенциал: -50% inventory + $300M annual savings** при 1% инвестиций (по ToolsGroup).
- Out-of-stock сокращены, lead time от заказа до полки сокращён.
- Стабильно входит в Gartner Supply Chain Top 25 («Hall of Fame» — disqualified из основного рейтинга, потому что слишком долго на топ-1).

**Урок:** P&G — пример, как S&OP перерастает в IBP с встроенным AI/ML. Но фундамент — годами выстроенный процесс с executive sponsorship. Не «ставим Kinaxis и заработало».

> **Аналогия:** для руководителя в SMB-сегменте (миллионы выручки vs миллиарды у P&G) — это direction of travel. AI demand sensing — недостижим, но базовый месячный S&OP-цикл с consensus forecast — это первый шаг по той же лестнице.

---

## 2. Coca-Cola — машинное обучение на демпленнинге

**Контекст.** $46B выручки, 200+ стран, локальные боттлеры. Спрос сильно сезонный, погодозависимый, с promo-эффектами.

**Проблема.**
- World-class accuracy в индустрии — около 70%, оставшиеся 30% компании «амортизируют» через инвентарь.
- Силосы между functions: sales говорил одно, ops — другое.
- Промо-планы выпадали из forecast.

**Что внедрили.**
1. **5-step monthly S&OP**: data review → demand → supply → pre-S&OP → executive.
2. **Multi-Horizon Forecasting** — отдельные модели для разных горизонтов:
   - Short-term (1-7 дней) — daily ops.
   - Medium-term (1-12 недель) — inventory planning.
   - Long-term (1-3 года) — strategic.
3. **AI/ML модели** — встроены в demand planning.
4. **Single source of truth** — все функции работают на одной платформе.

**Результаты.**
- **Forecast accuracy: с 70% до 90%** благодаря AI-driven forecasting.
- **Sales boost: +8%** через лучшее предсказание спроса.
- **+$40M revenue** через сокращение lost sales (better inventory).
- Production planning стал точнее, excess inventory сокращён.

**Урок:** даже в зрелом FMCG апгрейд forecast accuracy с 70 до 90% даёт двузначный ROI. Ключ — не сам алгоритм, а интеграция в S&OP cycle (модель → demand review → consensus → план).

---

## 3. Cisco — рекавери после кризиса 2001 → world-class supply chain

**Контекст.** $50B+ выручки в технологиях, configure-to-order модель, тысячи SKU, глобальная цепочка с outsourced manufacturing.

**Проблема (2001).**
- Cisco в Q3 2001 списал **$2.25 млрд excess inventory** — один из самых громких inventory writedown в истории.
- Forecast спроса полностью разошёлся с реальностью после dot-com bust.
- Видимости в supply chain не было — заказывали под прогноз, который уже не работал.

**Что внедрили (2001-2010).**
1. **Сегментация supply chain** по типу продукта (high-volume standardized vs configure-to-order vs new product).
2. **Strategic outsourcing** с долгосрочными контрактами и shared visibility.
3. **Risk management framework** — supply chain risk officer на уровне C-suite, supply chain risk council.
4. **Integrated S&OP** с сильным финансовым blanket.
5. **Real-time visibility** — Kinaxis RapidResponse для concurrent planning.
6. **Lean manufacturing** + business continuity planning после cunami 2011 (Япония) и Тайских наводнений.

**Результаты (по AMR/MIT/Cisco публикациям).**
- Cisco стабильно в **Gartner Supply Chain Top 25** (2007-2020+, лидер несколько лет).
- **Inventory turns** значительно выше индустрии (20+).
- **Recovery time** после tsunami 2011 — несколько недель vs месяцы у конкурентов.
- **Supply chain признан стратегическим рычагом** во время M&A — интеграция новых компаний (Acacia, AppDynamics) на существующую SCM-платформу.
- Известная цитата CFO: «supply chain saves more money than any single revenue initiative we have».

**Урок:** S&OP — это не просто планирование, это система раннего предупреждения. Cisco — единственная компания, открыто опубликовавшая свой инвентарный кризис как case study, — превратила боль в core competency.

---

## 4. Unilever — IBP + iOps цифровая трансформация

**Контекст.** $60B выручки, 400+ брендов в 190 странах. FMCG со сложным портфелем: foods, home care, personal care.

**Проблема (2010-е).**
- Сложный multi-category, multi-geography портфель.
- Силосы между Beauty/Personal Care, Food/Refreshment, Home Care.
- Высокая стоимость inventory из-за не-синхронизации.

**Что внедрили.**
1. **Integrated Operations (iOps) program** — индустриальный first, end-to-end visibility customer value chain.
2. **Kinaxis RapidResponse** для интегрированного supply chain planning (concurrent planning across regions).
3. **AI-driven demand prediction**, integration с suppliers и logistics.
4. **IBP-process** на корпоративном уровне с финансовой реконсиляцией.

**Результаты.**
- **Operational cost reduction** (конкретные цифры — trade secret, но публично — significant).
- **Improved planner productivity** — fewer planners on routine, more on exceptions.
- **Higher service level при lower inventory** — структурный сдвиг кривой trade-off.
- **End-to-end visibility** — впервые единая картина от сырья до полки.

**Урок:** для сложного multi-category business — IBP интегрированный с операционной платформой превращается в стратегическое оружие. Unilever — частый case study в академической литературе по supply chain transformation.

---

## 5. Eli Lilly — S&OP / supply network для GLP-1 boom

**Контекст.** $45B+ выручки фармы. Текущий вызов (2024-2026): GLP-1 препараты (Mounjaro, Zepbound) дали взрывной рост спроса на ozempic-класс. Спрос превышал предложение в 2-5x.

**Проблема.**
- Demand для GLP-1 взлетел в 10x за 18 месяцев.
- Производственные мощности (sterile fill-finish) — узкое горлышко.
- Регуляторные ограничения на смену площадок.
- Глобальный backorder, потеря market share к Novo Nordisk.

**Что внедрили / делают.**
1. **Risk-based S&OP** — формализованный процесс предотвращения product shortage.
2. **Massive supply network expansion**: $27B инвестиций в 4 новых US site (API + injectable), плюс расширение в Ирландии и Германии.
3. **AI strategy** для R&D + supply chain — Lilly активно деплоит ML на demand sensing и production planning.
4. **Capacity reservation** для критических lifesaving SKU.
5. **Long-horizon S&OP** — 36+ месяцев из-за лидтайма строительства фарм-завода 3-5 лет.

**Результаты (промежуточные, ongoing).**
- **2024-2026:** Lilly растёт быстрее всего big pharma; revenue по GLP-1 — десятки миллиардов.
- **Supply situation улучшилась** — большая часть SKU вышла из FDA shortage list.
- **Manufacturing capacity** доступна для следующего цикла продуктов.
- Stock price удвоился с 2023.

**Урок:** для long-leadtime индустрий (фарма, semicon, химия) S&OP должен иметь горизонт 3-5+ лет, иначе компания структурно опаздывает за спросом. Это уже не S&OP, а Long-Range Supply Network Planning — но методологически из той же семьи.

---

## 6. Lenovo — supply chain digital transformation

**Контекст.** $60B+ выручки в PC/server, configure-to-order, глобальная сеть с китайским manufacturing core, после поглощения IBM ThinkPad и Motorola.

**Проблема (2017-2019).**
- Inventory **+50% год к году** (excess из-за разнобоя в forecast).
- Slow delivery performance, slow response к demand patterns.
- Disparate data sources после M&A.

**Что внедрили.**
1. **Digital Transformation for Supply Chain Intelligence** — общая платформа.
2. **Single SAP instance** глобально (с локальными вариациями).
3. **Real-time analytics** — supply chain control tower.
4. **S&OP cycle** с executive sponsorship.

**Результаты.**
- **Cost basis: -$600M+** при изменении KPI на customer experience.
- Восстановление delivery performance.
- Стабильный рост margin в PC business при сжатии рынка.

**Урок:** после M&A первоочерёдная задача — единая S&OP-инфраструктура. Иначе унаследованные процессы конкурируют, инвентарь умножается на число brand'ов.

---

## Сравнительная таблица по KPI

| Компания | Forecast accuracy ↑ | Inventory ↓ | Cash/Cost benefit | S&OP/IBP зрелость (Gartner) |
|----------|---------------------|-------------|-------------------|----------------------------|
| P&G | ~50% reduction в forecast error | до 50% potential | $300M+ annually | Stage 5 (Hall of Fame) |
| Coca-Cola | 70% → 90% | n/a | +$40M revenue, +8% sales | Stage 4-5 |
| Cisco | n/a (concurrent planning) | turns 20+ | inventory writedown $2.25B → world-class | Stage 4-5 |
| Unilever | improved | reduced | significant (private) | Stage 4 |
| Eli Lilly | в работе | n/a | $27B capex unlocks growth | Stage 3-4 |
| Lenovo | improved | reduced post-tx | -$600M cost basis | Stage 3 |

## Общие паттерны успешных кейсов

1. **Executive sponsor от первого лица** (CEO/COO) во всех 6 кейсах.
2. **Внедрение 12-36 месяцев** — это не быстрая победа.
3. **Технология как enabler, не как решение** — сначала процесс, потом софт.
4. **Финансовая интеграция** — план в долларах, а не только штуках.
5. **Continuous improvement** — каждые 6-12 месяцев процесс эволюционирует.
6. **Единая платформа данных** — без неё S&OP сваливается в Excel-войны.
7. **Внешняя интеграция** — supplier и customer collaboration.

## Связанные заметки

- [[03-Best-practices-US|US best practices]] — рамка, в которой эти кейсы укладываются
- [[05-IBP-evolution|IBP evolution]] — куда P&G/Unilever ушли от классического S&OP
- [[06-Tools-software|Software]] — Kinaxis в Cisco/Unilever, ToolsGroup/Terra в P&G
- [[index|S&OP Index]]

## Источники

- [ToolsGroup — How P&G Supply Chain Thrives on Complexity](https://www.toolsgroup.com/blog/procter-gamble-supply-chain-complexity/)
- [Consumer Goods — P&G Implements Global Demand Sensing](https://consumergoods.com/pg-implements-global-demand-sensing)
- [Infios — Inside P&G's Inventory Playbook](https://www.infios.com/en/knowledge-center/blog/inside-procter-and-gambles-inventory-playbook)
- [SDC Exec — Planning to Succeed at Procter & Gamble](https://www.sdcexec.com/sourcing-procurement/project-management-software/article/10289777/procter-gamble-planning-to-succeed-at-procter-gamble)
- [SupplyChainBrain — Demand Planning at Coca-Cola](https://www.supplychainbrain.com/blogs/1-think-tank/post/20951-demand-planning-at-coca-cola-whats-the-secret-formula)
- [Coderio — Coca-Cola Demand Prediction with AI](https://www.coderio.com/success-story/demand-prediction-with-ai/)
- [Cisco — Supply Chain Case Studies (PDF)](https://www.cisco.com/c/dam/m/en_us/about/purpose/reporting-hub/_pdf/supply-chain-case-studies.pdf)
- [MIT CTL — Cisco Supply Chain Risk Management](https://ctl.mit.edu/sites/ctl.mit.edu/files/attachments/tab%207a%20Cisco%20Case.pdf)
- [Unilever — How Digital Transformation Drives Operational Excellence](https://www.unilever.com/news/news-search/2025/how-unilevers-digital-transformation-is-driving-operational-excellence/)
- [RFGen — Unilever Supply Chain Lessons](https://www.rfgen.com/blog/unilever-supply-chain-lessons-learned-on-digital-transformation/)
- [Pharma Manufacturing — Eli Lilly Manufacturing Expansion](https://www.pharmamanufacturing.com/industry-news/news/55269723/eli-lilly-undertakes-significant-manufacturing-expansion-initiatives-to-shore-up-supply)
- [Klover.ai — Eli Lilly AI Strategy](https://www.klover.ai/eli-lilly-ai-strategy-dominance-ai-driven-pharmaceutical-era/)
- [McKinsey — Speed for Simplicity (Lenovo)](https://www.mckinsey.com/industries/technology-media-and-telecommunications/our-insights/speed-for-simplicity-an-interview-with-lenovos-gerry-smith)

<!-- IMG: сводная диаграмма "до/после" по 5 кейсам (forecast accuracy, inventory, cost) | https://www.toolsgroup.com/wp-content/uploads/sop-case-comparison.png -->
