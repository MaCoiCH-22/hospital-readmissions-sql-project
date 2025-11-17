🏥 Hospital Readmissions & Length of Stay Analysis (SQL Project)

This project analyzes synthetic hospital encounter data to explore 30-day readmission patterns, length of stay (LOS), and utilization trends across departments, insurance types, and age groups.
It demonstrates SQL skills commonly used in healthcare analytics, quality reporting, and population health management.

📂 Files in This Repository
File	Description
hospital_readmissions_project.sql	Full SQL script: creates schema, loads sample data, runs analysis queries
hospital_readmissions.sqlite / SQLite(1).db	SQLite database file containing all tables + data
📊 Project Overview

The goal of this project is to evaluate key hospital performance indicators, including:

✔ 30-day readmission rate
✔ Average length of stay (LOS)
✔ High-utilizer patients
✔ Differences by insurance type
✔ Differences by age group
✔ Department-level performance
✔ Encounter outcomes (discharged, transferred, deceased)

The dataset is synthetic, created solely for educational and portfolio purposes.

🗂 Database Schema
+------------------+         +----------------------+
|     Patients     |         |      Encounters      |
+------------------+         +----------------------+
| patient_id  PK   |  1   ─▶ | patient_id   FK      |
| gender           |         | encounter_id   PK    |
| age_group        |         | admit_date           |
| insurance_type   |         | discharge_date       |
|                  |         | department           |
|                  |         | outcome              |
|                  |         | readmitted_30d       |
+------------------+         +----------------------+

Data Dictionary
Patients
Column	Description
patient_id	Unique ID for each patient
gender	Male / Female
age_group	18–39, 40–64, 65+
insurance_type	Medicaid, Medicare, Private, Uninsured
Encounters
Column	Description
encounter_id	Unique encounter ID
patient_id	Links encounter to a patient
admit_date	Admission date
discharge_date	Discharge date
department	Emergency, Oncology, Cardiology, etc.
outcome	Discharged, Transferred, Deceased
readmitted_30d	Yes / No
🔍 Analysis Questions Answered

The SQL file answers:
1️. How many encounters occurred?
2️. What is the overall 30-day readmission rate?
3️. Which departments have the longest average LOS?
4️. Does readmission rate differ by insurance type?
5️. Which patients have multiple encounters (high utilizers)?
6. Which departments have the highest readmission rates?
7. Do readmissions vary by age group?
8. What is the distribution of outcomes (discharged, deceased, transferred)?

Key Findings 
Total Encounters: 15
Overall Readmission Rate: ~20%
Highest LOS:
Oncology had the longest average stay
Emergency had the shortest LOS
Highest Readmission Rate:
Cardiology and Emergency showed elevated readmission patterns
High Utilizer Patients:
A few patients had multiple encounters within the dataset
Some were readmitted within 30 days
Insurance-Type Differences:
Medicaid and Medicare groups showed higher readmission rates
Private insurance showed fewer readmissions
Age Group Differences:
Older adults (65+) had higher readmission likelihood
