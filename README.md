➡️ **View the full SQL script:**  
[hospital_readmissions_project.sql](hospital_readmissions_project.sql)

➡️ **Download the SQLite database (.db):**  
[SQLite database](SQLite%20(1).db)

# Hospital Readmissions & Length of Stay Analysis (SQL Project)

This project analyzes **synthetic hospital encounter data** to explore:

- 30-day readmission patterns  
- Length of stay (LOS)  
- High-utilizer patients  
- Differences by insurance type and age  
- Department-level performance  

It showcases SQL skills used in **healthcare analytics, quality reporting, and population health**.  
_All data are fully synthetic and safe for portfolio use._

---

## Files in This Repository

| File | Description |
|------|-------------|
| hospital_readmissions_project.sql | SQL script that creates the schema, loads sample data, and runs analysis queries. |
| hospital_readmissions.sqlite | SQLite database file containing all tables and sample data. |
| screenshots/ | Folder containing screenshots of query outputs and dashboard views. |

---

## Database Schema

Below is the ASCII schema diagram (shown using 4-space indentation so GitHub renders it correctly):

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

---

## Data Dictionary

### **Patients Table**

| Column | Description |
|--------|-------------|
| patient_id | Unique identifier for each patient |
| gender | Male or Female |
| age_group | Age group category (18–39, 40–64, 65+) |
| insurance_type | Medicaid, Medicare, Private, Uninsured |

---

### **Encounters Table**

| Column | Description |
|--------|-------------|
| encounter_id | Unique encounter identifier |
| patient_id | Foreign key linked to Patients |
| admit_date | Hospital admission date |
| discharge_date | Hospital discharge date |
| department | Department (Emergency, Oncology, Cardiology, etc.) |
| outcome | Discharged, Transferred, Deceased |
| readmitted_30d | Yes/No indicator for 30-day readmission |

---

## Analysis Questions Answered

- How many total encounters occurred?  
- What is the overall 30-day readmission rate?  
- Which departments have the longest average LOS?  
- Do readmission rates differ by insurance type?  
- Which patients are high utilizers (multiple encounters)?  
- Which departments have the highest readmission rates?  
- Do readmissions vary by age group?  
- What is the distribution of outcomes?

---

## Key Findings (From Synthetic Dataset)

- **Total encounters:** 15  
- **30-day readmission rate:** ~20%  
- **Departments with longest LOS:** Oncology and Neurology  
- **Most readmissions:** Cardiology and Emergency  
- **High utilizers:** Several patients with multiple encounters  
- **Insurance differences:** Medicaid & Medicare have higher readmissions  
- **Age differences:** 65+ group has higher readmission likelihood  
- **Outcome distribution:** Majority discharged; fewer transfers & deaths  

---

## How to Run This Project

### **Option A — SQLiteOnline (Browser)**

1. Go to https://sqliteonline.com  
2. Select **SQLite**  
3. Paste the contents of hospital_readmissions_project.sql  
4. Run the script  
5. View outputs directly in the results window  

---

### **Option B — DB Browser for SQLite (Desktop)**

1. Install DB Browser for SQLite  
2. Open `hospital_readmissions.sqlite`  
3. Browse the tables  
4. Use the Execute SQL tab to run analysis queries  



# Screenshots

### 1. Raw Encounter Data
![Screenshot 1](screenshots/%231%20screenshot.png)

### 2. Readmission Rate Summary
![Screenshot 2](screenshots/%232%20screenshot.png)

### 3. Length of Stay by Department
![Screenshot 3](screenshots/%233%20screenshot.png)


# Skills Demonstrated

-   SQL table creation and relationships
-   Data modeling (fact and dimension tables)
-   JOINs and aggregations
-   Calculating LOS using date functions
-   Readmission metric calculation
-   Identifying high-utilizer patients
-   Healthcare analytics reporting
-   GitHub documentation and version control


# End of Project

This project showcases core SQL skills used in healthcare analytics and
can be extended with dashboards, additional metrics, or automated
reporting workflows.
