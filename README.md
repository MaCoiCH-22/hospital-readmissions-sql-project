➡️ **View the full SQL script:**  
[hospital_readmissions_project.sql](hospital_readmissions_project.sql)

➡️ **Download the SQLite database (.db):**  
[SQLite database](SQLite%20(1).db)

# Hospital Readmissions & Length of Stay Analysis (SQL Project)

This project analyzes synthetic hospital encounter data to explore
30-day readmission patterns, length of stay, and utilization trends
across patient demographics and hospital departments. It demonstrates
SQL skills relevant to healthcare analytics, quality reporting, and
population health.

## Files in This Repository

  ------------------------------------------------------------------------------------
  File                                Description
  ----------------------------------- ------------------------------------------------
  hospital_readmissions_project.sql   SQL script that creates tables, loads sample
                                      data, and runs analysis queries

  hospital_readmissions.sqlite        SQLite database file containing all tables and
                                      sample data
  ------------------------------------------------------------------------------------

# Project Overview

This project evaluates key hospital performance indicators, including:

-   30-day readmission rate
-   Average length of stay (LOS)
-   High-utilizer patients
-   Differences by insurance type
-   Differences by age group
-   Department-level performance
-   Encounter outcome distribution

The dataset is synthetic and used for educational and portfolio
purposes.

# Database Schema

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

# Data Dictionary

## Patients Table

  Column           Description
  ---------------- ------------------------------------------
  patient_id       Unique identifier for each patient
  gender           Male or Female
  age_group        Age group category (18--39, 40--64, 65+)
  insurance_type   Medicaid, Medicare, Private, Uninsured

## Encounters Table

  -----------------------------------------------------------------------
  Column                      Description
  --------------------------- -------------------------------------------
  encounter_id                 Unique encounter identifier

  patient_id                   Foreign key linking to the Patients table

  admit_date                   Hospital admission date

  discharge_date               Hospital discharge date

  department                   Department of care (Emergency, Oncology,
                              Cardiology, etc.)

  outcome                      Discharged, Transferred, Deceased

  readmitted_30d               Yes/No indicator for 30-day readmission
  -----------------------------------------------------------------------

# Analysis Questions Answered

1.  How many total encounters occurred?
2.  What is the overall 30-day readmission rate?
3.  Which departments have the longest average length of stay?
4.  Does readmission rate differ by insurance type?
5.  Which patients have multiple encounters (high utilizers)?
6.  Which departments have the highest readmission rates?
7.  Do readmissions vary by age group?
8.  What is the distribution of outcomes (discharged, deceased,
    transferred)?

# Key Findings

### Total Encounters

15 total encounters were recorded.

### Overall 30-Day Readmission Rate

Approximately 20 percent.

### Departments with the Longest LOS

Oncology and Neurology had the highest average LOS.

### Departments with Higher Readmissions

Cardiology and Emergency showed elevated readmission frequency.

### High-Utilizer Patients

Several patients had multiple encounters, including 30-day readmissions.

### Insurance Type Differences

Medicaid and Medicare patients showed higher readmission patterns.

### Age Group Differences

Patients aged 65+ had higher readmission likelihood.

# How to Run This Project

## Option A --- SQLiteOnline (Web-Based)

1.  Visit https://sqliteonline.com
2.  Select SQLite
3.  Paste or upload the hospital_readmissions_project.sql file
4.  Run the script to create and populate the tables
5.  Execute analysis queries

## Option B --- DB Browser for SQLite (Desktop)

1.  Install DB Browser for SQLite
2.  Open the .sqlite file
3.  Use the Execute SQL tab to run queries

# Screenshots

Place screenshots into a folder named `screenshots`.

Recommended images: - Output of SELECT \* FROM Encounters\
- Readmission-rate query output
- LOS by department output

# Skills Demonstrated

-   SQL table creation and relationships
-   Data modeling (fact and dimension tables)
-   JOINs and aggregations
-   Calculating LOS using date functions
-   Readmission metric calculation
-   Identifying high-utilizer patients
-   Healthcare analytics reporting
-   GitHub documentation and version control

  ## Screenshots

### 1. Raw Encounter Data
![Screenshot 1](screenshots/%231%20screenshot.png)

### 2. Readmission Rate Summary
![Screenshot 2](screenshots/%232%20screenshot.png)

### 3. Length of Stay by Department
![Screenshot 3](screenshots/%233%20screenshot.png)


# End of Project

This project showcases core SQL skills used in healthcare analytics and
can be extended with dashboards, additional metrics, or automated
reporting workflows.
