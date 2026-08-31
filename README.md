# medical-operations-dashboard-team-a-batch-2

🏥 Medical Operations Intelligence Dashboard

## Project Overview

The **Medical Operations Intelligence Dashboard** is a healthcare analytics platform developed to monitor and analyze hospital operational performance. The project integrates multiple healthcare datasets, calculates key operational metrics, identifies trends, and provides actionable insights for hospital administrators.

The objective is to transform raw healthcare operational data into meaningful intelligence that supports data-driven decision-making, resource optimization, and improved patient service delivery.

---

# Project Objectives

* Integrate healthcare operational datasets.
* Clean and preprocess healthcare data.
* Calculate operational Key Performance Indicators (KPIs).
* Analyze patient flow and service demand.
* Monitor resource utilization and operational capacity.
* Generate operational insights through trend analysis.
* Build interactive dashboards for healthcare management.

---

# Key Features

### Module 1 – Healthcare Data Integration & Operational Analytics

* Healthcare data generation       | ✅ Completed |
* Data cleaning and preprocessing  | ✅ Completed |
* Data integration
* KPI calculation
* Trend analysis
* Operational insights generation
* Data validation

# Project Structure

```text
Medical Dashboard Project/
│
├── data/
│   ├── raw/                    | ✅ Completed |
│   │   ├── patients.csv        | ✅ Completed |
│   │   ├── admissions.csv      | ✅ Completed |
│   │   ├── treatments.csv      | ✅ Completed |
│   │   ├── staff.csv           | ✅ Completed |
│   │   ├── beds.csv            | ✅ Completed |
│   │   └── facilities.csv      | ✅ Completed |
│   │
│   └── processed/
│       ├── cleaned_patients.csv            | ✅ Completed |
│       ├── cleaned_admissions.csv          | ✅ Completed |
│       ├── cleaned_treatments.csv          | ✅ Completed |
│       ├── cleaned_staff.csv               | ✅ Completed |
│       ├── cleaned_beds.csv                | ✅ Completed |
│       ├── cleaned_facilities.csv          | ✅ Completed |
│       ├── integrated_healthcare_data.csv  | ✅ Completed |
│       ├── operational_kpis.csv            | ✅ Completed |
│       ├── department_workload.csv         | ✅ Completed |
│       ├── treatment_demand.csv            | ✅ Completed |
│       ├── monthly_admissions.csv          | ✅ Completed |
│       ├── monthly_discharges.csv          | ✅ Completed |
│       ├── monthly_treatments.csv          | ✅ Completed |
│       └── department_monthly_workload.csv | ✅ Completed |
│
├── notebooks/
│   └── eda_analysis.ipynb       | ✅ Completed |
│
├── src/
│   ├── generate_data.py        | ✅ Completed |
│   ├── data_cleaning.py        | ✅ Completed |
│   ├── data_integration.py     | ✅ Completed |
│   ├── kpi_calculation.py      | ✅ Completed |
│   ├── trend_analysis.py       | ✅ Completed |
│   ├── operational_insights.py | ✅ Completed |
│   
│
├── README.md           | ✅ Updated Till Module 2 |
```

---

# Dataset Description

The project uses six operational healthcare datasets.

## Patients

Stores patient demographic information.

Columns:

* patient_id
* patient_name
* age
* gender
* city
* blood_group
* registration_date

---

## Admissions

Stores hospital admission records.

Columns:

* admission_id
* patient_id
* department
* admission_date
* discharge_date
* admission_type
* diagnosis

---

## Treatments

Stores treatment-related information.

Columns:

* treatment_id
* patient_id
* department
* treatment_type
* treatment_date
* treatment_status
* treatment_cost

---

## Staff

Stores hospital workforce information.

Columns:

* staff_id
* staff_name
* role
* department
* experience_years
* shift
* shifts_assigned
* shifts_worked

---

## Beds

Stores hospital bed utilization data.

Columns:

* bed_id
* department
* room_number
* status
* bed_type

---

## Facilities

Stores healthcare facility information.

Columns:

* facility_id
* facility_name
* city
* capacity
* utilization_rate

---

# Technologies Used

* Python 3.x
* Pandas
* NumPy
* Plotly
* Dash
* Matplotlib
* Folium
* GeoPandas

---

# Module 1 Workflow

