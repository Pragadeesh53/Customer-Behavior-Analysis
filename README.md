# 🛍️ Customer Shopping Behavior Analysis

### 📘 Project Overview

This project analyzes **customer shopping behavior** using transactional data from **3,900 purchases** across multiple product categories.
The main objective is to uncover insights into **spending patterns**, **customer segments**, **product preferences**, and **subscription behavior** — helping businesses make informed, data-driven decisions.

---

## 📊 Dataset Summary

| Attribute          | Description                                                                                                                                                                                                                                                        |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Rows**           | 3,900                                                                                                                                                                                                                                                              |
| **Columns**        | 18                                                                                                                                                                                                                                                                 |
| **Key Features**   | Customer demographics (Age, Gender, Location, Subscription Status), Purchase details (Item Purchased, Category, Purchase Amount, Season, Size, Color), Shopping behavior (Discount Applied, Promo Code Used, Review Rating, Frequency of Purchases, Shipping Type) |
| **Missing Values** | 37 missing entries in the `review_rating` column                                                                                                                                                                                                                   |

---

## 🧹 Data Cleaning & Preparation (Python)

Performed preprocessing and transformation using **Pandas**:

* Imported dataset and explored with `.info()` and `.describe()`
* Handled missing values by imputing **median review rating per category**
* Standardized column names using **snake_case**
* Engineered new columns:

  * `age_group` → grouped by quantiles
  * `purchase_frequency_days` → converted from categorical to numeric (e.g., weekly → 7 days)
* Removed redundant fields (`promo_code_used`)
* Connected to **PostgreSQL** database using **SQLAlchemy** for structured analysis

---

## 🧩 SQL-Based Business Analysis

Conducted advanced analysis in **PostgreSQL** to derive actionable insights:

| #  | Analysis Goal                      | Description                                                           |
| -- | ---------------------------------- | --------------------------------------------------------------------- |
| 1  | **Revenue by Gender**              | Compare total revenue between male and female customers               |
| 2  | **High-Spending Discount Users**   | Identify customers who use discounts but spend above average          |
| 3  | **Top 5 Products by Rating**       | Find items with highest average review rating                         |
| 4  | **Shipping Type Analysis**         | Compare average purchase amount between standard and express shipping |
| 5  | **Subscribers vs Non-Subscribers** | Compare average and total spending by subscription status             |
| 6  | **Discount-Dependent Products**    | Find products with highest percentage of discounted purchases         |
| 7  | **Customer Segmentation**          | Categorize customers into New, Returning, and Loyal segments          |
| 8  | **Top 3 Products per Category**    | Identify top-selling products in each category                        |
| 9  | **Repeat Buyers vs Subscriptions** | Check if frequent buyers are more likely to subscribe                 |
| 10 | **Revenue by Age Group**           | Measure total revenue by different age segments                       |

---

## 📈 Power BI Dashboard

Developed an interactive **Power BI Dashboard** showcasing:

* Total revenue by **gender** and **age group**
* **Top products** by rating and discount percentage
* **Subscription-based** revenue distribution
* Purchase **frequency** trends and category performance

---

## 💡 Business Recommendations

* **Boost Subscriptions:** Promote exclusive benefits for subscribers
* **Loyalty Programs:** Reward repeat buyers to encourage retention
* **Review Discount Policy:** Maintain a balance between sales volume and profit margins
* **Product Positioning:** Highlight top-rated and best-selling products in marketing campaigns
* **Targeted Marketing:** Focus on high-revenue age groups and express-shipping users

---

## 🛠️ Tech Stack

* **Languages:** Python, SQL
* **Libraries:** Pandas, SQLAlchemy
* **Database:** MySQL
* **Visualization:** Power BI
* **Tools:** Jupyter Notebook, DBeaver

---

## 🚀 How to Run

1. Clone this repository

   ```bash
   git clone https://github.com/<your-username>/customer-shopping-behavior-analysis.git
   cd customer-shopping-behavior-analysis
   ```
2. Install dependencies

   ```bash
   pip install pandas sqlalchemy pymysql psycopg2
   ```
3. Update database credentials in your Python script
4. Run the Python notebook to clean and load data
5. Open Power BI to visualize the final dashboard

---

## 📂 Project Structure

```
├── data/
│   └── customer_shopping_data.csv
├── notebooks/
│   └── data_cleaning_and_analysis.ipynb
├── sql/
│   └── business_queries.sql
├── dashboard/
│   └── customer_behavior.pbix
├── README.md
└── requirements.txt
```

---

## 👤 Author

**Pragadeesh N**
💼 Data Analyst | 📊 SQL | 🐍 Python | 📈 Power BI

📫 *Reach me on GitHub or LinkedIn for collaboration!*
