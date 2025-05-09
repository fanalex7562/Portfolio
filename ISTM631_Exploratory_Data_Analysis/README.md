# ISTM 631 – Exploratory Data Analysis using Python

**Course:** ISTM 631 – Business Analytics Programming  
**Project:** Exploratory Data Analysis
**Dataset:** Superstore Dataset (Kaggle)  
**Tools:** Python, NumPy, pandas, matplotlib

---

## 📊 Project Overview

The goal of this project was to explore a real-world dataset using Python and apply various exploratory data analysis techniques to identify patterns in business performance. We produced a 1x3 grid of subplots using `matplotlib`, where each chart type and its corresponding insights highlighted different facets of the Superstore's operations.

We explored three dimensions of the business:
- Sales by **product category**
- Sales by **geographic region**
- **Sales trends over time**

---

## 🧾 Report Breakdown

### 1. 🧮 Data Description

We used NumPy arrays and lists to store structured data for three distinct business views:
- **Category sales values**: Furniture, Office Supplies, Technology
- **Regional sales distribution**: Central, East, South, West
- **Time-series sales**: From Oct 2014 to Dec 2017

All data used was derived from a subset of the Superstore dataset, processed externally (in SQL) before being visualized in Python.

---

### 2. 📈 Subplot Design & Unique Features

Each subplot follows a distinct chart type and integrates a unique design feature:

#### 🔹 Bar Chart – Sales by Category
- Compares revenue across Furniture, Office Supplies, and Technology.
- **Unique Feature:** Displays sales value labels above each bar.

#### 🔹 Pie Chart – Sales by Region
- Shows sales distribution across the U.S. (Central, East, South, West).
- **Unique Feature:** A hollow center with embedded explanatory text improves readability.

#### 🔹 Line Chart – Sales Trend Over Time
- Plots total sales from 2014 to 2017 alongside a moving average.
- **Unique Feature:** Overlays a 2-year moving average line to smooth fluctuations and highlight the trend.

---

### 3. 💻 Code Implementation

The project was implemented in a single Python script using:
- `numpy` for array manipulation
- `pandas` for date handling and moving average calculations
- `matplotlib` for all plots

🗂️ See: [`EDA_Project_Code.txt`](./EDA_Project_Code.txt)

---

### 4. 💡 Recommendations for Future Enhancements

For each visualization, we suggested an additional feature to increase interactivity or depth:
- **Bar Chart:** Add a stacked bar to show both sales and profit per category.
- **Pie Chart:** Make the chart interactive (e.g., hover-to-zoom or show detailed tooltips).
- **Line Chart:** Apply smoothed lines or increase data points for larger datasets.

---

## 📂 Project Files

| File                          | Description                                 |
|-------------------------------|---------------------------------------------|
| `EDA_Report.pdf`              | Written report covering the entire project  |
| `EDA_Presentation_Slides.pdf`| Summary deck for classroom presentation      |
| `EDA_Project_Code.txt`        | Python code with comments and docstrings    |
| `README.md`                   | This file – documentation overview          |

---

## 📌 Key Takeaways

- Learned to structure data for clean visual analysis using core Python libraries.
- Practiced applying best practices in data visualization (diverse charts, labels, readability).
- Built a cohesive, reproducible analytical workflow that communicates insights clearly.

