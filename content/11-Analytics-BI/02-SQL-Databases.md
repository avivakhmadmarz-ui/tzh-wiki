---
title: "02 — SQL и базы данных"
aliases: ["SQL", "Databases", "OLAP", "Star Schema", "Window Functions"]
type: note
status: active
domain: education
module: 11-Analytics-BI
tags: [education, analytics, sql, databases, olap, oltp, star-schema, data-warehouse]
created: 2026-05-19
updated: 2026-05-19
---

# 02 — SQL и базы данных

> SQL (Structured Query Language — структурированный язык запросов) — это **минимальная грамотность** руководителя для прямой работы с данными. Без него вся аналитика проходит через посредника (аналитика), что замедляет цикл «вопрос → ответ» в 5-10 раз. Понимание базовых конструкций (SELECT, JOIN, GROUP BY, оконные функции) и принципов проектирования данных (звезда vs снежинка, OLTP vs OLAP) даёт самостоятельность в 70% повседневных аналитических задач.

## Карта раздела

![](attachments/diagrams/11-sql-query-anatomy.svg)

## 1. Зачем SQL руководителю

### 1.1 Контекст и легитимность

SQL — стандарт ANSI с 1986 года, поддерживается всеми реляционными СУБД (PostgreSQL, MySQL, Microsoft SQL Server, Oracle, ClickHouse, BigQuery, Snowflake). Каноничные книги — **Anthony Molinaro, «SQL Cookbook»** (O'Reilly, 2-е изд. 2020) и **Markus Winand, «SQL Performance Explained»** (Markus Winand, 2012).

В корпоративной аналитике SQL — **обязательный навык**: 90%+ корпоративных данных хранится в реляционных СУБД, и Power BI / Tableau / Excel под капотом генерируют SQL-запросы.

### 1.2 Зачем руководителю самому писать SQL

Аргументы против («у меня же аналитики»):

- **Скорость:** запрос «сколько мы продали категории X в неделю Y» аналитик делает за 30 минут (постановка + код + проверка), руководитель сам — за 2 минуты
- **Доверие к данным:** запрос написал — увидел исходные таблицы — понял ограничения данных
- **Точность вопроса:** формулировка SQL заставляет уточнить, что именно ищется
- **Снижение зависимости:** не ждать «когда у аналитика будет время»

### 1.3 Минимальный набор для руководителя

| Уровень | Что уметь | За какое время осваивается |
|---------|-----------|---------------------------|
| **Базовый** | SELECT / FROM / WHERE / ORDER BY / LIMIT | 1 неделя |
| **Средний** | JOIN, GROUP BY, агрегаты, подзапросы | 2-3 недели |
| **Продвинутый** | Window functions, CTE (Common Table Expressions), CASE WHEN | 1-2 месяца |
| **Экспертный** | Query optimization, индексы, EXPLAIN, materialized views | 6+ месяцев |

Для руководителя цель — **средний уровень**. Продвинутый и экспертный — для аналитиков.

**Ключевой вывод 1.** SQL — самая высокая отдача от часа обучения среди технических навыков руководителя. 20-30 часов практики дают навык, экономящий тысячи часов через карьеру.

## 2. Анатомия SQL-запроса

### 2.1 Шесть обязательных частей

![](attachments/diagrams/11-sql-query-anatomy.svg)

Стандартный SELECT-запрос содержит до шести частей, в строгом порядке:

```sql
SELECT       -- какие колонки или агрегаты вернуть
  category,
  SUM(revenue) AS total_revenue,
  COUNT(*) AS orders_count
FROM         -- основная таблица
  orders
JOIN         -- связанные таблицы
  products ON orders.product_id = products.id
WHERE        -- фильтр строк ДО группировки
  order_date >= '2024-01-01'
GROUP BY     -- группировка
  category
HAVING       -- фильтр групп ПОСЛЕ агрегации
  SUM(revenue) > 1000000
ORDER BY     -- сортировка
  total_revenue DESC
LIMIT 10;    -- ограничение результата
```

### 2.2 Порядок логического выполнения

SQL выполняется **не в порядке написания**. Реальная последовательность:

1. **FROM + JOIN** — определяем источник данных
2. **WHERE** — фильтруем строки
3. **GROUP BY** — группируем
4. **HAVING** — фильтруем группы
5. **SELECT** — вычисляем выражения
6. **ORDER BY** — сортируем
7. **LIMIT** — ограничиваем

Понимание порядка снимает большинство ошибок начинающих («почему я не могу использовать алиас из SELECT в WHERE»).

### 2.3 Главные ошибки начинающих

- **`SELECT *`** — выгружает все колонки, медленнее и менее читаемо
- **`WHERE` после `GROUP BY`** — должно быть `HAVING`
- **`JOIN` без условия** — даёт декартово произведение, миллионы строк
- **Забытый `GROUP BY`** — при использовании агрегатов выдаст ошибку
- **`NULL` сравнение** — `WHERE x = NULL` всегда FALSE, надо `IS NULL`

**Ключевой вывод 2.** Запоминание шести частей запроса и логического порядка выполнения — 80% базового SQL. Дальше — практика.

## 3. JOIN — соединение таблиц

### 3.1 Четыре типа JOIN

Бизнес-данные почти всегда лежат в нескольких таблицах. JOIN соединяет их по ключу.

| Тип JOIN | Что возвращает |
|----------|----------------|
| **INNER JOIN** | Только строки, где ключ есть в обеих таблицах |
| **LEFT JOIN** | Все строки из левой + совпадения из правой (NULL, если нет) |
| **RIGHT JOIN** | Все строки из правой + совпадения из левой |
| **FULL OUTER JOIN** | Все строки из обеих таблиц |

В практике 95% JOIN — это **INNER** или **LEFT**. RIGHT редко (можно переписать как LEFT), FULL OUTER — для специфических задач сверки.

### 3.2 Типичные паттерны

**Продажи с категориями и регионами:**

```sql
SELECT
  o.order_id, o.order_date,
  p.product_name, p.category,
  c.city, c.region
FROM orders o
INNER JOIN products p ON o.product_id = p.id
INNER JOIN customers c ON o.customer_id = c.id
WHERE o.order_date >= '2024-01-01';
```

**Клиенты с количеством заказов (LEFT JOIN покажет всех, включая не покупавших):**

```sql
SELECT
  c.customer_id, c.name,
  COUNT(o.order_id) AS orders_count
FROM customers c
LEFT JOIN orders o ON c.customer_id = o.customer_id
GROUP BY c.customer_id, c.name;
```

### 3.3 Проблема «звёздочки»: SELECT * в JOIN

При JOIN таблиц с одинаковыми именами колонок `SELECT *` создаёт неоднозначность. Хорошая практика — **алиасы таблиц** (o, p, c) и **явные колонки**.

**Ключевой вывод 3.** JOIN — самая сложная часть базового SQL для начинающих. После освоения INNER и LEFT 90% запросов становятся доступны.

## 4. GROUP BY и агрегатные функции

### 4.1 Концепция группировки

GROUP BY группирует строки по одной или нескольким колонкам, после чего применяются **агрегатные функции** к каждой группе:

| Функция | Что считает |
|---------|-------------|
| `COUNT(*)` | Количество строк |
| `COUNT(DISTINCT x)` | Количество уникальных значений x |
| `SUM(x)` | Сумма x |
| `AVG(x)` | Среднее x |
| `MIN(x)` / `MAX(x)` | Минимум / максимум |
| `STDDEV(x)` | Стандартное отклонение |
| `PERCENTILE_CONT(0.5) WITHIN GROUP (ORDER BY x)` | Медиана x |

### 4.2 Типичные паттерны

**Топ-10 категорий по выручке:**

```sql
SELECT
  category,
  SUM(revenue) AS total_revenue,
  COUNT(DISTINCT customer_id) AS unique_customers
FROM orders
JOIN products ON orders.product_id = products.id
WHERE order_date >= '2024-01-01'
GROUP BY category
ORDER BY total_revenue DESC
LIMIT 10;
```

**Месячная динамика продаж:**

```sql
SELECT
  DATE_TRUNC('month', order_date) AS month,
  SUM(revenue) AS revenue,
  COUNT(*) AS orders,
  AVG(revenue) AS avg_order_value
FROM orders
GROUP BY DATE_TRUNC('month', order_date)
ORDER BY month;
```

### 4.3 GROUP BY ROLLUP / CUBE

Расширения GROUP BY для построения многоуровневых сводок:

- **ROLLUP** — иерархические суммы (категория → подкатегория → SKU + итоги)
- **CUBE** — все возможные комбинации группировок
- **GROUPING SETS** — выборочные комбинации

В отчётности «по категории и каналу с итогом по каждому измерению» — это ROLLUP.

**Ключевой вывод 4.** Освоение GROUP BY + агрегатные функции = 60% повседневных аналитических запросов. Без них SQL остаётся декларативным «дай мне данные», а не аналитическим инструментом.

## 5. Window functions — оконные функции

### 5.1 Зачем window functions

Обычные агрегаты «сжимают» строки в одно значение на группу. Window functions считают агрегат **по окну строк**, не теряя самих строк.

Классические задачи:

- **Накопительная сумма** (running total) — продажи нарастающим итогом по дням
- **Скользящее среднее** — 7-дневное среднее продаж
- **Ранжирование** — топ-3 SKU в каждой категории
- **Сравнение с предыдущим периодом** — % роста vs прошлый месяц
- **Доля от целого** — какой % выручки даёт каждый SKU в категории

### 5.2 Синтаксис

```sql
function() OVER (PARTITION BY ... ORDER BY ... ROWS BETWEEN ...)
```

- **PARTITION BY** — как «GROUP BY», но без сжатия строк
- **ORDER BY** — порядок внутри окна (нужен для running total, lag/lead, ranking)
- **ROWS BETWEEN** — границы окна (для скользящих средних)

### 5.3 Примеры

**Топ-3 SKU в каждой категории по выручке:**

```sql
SELECT category, sku, revenue
FROM (
  SELECT
    category, sku, revenue,
    ROW_NUMBER() OVER (PARTITION BY category ORDER BY revenue DESC) AS rank
  FROM products_sales
)
WHERE rank <= 3;
```

**Скользящее 7-дневное среднее:**

```sql
SELECT
  order_date,
  daily_revenue,
  AVG(daily_revenue) OVER (
    ORDER BY order_date
    ROWS BETWEEN 6 PRECEDING AND CURRENT ROW
  ) AS rolling_7d_avg
FROM daily_sales;
```

**Сравнение с прошлым месяцем:**

```sql
SELECT
  month,
  revenue,
  LAG(revenue, 1) OVER (ORDER BY month) AS prev_month,
  (revenue - LAG(revenue, 1) OVER (ORDER BY month)) * 100.0 /
    LAG(revenue, 1) OVER (ORDER BY month) AS growth_pct
FROM monthly_sales;
```

**Ключевой вывод 5.** Window functions — водораздел между «начинающий» и «средний уровень» SQL. После освоения большинство аналитических задач решается одним запросом, без выгрузки в Excel.

## 6. CTE — Common Table Expressions

### 6.1 Зачем CTE

CTE (Common Table Expression — общее табличное выражение) — это «временная именованная таблица» внутри запроса. Альтернатива вложенным подзапросам, но **читаемая**.

### 6.2 Синтаксис

```sql
WITH
  monthly_sales AS (
    SELECT DATE_TRUNC('month', order_date) AS month,
           SUM(revenue) AS revenue
    FROM orders
    GROUP BY month
  ),
  monthly_growth AS (
    SELECT month, revenue,
           LAG(revenue) OVER (ORDER BY month) AS prev_month
    FROM monthly_sales
  )
SELECT month, revenue, prev_month,
       (revenue - prev_month) * 100.0 / prev_month AS growth_pct
FROM monthly_growth
ORDER BY month;
```

Запрос читается **сверху вниз**: сначала monthly_sales, потом monthly_growth, потом финал. Без CTE этот запрос был бы тройным вложенным подзапросом.

### 6.3 Рекурсивные CTE

`WITH RECURSIVE` — для иерархических запросов (например, обход дерева категорий или подчинения сотрудников). Применяется реже, но критично, когда нужно.

**Ключевой вывод 6.** CTE — обязательный приём для сложных запросов. Превращает «лапшу подзапросов» в линейный читаемый код.

## 7. OLTP vs OLAP — два типа баз данных

### 7.1 OLTP — Online Transaction Processing

**OLTP** (Online Transaction Processing — оперативная обработка транзакций) — операционные базы данных, оптимизированные для **быстрой записи** и **точечных чтений**:

- ERP (SAP, Oracle, 1С) — учёт операций
- CRM (Salesforce, Bitrix24) — клиенты
- E-commerce платформы (Magento, Shopify) — заказы

**Характеристики:**
- Тысячи коротких транзакций в секунду
- ACID-гарантии (Atomicity, Consistency, Isolation, Durability — атомарность, согласованность, изолированность, надёжность)
- Нормализованная схема (3NF — третья нормальная форма): много таблиц, минимум дублирования
- Аналитические запросы выполняются **медленно** (минуты на агрегацию миллионов строк)

### 7.2 OLAP — Online Analytical Processing

**OLAP** (Online Analytical Processing — аналитическая обработка) — аналитические хранилища, оптимизированные для **сложных чтений по большим объёмам**:

- Data Warehouse (Snowflake, BigQuery, ClickHouse, Greenplum)
- OLAP-кубы (Microsoft SSAS — SQL Server Analysis Services)

**Характеристики:**
- Запросы выполняются за секунды на терабайтах данных
- Денормализованная схема (звезда / снежинка)
- Колоночное хранение (columnar storage) — выгодно для агрегатов
- Часто отсутствуют обновления (data warehouse как append-only)

### 7.3 ETL / ELT — перенос данных из OLTP в OLAP

**ETL** (Extract, Transform, Load — извлечение, трансформация, загрузка) — классический подход: вытащить из OLTP, преобразовать на промежуточном сервере, загрузить в OLAP.

**ELT** (Extract, Load, Transform) — современный подход: вытащить, сразу загрузить в OLAP, преобразовать там. Возможно благодаря мощности современных DWH (Data Warehouse — хранилищ данных).

Инструменты: Airflow, dbt, Fivetran, Stitch, Talend, Informatica.

**Ключевой вывод 7.** Понимание разницы OLTP vs OLAP критично для руководителя: оперативные данные «нельзя гонять для аналитики», аналитические — «нельзя обновлять каждые 5 секунд». Это разные миры с разной архитектурой.

## 8. Схемы данных — звезда и снежинка

### 8.1 Star Schema — звезда

![](attachments/diagrams/11-star-vs-snowflake.svg)

В центре — **fact table** (таблица фактов): операции (продажи, заказы, транзакции). Колонки: ключи (FK — Foreign Keys — внешние ключи) на измерения + меры (количество, выручка, прибыль).

Вокруг — **dimension tables** (таблицы измерений): описание ключей. Дата, продукт, клиент, регион, канал.

**Плюсы:**
- Простая структура
- Быстрые запросы (один JOIN на измерение)
- Понятно бизнесу

**Минусы:**
- Дублирование данных в измерениях (например, регион клиента дублируется для каждого клиента)
- Больше места

### 8.2 Snowflake Schema — снежинка

Расширение star: измерения сами разбиваются на под-таблицы. Например, продукт → категория → отдел.

**Плюсы:**
- Минимум дублирования (3NF)
- Меньше места

**Минусы:**
- Больше JOIN на запрос (медленнее)
- Сложнее для бизнеса

### 8.3 Когда что выбирать

| Сценарий | Схема |
|----------|-------|
| Корпоративное хранилище общего назначения | **Star** (стандарт) |
| Маленький data mart | **Star** |
| Очень большой объём измерений (тысячи атрибутов) | **Snowflake** |
| Strict 3NF требуется регуляторно | **Snowflake** |

В 80% корпоративных DWH побеждает **star schema** благодаря производительности и понятности.

### 8.4 Data Vault и современные альтернативы

**Data Vault** (Dan Linstedt, 2000) — гибрид: хабы (бизнес-ключи), линки (связи), сателлиты (атрибуты с историей). Подходит для регуляторно сложных индустрий (банки, страховые), где требуется полная история изменений.

**Lakehouse** (Databricks, 2020-е) — объединение data lake (raw файлы) и DWH в одной платформе. Тренд последних лет.

**Ключевой вывод 8.** Star schema — рабочий стандарт. Знание её устройства даёт интуицию для BI-моделей (Power BI Tabular, Tableau Extracts).

## 9. Производительность и оптимизация

### 9.1 Базовые принципы

Если запрос медленный, проверка по порядку:

1. **EXPLAIN / EXPLAIN ANALYZE** — план выполнения. Покажет, где «затыкается»
2. **Индексы** — есть ли индекс на колонках в WHERE и JOIN
3. **Размер таблицы** — может, нужен партиционинг
4. **Селективность WHERE** — фильтр сужает 99% строк или 5%?
5. **JOIN-порядок** — оптимизатор обычно справляется, но иногда подсказка нужна

### 9.2 Materialized Views — материализованные представления

Сохранённый результат запроса, обновляемый по расписанию. Для тяжёлых аналитических запросов, которые гоняются регулярно. Запрос к MV выполняется как обычный SELECT по таблице — за миллисекунды.

### 9.3 Когда обращаться к DBA / data engineer

Для руководителя достаточно базового SQL и понимания EXPLAIN. Глубокая оптимизация (индексы, партиционинг, физическая модель) — задача DBA (Database Administrator — администратора БД) или data engineer.

**Ключевой вывод 9.** Производительность SQL — отдельная глубокая тема. Базовая интуиция (используйте индексы, фильтруйте рано, не загружайте лишнее) даёт 80% результата.

## Сводный практический протокол

Маршрут изучения SQL для руководителя:

| Неделя | Тема | Артефакт |
|--------|------|----------|
| 1 | SELECT, FROM, WHERE, ORDER BY | 20 простых запросов к собственным данным |
| 2 | JOIN (INNER, LEFT) | 10 запросов с двумя-тремя таблицами |
| 3 | GROUP BY, агрегаты | Топ-N отчёты по своим данным |
| 4 | Подзапросы и CTE | Сложные многошаговые запросы |
| 5-6 | Window functions | Running totals, ранжирование, скользящие средние |
| 7-8 | Чтение схемы данных | Self-service отчёты в Power BI на собственных запросах |

Цель: к концу 2 месяцев — самостоятельно отвечать на 70% аналитических вопросов через прямой SQL к корпоративному хранилищу.

## Применение для руководителя

| Целевая роль | Главные применения |
|--------------|---------------------|
| **COO** | Базовые запросы к ERP-данным; чтение SQL аналитиков для контроля; запросы по операционным KPI |
| **Директор закупок** | Запросы к 1С / SAP по поставщикам, ценам, оборачиваемости; самостоятельная подготовка отчётов для совета |
| **Директор продукта** | A/B-данные через SQL; когортный анализ; ретроспектива запусков |
| **Категорийный менеджер** | Прямой доступ к данным продаж по SKU / клиентам / регионам; быстрая проверка гипотез |
| **CDO / Head of Analytics** | Архитектура DWH; выбор star vs snowflake; ETL / ELT pipelines |
| **CFO** | Финансовые запросы к корпоративному DWH; сверка управленческой и финансовой отчётности через SQL |

## Связь с другими модулями

- [[01-Analytical-Thinking|01 Аналитическое мышление]] — SQL как инструмент проверки гипотез
- [[03-BI-Tools|03 BI-инструменты]] — Power BI / Tableau под капотом генерируют SQL
- [[04-Statistics-Experimentation|04 Статистика и эксперименты]] — данные для статистики достаются через SQL
- [[05-Machine-Learning-Operations|05 Machine Learning]] — feature engineering начинается с SQL
- [[../12-ERP-Digital/index|Модуль 12: ERP & Digital]] — ERP как источник OLTP-данных
- [[../14-Planning/index|Модуль 14: Planning]] — S&OP данные требуют SQL-выгрузок

## Источники

### Книги (приоритет чтения)

- Anthony Molinaro, Robert de Graaf, **«SQL Cookbook»** («SQL: сборник рецептов», O'Reilly, 2-е изд. 2020) — стандартный справочник по практическим запросам
- Alan Beaulieu, **«Learning SQL»** («Изучаем SQL», O'Reilly, 3-е изд. 2020) — обучающий путь от нуля
- Markus Winand, **«SQL Performance Explained»** («Производительность SQL», Markus Winand, 2012) — оптимизация запросов
- Ralph Kimball, Margy Ross, **«The Data Warehouse Toolkit»** («Инструментарий хранилища данных», Wiley, 3-е изд. 2013) — стандарт по dimensional modeling, источник star schema
- Bill Inmon, **«Building the Data Warehouse»** («Построение хранилища данных», Wiley, 4-е изд. 2005) — альтернативный подход (Inmon vs Kimball)
- Joe Celko, **«SQL for Smarties»** («SQL для умных», Morgan Kaufmann, 5-е изд. 2015) — углублённые приёмы
- Dan Linstedt, Michael Olschimke, **«Building a Scalable Data Warehouse with Data Vault 2.0»** (Morgan Kaufmann, 2015) — Data Vault методология

### Статьи

- Microsoft Learn: **«T-SQL Reference»** — официальная документация
- PostgreSQL Documentation, особенно **«Window Functions»** и **«CTEs»** — каноничные референсы
- Mode Analytics blog — практические разборы аналитических запросов
- Snowflake / BigQuery / ClickHouse blogs — современные DWH-практики

### Онлайн-ресурсы

- **Mode Analytics SQL School (modeanalytics.com/sql-tutorial)** — бесплатный полный курс
- **SQLZoo (sqlzoo.net)** — практика интерактивно
- **Hackerrank SQL track** — задачи разной сложности
- **LeetCode SQL** — задачи уровня собеседования
- **DataCamp / Stratascratch** — платформы практики
- **PostgreSQL Tutorial (postgresqltutorial.com)** — углублённый референс

### Сертификации

- **Microsoft Certified: Azure Data Engineer Associate** — для облачных DWH
- **Snowflake SnowPro Core / Advanced** — для Snowflake-экосистемы
- **Google Cloud Professional Data Engineer** — для BigQuery
- **Oracle Database SQL Certified Associate** — для Oracle DBA-трека

### Кейсы

- **Amazon DWH evolution** — переход с Oracle на Redshift, потом на S3 + Athena (публичные лекции AWS re:Invent)
- **Netflix data platform** — публичные доклады о масштабной аналитической инфраструктуре
- **Российские:** Яндекс ClickHouse (open-source), Сбер DWH на Greenplum, X5 на Snowflake (по открытым публикациям)
## Связанные документы

- [[index|Модуль 11: Analytics & BI]]
- [[../index|Education Index]]
- [[01-Analytical-Thinking|01 Аналитическое мышление]]
- [[03-BI-Tools|03 BI-инструменты]]