```
Raw Healthcare Data
        │
        ▼
Data Generation
        │
        ▼
Data Cleaning
        │
        ▼
Data Integration    
        │
        ▼
KPI Calculation     
        │
        ▼
Trend Analysis      
        │
        ▼
Operational Insights 
        │
        ▼
Module 1 Validation Done
```

---

## 📊 Exploratory Data Analysis (EDA)

An Exploratory Data Analysis (EDA) was performed on the cleaned healthcare datasets to understand data distribution, identify trends, validate data quality, and generate meaningful operational insights.

### EDA Objectives
- Analyze patient demographics and registration patterns.
- Study hospital admission and discharge trends.
- Evaluate treatment demand and service utilization.
- Assess staff distribution and workforce efficiency.
- Analyze bed occupancy and resource utilization.
- Examine healthcare facility distribution and capacity.
- Identify relationships between numerical variables using correlation analysis.

### EDA Components

#### 1. Data Understanding
- Dataset overview
- Dataset dimensions
- Data types
- Statistical summary
- Missing value analysis
- Duplicate record analysis

#### 2. Patient Analysis
- Age Distribution
- Gender Distribution
- Patient Distribution by City

#### 3. Admission Analysis
- Admissions by Department
- Admission Type Distribution
- Monthly Admission Trend
- Length of Stay Distribution

#### 4. Treatment Analysis
- Treatment Type Distribution
- Treatment Status Distribution
- Monthly Treatment Trend

#### 5. Staff Analysis
- Staff Distribution by Department
- Staff Distribution by Role
- Staff Efficiency Distribution

#### 6. Bed Analysis
- Bed Occupancy Status
- Bed Distribution by Department

#### 7. Facility Analysis
- Facility Capacity (Total Beds)
- Facility Type Distribution
- Facility Distribution by City

#### 8. Correlation Analysis
- Correlation Matrix for Numerical Features

#### 9. Key Insights
- Highest admission month identified.
- Department with the highest patient workload identified.
- Most demanded treatment identified.
- Bed utilization patterns analyzed.
- Staff efficiency evaluated.
- Operational trends summarized for decision-making.

---

## 📈 EDA Outcome

The exploratory data analysis provided valuable insights into healthcare operations by identifying patient flow patterns, treatment demand, workforce utilization, bed occupancy, and facility distribution. The findings establish a strong analytical foundation for developing the Medical Operations Intelligence Dashboard in the subsequent project modules.

---

## 📁 EDA Notebook

```
notebooks/
└── eda_analysis.ipynb
```


---------

# Operational KPIs

The system calculates:

* Total Patients
* Total Admissions
* Total Discharges
* Average Length of Stay
* Bed Utilization
* Staff Efficiency
* Department Workload
* Treatment Demand

---

# Trend Analysis

The system generates:

* Monthly Admission Trends
* Monthly Discharge Trends
* Monthly Treatment Trends
* Department Monthly Workload

---

# Operational Insights

The project automatically identifies:

* Highest Admission Month
* Lowest Admission Month
* Highest Workload Department
* Most Demanded Treatment
* Bed Utilization Status
* Staff Efficiency Status

---

# Module 2 - Healthcare Operations Analysis

## Objective

The objective of Module 2 was to perform deeper operational analysis using the cleaned healthcare datasets and prepare insights that could support hospital management decisions.

The main areas covered were:

1. Patient Flow Analysis
2. Service Demand Analysis
3. Department Workload Analysis
4. Operational Bottleneck Analysis
5. Department Performance Analysis
6. Monthly Department Trend Analysis
7. Treatment Completion Analysis
8. Operational Risk Analysis
9. Power BI Dashboard Development

---

# 1. Patient Flow Analysis

The admissions dataset was analyzed to understand patient movement and admission patterns.

### Analyses Performed

- Monthly admissions
- Monthly discharges
- Admission type distribution
- Department-wise patient flow
- Average length of stay

### Results

Average Length of Stay:

**7.58 days**

Admission types:

- Referral: **682**
- Routine: **664**
- Emergency: **654**

Department patient flow:

| Department | Patients |
|---|---:|
| General Medicine | 272 |
| Oncology | 263 |
| Dermatology | 262 |
| Emergency | 258 |
| Cardiology | 256 |
| Neurology | 249 |
| Pediatrics | 221 |
| Orthopedics | 219 |

---

# 2. Service Demand Analysis

Treatment data was analyzed to understand the demand for different healthcare services.

