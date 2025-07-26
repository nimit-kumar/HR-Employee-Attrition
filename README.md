# HR Analytics Dashboard 📊

This Power BI dashboard provides a comprehensive analysis of employee data from an HR perspective. It focuses on employee attrition, demographic distributions, and departmental insights to help HR managers make informed decisions.

---

## 🧠 Objective

To visualize and analyze key HR metrics such as:
- Total Employees
- Attrition Count & Rate
- Average Monthly Income
- Attrition trends based on Age, Gender, Department, and Job Role
- Employee distribution across Departments and Education Fields

---

## 📁 Dataset

- **Source**: [IBM HR Analytics Employee Attrition & Performance Dataset](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)
- **Rows**: 1,470
- **Columns**: 35+
- **Format**: CSV

---

## 🧹 Data Cleaning & Transformation

Performed in Power BI using Power Query Editor:
- Removed unnecessary columns (e.g., Over18, EmployeeCount)
- Renamed columns for readability
- Created bins for Age groups (e.g., 20–30, 31–40)
- Added calculated columns and DAX measures:
  - `Total Employees`
  - `Total Attrition`
  - `Attrition Rate %`
  - `Average Monthly Income`

---

## 📊 Key Visuals in Dashboard

| Visual Type            | Description                                         |
|------------------------|-----------------------------------------------------|
| **KPI Cards**          | Total Employees, Attrition Count, Avg Income       |
| **Donut Chart**        | Attrition by Gender                                 |
| **Stacked Bar Chart**  | Employees by Department & Gender                    |
| **Bar Chart**          | Attrition by Job Role                               |
| **Line Chart**         | Attrition trend by Age                              |
| **Treemap**            | Employees by Education Field                        |
| **Slicers**            | Filter by Department, Gender, Age, Education Field  |

---

## 🧮 DAX Measures Used

```DAX
Total Employees = COUNT('HR_Data'[EmployeeID])

Total Attrition = CALCULATE(COUNT('HR_Data'[EmployeeID]), 'HR_Data'[Attrition] = "Yes")

Attrition Rate % = DIVIDE([Total Attrition], [Total Employees]) * 100

Average Monthly Income = AVERAGE('HR_Data'[MonthlyIncome])
