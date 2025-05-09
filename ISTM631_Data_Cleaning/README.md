# ISTM 631 – Data Cleaning Using Python

**Course:** ISTM 631 – Business Analytics Programming  
**Project:** Data Pre-processing and Cleaning (Project 2)  
**Team Members:** Yisi Lu, Kenny Lei, Alex Fan  
**Dataset:** Cafe Sales Dataset (Kaggle)  
**Tools:** Python, pandas, NumPy

---

## 🧼 Project Overview

The goal of this project was to clean a raw sales dataset from a cafe that contained numerous data quality issues such as missing values, inconsistent formats, incorrect data types, and duplicate entries. Using Python, we implemented a comprehensive data cleaning pipeline consisting of eight distinct steps, followed by a visualization of the cleaned dataset using the `pandas` plotting utility.

---

## 🧾 Report Breakdown

### 1. 📥 Data Collection

We selected the **Cafe Sales** dataset from Kaggle, which includes 10,000 rows and 8 columns spanning numerical, categorical, and date/time data types. It was chosen specifically for its realistic messiness:
- Missing or incorrect values
- Mixed data types
- Duplicates and inconsistent formatting
- Invalid transaction dates
- Mismatches in calculated totals

---

### 2. 🧹 Data Cleaning Process

We performed the following **8 distinct data cleaning steps**:

1. **Remove Duplicates** – Eliminated repeated rows.
2. **Convert Data Types** – Ensured numeric fields were stored as numerical types.
3. **Impute Missing Values** – Used median for numeric and mode for categorical data.
4. **Standardize Text Fields** – Converted to title case and removed leading/trailing whitespace.
5. **Fix Date Formats** – Converted 'Transaction Date' to proper datetime format.
6. **Drop Invalid Dates** – Removed rows where date parsing failed.
7. **Correct Calculations** – Recalculated `Total Spent` and corrected mismatches.
8. **Reset Index** – Reindexed the cleaned DataFrame for clarity.

📄 See: [`DC_Project_Code.txt`](./DC_Project_Code.txt)

---

### 3. 📊 Final Dataset Summary

| Metric           | Before Cleaning | After Cleaning |
|------------------|------------------|----------------|
| Rows             | 10,000           | 9,540          |
| Columns          | 8                | 8              |
| Data Type Issues | Present          | Resolved       |

All columns now contain valid, consistently formatted, and correctly typed data.

---

### 4. 📈 Plot the Clean Data

We visualized the **total sales by payment method** using a horizontal bar chart built with `pandas.plot()`.

- Grouped data by `Payment Method`
- Summed the `Total Spent`
- Sorted the results for better readability
- Labeled the bars with exact dollar amounts

✅ This plot provides quick insight into which payment methods are most used by customers.

---

### 5. 🔧 Challenges and Solutions

| Challenge                                               | How We Addressed It                                         |
|----------------------------------------------------------|--------------------------------------------------------------|
| Type conversions caused script crashes on bad input      | Used `errors='coerce'` for safe type handling                |
| Detecting incorrect totals across rows                   | Used `np.abs()` with logical masking to catch inaccuracies   |
| Partial correction logic in early drafts                 | Improved targeting via Boolean masks                        |
| Summarizing by group was messy with raw data             | Used `groupby` + `agg()` for clean, efficient summarization  |
| Cleaned file was misplaced                               | Used `os.path.abspath()` to confirm save location            |

---

## 📂 Project Files

| File                          | Description                                 |
|-------------------------------|---------------------------------------------|
| `dirty_cafe_sales.xlsx`       | Original unclean dataset                    |
| `CleanedCafeSales.xlsx`       | Final cleaned dataset                       |
| `DC_Report.pdf`               | Full report documenting the process         |
| `DC_Presentation_Slides.pdf`  | Summary slides for classroom presentation   |
| `DC_Project_Code.txt`         | Python code with docstrings and comments    |

---

## 📌 Key Takeaways

- Practiced systematic data cleaning using Python and pandas
- Learned to handle messy real-world data: missing values, invalid types, and structural inconsistencies
- Developed robust and reproducible scripts that corrected critical errors in the dataset
- Created clear visualizations to support business analysis after cleaning


