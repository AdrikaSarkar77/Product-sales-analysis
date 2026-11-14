# Product-sales-analysis
Developed an interactive Sales &amp; Management Dashboard using Microsoft Excel , MySQL and Power BI to analyze sales performance, profit trends, customer insights, and business KPIs. Utilized Pivot Tables, Pivot Charts, Slicers, and data visualization techniques to transform raw data into actionable business insights.
# Product Sales Analysis – Excel Dashboard & MySQL

## Project overview
This project analyzes product sales transactions using an Excel dashboard and MySQL queries.

## Repository files
- `Product-Sales.xlsx` – original workbook containing the dataset (`Sheet1`), dashboard, pivot table and detail sheets.
- `product_sales_mysql.sql` – MySQL 8.0+ script that creates the database and table, loads the source records, adds indexes, and includes dashboard-style analysis queries.
- `README.md` – project documentation and setup instructions.

## Dataset
- Source sheet: `Sheet1`
- Records loaded: 1,500
- Columns: 20
- Date range: 2023-01-01 to 2025-06-30
- Primary key: `OrderID`
- Missing `Promotion` values are retained as SQL `NULL`.
- The trailing blank spreadsheet row is excluded. Category text is preserved as it appears in the source workbook.

## Tools
- Microsoft Excel (dataset, pivot tables and dashboard)
- MySQL 8.0+ / MySQL Workbench
- Git and GitHub

## Run the SQL script
1. Open MySQL Workbench and connect to your MySQL Server.
2. Select **File → Open SQL Script**.
3. Open `product_sales_mysql.sql`.
4. Click the lightning-bolt **Execute** button.
5. The script creates and selects `product_sales_db`, creates `product_sales`, imports the 1,500 records, and runs validation and analysis queries.
6. Verify the import with:
   ```sql
   USE product_sales_db;
   SELECT COUNT(*) FROM product_sales;
   ```

## Included SQL analysis
- KPI summary: orders, units sold, total sales, average order value and returned orders
- Sales by year and month
- Sales by region, product, store and salesperson
- Sales by customer type and payment method
- Return and promotion analysis
- Top 10 customers
- Average delivery duration

## Suggested GitHub repository structure
```text
Product-Sales-Analysis/
├── dataset/
│   └── Product-Sales.xlsx
├── sql/
│   └── product_sales_mysql.sql
└── README.md
```

The dashboard and pivot tables are already inside `Product-Sales.xlsx`, so upload that workbook once under `dataset/`; a separate duplicate dashboard file is not needed.

## Notes
This SQL script targets MySQL 8.0+. It preserves the source workbook's category values rather than silently normalizing them. The Excel workbook remains the source of the dashboard and pivot tables.
