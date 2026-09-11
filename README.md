# Healthcare Analytics & Hospital Performance Dashboard

## 📌 Project Overview

This project analyzes healthcare and hospital admission data to identify patterns in **patient volume, billing, length of stay, medical conditions, admission types, age groups, and insurance providers**.

The workflow includes **data cleaning, feature engineering, exploratory data analysis (EDA), and interactive dashboard development**.

---

## 🎯 Project Objectives

* Clean and prepare the healthcare dataset for analysis.
* Identify patterns in patient admissions, billing, and length of stay.
* Compare healthcare metrics across medical conditions, age groups, admission types, and insurance providers.
* Develop an interactive dashboard for clear, management-relevant insights.

---

## 📊 Dataset

The dataset contains **55,500 records and 15 columns** covering:

* Patient Name
* Age
* Gender
* Blood Type
* Medical Condition
* Date of Admission
* Doctor
* Hospital
* Insurance Provider
* Billing Amount
* Room Number
* Admission Type
* Discharge Date
* Medication
* Test Results

**Admission period:** May 8, 2019 – May 7, 2024

---

## 🔧 Data Preparation

### Data Cleaning

* Checked dataset structure, data types, and statistical summaries.
* **No missing values** were found.
* Identified and removed **534 duplicate records**.
* Final analysis dataset: **54,966 records**.
* Converted admission and discharge dates to datetime format.
* Standardized categorical/text values by removing unnecessary whitespace and applying consistent capitalization.
* Standardized Blood Type values to uppercase.

### Feature Engineering

Created the following analytical fields:

* **Admission Year**
* **Admission Month**
* **Length of Stay**
* **Age Group**
* **Stay Category**

Age Groups:

* `<18`
* `18-35`
* `36-50`
* `51-65`
* `65+`

Stay Categories:

* Short Stay
* Medium Stay
* Long Stay

---

## 🔍 Exploratory Data Analysis

The analysis examined:

* Patient volume by medical condition.
* Patient distribution by age group.
* Billing across medical conditions.
* Billing across insurance providers.
* Length of stay by admission type.
* Monthly admission trends.
* Monthly billing trends.

---

## ⚠️ Data Quality & Outlier Analysis

### Billing Amount

* Minimum billing: approximately **-$2,008**
* Maximum billing: approximately **$52,764**
* Average billing: approximately **$25,544**
* **106 negative billing records** were identified.

Negative billing records were **flagged rather than removed** because the dataset does not provide enough information to determine whether they represent refunds, adjustments, corrections, or another business process.

### Length of Stay

* Minimum: **1 day**
* Maximum: **30 days**
* Average: approximately **15.5 days**
* IQR analysis identified **0 statistical outliers**.

---

## 📈 Key Analysis Results

* The final cleaned dataset contains **54,966 records**.
* Patient volumes across the six medical conditions are relatively similar.
* **65+** is the largest age group.
* Average length of stay is approximately **15.5 days**.
* Average billing is approximately **$25.5K**.
* Average billing is relatively similar across medical conditions and insurance providers.
* Average length of stay is similar across **Emergency, Elective, and Urgent** admissions.
* **106 negative billing records** require further business validation.
* The dataset alone does **not provide enough evidence to determine causal reasons** behind billing or length-of-stay differences.

---

## 📊 Dashboard

The interactive dashboard was developed using **Google Looker Studio**.

### KPI Metrics

* Total Patients: **54,966**
* Total Billing: approximately **$1.4B**
* Average Billing: approximately **$25.5K**
* Average Length of Stay: approximately **15.5 days**
* Negative Billing Records: **106**

### Dashboard Visualizations

1. Patient Volume by Medical Condition
2. Patient Distribution by Age Group
3. Average Billing by Medical Condition
4. Total Billing by Insurance Provider
5. Average Length of Stay by Admission Type
6. Monthly Patient Admissions
7. Monthly Billing Trend

### Dashboard Filters

* Date of Admission
* Medical Condition
* Admission Type
* Insurance Provider
* Gender

---

## 🛠️ Tools & Technologies

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **Jupyter Notebook**
* **Google Looker Studio**
* **GitHub**

---

## 📁 Project Structure

```text
Healthcare-Analytics/
│
├── README.md
├── healthcare_dataset.csv
└── healthcare_analysis.ipynb
```

---

## 📝 Conclusion

This project transforms raw healthcare records into an **analysis-ready dataset** and presents meaningful operational insights through **Python-based EDA and an interactive Looker Studio dashboard**.

The analysis focuses on patient volume, billing, length of stay, demographics, admission types, and insurance providers while separately identifying **data-quality issues requiring further validation**.
