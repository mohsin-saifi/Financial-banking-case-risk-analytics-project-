# Financial-banking-case-risk-analytics-project-
Power BI Banking Risk Analytics Dashboard analyzing loans, deposits, fees, and client engagement using Excel, SQL, Python, and DAX. Demonstrates data modeling,
KPI design, and how banks use data visualization and risk analytics to make better lending decisions from customer profiles.
Banking Risk Analytics Dashboard (Power BI)

This project demonstrates how banks can use Risk Analytics and Data Visualization to make better lending decisions using customer data. The dashboard is built in Power BI with data prepared using Excel, SQL, and Python and advanced calculations using DAX.

Project documentation and dashboard flow are based on the report provided here: 

Banking Report summary

📌 Problem Statement

Banks face the challenge of minimizing the risk of losing money while lending to customers. This project shows how analyzing client profiles, loans, deposits, and engagement data helps banks decide whether a customer is likely to repay a loan.

🎯 Project Objective

Analyze banking data to understand loan and deposit patterns

Track customer engagement with the bank

Measure important banking KPIs

Build dashboards that help in risk-based lending decisions

🗂️ Dataset Overview

The dataset consists of multiple related tables:

Banking Relationship

Client Banking

Gender

Investment Advisor

Period

These tables are connected using primary and foreign keys for proper data modeling.

🧹 Data Cleaning & Feature Engineering

New analytical columns created:

Engagement Timeframe – Duration of client relationship

Engagement Days – Days since client joined (using DATEDIFF)

Income Band – Low, Mid, High based on estimated income

Processing Fees – Derived from Fee Structure using SWITCH

🧮 Important DAX Calculations
Total Clients = DISTINCTCOUNT('Clients - Banking'[Client ID])

Total Loan = [Bank Loan] + [Business Lending] + [Credit Cards Balance]

Total Fees =
SUMX(
    'Clients - Banking',
    [Total Loan] * 'Clients - Banking'[Processing Fees]
)


DAX functions used:

SUM

SUMX

DISTINCTCOUNT

SWITCH

DATEDIFF

📊 Key KPIs in Dashboard

Total Clients

Total Loan

Bank Loan

Business Lending

Total Deposit

Total Fees

Checking Account Amount

Savings Account Amount

Foreign Currency Account

Credit Card Balance

Engagement Length

📈 Dashboard Pages

Home Dashboard – Overall KPIs

Loan Analysis – Loan insights by gender, relationship, nationality

Deposit Analysis – Account-wise deposit insights

Summary Dashboard – Complete banking overview

💡 Insights Derived

Private banks have more clients

Income band influences loan and deposit behavior

Engagement length impacts customer value

Certain nationalities hold higher loan values

Processing fees contribute significantly to revenue

🛠️ Tools & Technologies Used

Excel – Data preparation

SQL – Data extraction & transformation

Python – Data handling

Power BI – Dashboard & visualization

DAX – KPI and calculated measures

Data Modeling – Relationship building

✅ Conclusion

This project shows how Power BI dashboards can be used in the banking sector for risk analytics, KPI monitoring, and data-driven lending decisions.
