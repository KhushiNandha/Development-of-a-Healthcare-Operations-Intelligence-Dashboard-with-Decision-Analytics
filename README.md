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
│       ├── integrated_healthcare_data.csv
│       ├── operational_kpis.csv
│       ├── department_workload.csv
│       ├── treatment_demand.csv
│       ├── monthly_admissions.csv
│       ├── monthly_discharges.csv
│       ├── monthly_treatments.csv
│       └── department_monthly_workload.csv
│
├── notebooks/
│   └── eda_analysis.ipynb       | ✅ Completed |
│
├── src/
│   ├── generate_data.py        | ✅ Completed |
│   ├── data_cleaning.py        | ✅ Completed |
│   ├── data_integration.py
│   ├── kpi_calculation.py
│   ├── trend_analysis.py
│   ├── operational_insights.py
│   └── module1_validation.py
│
├── README.md           | ✅ Updated Till Now |
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
Data Integration    | 🔄 Planning  |
        │
        ▼
KPI Calculation     | 🔄 Planning  |
        │
        ▼
Trend Analysis      | 🔄 Planning  |
        │
        ▼
Operational Insights | 🔄 Planning  |
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

The notebook contains all data exploration steps, visualizations, observations, and conclusions generated during Module 1.

---------

# Operational KPIs
| 🔄 Planning  |
---

# Trend Analysis
| 🔄 Planning  |

---

# Operational Insights  
| 🔄 Planning  |
---

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
| Module 1 – Data Integration & Operational Analytics      | 🔄 Planning  |
| Module 2 – Patient Flow Intelligence                     | Not Working  |
| Module 3 – Resource Utilization Intelligence             | Not Working  |
| Module 4 – Geographic Intelligence & Executive Dashboard | Not working  |

---

