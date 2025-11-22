# 🌀 Atlantic Hurricane Data Insights (Excel) ⛈️🌪️

>This dataset provides a historical look at some of the most destructive and powerful Atlantic hurricanes🌊, capturing key metrics like estimated damage and Saffir-Simpson category. It's a great resource for quick analysis on hurricane severity and historical trends! 🧐📈

---

## 💡 Overview ✨

This project provides a detailed, formula-driven analysis of the provided hurricane dataset (`Biggest Atlantic Hurricanes.csv`). The primary goal is to leverage core Excel functionalities to perform data transformation, calculate severity categories, and generate actionable summaries without relying on external programming languages. 💻

The analysis deliverables include:
* **Data Cleansing:** Standardizing date and text formats. 🧹
* **Classification:** Creating a severity column using conditional functions. 🚦
* **Summary Reporting:** Generating frequency tables and statistics using PivotTables. 📝

---

## 🛠️ Analysis Tools 🧰

* **Microsoft Excel:** Used for all data manipulation, analysis, and visualization.
* **Excel Power Query (Optional):** Used for initial data import and transformation if needed. 🔗

---
### 📋 Data Dictionary (Table Structure)

The dataset contains the following key columns, which provide details on each major storm: 🌪️

| Column Name | Description | Data Type | Example |
| :--- | :--- | :--- | :--- |
| **Name** | The name given to the Atlantic hurricane. 🏷️ | Text | `Katrina` |
| **Start Date** | The date the hurricane first formed or was officially tracked. 🗓️ | Date | `August 23, 2005` |
| **Damage (USD Millions)** | The estimated total damage caused by the storm, in millions of US dollars. 💰 | Number (Float/Currency) | `125000` |
| **Category (Saffir-Simpson)** | The hurricane's maximum intensity rating based on the **Saffir-Simpson Hurricane Wind Scale**. A value of 5 is the most intense. 5️⃣ | Number (Integer) | `5` |
| **Max Wind Speed** | The maximum sustained wind speed recorded for the hurricane, typically in miles per hour (mph). 💨 | Text/Number | `157 and over` |

> *Note: Some columns related to testing (e.g., `Switch Value TEST`, `Speed TEST`) and lookup tables were present in the original Excel file and have been omitted here for clarity. 🧹*
---
## ⚙️ Core Excel Functions Explained 🧮

The following key functions were used to derive the main insights and calculated fields within the spreadsheet:

### 1. `IF` and `IFS` for Conditional Classification 🎯

These functions are used to assign a **Saffir-Simpson Category (1-5)** to each storm based on its `Max Wind (mph)`. 🌬️

* **`IF` (Basic):** Used for a simple true/false condition. ✅/❌
    * **Explanation:** Checks if a condition is met. If **TRUE**, it returns one value; if **FALSE**, it returns another.
    * **Example Usage:** `=IF(C2>157, "Cat 5", "Lower")`

* **`IFS` (Advanced):** Used for multiple nested conditions, providing a cleaner alternative to multiple nested `IF` statements.
    * **Explanation:** Checks multiple conditions in the order they are listed and returns the value corresponding to the first true condition. This is similar to the `SWITCH(TRUE(),...)` logic.
    * **Example Usage:** Used to check wind speed against Category thresholds sequentially (e.g., Cat 5, then Cat 4, then Cat 3, etc.). 🪜

### 2. `SWITCH` for Categorical Mapping 🚦

Used to quickly map a specific input value to a corresponding descriptive output. 🗺️

* **`SWITCH`:**
    * **Explanation:** Evaluates an **expression** (like a Category number) against a list of specific values. When it finds a match, it returns a corresponding result. It is a cleaner, more efficient way to replace multiple, sequential `IF` statements for **exact matches**. ⚡
    * **Example Usage:** Used to convert the numeric Saffir-Simpson category (1-5) into a text description for a report.
        `=SWITCH(Category*, 5, "Catastrophic 🛑", 4, "Extreme ⚠️", 3, "Major", "Minor")`

### 3. `VLOOKUP` or `XLOOKUP` for Data Enrichment 🔍

Used to pull descriptive information or standard values from a separate lookup table. 📚

* **`VLOOKUP` / `XLOOKUP`:**
    * **Explanation:** Searches for a value in the first column of a table (or range) and returns a value in the same row from a specified column. **`XLOOKUP`** is the modern, more flexible replacement. 🔑
    * **Example Usage:** Used to match a `Year` to a **Decade Grouping** (e.g., 1980s, 1990s) stored in a separate sheet for time-series analysis. 📅

### 4. `COUNTIFS` for Summary Statistics 🔢

Used to quickly count the frequency of storms based on specific criteria. 📊

* **`COUNTIFS`:**
    * **Explanation:** Counts the number of rows that satisfy one or more criteria. This is the **formula equivalent** of generating a frequency report via a PivotTable. 🎯
    * **Example Usage:** `=COUNTIFS(Severity_Column, "Category 5", Year_Column, ">2000")` to count Category 5 storms that occurred after the year 2000.

***

## 📈 Key Analysis Outputs 📊

In this context, SWITCH is likely used to automatically determine the Wind Speed Range or a Severity Label based on the Hurricane Category🌪️.


<img width="1233" height="566" alt="image" src="https://github.com/user-attachments/assets/f1568192-5e83-407e-8a00-669a2074a076" />



---

## 📂 Project Structure 🗂️

* `Biggest Atlantic Hurricanes.xlsx`: The final workbook containing the raw data, calculated columns, PivotTables, and charts.
* `Biggest Atlantic Hurricanes.csv`: The original raw data file. 🧾

---

## 🚀 How to Use the Analysis ⚙️

1.  **Download** 📥 the `Biggest Atlantic Hurricanes.xlsx` file.
2.  **Open** the workbook in Microsoft Excel. 💻
3.  Navigate to the `Analysis` or `Dashboard` sheet to review the pre-built reports and charts. You can expand the data source of the PivotTables to include new data if necessary. 🖱️


---

