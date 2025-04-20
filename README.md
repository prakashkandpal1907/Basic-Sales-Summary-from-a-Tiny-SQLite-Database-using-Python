# Basic-Sales-Summary-from-a-Tiny-SQLite-Database-using-Python
Use SQL inside Python to pull simple sales info (like total quantity sold, total revenue), and display it using basic print statements and a simple bar chart.
# 🛒 Task 7: Basic Sales Summary Using SQLite and Python

## 📌 Objective
This task was completed as part of a Data Analyst Internship. The goal was to create a simple SQLite database, run basic SQL queries in Python, and visualize sales data.

---

## 🧰 Tools Used
- Python
- SQLite3
- pandas
- matplotlib

---

## 🗂️ Dataset
A sample SQLite database (`sales_data.db`) was created with one table:

**Table: `sales`**
| Column   | Type    |
|----------|---------|
| product  | TEXT    |
| quantity | INTEGER |
| price    | REAL    |

Sample data includes 3 products (`Product A`, `Product B`, `Product C`) with varying quantities and prices.

---

## 📊 What This Script Does
1. Connects to a SQLite database
2. Creates and populates a `sales` table
3. Runs an SQL query to get:
   - Total quantity sold per product
   - Total revenue per product
4. Loads data into a pandas DataFrame
5. Prints the result
6. Visualizes revenue per product using a bar chart

---

## 🧠 SQL Used
```sql
SELECT 
    product, 
    SUM(quantity) AS total_quantity, 
    SUM(quantity * price) AS total_revenue
FROM sales
GROUP BY product;

