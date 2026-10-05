# Financial Fraud Analytics: AML Typology Benchmarking

This is a personal project where I benchmark **SQL (DuckDB)** against **Pandas** using the PaySim dataset to identify high-risk financial transaction patterns for Anti-Money Laundering (AML) monitoring.

---

##  What's Done So Far (Day 1)

### Day 1: High-Risk CASH_IN Transactions (Structuring / Smurfing)
In the first part of this project, I focused on analyzing high-risk `CASH_IN` transactions to spot potential structuring activities. Large or frequent cash deposits are often a primary red flag in transaction monitoring systems.

**Key Metrics Tracked:**
* `customer_id`: Unique identifier for the account originating the transaction.
* `total_txn_count`: Total number of `CASH_IN` transactions made by the customer.
* `total_amount`: Total value of cash deposited into the account.
* `avg_txn_amount`: Average deposit size.
* `max_single_txn`: The largest single deposit recorded for that account.

---

##  Quick Performance Comparison

I tested the same analytical query on both DuckDB and Pandas to compare their efficiency on large CSV files:

* **DuckDB (SQL):** ~0.54 seconds
* **Pandas:** ~5,12 seconds

**Takeaway:** DuckDB is noticeably faster for querying CSV data directly without needing to load the entire dataset into memory first.


```text
├── 01_Structuring_Analysis.ipynb   # Day 1 SQL vs Pandas analysis
├── README.md                       # Project overview
