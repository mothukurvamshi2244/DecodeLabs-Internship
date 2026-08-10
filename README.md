
# 📊 E-Commerce Sales Data Analysis
Turning raw transactional data into meaningful business insights








### 👋 Project Overview

This project demonstrates an end-to-end Exploratory Data Analysis (EDA) workflow on an e-commerce transactional dataset.

The objective was to transform raw order-level data into structured, reliable information and uncover patterns around sales performance, products, customer activity, order status, referral sources, and sales trends over time.

Rather than simply generating charts, the project follows an analytical workflow:

Raw Data → Data Quality → Cleaning → EDA → KPIs → Trends → Business Insights

The dataset contains 1,200 orders across 14 attributes, including product, quantity, unit price, payment method, order status, coupon usage, referral source, and total price.

### 🎯 Business Objectives

The analysis was designed to answer questions such as:

What is the overall sales performance?
What is the average order value?
Which products generate the most orders?
How are orders distributed across different statuses?
Which referral sources generate the most activity?
How do sales change over time?
Are there missing values or duplicate records?
What data-quality issues need to be addressed before analysis?
### 📁 Dataset

The dataset contains 1,200 records and 14 columns.

Key Variables
Category	Variables
Order Information	OrderID, Date, OrderStatus
Customer Information	CustomerID, ShippingAddress
Product Information	Product, Quantity, UnitPrice
Cart & Revenue	ItemsInCart, TotalPrice
Marketing	CouponCode, ReferralSource
Payment & Fulfillment	PaymentMethod, TrackingNumber

The notebook confirms that the numerical analysis focused on Quantity, UnitPrice, ItemsInCart, and TotalPrice.

### 🧹 Data Cleaning & Quality Checks

A major part of the project was ensuring the dataset was reliable before extracting insights.

Data-quality checks performed
Checked dataset dimensions
Inspected column names
Validated data types
Identified missing values
Handled missing coupon information
Checked duplicate rows
Checked duplicate Order IDs
Validated date format
Converted numerical columns into numeric format
Removed unnecessary whitespace from text fields
Performed final validation checks
Missing Values

The only missing field identified was CouponCode, with 309 missing records.

These values were handled by replacing them with:

No Coupon

After cleaning, the dataset contained zero missing values.

Duplicate Validation

The analysis found:

Duplicate rows: 0
Duplicate Order IDs: 0
Invalid dates: 0

This provided a clean foundation for downstream analysis.

### 📈 Key Performance Indicators

The analysis produced several important business metrics.

KPI	Result
Total Orders	1,200
Total Sales	$1,264,761.96
Average Order Value	$1,053.97
Minimum Order Value	$11.39
Maximum Order Value	$3,456.40
Average Quantity per Order	2.95
Average Items in Cart	5.49
The calculated total sales were $1,264,761.96, while the average order value was approximately $1,053.97.
### 🛍️ Product Analysis

Product-level order analysis showed the following distribution:

Product	Orders
🖨️ Printer	181
📱 Tablet	179
🪑 Chair	178
💻 Laptop	173
🗄️ Desk	170
🖥️ Monitor	163
📱 Phone	156

Printer recorded the highest number of orders, followed closely by Tablet and Chair.

### 📦 Order Status Analysis

Order status distribution was also examined to understand the order lifecycle.

Status	Orders
Cancelled	250
Returned	247
Pending	237
Shipped	235
Delivered	231

The distribution highlights the importance of monitoring cancellations, returns, pending orders, and successful deliveries as part of operational performance analysis.

### 📣 Referral Source Analysis

The project also investigated the sources contributing to customer/order activity.

Referral Source	Orders
Instagram	259
Email	250
Google	241
Facebook	228
Referral	222

Instagram generated the highest number of orders among the referral sources analyzed.

### 📅 Time-Series Analysis

The project extracted:

Month
Year

from the transaction date and used them to analyze sales patterns over time.

Yearly sales were calculated using:

yearly_sales = df.groupby("Year")["TotalPrice"].sum()

