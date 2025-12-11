<p align="center">
  <img src="https://github.com/user-attachments/assets/11c9bf01-dd06-4f01-a29e-9eb54f80a998" width="90" alt="StudentSight Logo"/>
</p>

# 🎓 **StudentSight**
### **Student Performance Analytics Dashboard**
> *A complete end-to-end educational data pipeline empowering data-driven decisions in schools.*

---

# 📘 **Project Overview**

StudentSight is a full analytical ecosystem designed to transform raw, unstructured student performance data into clear, actionable insights.  
Using a pipeline powered by **PySpark**, **SQL databases**, **PostgreSQL**, **Docker**, and **Power BI**, the project centralizes performance records, cleans and standardizes the data, builds a structured analytical warehouse, and visualizes the results through an interactive dashboard.

The final platform helps teachers, administrators, and stakeholders monitor academic performance, identify struggling students early, and make informed, data-driven decisions.

---

# ❗ Problem & 🎯 Solution Scope

## 🔍 The Problem
Schools and training institutions often face recurring issues:

- Scattered spreadsheets and manual entries  
- Difficulty identifying struggling students early  
- No link between attendance, grades, and demographic data  
- Missing real-time insights for administrators  
- Late academic feedback  
- No standardized data structure or validation  

These gaps cause **delayed interventions**, **inaccurate insights**, and **lost opportunities for improvement**.

---

## 💡 The Solution: StudentSight

StudentSight solves these challenges with a scalable data pipeline that:

1. **Centralizes** academic and behavior data  
2. **Cleans & transforms** raw input using PySpark  
3. **Stores** validated data in SQL & PostgreSQL warehouses  
4. **Enables reliable analysis** using dimensional modeling  
5. **Visualizes insights** with interactive Power BI dashboards  

Becoming the **single source of truth**, the system enables stakeholders to explore:

- Performance trends  
- Attendance correlations  
- Class vs. student outcomes  
- High achievers and at-risk students  

---

