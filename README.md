# Sales Insights and Data Analysis of a Hardware Company

# Problem Statement :
In This project Created Tableau Dashboards which help to generate important sales insight. this dashboards visualize the data on the basis of sales, profit, customer type and region.

# Used Tools:
- Mysql
- Mysql Workbench
- Tableau Desktop

# Steps involved in the project:

- Importing csv file in MYsql and performing queries to get initial sales insights.
- Connecting the MYsql database in Tableau and performing data cleaning and data transformation.
- Creating measures.
- Building Tableau Dashboard.

# Performed SQL queries
  - Show all customer records

    `SELECT * FROM customers;`

  - Show total number of customers

    `SELECT count(*) FROM customers;`

  - Show transactions for Chennai market (market code for chennai is Mark001)

    `SELECT * FROM transactions where market_code='Mark001';`

  - Show distrinct product codes that were sold in chennai

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

  - Show transactions where currency is US dollars

    `SELECT * from transactions where currency="USD"`

  - Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

  - Show total revenue in year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
  - Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

  - Show total revenue in year 2020 in Chennai

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark001";`





![T dashbord 1](https://github.com/nild-ds/SQL-Tableau-project/assets/167008575/646165f3-103b-4358-ab1f-4bcaef8bc50a)


![T dashbord 2](https://github.com/nild-ds/SQL-Tableau-project/assets/167008575/492e340a-07a7-4867-b49f-2181f9979c6a)
