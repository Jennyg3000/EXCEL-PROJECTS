# 📊 Bike Sales Performance Analysis: The Pivot Lab

> A project demonstrating the power of **Microsoft Excel PivotTables** for complex data aggregation, segmentation, and multi-dimensional profit analysis using global bike sales data.

---

## 💡 Overview

This project uses a large transactional dataset of bike sales (`Bike Sales.csv`) to create sophisticated summary reports through PivotTables. The core goal is to generate actionable insights into profitability and sales volume across key dimensions: customer demographics (Age/Gender) and geographic location (Country/County).

The Excel workbook is structured around the following key outputs:
1.  **Raw Data Sheet:** The primary source for all pivots and calculations.
2.  **Profit Segmentation Pivot:** Detailed analysis of profit contribution by customer segment and country.
3.  **Sales Volume by County:** Analysis of product sales volume by specific local area.

---

## ⚙️ Core Excel Functions & Features Explained

Since this is a "Pivot Lab," the analysis relies heavily on Excel's built-in data summarization tools.

### 1. PivotTables & PivotCharts (Core Tool)
* **Explanation:** The fundamental feature used to automatically group, summarize, and aggregate data (e.g., summing `Profit` or counting `Order_Quantity`) without using formula rows.
* **Usage:** Used universally across all summary sheets to transform raw transaction data into the final tables.

### 2. Calculated Fields & Items (Within PivotTable)
* **Explanation:** Formulas created *inside* the PivotTable to perform calculations on aggregated data (e.g., calculating **Profit Margin** as a percentage).
* **Usage:** Could be used to calculate a Profit Rate column within the Segmentation Pivot.

### 3. `IF` or `IFS` (Data Preparation)
* **Explanation:** Used on the **Raw Data Sheet** to create categorical grouping columns necessary for the pivots.
* **Example Usage:** Used to create the **Age\_Group** column from the raw `Customer_Age` data (`Youth`, `Young Adults`, `Adults`).

### 4. `SUMIFS` / `GETPIVOTDATA` (Reporting & Dashboard)
* **`SUMIFS`:** Could be used on a separate dashboard sheet to pull specific totals from the raw data based on complex criteria.
* **`GETPIVOTDATA`:** Used to reliably retrieve data from the PivotTable for use in other parts of a dashboard sheet.

---

## 📊 Detailed Sheet Analysis

### Sheet 1: Profit Segmentation Pivot

This PivotTable provides a multi-dimensional analysis of profit, allowing managers to view the profitability of each **Age Group** segmented by **Customer Gender** across different **Countries**.

* **Data Aggregated:** Sum of Profit.
* **Key Filters:** Country, Age\_Group, Customer\_Gender.
* **Table Snapshot (Abridged):**

| Age\_Group | Customer\_Gender | Australia | France | United States | Grand Total |
| :---: | :---: | :---: | :---: | :---: | :---: |
| Youth (<25) | F | 0.0138 | 0.0384 | 0 | 0.0587 |
| | M | 0.0029 | 0.0257 | 0 | 0.0394 |
| **Youth Total** | | **0.0168** | **0.0642** | **0** | **0.0981** |
| Young Adults (25-34) | F | 0.0991 | 0.0463 | 0.0921 | 0.2980 |

* **Visualization:** **Profit Contribution by Segment** 

<img width="1029" height="516" alt="image" src="https://github.com/user-attachments/assets/6efbcd7d-f7bc-4eed-8254-e76bf539778c" />


    * *Insight:* The chart quickly shows which specific gender/age group combination (e.g., Young Adults - Female in Australia) contributes the largest percentage of total profit.

---

### Sheet 2: Sales Volume by County

This sheet uses a simple PivotTable (or structured summary) to track the quantity of products sold across different local geographic areas (`County`).

* **Data Aggregated:** Sum of Sales Volume.
* **Key Filters:** County, Product.
* **Table Snapshot (Summarized Pivot):**

| County | Laptops | Printers | Smartphones | Grand Total |
| :---: | :---: | :---: | :---: | :---: |
| Cornwall | 700 | 400 | 0 | 1100 |
| Durham | 250 | 300 | 0 | 550 |
| Essex | 0 | 800 | 300 | 1100 |
| Lancashire | 600 | 0 | 150 | 750 |
| Yorkshire | 500 | 0 | 200 | 700 |
| **Grand Total** | **2450** | **1500** | **1250** | **5200** |

* **Visualization:** **Product Volume Distribution** 

[Image of a Bar Chart]

    * *Insight:* A stacked bar chart visualization helps compare total sales across counties and visually assess the product mix sold in each region (e.g., Laptops dominate volume).

---

## 📂 Project Structure

* `Bike_Sales_Pivot_Lab.xlsx`: The final workbook containing the raw data, PivotTables, and associated PivotCharts.
* `Bike_Sales_Pivot_Lab.xlsx - Bike Sales.csv`: Original raw transactional data file.

---

## 🚀 How to Use the Analysis

1.  **Download** the final Excel file.
2.  **Open** the workbook in Microsoft Excel.
3.  Navigate through the pivot sheets (e.g., `Profit Segmentation Pivot`) to review the summary reports. You can easily drag and drop fields within the PivotTables to create new views.

---

## 📧 Contact

* **GitHub:** [@YourUsername](https://github.com/YourUsername)
* **LinkedIn:** [Your LinkedIn Profile URL]
