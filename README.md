# Credit_Card_Financials_Power_BI_Project
Creating and developing a thorough weekly dashboard for credit cards that offers stakeholders real-time insights into important performance indicators and patterns, allowing them to efficiently monitor and assess credit card operations.

# Credit-Card-Financials-Power-BI

<img src="https://github.com/Karthikc22/Credit_Card_Financials_Power_BI_Project/blob/main/Credit_Card_Transaction.jpg" width="40%" height="60%">  <img src="https://github.com/Karthikc22/Credit_Card_Financials_Power_BI_Project/blob/main/CC_Customer_Report.jpg" width="40%" height="60%">

### Projective Objective 
To create a thorough weekly dashboard for credit cards that offers stakeholders real-time insights into important performance indicators and patterns, allowing them to efficiently monitor and assess credit card operations.


### Steps included 
1. Understanding data and requirements
2. Import data to SQL Database
3. Connecting SQL Database to power BI
4. Data cleaning in power query
5. Writing DAX Measures
6. Creating Dashboards in Power BI
7. Deriving project insights



### Understanding data and requirements
1. Brief understanding of data is very important before starting the actual work.
2. We have data related to credit card transactions on a weekly basis.
3. Also we have customer details on a weekly basis.
4. Went thoroughly through the data and understood what to be done further.
5. Generated few ideas on which columns to be used further to derive insights.



### Import data to SQL Database
1. Prepare CSV files.
2. Create Database in PostgreSQL.
3. Create tables in SQL.
4. Import CSV file into SQL.

### Credit_card_transaction_data : 
    https://github.com/Karthikc22/Credit_Card_Financials_Power_BI_Project/blob/main/credit_card.csv
    
### Customer_data : 
    https://github.com/Karthikc22/Credit_Card_Financials_Power_BI_Project/blob/main/customer.csv
    
### Additional_data :
    https://github.com/Karthikc22/Credit_Card_Financials_Power_BI_Project/blob/main/cc_add.csv
    https://github.com/Karthikc22/Credit_Card_Financials_Power_BI_Project/blob/main/cust_add.csv

   

### Connecting SQL Database to power BI
1. Database from PostgreSQL should be connected to Power BI
2. Further work like data cleaning and modeling is done in power query



### Data cleaning in power query
1. Before creating dashboard data is cleaned in the Power query
2. Data loaded to power BI is further taken to power query and performed data cleaning and data modeling



### Writing DAX Measures

1. query 1
   
   AgeGroup = SWITCH(
TRUE(),
'public cust_detail'[customer_age] < 30, "20-30",
'public cust_detail'[customer_age] >= 30 && 'public cust_detail'[customer_age] < 40,
"30-40",
'public cust_detail'[customer_age] >= 40 && 'public cust_detail'[customer_age] < 50,
"40-50",
'public cust_detail'[customer_age] >= 50 && 'public cust_detail'[customer_age] < 60,
"50-60",
'public cust_detail'[customer_age] >= 60, "60+",
"unknown"
)I
ncomeGroup = SWITCH(
TRUE(),
'public cust_detail'[income] < 35000, "Low",
'public cust_detail'[income] >= 35000 && 'public cust_detail'[income] <70000, "Med",
'public cust_detail'[income] >= 70000, "High",
"unknown"
)


2. query 2
   
   week_num2 = WEEKNUM('public cc_detail'[week_start_date])
Revenue = 'public cc_detail'[annual_fees] + 'public
cc_detail'[total_trans_amt] + 'public cc_detail'[interest_earned]
Current_week_Reveneue = CALCULATE(
SUM('public cc_detail'[Revenue]),
FILTER(
ALL('public cc_detail'),
'public cc_detail'[week_num2] = MAX('public cc_detail'[week_num2])))
Previous_week_Reveneue = CALCULATE(
SUM('public cc_detail'[Revenue]),
FILTER(
ALL('public cc_detail'),
'public cc_detail'[week_num2] = MAX('public
cc_detail'[week_num2])-1))



###  Creating Dashboards in Power BI
<img src="https://github.com/Karthikc22/Credit_Card_Financials_Power_BI_Project/blob/main/Credit_Card_Transaction.jpg" width="80%" height="60%"> ## Credit_card_financials_dashboard
   https://github.com/Karthikc22/Credit_Card_Financials_Power_BI_Project/blob/main/Credit_Card_Transaction.jpg
   

<img src="https://github.com/Karthikc22/Credit_Card_Financials_Power_BI_Project/blob/main/CC_Customer_Report.jpg" width="80%" height="60%"> ## Customer_details_weekly_dashboards
   https://github.com/Karthikc22/Credit_Card_Financials_Power_BI_Project/blob/main/CC_Customer_Report.jpg


### Deriving project insights

1.  Revenue increased by 28.8%
2.  Overall revenue is 57M
3.  Total interest is 8M
4.  Total transaction amount is 46M
5.  Male customers are contributing more in revenue 31M, female 26M
6.  Blue & Silver credit card are contributing to 93% of overall transactions
7.  TX, NY & CA is contributing to 68%
8.  Overall Activation rate is 57.5%
9.  Overall Delinquent rate is 6.06%


## Skills
### Learnt Power BI fundamentals
  1. Creation of calculation columns and DAX measurements
  2. Making use of data modeling, data validation techniques, and KPI indicators
  3. Titles that vary according to the standards that are applied
  4. PowerBI services for publishing and exchanging reports online
  5. Data via the gateway's auto-refresh configuration
  6. Making a date table with the M language


### Tech Stacks
  1. SQL
  2. PowerBI
  3. Power Query
  4. DAX Meaures
  5. Dax studio( TO REDUCE FILE SIZE)
  6. Project Charter file
  7. stakeholder management
  8. Data and Business Analysis


### Live Dashboard Link:


### Checkout the project on linked in:


###  Dashboards:
https://github.com/Karthikc22/Credit_Card_Financials_Power_BI_Project/blob/main/Credit_Card_financial_Report.pbix

###  Insights_generated
Report: https://github.com/Karthikc22/Credit_Card_Financials_Power_BI_Project/blob/main/Credit%20card%20Financials.pdf