### Treatment Demand

| Treatment Type | Count |
|---|---:|
| Consultation | 432 |
| Surgery | 401 |
| Medication | 392 |
| Diagnostics | 388 |
| Therapy | 387 |

### Treatment Status

| Status | Count |
|---|---:|
| Completed | 1501 |
| Pending | 396 |
| Cancelled | 103 |

### Key Finding

**Consultation** was the most demanded treatment with **432 treatments**.

---

# 3. Department Workload Analysis

Department workload was calculated using admissions and treatments.

### Results

| Department | Admissions | Treatments | Total Workload | Rank |
|---|---:|---:|---:|---:|
| Neurology | 249 | 291 | 540 | 1 |
| Oncology | 263 | 260 | 523 | 2 |
| Dermatology | 262 | 244 | 506 | 3 |
| Cardiology | 256 | 249 | 505 | 4 |
| Emergency | 258 | 247 | 505 | 5 |
| General Medicine | 272 | 218 | 490 | 6 |
| Pediatrics | 221 | 247 | 468 | 7 |
| Orthopedics | 219 | 244 | 463 | 8 |

### Key Findings

- Highest workload department: **Neurology**
- Lowest workload department: **Orthopedics**
- Neurology had a total workload of **540**.

---

# 4. Operational Bottleneck Analysis

An operational bottleneck report was created to identify important operational pressure points.

### Results

| Metric | Result |
|---|---|
| Highest Admission Month | 2025-08 |
| Lowest Admission Month | 2025-09 |
| Highest Discharge Month | 2025-08 |
| Lowest Discharge Month | 2026-07 |
| Highest Workload Department | Neurology |
| Lowest Workload Department | Orthopedics |
| Most Demanded Treatment | Consultation |
| Most Common Admission Type | Referral |
| Average Length of Stay | 7.58 days |

This analysis helps identify periods and departments requiring closer operational monitoring.

---

# 5. Department Performance Analysis

Department performance was evaluated using admissions, average length of stay, treatments, workload, and a calculated performance score.

### Results

| Department | Admissions | Avg. Length of Stay | Treatments | Workload | Performance Score | Rank |
|---|---:|---:|---:|---:|---:|---:|
| Neurology | 249 | 8.00 | 291 | 540 | 100.00 | 1 |
| Oncology | 263 | 7.72 | 260 | 523 | 96.85 | 2 |
| Dermatology | 262 | 7.55 | 244 | 506 | 93.70 | 3 |
| Cardiology | 256 | 7.37 | 249 | 505 | 93.52 | 4 |
| Emergency | 258 | 7.25 | 247 | 505 | 93.52 | 5 |
| General Medicine | 272 | 7.37 | 218 | 490 | 90.74 | 6 |
| Pediatrics | 221 | 7.91 | 247 | 468 | 86.67 | 7 |
| Orthopedics | 219 | 7.53 | 244 | 463 | 85.74 | 8 |

### Key Findings

- Top performing department: **Neurology**
- Average department performance score: **92.59**

---

# 6. Monthly Department Trend Analysis

Monthly trends were analyzed by combining departmental admissions and treatments.

The analysis generated **144 department-month records**.

The following metrics were included:

- Department
- Month
- Admissions
- Treatments
- Total Workload

This analysis helps understand how workload changes across departments over time.

---

# 7. Treatment Completion Analysis

Treatment completion performance was analyzed for each department.

### Results

| Department | Total Treatments | Completed | Pending | Cancelled | Completion Rate |
|---|---:|---:|---:|---:|---:|
| Neurology | 291 | 228 | 49 | 14 | 78.35% |
| Orthopedics | 244 | 187 | 44 | 13 | 76.64% |
| Emergency | 247 | 189 | 45 | 13 | 76.52% |
| Pediatrics | 247 | 188 | 48 | 11 | 76.11% |
| Cardiology | 249 | 188 | 53 | 8 | 75.50% |
| General Medicine | 218 | 162 | 41 | 15 | 74.31% |
| Oncology | 260 | 191 | 56 | 13 | 73.46% |
| Dermatology | 244 | 168 | 60 | 16 | 68.85% |

### Key Findings

- Best performing department: **Neurology**
- Average completion rate: **74.97%**
- Dermatology had the lowest completion rate at **68.85%**.
- Dermatology also had the highest pending rate at **24.59%**.

---