A bar chart was then created to visualize the Yearly Sales Trend.

### 🔎 Exploratory Data Analysis

The analysis included descriptive statistics for the major numerical variables.

Distribution Summary
Metric	Mean	Median
Quantity	2.95	3.00
Unit Price	$356.41	$364.21
Items in Cart	5.49	5.00
Total Price	$1,053.97	$823.62

The difference between mean and median Total Price provides an important signal for investigating the distribution of order values and potential high-value transactions.

### 💡 Business Insights

Based on the analysis, several practical observations emerged:

1. Strong overall sales volume

The dataset generated approximately $1.26M in total sales, demonstrating substantial transaction value across the analyzed orders.

2. Printer leads product order volume

Printer had the highest order count with 181 orders, making it an important product for inventory and sales monitoring.

3. Instagram is the strongest referral source

Instagram generated 259 orders, slightly ahead of Email at 250, suggesting strong customer acquisition activity through social media.

4. Order-status distribution requires attention

Cancelled and returned orders accounted for a substantial portion of the dataset, indicating that fulfillment and customer-experience metrics could be valuable areas for deeper analysis.

5. Order values show variation

The average order value was approximately $1,054, while the median was approximately $824, suggesting that higher-value orders influence the average.

### 🧰 Tech Stack
Programming
Python
Data Analysis
Pandas
NumPy
Visualization
Matplotlib
Development Environment
Jupyter Notebook
🧠 Skills Demonstrated

This project demonstrates practical experience in:

Exploratory Data Analysis
Data Cleaning
Data Quality Validation
Missing Value Treatment
Duplicate Detection
Data Type Validation
Descriptive Statistics
KPI Calculation
Aggregation & Grouping
Time-Series Analysis
Product Analysis
Order Analysis
Marketing/Referral Analysis
Data Visualization
Business Insight Generation

### 📂 Project Structure
E-Commerce-Sales-Analysis/

├── 📊 Dataset for Data Analytics.xlsx

├── 📓 DecodeLabsP1.ipynb

├── 📓 DecodeLabsP2.ipynb

└── 📄 README.md

### Notebook 1 — Data Cleaning
DecodeLabsP1.ipynb

Focuses primarily on:

Data inspection
Missing-value treatment
Duplicate validation
Date validation
Data-type conversion
Text cleaning
Final data-quality checks

### Notebook 2 — Exploratory Data Analysis
DecodeLabsP2(2).ipynb

Focuses on:

Descriptive statistics
Sales KPIs
Product analysis
Order-status analysis
Referral-source analysis
Time-based analysis
Sales visualization

### 🚀 Analytical Workflow
                 ┌──────────────────┐
                 │    Raw Dataset   │
                 └────────┬─────────┘
                          ↓
                 ┌──────────────────┐
                 │ Data Inspection  │
                 └────────┬─────────┘
                          ↓
                 ┌──────────────────┐
                 │ Data Cleaning    │
                 │ & Validation     │
                 └────────┬─────────┘
                          ↓
                 ┌──────────────────┐
                 │ Exploratory      │
                 │ Data Analysis    │
                 └────────┬─────────┘
                          ↓
                 ┌──────────────────┐
                 │ KPI & Trend      │
                 │ Analysis         │
                 └────────┬─────────┘
                          ↓
                 ┌──────────────────┐
                 │ Business         │
                 │ Insights         │
                 └──────────────────┘
### 🎯 Why This Project Matters

A good analyst does more than calculate numbers.

This project demonstrates the ability to move from:

Raw Data → Reliable Data → Analysis → Insights → Business Understanding

The focus was not only on writing Python code, but on understanding what the data says and how those findings could support business decisions.

### 👨‍💻 About Me

Vamshi Goud
Aspiring Data Analyst | 

I enjoy using data to understand business problems, identify patterns, and communicate insights clearly.

Core Skills

Python · Pandas · NumPy · SQL · Excel · Power BI · Data Visualization · EDA
