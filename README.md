# Hospital Readmissions & Length of Stay Analysis (SQL Project)

This project analyzes synthetic hospital encounter data to explore 30-day readmission patterns, length of stay, and utilization trends across patient demographics and hospital departments.
It demonstrates SQL skills commonly used in healthcare analytics, quality reporting, and population health management.

---

## Files in This Repository

## Database Schema
```
+------------------+         +----------------------+
|     Patients     |         |      Encounters      |
+------------------+         +----------------------+
| patient_id  PK   |  1   ─▶ | patient_id   FK      |
| gender           |         | encounter_id   PK     |
| age_group        |         | admit_date            |
| insurance_type   |         | discharge_date        |
|                  |         | department            |
|                  |         | outcome               |
|                  |         | readmitted_30d        |
+------------------+         +----------------------+
```
---

# Project Overview

This project evaluates key hospital performance metrics, including:

- 30-day readmission rate  
- Average length of stay (LOS)  
- High-utilizer patients  
- Differences by insurance type  
- Differences by age group  
- Department-level performance  
- Encounter outcome distribution  

The dataset is synthetic, created solely for educational and portfolio purposes.

---

# Database Schema

+------------------+         +----------------------+
|     Patients     |         |      Encounters      |
+------------------+         +----------------------+
| patient_id  PK   |  1   ─▶ | patient_id   FK      |
| gender           |         | encounter_id   PK     |
| age_group        |         | admit_date            |
| insurance_type   |         | discharge_date        |
|                  |         | department            |
|                  |         | outcome               |
|                  |         | readmitted_30d        |
+------------------+         +----------------------+


---

# Data Dictionary

### Patients
| Column | Description |
|--------|-------------|
| patient_id | Unique patient identifier |
| gender | Male or Female |
| age_group | 18–39, 40–64, 65+ |
| insurance_type | Medicaid, Medicare, Private, Uninsured |

### Encounters
| Column | Description |
|--------|-------------|
| encounter_id | Unique encounter identifier |
| patient_id | Links encounter to a patient |
| admit_date | Admission date |
| discharge_date | Discharge date |
| department | Emergency, Oncology, Cardiology, etc. |
| outcome | Discharged, Transferred, Deceased |
| readmitted_30d | Yes/No flag for 30-day readmission |

---

# Analysis Questions Answered

1. How many total encounters occurred?  
2. What is the overall 30-day readmission rate?  
3. Which departments have the longest average length of stay?  
4. Does readmission rate differ by insurance type?  
5. Which patients have multiple encounters (high utilizers)?  
6. Which departments have the highest readmission rates?  
7. Do readmissions vary by age group?  
8. What is the distribution of outcomes (discharged, deceased, transferred)?  

---

# Key Findings (Based on SQL Results)

### Total Encounters  
15

### Overall Readmission Rate  
Approximately 20 percent

### Longest Average Length of Stay  
Oncology and Neurology departments had the highest LOS.

### Highest Readmission Patterns  
Cardiology and Emergency showed elevated readmission rates.

### High Utilizers  
A few patients had multiple encounters, including 30-day readmissions.

### Insurance Type Differences  
Higher readmission frequency among Medicaid and Medicare groups.

### Age Group Differences  
Patients aged 65+ had higher readmission likelihood.

---

# How to Run This Project

### Option A — SQLiteOnline (Web-Based)
1. Go to https://sqliteonline.com  
2. Select SQLite  
3. Open the hospital_readmissions_project.sql file  
4. Run the script to create tables and load data  
5. Execute the SELECT queries to reproduce results

### Option B — DB Browser for SQLite (Desktop)
1. Install DB Browser for SQLite  
2. Open the .sqlite file included in this repository  
3. Use the “Execute SQL” tab to run queries  

---

# Screenshots

Create a folder named `screenshots` and upload images such as:
- Table previews  
- Readmission rate output  
- LOS by department output  

---

# Skills Demonstrated

- SQL table creation and data modeling  
- Working with primary and foreign keys  
- JOIN operations  
- Aggregate functions and grouping  
- Calculating LOS with date functions  
- Healthcare quality metric analysis  
- Identifying high-utilizer patients  
- GitHub documentation and version control  

---

# End of Project

This project provides a portfolio-ready example of SQL-based healthcare analytics. Additional metrics or dashboards may be added for expansion.