# 8. Operational Risk Analysis

Operational risks were identified using department workload and treatment completion performance.

### Risks Identified

| Department | Risk Type | Severity | Recommendation |
|---|---|---|---|
| Neurology | High Workload | High | Review staffing and resource allocation |
| Oncology | High Workload | High | Review staffing and resource allocation |
| Oncology | Low Completion Rate | Medium | Investigate treatment delays |
| Dermatology | High Workload | High | Review staffing and resource allocation |
| Dermatology | Low Completion Rate | Medium | Investigate treatment delays |
| Cardiology | High Workload | High | Review staffing and resource allocation |
| Emergency | High Workload | High | Review staffing and resource allocation |
| General Medicine | Low Completion Rate | Medium | Investigate treatment delays |

### Total Risks Identified

**8 risks**

---

# Module 2 Power BI Dashboard

The final Power BI dashboard was developed using the healthcare datasets available in the project.

## Data Tables Used in Power BI

The Power BI model contains the following tables:

- `admissions`
- `beds`
- `Date`
- `facilities`
- `patients`
- `staff`
- `treatments`

The `Date` table is used for date-based analysis and trends.

---

# Final Dashboard Pages

The final Power BI dashboard contains **six pages**.

## 1. Executive Dashboard

The Executive Dashboard provides an overall view of hospital operations.

### Main KPIs

- Total Patients
- Total Admissions
- Total Treatments
- Total Staff
- Total Facilities
- Total Beds

### Main Visuals

- Admissions by Department
- Monthly Admissions Trend
- Patient Distribution by City
- Patients by Gender
- Department and other filtering options

This page provides hospital management with a high-level overview of operational activity.

<img width="1330" height="746" alt="image" src="https://github.com/user-attachments/assets/be108e94-19c6-4e45-b745-8b97676566d5" />


---

# 2. Patient Analytics Dashboard

The Patient Analytics page focuses on patient demographics and registration patterns.

### Main KPIs

- Total Patients
- Average Age
- Male Patients
- Female Patients
- Cities Covered

### Main Visuals

- Patients by Age Group
- Top 5 Cities by Patients
- Patients by Gender
- Patient Age Distribution
- Patient Registration Trend

### Filters

- Gender
- City
- Registration Date

<img width="1323" height="744" alt="image" src="https://github.com/user-attachments/assets/866ae029-c71d-4bba-8911-69e137e08268" />


---

# 3. Admissions Analytics Dashboard

The Admissions Analytics page focuses on admission activity and patient flow.

### Main KPIs

- Total Admissions
- Average Length of Stay
- Emergency Admissions
- Routine Admissions
- Discharged Admissions

### Main Visuals

- Admissions by Department
- Admissions by Type
- Admissions by Length of Stay
- Monthly Admissions Trend
- Admissions by Department & Type

### Filters

- Admission Type
- Department
- Admission Date
- Discharge Date

<img width="1323" height="749" alt="image" src="https://github.com/user-attachments/assets/e0983587-5ec4-42b5-9de5-3f83737fce37" />


---

# 4. Facilities Analytics Dashboard

The Facilities Analytics page provides information about hospital facilities and bed capacity.

### Main KPIs

- Total Facilities
- Total Beds
- Cities Covered
- Average Beds per Facility
- Maximum Facility Beds

### Main Visuals

- Facilities by Type
- Beds by Facility Type
- Top 10 Facilities by Bed Capacity
- Facilities by City

### Filters

- Facility Type
- City
- Facility Name

<img width="1328" height="735" alt="image" src="https://github.com/user-attachments/assets/965c22a0-7d8e-4ea6-8b03-3391a877c615" />


---

# 5. Staff Analytics Dashboard

The Staff Analytics page focuses on workforce distribution, shifts, and staff efficiency.

### Main KPIs

- Total Staff
- Total Shifts Worked
- Total Shifts Assigned
- Departments Covered
- Average Staff Efficiency

### Main Visuals

- Staff by Department
- Staff by Role
- Shifts Worked vs Assigned by Department
- Staff Efficiency by Role
- Staff Efficiency by Department

### Filters

- Department
- Role

<img width="1327" height="742" alt="image" src="https://github.com/user-attachments/assets/67b1aa6c-f01e-4f19-afe4-eb020e09d6f7" />


---

# 6. Treatment Analytics Dashboard

The Treatment Analytics page focuses on healthcare service demand and treatment completion.

