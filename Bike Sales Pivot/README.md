# 🚴 Global Bike Sales Performance Analysis (Excel)

> An in-depth analysis of global bike sales data, leveraging **Microsoft Excel's advanced functions and PivotTables** to uncover trends in revenue, profit, and customer demographics across different product categories and countries.

---

## 💡 Overview

This project provides a comprehensive, formula-driven analysis of the provided bike sales data. The core objective is to utilize Excel's powerful features to perform data transformation, calculate profitability metrics, and generate clear, actionable reports for business stakeholders across key areas: time-series growth, customer segmentation, and geographic performance.

---

## ⚙️ Core Excel Functions Explained

The analysis and creation of the summary sheets were heavily reliant on the following Excel functions for data manipulation and aggregation:

### 1. `SUMIFS` / `AVERAGEIFS` for Conditional Aggregation
These functions are essential for calculating totals or averages based on specific criteria.

* **Explanation:** Sums or averages values in a range that meet **multiple criteria** specified in separate ranges. This is the non-PivotTable method for summarizing data by dimension (e.g., country, product).
* **Example Usage:** Used to calculate **Total Revenue** for a specific product in a given year.
    * `=SUMIFS(Revenue_Column, Year_Column, 2021, Category_Column, "Bikes")`

### 2. `IFS` for Logic and Classification
This function allows for clean, multi-condition logic, crucial for segmenting customers.

* **Explanation:** Checks **multiple logical tests** in sequence and returns the value corresponding to the **first test that is TRUE**. It is superior to nested `IF` statements.
* **Example Usage:** Used to categorize customers into age groups (`Youth`, `Adults`, `Seniors`) from the raw `Customer_Age` column.

### 3. `TEXT` and `CONCATENATE` for Data Preparation
These functions ensure that data is properly formatted for consistent reporting.

* **`TEXT`:** Converts a numeric value (like a date) to a text string in a specified number format.
    * **Example Usage:** Used to extract a consistent `YYYY` format from the date column for annual analysis.
* **`CONCATENATE` / `&` Operator:** Joins two or more text strings.
    * **Example Usage:** Used to combine `Product Category` and `Sub-Category` into a single reporting label.

---

## 📊 Detailed Sheet Analysis

### Sheet 1: Sales Data (Raw Transactional Data)

This sheet contains the full, raw, transaction-level data used as the source for all analysis.

* **Content:** Includes columns for `Date`, `Customer_Age`, `Age_Group` (a calculated column), `Country`, `State`, `Product_Category`, `Revenue`, and `Profit`.
* **Key Role:** This sheet is where the **`IFS`** and **`TEXT`** functions are first applied to clean and transform the data before aggregation.

---

### Sheet 2: Revenue and Profit by Year (Time Series Analysis)

This sheet aggregates the raw transaction data to show overall annual performance trends.

* **Key Function Used:** **`SUMIFS`** (Used to total Profit and Revenue columns, with `Year` as the criteria).
* **Table Snapshot (Summarized Data):**

| Year | Annual Profit | Annual Revenue |
| :---: | :---: | :---: |
| 2017 | \$4,065,680 | \$10,289,670 |
| 2019 | \$7,417,353 | \$15,705,990 |
| 2021 | \$12,986,202 | \$29,747,226 |

* **Visualization:** **Revenue and Profit Trend** 

[Image of a Line Chart showing revenue and profit trend over several years]
<img width="793" height="482" alt="image" src="https://github.com/user-attachments/assets/9ce8254c-d63d-496d-b68d-228fb6aa8bc7" />


    * *Insight:* The chart helps visualize the year-over-year growth and identify periods of stagnation (e.g., the dip in 2019).

---

### Sheet 3: Revenue by Age Group (Customer Segmentation)

This sheet is crucial for customer segmentation, identifying which demographic drives the most revenue using `IFS` logic to categorize customers.

* **Key Function Used:** **`IFS`** (Used to create the **Age\_Group** classification) and **PivotTable Aggregation**.
* **Table Snapshot (Summarized Data):**

| Age Group | Sum of Revenue |
| :---: | :---: |
| Adults (35-64) | \$47,323,876 |
| Young Adults (25-34) | \$34,310,905 |
| Youth (<25) | \$13,201,837 |
| Seniors (64+) | \$339,700 |

* **Visualization:** **Revenue by Age Group Chart** 

<img width="791" height="476" alt="image" src="https://github.com/user-attachments/assets/44bd758f-6ad2-4e6a-8b40-4334882a4226" />


    * *Insight:* The bar chart confirms that the **Adults (35-64)** segment is the most valuable and should be prioritized.

---

### Sheet 4: Product Revenue by Country (Geographic and Product Analysis)

This sheet uses a two-dimensional PivotTable structure to analyze both geographic performance and product category success simultaneously.

* **Key Function Used:** Driven primarily by **PivotTable Row and Column fields** using the raw data.
* **Table Snapshot (Top Countries):**

| Country | Accessories Revenue | Bikes Revenue | Clothing Revenue | Total Revenue |
| :---: | :---: | :---: | :---: | :---: |
| United States | \$5.8M | \$21.5M | \$3.4M | \$30.8M |
| Australia | \$3.3M | \$20.2M | \$1.9M | \$25.4M |
| United Kingdom | \$1.9M | \$8.1M | \$0.9M | \$11.1M |
| Germany | \$1.7M | \$7.5M | \$0.7M | \$9.9M |

* **Visualization:** **Stacked Column Chart (Revenue by Country & Product Category)** 

<img width="863" height="518" alt="image" src="https://github.com/user-attachments/assets/3fada5b0-d992-47a2-a4bd-f1ea4ce5e97d" />


    * *Insight:* The visual confirms the **United States** as the largest market and that **Bikes** constitute the overwhelming majority of revenue in all regions.

---

## 📂 Project Structure

* `Bike_Sales_Final_Analysis.xlsx`: The final workbook containing all calculated columns, formulas, PivotTables, and charts.
* `Bike_Sales_Visualizations_Lab.xlsx - Sales Data.csv`: Original raw transaction data.

---

## 🚀 How to Use the Analysis

1.  **Download** the final Excel file.
2.  **Open** the workbook in Microsoft Excel.
3.  Navigate through the various sheets (e.g., `Revenue by Age Group`, `Product Revenue by Country`) to review the live tables and charts.

---

## 📧 Contact

* **GitHub:** [@YourUsername](https://github.com/YourUsername)
* **LinkedIn:** [Your LinkedIn Profile URL]
