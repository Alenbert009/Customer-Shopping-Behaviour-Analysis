# Customer Shopping Behavior Analysis | End-to-End Retail Intelligence 🛒📊

---

## 📌 Project Overview
This end-to-end data analytics project analyzes customer shopping behavior using transactional data from 3,900 purchases across various product categories. The primary goal is to uncover actionable insights into spending patterns, customer segments, product preferences, and subscription behaviors to guide strategic business decisions.

## 🛠️ Tech Stack
* **Python:** Exploratory Data Analysis (EDA), data cleaning, and feature engineering using the `pandas` library and connecting to Postgre SQL.
* **PostgreSQL:** Advanced structured data analysis and querying of business transactions.
* **Power BI:** Interactive data visualization and dashboard creation.

## 📊 Dataset Summary
* **Size:** 3,900 rows and 18 columns.
* **Key Features:** Customer demographics (Age, Gender, Location, Subscription Status), Purchase details (Item, Category, Amount, Season, Size, Color), and Shopping behavior (Discount Applied, Promo Code, Frequency, Review Rating, Shipping Type).

## 🚀 Project Workflow

### 1. Exploratory Data Analysis (EDA) in Python
The project began with thorough data preparation and cleaning in Python.
* **Data Cleaning:** Checked for missing values and imputed 37 missing entries in the `Review Rating` column using the median rating of each respective product category.
* **Standardization:** Renamed columns to snake_case to ensure better readability and database compatibility.
* **Feature Engineering:** Created an `age_group` column by binning customer ages into distinct categories (Young Adult, Adult, Middle Aged, Senior). Additionally, generated a `purchase_frequency_days` column by mapping frequency strings (e.g., 'Weekly', 'Monthly') to numerical day values.
* **Database Integration:** Connected the Python script directly to PostgreSQL and loaded the cleaned DataFrame into the database to prepare for structured SQL analysis.

### 2. Data Analysis using SQL
Structured queries were executed in PostgreSQL to answer critical business questions and extract behavioral trends:
* **Revenue by Gender:** Revealed that male customers generated significantly higher total revenue ($157,890) compared to female customers ($75,191).
* **Shipping Comparison:** Compared average purchase amounts, noting Express shipping ($60.48) performed slightly higher than Standard shipping ($58.46).
* **Customer Segmentation:** Classified users into Loyal (3,116), Returning (701), and New (83) segments based on their purchase history.
* **Product Performance:** Identified the top 5 products by average review rating (Gloves, Sandals, Boots, Hat, Skirt) and extracted the top 3 most purchased items per individual category.
* **Subscription Analysis:** Discovered that non-subscribers actually represent a larger group of repeat buyers (2,518) than active subscribers (958).

### 3. Power BI Dashboard
An interactive Customer Behavior Dashboard was developed to provide stakeholders with a comprehensive view of the data.
* **Interactivity:** Features dynamic filtering capabilities by Subscription Status, Age Group, Category, Gender, and Shipping Type.
* **KPIs:** Highlights key metrics including 4K total customers, a $59.76 average purchase amount, and a 3.75 average review rating.
* **Visualizations:** Effectively visualizes Revenue by Age Group, Sales by Category, and a critical breakdown showing a 73% non-purchase rate among browsing customers.

## 💡 Business Recommendations
Based on the synthesized data, the following strategic actions are recommended:
1. **Target High-Value Age Groups:** Focus marketing campaigns, personalized product recommendations, and loyalty offers specifically on Young Adults and Middle-Aged customers, as they contribute the highest revenue.
2. **Reduce the High Non-Purchase Rate:** Introduce first-purchase discounts, retargeting ads, and reminder emails to actively convert the 73% of customers who browse but do not complete a transaction.
3. **Optimize Low-Performing Categories:** Increase overall visibility, offer appealing bundle deals, and run seasonal promotions for Footwear and Outerwear to improve category sales.
4. **Improve Customer Satisfaction:** Enhance service quality—focusing on delivery speed, packaging, and post-purchase support—to boost the average review rating of 3.75, increase customer trust, and drive repeat purchases.

## 📂 Repository Blueprint

The repository maintains a flat production-ready architecture, structured as follows:

```text
├── Customer Shopping Behavior Analysis report.pdf      # Enterprise analytical report (PDF)
├── Customer-Shopping-Behavior-Analysis.pptx         # Slide deck for executive stakeholders
├── Dashboard.pbix                                    # Production Power BI desktop application
├── README.md                                         # Comprehensive project documentation
├── background.jpg                                    # Custom UI dashboard canvas
├── customer_behavior_sql_queries.sql                # Secondary SQL analysis script
├── customer_shopping_behavior.csv                     # Raw transactional master dataset
├── customer_shopping_behavior_analysis.ipynb         # Python notebook for ETL, EDA & SQL loading
└── sql_queries_main.sql                              # Primary production SQL analysis script