### Main KPIs

- Total Treatments
- Pending Treatments
- Cancelled Treatments
- Completed Treatments
- Treatment Types

### Main Visuals

- Treatments by Type
- Treatment Status Distribution
- Monthly Treatment Trend
- Treatments by Department
- Treatments by Department & Type

### Filters

- Treatment Status
- Treatment Type
- Department
- Date

<img width="1327" height="731" alt="image" src="https://github.com/user-attachments/assets/a82cc236-8aef-4e90-806e-1d1a338e189a" />


---

# Power BI Dashboard Features

The final dashboard provides interactive analysis through:

- KPI cards
- Bar charts
- Donut charts
- Line charts
- Stacked column charts
- Maps
- Date filters
- Department filters
- Gender filters
- City filters
- Treatment filters
- Interactive navigation between dashboard pages

The dashboard allows hospital management to explore operational data from multiple perspectives.

---

# Key Module 2 Insights

The major insights obtained during Module 2 include:

1. **Neurology** had the highest overall department workload.
2. **Orthopedics** had the lowest department workload.
3. **Consultation** was the most demanded treatment.
4. The average length of stay was **7.58 days**.
5. **Neurology** had the highest treatment completion rate of **78.35%**.
6. **Dermatology** had the lowest treatment completion rate of **68.85%**.
7. **8 operational risks** were identified.
8. August 2025 had the highest admission activity.
9. September 2025 had the lowest admission activity.
10. Referral was the most common admission type.
11. Staff efficiency averaged approximately **84.34%**.
12. The final Power BI dashboard provides six analytical views of hospital operations.

---

# Tools & Technologies

## Programming & Analysis

- Python
- Pandas
- Matplotlib
- Jupyter Notebook

## Visualization & Business Intelligence

- Microsoft Power BI

## Development Environment

- VS Code
- Jupyter Notebook

## Version Control

- Git
- GitHub

---

# Project Progress

## Module 1

 Dataset Collection
 Data Cleaning
 Data Preparation
 Data Integration
 KPI Generation
 Exploratory Data Analysis
 EDA Charts
 README Documentation
 GitHub Pull Request

## Module 2

 Patient Flow Analysis
   Service Demand Analysis
   Department Workload Analysis
   Operational Bottleneck Analysis
   Department Performance Analysis
   Monthly Department Trend Analysis
   Treatment Completion Analysis
   Operational Risk Analysis
   Power BI Data Model
   Executive Dashboard
   Patient Analytics Dashboard
   Admissions Analytics Dashboard
   Facilities Analytics Dashboard
   Staff Analytics Dashboard
   Treatment Analytics Dashboard

# Module 3 

 Bed utilization
 Staff utilization
 Facility capacity
 Department resource utilization
 Resource efficiency
 Resource bottlenecks
 Utilization trends

---

# Conclusion

Module 1 established the cleaned and structured healthcare data foundation for the project.

Module 2 expanded the project into operational intelligence by analyzing patient flow, treatment demand, department workload, department performance, treatment completion, operational bottlenecks, and operational risks.

The final Power BI implementation contains six interactive dashboard pages:

1. Executive Dashboard
2. Patient Analytics
3. Admissions Analytics
4. Facilities Analytics
5. Staff Analytics
6. Treatment Analytics

Together, these dashboards provide a comprehensive view of hospital operations and help management understand patient activity, admission patterns, facility capacity, workforce utilization, treatment demand, and operational performance.

## Next Steps

The next module will focus on extending the project based on the requirements of the next milestone, using the existing healthcare data, analysis, and Power BI dashboard as the foundation.

# How to Run the Project

## Install Dependencies

```bash
pip install pandas numpy matplotlib plotly dash folium geopandas
pip install pandas numpy matplotlib seaborn plotly dash folium geopandas jupyter notebook openpyxl missingno

```

## Execute Scripts

```bash
python src/generate_data.py
python src/data_cleaning.py

```

---

# Current Status

| Module                                                   | Status      |
| -------------------------------------------------------- | ----------- |
| Module 1 – Data Integration & Operational Analytics      | ✅ Completed  |
| Module 2 – Patient Flow Intelligence                     | ✅ Completed  |
| Module 3 – Resource Utilization Intelligence             | ✅ Completed  |
| Module 4 – Geographic Intelligence & Executive Dashboard | Not working  |

---

