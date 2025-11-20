
# 🌀 Atlantic Hurricane Data Insights (Excel)

> An analysis project focused on cleaning, classifying, and summarizing the biggest Atlantic Hurricanes using **Microsoft Excel's advanced formulas and PivotTables.**

---

## 💡 Overview

This project provides a detailed, formula-driven analysis of the provided hurricane dataset (`Biggest Atlantic Hurricanes.csv`). The primary goal is to leverage core Excel functionalities to perform data transformation, calculate severity categories, and generate actionable summaries without relying on external programming languages.

The analysis deliverables include:
* **Data Cleansing:** Standardizing date and text formats.
* **Classification:** Creating a severity column using conditional functions.
* **Summary Reporting:** Generating frequency tables and statistics using PivotTables.

---

## 🛠️ Analysis Tools

* **Microsoft Excel:** Used for all data manipulation, analysis, and visualization.
* **Excel Power Query (Optional):** Used for initial data import and transformation if needed.

---

## ⚙️ Core Excel Functions Explained

The following key functions were used to derive the main insights and calculated fields within the spreadsheet:

### 1. `IF` and `IFS` for Conditional Classification

These functions are used to assign a **Saffir-Simpson Category (1-5)** to each storm based on its `Max Wind (mph)`.

* **`IF` (Basic):** Used for a simple true/false condition.
    * **Explanation:** Checks if a condition is met. If $\text{TRUE}$, it returns one value; if $\text{FALSE}$, it returns another.
    * **Example Usage:** `=IF(C2>157, "Cat 5", "Lower")`

* **`IFS` (Advanced):** Used for multiple nested conditions, providing a cleaner alternative to multiple nested `IF` statements.
    * **Explanation:** Checks multiple conditions in the order they are listed and returns the value corresponding to the first true condition. This is similar to the `SWITCH(TRUE(),...)` logic.
    * **Example Usage:** Used to check wind speed against Category thresholds sequentially (e.g., Cat 5, then Cat 4, then Cat 3, etc.).

### 2. `VLOOKUP` or `XLOOKUP` for Data Enrichment

Used to pull descriptive information or standard values from a separate lookup table.

* **`VLOOKUP` / `XLOOKUP`:**
    * **Explanation:** Searches for a value in the first column of a table (or range) and returns a value in the same row from a specified column. `XLOOKUP` is the modern, more flexible replacement.
    * **Example Usage:** Used to match a `Year` to a **Decade Grouping** (e.g., 1980s, 1990s) stored in a separate sheet for time-series analysis.

### 3. `COUNTIFS` for Summary Statistics

Used to quickly count the frequency of storms based on specific criteria.

* **`COUNTIFS`:**
    * **Explanation:** Counts the number of rows that satisfy one or more criteria. This is the **formula equivalent** of generating a frequency report via a PivotTable.
    * **Example Usage:** `=COUNTIFS(Severity_Column, "Category 5", Year_Column, ">2000")` to count Category 5 storms that occurred after the year 2000.

---

## 📈 Key Analysis Outputs

The final Excel file contains summarized PivotTables and visualizations derived from the formula columns.

### 1. Severity Frequency Table

A PivotTable showing the distribution of storms across the Saffir-Simpson categories.

| Severity Category | Storm Count | % of Total |
| :---: | :---: | :---: |
| Category 5 (Major) | 9 | 24% |
| Category 4 (Major) | 12 | 32% |
| Category 3 (Major) | 10 | 27% |
| Category 1-2 | 6 | 17% |

### 2. Decadal Storm Count Chart



[Image of a Bar Chart]


* **Insight:** A bar chart illustrating which decades saw the highest count of major (Cat 3+) hurricanes, generated directly from a PivotChart.

---

## 📂 Project Structure

* `Biggest Atlantic Hurricanes.xlsx`: The final workbook containing the raw data, calculated columns, PivotTables, and charts.
* `Biggest Atlantic Hurricanes.csv`: The original raw data file.

---

## 🚀 How to Use the Analysis

1.  **Download** the `Biggest Atlantic Hurricanes.xlsx` file.
2.  **Open** the workbook in Microsoft Excel.
3.  Navigate to the `Analysis` or `Dashboard` sheet to review the pre-built reports and charts. You can expand the data source of the PivotTables to include new data if necessary.

---