# 🛠 **Technologies Used**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![PySpark](https://img.shields.io/badge/PySpark-FDEE21?style=for-the-badge&logo=apachespark&logoColor=black)
![MySQL](https://img.shields.io/badge/MySQL-005E87?style=for-the-badge&logo=mysql&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=for-the-badge&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Power BI](https://img.shields.io/badge/PowerBI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)

---

# 🏗 **Architecture**

### 🔸 1. Data Extraction  
Raw academic data (scores, attendance, demographic details) is collected from multiple sources.

### 🔸 2. PySpark Transformation  
Performs:
- Data cleaning  
- Validation  
- Deduplication  
- Feature engineering  
- Standardization  

### 🔸 3. MySQL Staging Layer  
Temporary storage for validated data before final modeling.

### 🔸 4. PostgreSQL Analytical Warehouse  
Supports:
- Fast queries  
- Relational modeling  
- Aggregated reporting  
- Historical tracking  

### 🔸 5. Power BI Reporting Layer  
Provides:
- Performance insights  
- Trends  
- Drill-down analysis  

---

# 🗄 **Database Design (High-Level)**

Structured using dimensional modeling.

### ✔ Dimensions  
Context tables for students, teachers, courses, families, and calendar metadata.

### ✔ Facts  
Event-based tables storing performance and attendance records.

Benefits:
- Fast aggregation  
- Flexible analysis  
- Strong referential integrity  
- Smooth Power BI integration  

---

# 📷 **Screenshots**

![Image](https://github.com/user-attachments/assets/c8cd660e-ff09-4495-8802-4ed67b5a8554)
![Image](https://github.com/user-attachments/assets/552664df-f558-41fa-beaf-ab9849bccc58)
![Image](https://github.com/user-attachments/assets/05616ab6-d417-4376-8d1d-bc5153c2ab55)
![Image](https://github.com/user-attachments/assets/6d0ad09a-bea6-41c7-b91f-17b0bb5cca85)
<img width="1601" height="1460" alt="Image" src="https://github.com/user-attachments/assets/0e4b0383-9309-4e11-af52-b02c56812787" />

---

# 🌟 **Key Features of the Dashboard**

The StudentSight dashboard is designed to give educators a clear, interactive, and intuitive understanding of student performance.  
Below are screenshots of the main report pages, followed by a detailed explanation of the visualizations and analytical logic behind them.

![Image](https://github.com/user-attachments/assets/161984af-1c28-42aa-80b8-d4bad8dc0dac)

![Image](https://github.com/user-attachments/assets/2c1b412c-12e4-4564-89e3-1bf426dd45c0)

---

## 📊 **Dashboard Visualization Overview**

The dashboard delivers a balanced blend of **high-level KPIs**, **analytical charts**, and **student-level drill-downs**, making it easy for teachers and administrators to evaluate academic performance from multiple angles.

It consists of the following major visualization components:

### **📌 Modern KPI Insights**
A set of card visuals providing fast, essential metrics, including:
- Total number of students  
- Average score across all courses  
- Overall pass rate  
- Attendance percentage  

These KPIs serve as the starting point for understanding school-wide academic health.

### **📌 Demographic & Academic Analytics**
Visualizations designed to help stakeholders understand *who* the students are and *how* they're performing:
- **Gender breakdown** to view population distribution  
- **Geographical segmentation** to assess family and regional grouping  
- **Grade distribution charts** that visually cluster students by performance categories  
- **Subject and course comparisons** to identify difficult or high-performing subjects  

These charts provide context behind the scores and highlight disparities between student groups.


### **📌 Deep Performance Intelligence**
Focused visuals that uncover patterns in achievement:
- Ranking tables that showcase **top performers**  
- Metrics that identify **students at academic risk**  
- Trend charts showing score progression across terms  
- Histogram-style visuals for **grade clustering** and score ranges  

These insights help teachers quickly identify outliers—both strong and weak.


### **📌 Attendance & Achievement Correlation**
A dedicated scatter plot showing:
- Student attendance percentage  
- Their corresponding average score  

This visualization reveals whether lower attendance is linked to weaker academic performance—an essential metric for early intervention.


### **📌 Drill-Down Student Profiles**
A detailed page designed for individual student analysis:
- Personal and demographic details  
- Attendance rate  
- Overall and course-specific average scores  
- Assigned grade  
- City and family data  

This level of granularity supports one-on-one student evaluations and parent-teacher discussions.


---

# 🧠 **Model View & DAX Measures**

![Image](https://github.com/user-attachments/assets/6f06a3e6-144e-4b1a-b74e-7705c3ffedba)

The Data Model was carefully structured to ensure smooth navigation and accurate analytical calculations:

### **🔗 Optimized Model View**
- The warehouse was imported into Power BI with a **snowflake-style dimensional model**, ensuring clean, one-directional relationships.  
- Fact tables were connected to their respective dimensions using **single-direction, many-to-one relationships** for reliable filtering.  
- Only essential relationships were activated to avoid ambiguity and improve performance.

### **🧮 Custom DAX Measures**
To enable accurate insights, several DAX measures were created, including:
- **Average Score** (ignoring blanks)  
- **Pass Rate %** based on dynamic filtering  
- **Attendance %** aggregated per student and across the whole dataset  
- **Top N performance measures** used for ranking  
- **Customized grade assignment logic** for visualization consistency  

These DAX expressions ensured that KPIs and visuals respond instantly to filters, slicers, and drill-down interactions without breaking model integrity.

Together, the dashboard, data model, and DAX logic create a seamless analytical experience—allowing educators to explore high-level trends and drill into individual student stories with ease. 

---

# 👥 **Team**

| Name | Role | Responsibilities |
|------|------|------------------|
| **Abdelrahman Mohamed Fathi (ME)** | **Team Leader & Head of Data Visualization** | **Led the team, managed workflow, directed system architecture, and built the core analytical visuals & dashboard storytelling in Power BI** |
| **Sabry Tarek Sabry** | PySpark ETL Developer & Docker Lead | ETL pipelines, containerization |
| **Ahmed Osama Ahmed** | SQL Database Architect | Warehouse schema & modeling |
| **Ahmed Moustafa Mahmoud** | Data Visualization Developer | Power BI visuals & analytics |
| **Esraa Mahmoud Abdelrahman** | Documentation & Presentation | Final report & content curation |


---

# 🔮 **Future Enhancements**

- Personalized dashboards  
- Predictive analytics (MLlib)  
- Automated ETL pipelines (Airflow)  
- Interactive app for parents & students 
- Real-time ingestion  

