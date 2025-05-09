# ISTM 624 – Kaggle Dataset Project

**Course:** ISTM 624 – Databases and Big Data Management
**Project:** Kaggle Dataset Project

## 📊 Project Overview

This project analyzed three diverse datasets from Kaggle to uncover business insights through predictive modeling and clustering techniques. Each dataset addressed a different business domain—revenue forecasting, digital marketing, and customer segmentation—using tools such as SQL, R, and RapidMiner.

---

## 🧾 Report Breakdown

### 1. 📥 Data Description

- **Dataset 1:** *Coffee Shop Daily Revenue* – Numeric data representing daily performance across 2000 days. (https://www.kaggle.com/datasets/himelsarder/coffee-shop-daily-revenue-prediction-dataset)
- **Dataset 2:** *Advertisement Click Dataset* – Behavioral and demographic data, including user engagement with ads.  (https://www.kaggle.com/datasets/gabrielsantello/advertisement-click-on-ad)
- **Dataset 3:** *Food App Business Data* – Purely numeric dataset with 2205 rows and 27 features about customer transactions, behaviors, and promotions. (https://www.kaggle.com/datasets/ybifoundation/food-app-business)

Each dataset was stored in a single table with a well-defined primary or composite key to ensure uniqueness.

---

### 2. 🔍 Analysis Approach & Results

#### ☕ Coffee Shop Revenue
- **Objective:** Identify top drivers of daily revenue.
- **Method:** Linear Regression (via RapidMiner)
- **Key Findings:**
  - **Most important drivers:** Average Order Value, Customer Count, Marketing Spend
  - **Insights:** Average order value had the highest coefficient (242.026). Operating hours, employee count, and foot traffic were not significant.

#### 📢 Advertisement Click-Throughs
- **Objective:** Analyze user engagement with online ads.
- **Method:** Logistic Regression (via R) and SQL aggregation
- **Key Findings:**
  - Lower-income users and short-time online users had the highest ad click rates.
  - Higher-income users and long-time internet users showed significantly lower engagement.

#### 🍽️ Food App Business
- **Objective:** Segment customers based on behavior and value.
- **Method:** K-Means Clustering (via RapidMiner)
- **Key Findings:**
  - 6 clusters identified based on income, web purchases, discounts used, etc.
  - High-income groups preferred online purchases and responded to quality offers.
  - Low-income users favored in-store orders and discounts.
  - Promotional effectiveness varied by cluster—demographics mattered more than promotions.

---

### 3. 📈 Visual Summaries

Each dataset included visual aids to illustrate findings:
- Revenue vs. Order Value & Marketing Spend (Regression Output)
- Ad Click Rate by Income and Time Spent (Bar Charts & Probability Curves)
- Heatmaps and Centroid Tables from K-Means Clustering

🗂️ See: [`kaggle_presentation.pdf`](./kaggle_presentation.pdf)

---

### 4. 💡 Business Recommendations

#### Coffee Shop:
- Cut costs in areas like labor and hours, which have little revenue impact.
- Focus on strategies that increase average order value.

#### Advertising:
- Target lower-income, low-time users more aggressively.
- Adjust ad pricing and delivery times for better ROI.

#### Food App:
- Use cluster insights for personalized promotions.
- Prioritize customer retention strategies for high-value clusters.
- Improve app UX to increase engagement across all customer types.

---

## 📂 Project Files

| File                      | Description                                  |
|---------------------------|----------------------------------------------|
| `whitepaper.pdf`          | Final written report with dataset analysis   |
| `kaggle_presentation.pdf` | 10-minute flash presentation slides          |
| `README.md`               | This file – summary of methods and insights  |

---

## 📌 Key Takeaways

- Leveraged multiple datasets and tools (SQL, R, RapidMiner) to explore real-world problems.
- Developed insights into customer behavior, marketing effectiveness, and business strategy.
- Practiced advanced methods such as logistic regression and k-means clustering.
- Communicated technical findings through written and visual formats tailored for business impact.
