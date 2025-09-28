# Bank Customer Analysis 

## 📌 Project Overview  
This project analyzes bank customers to understand **customer churn vs. retention**.  
The goal is to uncover key demographics and behaviors influencing customer loyalty.  

The project combines **Python (for data preparation)** and **Power BI (for visualization)** to deliver an interactive and insightful dashboard.  

---

## ⚙️ Data Workflow  

### **1. Data Cleaning & Transformation (Python - Pandas)**  
I used **Python Pandas** for preprocessing before loading the dataset into Power BI because it provided more flexibility in handling messy data. The steps included:  

- **Importing Data**: Loaded **Sheet 1** and **Sheet 2**.  
- **Initial Checks**: Used `.info()` to inspect structure and data types.  
- **Duplicates**: Checked for duplicate rows and dropped them.  
- **Missing Values**: Checked null values and filled where required.  
- **Standardization**:  
  - Replaced inconsistent values (e.g., `French` and `FRA` → `France`).  
  - Removed symbols (e.g., `€` in Balance and Estimated Salary).  
- **Column Handling**:  
  - Dropped `Tenure` column from one sheet.  
  - Joined both sheets on **Customer ID**.  
- **Data Type Conversion**: Converted `Age`, `Balance`, and `Estimated Salary` into integers.  
- **Outlier Handling**:  
  - Checked for negative values in `Balance` and `Estimated Salary`.  
  - Replaced invalid negative values with the **mean Estimated Salary**.  
- **Feature Engineering**:  
  - Created **categorical bands** for Credit Score, Age, Tenure, Balance, and Estimated Salary (Low / Medium / High).  
  - Created **range-based columns** (e.g., Age group: `28–38`).  
- **Final Checks**: Validated with `.info()` and exported the cleaned dataset.  

✅ By doing this, I ensured the dataset was **clean, consistent, and analysis-ready** before loading into Power BI.  

---

### **2. Data Visualization (Power BI)**  
The Power BI dashboard was structured into three key pages:  

- **Main Page**:  
  - Shows **Total Customers** and their demographics.  
  - Contains **drill-through cards**:  
    - **Churn Customers Card** → takes you to churn analysis.  
    - **Retain Customers Card** → takes you to retention analysis.  

- **Churn Customers Page**:  
  - Demographics and insights on customers who left the bank.  

- **Retain Customers Page**:  
  - Demographics and insights on customers who stayed with the bank.  

---

## 📊 Key Features  
- **Python + Power BI workflow**: Clean in Python, visualize in Power BI.  
- **Drill-through analysis** for churn vs. retention.  
- **Customer segmentation** by demographics and financial attributes.  
- **Feature engineering** to categorize continuous variables into ranges.  

---

## 🛠️ Tools & Technologies  
- **Python (Pandas, NumPy)** → Data cleaning & transformation.  
- **Power BI** → Dashboard creation and visual analysis.  

---

## 🚀 Insights  
- Identified churn trends based on **age, balance, and salary groups**.  
- Detected **data quality issues** (negative salary values) and corrected them.  
- Segmented customers into **risk groups** for targeted retention strategies.  

---

## 📂 Project Structure 
- [Data Cleaning & Transformation Script](./BankData.ipynb) → Python Code for Cleaning and Transforming data.
- [Demo Video](https://drive.google.com/file/d/19ZEPAdHubWQDdfs8a1nYmxbj4ZQ90GtZ/view?usp=sharing) → Demonstration of How Report Works.
- [Live Report](https://app.powerbi.com/view?r=eyJrIjoiMjAzNDM1MzMtNmY5NS00OWZmLWE0NGYtZDZiZTQ4YTgyMGVjIiwidCI6ImQyNzJiNzg4LTU4YzctNGM0NS1hMWRmLTk3ODYyYzE3ODkyOSJ9) → View Interactive Report.

