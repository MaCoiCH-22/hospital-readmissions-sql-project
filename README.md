Hospital Readmissions & Length of Stay Analysis (SQL Project)

This project analyzes synthetic hospital encounter data to explore 30-day readmission patterns, length of stay, and utilization trends across patient demographics and hospital departments.
It demonstrates SQL skills commonly used in healthcare analytics, quality reporting, and population health management.

Files in This Repository
File	Description
hospital_readmissions_project.sql	Full SQL script: creates schema, loads sample data, and runs analysis queries
hospital_readmissions.sqlite / SQLite(1).db	SQLite database file containing all tables and sample data
Project Overview

This project evaluates key hospital performance metrics, including:

30-day readmission rate

Average length of stay (LOS)

High-utilizer patients

Differences by insurance type

Differences by age group

Department-level performance

Encounter outcome distribution

The dataset is synthetic, created solely for educational and portfolio purposes.

Database Schema
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
patient_id	Unique patient identifier
gender	Male or Female
age_group	18–39, 40–64, 65+
insurance_type	Medicaid, Medicare, Private, Uninsured
Encounters
Column	Description
encounter_id	Unique encounter identifier
patient_id	Links encounter to a patient
admit_date	Admission date
discharge_date	Discharge date
department	Emergency, Oncology, Cardiology, etc.
outcome	Discharged, Transferred, Deceased
readmitted_30d	Yes/No flag for 30-day readmission
Analysis Questions Answered

How many total encounters occurred?

What is the overall 30-day readmission rate?

Which departments have the longest average length of stay?

Does readmission rate differ by insurance type?

Which patients have multiple encounters (high utilizers)?

Which departments have the highest readmission rates?

Do readmissions vary by age group?

What is the distribution of outcomes (discharged, deceased, transferred)?

Key Findings (Based on SQL Results)
Total Encounters

15

Overall Readmission Rate

Approximately 20 percent

Longest Average Length of Stay

Departments with the longest LOS include Oncology and Neurology.

Highest Readmission Patterns

Cardiology and Emergency showed elevated readmission rates.

High Utilizers

A small number of patients had multiple encounters, including readmissions.

Insurance Type Differences

Higher readmission frequency among Medicaid and Medicare groups.

Age Group Differences

Patients aged 65 and above showed higher readmission rates.

How to Run This Project
Option A — SQLiteOnline (Web-Based)

Visit: https://sqliteonline.com

Select SQLite

Open the hospital_readmissions_project.sql file

Run the script to create tables and load data

Execute the SELECT queries to reproduce results

Option B — DB Browser for SQLite (Desktop App)

Install DB Browser for SQLite

Open the .sqlite file included in this repository

Use the “Execute SQL” tab to run queries

Screenshots

Add screenshots into a folder named screenshots.

Suggested images:

Table previews (SELECT * FROM Encounters)

Readmission rate query output

LOS by department output

Skills Demonstrated

SQL table creation and data modeling

Use of primary and foreign keys

JOIN operations

Aggregate functions and grouping

Calculating length of stay using date functions

Healthcare quality metric calculation

Identifying high-utilizer patients

GitHub project documentation and version control

End of Project

This project represents a realistic example of SQL-based healthcare analytics and can be expanded with additional metrics or dashboards as needed.
