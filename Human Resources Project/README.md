# 🧑‍💻 Human Resources Data Analysis: Payroll & Headcount (Excel)

> A Microsoft Excel project focused on core Human Resources and Financial analysis, leveraging powerful functions like **`SUMIF`** and **`TRANSPOSE`** to manage detailed **payroll calculation** and summarize **departmental headcount & salary** costs.

---

## 💡 Overview

This project provides a robust, formula-driven framework for managing and analyzing key HR financial metrics. The workbook uses two primary sheets to transform raw employee data into actionable financial and staffing summaries:

* **Payroll:** Calculates gross pay, deductions, and final net pay using hourly rates and standard deduction rules.
* **Headcount & Salaries:** Aggregates employee data to provide summaries of total salary expenditure and staffing levels by department.

---

## ⚙️ Core Excel Functions Explained

The accuracy, calculation speed, and flexible reporting capabilities of the workbook are built upon these essential Excel functions:

### 1. Arithmetic & Aggregation (`*`, `-`, `/`, `+`, `SUM`)
These are the foundational tools for all financial totals and calculations.

* **Explanation:** Used for all fundamental financial calculations and to total ranges.
* **Example Usage 1 (Payroll Sheet - Gross Pay):** Calculating **Gross Pay** by multiplying **Hourly Rate** by **Total Hours Worked**.
    ```excel
    =Hourly_Rate * Total_Hours_Worked
    ```
* **Example Usage 2 (Payroll Sheet - Net Pay):** Calculating **Net Pay** by subtracting deductions (Tax, SS, Pension) from **Gross Pay**.
    ```excel
    =Gross_Pay - (Tax_Deduction + SS_Deduction + Pension_Deduction)
    ```
* **Example Usage 3 (Headcount & Salaries - Grand Total):** Calculating the **total company payroll** for the year.
    ```excel
    =SUM(Salary_Column)
    ```

### 2. Conditional Aggregation (`SUMIF` / `COUNTIF`)
These functions are critical for creating the dynamic summary tables on the **Headcount & Salaries** sheet.

* **Explanation:** Aggregates (sums or counts) values based on a single specified criteria (e.g., matching a specific Department name).
* **Example Usage 1 (Total Salary Cost):** Calculating the total salary cost for the 'Sales' department.
    ```excel
    =SUMIF(Department_Range, "Sales", Salary_Range)
    ```
* **Example Usage 2 (Headcount):** Calculating the number of employees in the 'Logistics' department (Headcount).
    ```excel
    =COUNTIF(Department_Range, "Logistics")
    ```

### 3. Data Restructuring (`TRANSPOSE`)
This function is used for flexible reporting and dashboard design.

* **Explanation:** Takes a vertical range of cells (a column) and converts it into a horizontal range (a row), or vice versa. This is used to present summary data in a horizontal format (e.g., Department names in the top row).
* **Usage:** Used on the `Headcount & Salaries` sheet to transform the standard vertical summary into a compact, horizontal report.
    ```excel
    =TRANSPOSE(Vertical_Summary_Range)
    ```

### 4. Data Retrieval (`VLOOKUP` / `XLOOKUP`)
* **Explanation:** Used to retrieve an associated value from another table based on a common identifier. This ensures consistency and centralizes data rules.
* **Example Usage:** Used to retrieve the employee's standard **Hourly Rate** or a fixed **Tax Rate** from a separate rule table.
    ```excel
    =XLOOKUP(Employee_Name, Name_List, Hourly_Rate_List)
    ```

---

## 🔁 Data Flow and Transport

The workbook demonstrates an efficient data transport model:

1.  **Raw Calculation (`Payroll`):** The sheet uses formulas to combine raw time data with fixed rules (via lookups or references) to calculate gross and net pay.
2.  **Aggregation (`Headcount & Salaries`):** Raw employee records (Name, Department, Salary) are funneled into the summary tables using **`SUMIF`** and **`COUNTIF`** for aggregation.
3.  **Presentation (`Headcount & Salaries`):** The aggregated data is then dynamically restructured using **`TRANSPOSE`** to create flexible, management-friendly views.

---

## 📊 Detailed Sheet Analysis

### Sheet 1: Payroll (Detailed Calculations)

This sheet calculates every employee's gross and net pay based on hourly rate and deduction rules.

* **Payroll Rules (Example Snapshot):**

| Deduction Type | Rate |
| :---: | :---: |
| **Tax** | 0.32 |
| **Social Security** | 0.08 |
| **Pension** | 0.05 |

* **Key Output Table (Abridged Employee Calculations):**

| Employee | Hourly Rate | Total Hours | Gross Pay | Net Pay |
| :---: | :---: | :---: | :---: | :---: |
| Johnny Caine | 18.20 | 43 | 782.77 | 468.61 |
| George Marley | 12.57 | 43 | 540.56 | 323.58 |
| Angelina Osbourne | 18.35 | 38 | 697.12 | 417.07 |

* **Visualization:** A simple Bar Chart comparing **Gross Pay vs. Net Pay** by employee would visually illustrate the impact of total deductions. 

[Image of a Bar Chart]


---

### Sheet 2: Headcount & Salaries (Summary Analysis)

This sheet provides executive-level staffing and cost summaries using conditional functions.

* **Table 1: Standard Vertical Summary (Uses `SUMIF` / `COUNTIF`)**

| Department | Total Salary | Headcount |
| :---: | :---: | :---: |
| **Sales** | \$179,898 | 6 |
| **Purchasing** | \$137,557 | 5 |
| **Logistics** | \$73,601 | 3 |
| **Total:** | **\$391,056** | **14** |

* **Table 2: Transposed Summary (Uses `TRANSPOSE()` on Table 1 for Dashboard View)**

| Metric | Sales | Purchasing | Logistics | Total: |
| :---: | :---: | :---: | :---: | :---: |
| **Salary** | 179,898 | 137,557 | 73,601 | 391,056 |
| **Headcount** | 6 | 5 | 3 | 14 |

* **Visualization:** **Salary Distribution by Department** 

[Image of a Bar Chart]

    * *Insight:* This chart provides an immediate comparison of departmental costs, clearly showing that **Sales** accounts for the largest portion of the total salary budget.

---

## 📂 Project Structure

* `Human Resources.xlsx`: The main workbook containing all data and analysis sheets.
    * `Payroll`: Detailed time/pay calculations.
    * `Headcount & Salaries`: Resource allocation summaries and analysis.

---

## 🚀 How to Use the Analysis

1.  **Download** the `Human Resources.xlsx` file.
2.  **Open** the workbook in Microsoft Excel.
3.  Examine the formulas on the `Headcount & Salaries` sheet to see how `SUMIF`, `COUNTIF`, and `TRANSPOSE` are used to aggregate and present the data dynamically.

---

