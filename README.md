# 📊 SQL Analytics & Data Quality (`dvdrental`)

## 📌 Project Overview
This repository contains a collection of analytical SQL queries and data validation scripts written for the sample **`dvdrental` database (PostgreSQL)**.

The primary goal of this project is to demonstrate practical skills in the following domains:
* **QA & Support (Data Integrity Verification):** Identifying "orphaned" records, anomalies, and broken relationships between tables.
* **Business Intelligence (BI):** Calculating key business metrics (store revenue, average transaction value, monthly sales trends).
* **Advanced SQL:** Utilizing Common Table Expressions (`CTE`), multi-level subqueries, and complex multi-table `JOIN`s.

---

## 🛠️ Tech Stack
* **DBMS:** PostgreSQL
* **Database:** `dvdrental` (a classic movie rental business simulator)
* **Tools:** DBeaver

---

## 🚀 Key Sections & Business Use Cases

### 1. Data Integrity & Anomaly Detection (QA / L2 Support)
* **Finding Rentals Without Payments:** Detecting "orphaned" records within a specific date range using `LEFT JOIN` and `IS NULL`.
* **Identifying Cities Without Stores:** Eliminating false positives in one-to-many relationships using subqueries (`NOT IN`).

### 2. Business Intelligence & Sales Reporting
* **Store & Staff Ranking:** Calculating total revenue broken down by physical store addresses (joining 4 relational tables).
* **Monthly Sales Trends:** Aggregating financial data with customized date formatting (`TO_CHAR`).
* **Average Ticket Size Analysis:** Calculating average payment amounts for the year 2006 with precision rounding (`ROUND`, `AVG`).

### 3. Advanced Analytics & Segmentation (CTE)
* **Customer Base Segmentation:** Identifying customers whose total number of rentals is strictly below the global average across the database, using **CTEs (`WITH`)**.

<details>
<summary><b>👀 View Sample Query Output for Customer Segmentation (click to expand)</b></summary>
<br>
<img width="1147" height="576" alt="Search_for_customers_with_rental_count_below_average" src="https://github.com/user-attachments/assets/7fbb1e25-7279-43b2-940e-33bfe1952edd" />

*Note: Showing partial result rows to demonstrate response structure. The overall database average is ~26.78 rentals.*

</details>

---

## 📂 Repository Structure
* `dvdrental_analytics_script.sql` - A single structured SQL script containing all annotated queries.
* `README.md` - Project documentation.
* `images` - Query execution result screenshots.

---

## 🛠️ Local Setup & Execution

1. Download and install the sample database: [**PostgreSQL `dvdrental`**](https://www.postgresqltutorial.com/postgresql-getting-started/postgresql-sample-database/).
2. Restore the database in PostgreSQL via `pg_restore` or your preferred GUI client (DBeaver / pgAdmin).
3. Open `dvdrental_analytics_script.sql` in your SQL editor and execute the queries.
