# SQL-Project
# SQL Practice & Assignments

A structured collection of SQL exercises covering everything from basic string functions to window functions, CTEs, subqueries, transactions, and stored procedures — built on a **Sales & Inventory** database in PostgreSQL, plus a **Hospital/School** practice dataset.

## 📁 Repository Structure
```
├── sales_inventory_assignment.sql    # 139 SQL questions (Sales & Inventory schema)
├── part_1_string_functions.sql        # String functions (UPPER, LOWER, CONCAT, LEFT)
├── part_2_number_functions.sql        # Number functions (ROUND, CEIL, FLOOR, aggregates)
├── part_3_date_and_time.sql           # Date functions (EXTRACT, AGE, TO_CHAR)
├── part_4_joins.sql                   # INNER, LEFT, RIGHT, multi-table joins
├── part_5_window_functions.sql        # ROW_NUMBER, RANK, NTILE, LAG, AVG OVER
├── part_6_set_operators.sql           # UNION, UNION ALL, INTERSECT
└── README.md
```

## 📘 Description

This repository is a **hands-on SQL learning portfolio** documenting my progression from fundamental to advanced SQL concepts. The main file (`sales_inventory_assignment.sql`) contains **139 solved problems** against a four-table sales database (`Customers`, `Products`, `Sales`, `Inventory`), while the `part_1` through `part_6` files apply the same concepts to a **school/hospital** dataset (`students`, `patients`, `doctors`, `appointments`, `exam_results`).

The goal is to demonstrate practical mastery of PostgreSQL for data analysis and reporting.

## 🗂️ Database Schemas

**Sales & Inventory:**
| Table | Key Columns |
|---|---|
| `customers` | customer_id, name, email, registration_date, membership_status |
| `products` | product_id, name, category, price, supplier, stock_quantity |
| `sales` | sale_id, customer_id, product_id, quantity_sold, sale_date, total_amount |
| `inventory` | product_id, stock_quantity |

**School & Hospital (parts 1–6):**
`students`, `subjects`, `exam_results`, `patients`, `doctors`, `appointments`, `prescriptions`

## 🧠 Topics Covered

| Section | Concepts |
|---|---|
| **A. String Functions** | UPPER, LOWER, LENGTH, LEFT, CONCAT |
| **B. Number Functions** | ROUND, CEIL, FLOOR, COUNT, AVG, MAX, MIN, SUM |
| **C. Date & Time** | EXTRACT, AGE, TO_CHAR, date arithmetic |
| **D. Joins** | INNER, LEFT, RIGHT, self-joins, multi-table joins |
| **E. Window Functions** | ROW_NUMBER, RANK, DENSE_RANK, NTILE, LAG, LEAD, running totals |
| **F. Set Operators** | UNION, UNION ALL, INTERSECT |
| **G. Subqueries** | Correlated & non-correlated, `IN`, `NOT IN`, `EXISTS` |
| **H. CTEs** | `WITH` clauses for intermediate results |
| **I. Advanced Analytics** | Top-N per group, running totals, rank-based filters |
| **J. DML & DDL** | UPDATE with CASE, ALTER TABLE, indexes |
| **K. Functions & Procedures** | `CREATE FUNCTION`, `CREATE PROCEDURE`, parameters |
| **L. Transactions** | BEGIN, COMMIT, ROLLBACK, validation logic |
| **M. Views** | `CREATE VIEW` for reusable reports |
| **N. Data Cleaning** | COALESCE, NULLIF, TRIM, LOWER |

## 🔍 Sample Insights
- **Top spenders** identified via `RANK()` and `NTILE()` bucketing.
- **Category revenue** ranked using `PARTITION BY` in window functions.
- **Repeat customers** found through `HAVING COUNT(*) > 1` self-grouping.
- **Unsold products** detected with `NOT EXISTS` and anti-joins.
- **Consecutive-month buyers** flagged using `LAG()` over monthly buckets.

## 🛠️ Setup
Requires **PostgreSQL 12+**.

```bash
psql -U postgres -f sales_inventory_assignment.sql
```

Or run any `part_*.sql` file individually against a database containing the hospital/school schema.

## 🎯 Learning Outcomes
- Write efficient multi-table joins and aggregations
- Use window functions for ranking, running totals, and comparisons
- Build reusable CTEs, views, and stored procedures
- Apply transaction control for data integrity
- Clean and transform data with built-in SQL functions

## 👤 Author
**Stephen Omengo** — SQL practice portfolio, 2026.
