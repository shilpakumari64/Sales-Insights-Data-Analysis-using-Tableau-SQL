# Sales-Insights-Data-Analysis-using-Tableau-SQL
Welcome to my GitHub repository for the Sales Insights project, where I performed data analysis using Tableau and SQL. This project focuses on analyzing the sales data of an India-based hardware company and drawing valuable insights to aid in decision-making.

About the Project :

The Sales Insights project involves analyzing the sales data of an India-based hardware company. I developed ETL mappings using SQL to extract data from unstructured sources and transform it into a staging area for data cleaning. Furthermore, I designed a star schema data model on Tableau to facilitate efficient analysis. The project culminates in a Tableau dashboard that provides visualizations and insights based on various parameters affecting the company's performance year on year.

Technologies Used ⚙
Advance Excel
MySQL | SQL Server
Tableau 
Statistics
Project - India-based Hardware Company Sales Insights - Data Analysis
Tableau Dashboard Link: https://public.tableau.com/app/profile/shilpa.kumari.m/viz/SalesInsights-DataAnalysisProjectusingTableau_16844068501830/Dashboard-RevenueAnalysis

Problem Statements :
During the analysis, the following problem statements were addressed:

Q1. Revenue breakdown by cities.

Q2. Revenue breakdown by years and months.

Q3. Top 5 customers by revenue and sales quantity.

Q4. Top 5 products by revenue.

Q5. Net Profit and Profit Margin by Market

Approach - Project Planning & Aims Grid
Purpose: The project aims to unlock sales insights that were previously unseen, providing decision support for the sales team and automating processes to reduce manual data gathering efforts.

Stakeholders: The stakeholders involved in this project include the Sales Director, I.T. Team, Customer Service Team, and Data & Analytics Team.

End Result: The objective is to develop an automated dashboard that offers quick and up-to-date sales insights to support data-driven decision-making.

Success Criteria: The success criteria for this project are as follows:

Dashboards that uncover sales order insights with the latest available data.
Sales team able to make better decisions and achieve 10% cost savings of the total spend.
Sales analysts no longer manually gather data, saving 20% of their business time to reinvest in value-added activities.
Data Analysis - Approach
To set up and perform the data analysis, follow these steps:

Setup Process :

Download the file: db_dump.xlsx

Import the file into MySQL and perform ETL (Extract, Transform, Load) if required.

Download Tableau Public (Free) or Tableau Desktop (14-day trial) for data analysis.

Connect Tableau with the MySQL or Excel database.

Save the file as .twb or .twbx.

Data Analysis Using SQL :
Here are some SQL queries that can be used for data analysis:


-- Show all customer records
SELECT * FROM customers;

-- Show the total number of customers
SELECT COUNT(*) FROM customers;

-- Show transactions for Chennai market (market code for Chennai is Mark001)
SELECT * FROM transactions WHERE market_code='Mark001';

-- Show distinct product codes that were sold in Chennai.
SELECT DISTINCT product_code FROM transactions WHERE market_code='Mark001';

-- Show transactions where the currency is US dollars.
SELECT * FROM transactions WHERE currency='USD';

-- Show transactions in 2020 joined by the date table.
SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date = date.date WHERE date.year = 2020;

-- Show total revenue in the year 2020.
SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date = date.date WHERE date.year = 2020 AND (transactions.currency = 'INR' OR transactions.currency = 'USD');

-- Show total revenue in the year 2020, January Month.
SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date = date.date WHERE date.year = 2020 AND date.month_name = 'January' AND (transactions.currency = 'INR' OR transactions.currency = 'USD');

-- Show total revenue in the year 2020 in Chennai.
SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date = date.date WHERE date.year = 2020 AND transactions.market_code = 'Mark001';


Tableau Dashboard - Revenue Analysis

Revenue Analysis Dashboard

Tableau Dashboard - Profit Analysis

Profit Analysis Dashboard

Feel free to explore the code and dashboards in this repository to gain insights into the sales performance of the India-based hardware company.

