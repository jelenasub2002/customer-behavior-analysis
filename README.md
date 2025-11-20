🛍️ Customer Shopping Behavior Analysis
🔍 Overview

This project provides an end-to-end analysis of customer shopping behavior using Python for data preprocessing and SQL for business analytics.
The goal is to clean and transform raw customer data, meaningful features, and answer key business questions related to spending patterns, discount usage, product performance, customer segmentation, and revenue contribution.

📁 Dataset

The dataset was loaded using Python and contains information on:

Customer demographics

Product categories and items purchased

Purchase amounts

Shipping type

Discounts and promo code usage

Review ratings

Frequency and history of purchases

Dataset preparation steps performed in Python:

Loaded dataset: customer_shopping_behavior.csv

Checked structure (info()), statistics (describe()), and missing values

Imputed missing review ratings using median per product category

Standardized all column names to lowercase and snake_case

Renamed purchase_amount_(usd) → purchase_amount

Created age groups using qcut (Young Adult, Adult, Middle-aged, Senior)

Mapped purchase frequency categories to numerical days

Identified duplicate discount fields and removed promo_code_used

Exported cleaned dataset as:

customer_behavior.csv

🛠️ Tools & Technologies

Python (Pandas)

SQL Server

Google Colab

CSV-based data storage

🔄 Project Steps
1️⃣ Data Loading (Python)

Performed in the notebook/script:

Read CSV into Pandas

Displayed first rows with head()

Inspected datatypes and missing values using info() and isnull().sum()

2️⃣ Exploratory Data Analysis

Basic descriptive statistics (describe())

Checked rating distribution and missing patterns

Evaluated discount-related fields and redundancy

3️⃣ Data Cleaning

Performed using Pandas transformations:

Median imputation for review_rating grouped by category

Cleaned and standardized column names

Created new derived fields:

age_group (quantile-based segmentation)

purchase_frequency_days (mapped numerical encoding)

Confirmed and removed duplicate column

Exported cleaned dataset for SQL analysis

4️⃣ SQL Analysis

After importing customer_behavior.csv into SQL Server (dbo.customer_behavior), several analytical queries were executed:

✔️ Key SQL operations:

Aggregations (SUM, AVG, COUNT)

Filtering with WHERE

Window functions (ROW_NUMBER())

Subqueries (AVG comparison)

CASE expressions (customer segmentation)

Grouped ranking and product performance analysis

✔️ Business questions answered:

Revenue by gender

Discount users who spent above average

Top 5 highest-rated products

Standard vs Express shipping spending

Subscriber vs non-subscriber revenue and average spend

Top discounted products

Customer segmentation: New, Returning, Loyal

Top 3 items per category using window functions

Do repeat buyers subscribe?

Revenue contribution by age group

5️⃣ Reporting

Insights can be exported and visualized through:

Power BI (dashboard-ready dataset)

SQL outputs for trend evaluation

Presentation (optional) based on extracted insights

📈 Results

The project provided insights such as:

Spending differences across gender, shipping types, and age groups

Which products receive the highest ratings

The relationship between subscription status and spending

Discount usage patterns across categories

Identification of top and loyal customer segments

These insights support business decisions related to pricing strategy, product ranking, targeted marketing, and customer retention.
