# Task7
Tiny SQLite Database using Python
Objective:
Use SQL inside Python to pull simple sales information (like total quantity sold, total revenue), and display it using basic print statements and a bar chart.

 Tools Used:
Python (built-in sqlite3, pandas, matplotlib)
SQLite (no external setup needed)
Jupyter Notebook or .py script

 Dataset:
A small SQLite database file sales_data.db with one table:
Table Name: sales
Table Columns:
id (INTEGER, Primary Key)
date (TEXT)
product (TEXT)
quantity (INTEGER)
price (REAL)
 Steps Performed:
Create SQLite Database (sales_data.db):
Created using sqlite3.connect()
Created a sales table
Inserted sample data (laptop, mouse, keyboard)

Write and Execute SQL Query:
Queried total quantity and revenue per product:
SELECT product, 
       SUM(quantity) AS total_qty, 
       SUM(quantity * price) AS revenue 
FROM sales 
GROUP BY product;
Load into Pandas:
Used pd.read_sql_query() to load SQL results into a DataFrame

Display Output:
Printed the DataFrame to show total sales summary
Plot a Bar Chart:
Used matplotlib to create and save a bar chart (sales_chart.png)

 Output:
Console: Total quantity and revenue per product
Image: sales_chart.png (bar chart of revenue by product)


