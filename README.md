
###  Development of a Healthcare Operations Intelligence Dashboard with Decision Analytics Group 2

**Batch 2 / Team A**

---

## 📌 Project Overview

The **Medical Operations Intelligence Dashboard** is a Power BI-based healthcare analytics project designed to provide an integrated view of hospital operations.

The final Power BI model shown in the project uses the following tables:

- `Dim_Department`
- `Dim_Patient`
- `Dim_Facility`
- `Dim_Date`
- `Fact_Admissions`
- `Fact_Treatments`
- `Fact_Beds`
- `Fact_Staff`
- `_Measures`

The dashboard brings patient, admission, treatment, staff, bed, facility, department, date and geographic information together for interactive analysis.

> **Data authenticity note:** This README documents the final Power BI model and dashboard. No new records are added here, and the original source dataset is not modified.

---

# 🎯 Project Objectives

- Analyze hospital admissions and patient activity.
- Monitor treatment demand and treatment status.
- Analyze department-level operational workload.
- Understand bed status and hospital capacity.
- Analyze staff shifts and staff efficiency.
- Compare facilities and cities.
- Track clinical and operational KPIs.
- Provide management-oriented insights through Power BI.

---

# 🏗️ Final Power BI Data Model

The final model is organized around dimension tables and fact tables.

```text
                    Dim_Department
                          │
                          │
        ┌─────────────────┼─────────────────┐
        │                 │                 │
        ▼                 ▼                 ▼
 Fact_Treatments    Fact_Admissions     Fact_Beds
        │                 │                 │
        │                 │                 ▼
        │                 │           Dim_Facility
        │                 │
        │                 ▼
        │              Dim_Date
        │
        ▼
   Dim_Patient

        │
        ▼
   Fact_Staff

              ┌───────────────┐
              │   _Measures   │
              │ DAX Measures  │
              └───────────────┘
```

The exact relationships and fields used in the final model are documented below according to the Power BI model.

---

# 🗃️ Tables in the Final Power BI Model

## 1. `Dim_Department`

The department dimension contains the department-level reference used across the operational fact tables.

### Field

| Field |
|---|
| `department` |

---

## 2. `Dim_Patient`

The patient dimension contains patient-level demographic and registration information.

### Fields

| Field |
|---|
| `age` |
| `city` |
| `gender` |
| `patient_id` |
| `registration date` |

---

## 3. `Fact_Treatments`

This fact table contains treatment/service activity.

### Fields

| Field |
|---|
| `department` |
| `patient id` |
| `treatment date` |
| `treatment id` |
| `treatment status` |
| `treatment type` |

---

## 4. `Fact_Admissions`

This fact table contains hospital admission activity and length-of-stay information.

### Fields

| Field |
|---|
| `admission date` |
| `admission id` |
| `admission type` |
| `department` |
| `discharge date` |
| `length of stay` |
| `patient id` |

---

## 5. `Fact_Beds`

This fact table contains bed-level operational information.

### Fields

| Field |
|---|
| `bed id` |
| `bed type` |
| `department` |
| `facility id` |
| `status` |

---

## 6. `Fact_Staff`

This fact table contains workforce and shift information.

### Fields

| Field |
|---|
| `department` |
| `role` |
| `shifts assigned` |
| `shifts worked` |
| `staff efficiency` |
| `staff id` |

---

## 7. `Dim_Facility`

The facility dimension contains facility and city-level capacity information.

### Fields

| Field |
|---|
| `city` |
| `facility id` |
| `facility name` |
| `facility type` |
| `total beds` |

---

## 8. `Dim_Date`

The date dimension provides the time attributes used for time-based analysis.

### Fields

| Field |
|---|
| `date` |
| `month` |
| `month number` |
| `quarter` |
| `year` |
| `year month` |

---

# 📐 Measures

The final Power BI model contains a dedicated `_Measures` table for analytical calculations.

The measures visible in the final model include:

- Admission Growth %
- Admissions
- Assigned Shifts
- Available Beds
- Avg LOS
- Avg Pressure
- Cancellation Rate
- Capacity Reconciliation Gap
- Completed Treatments
- Completion Benchmark
- Completion Rate
- Demand Concentration %
- Department Demand
- Discharge Growth %
- Discharges
- Facilities
- Fulfillment Rate
- LOS Benchmark
- Maintenance Beds
- Net Flow

These measures are used by the Power BI visuals and KPI calculations.

---

# 📊 Final Dashboard

The final Power BI report contains the following analytical pages:

1. **Executive Dashboard**
2. **Patient Analytics**
3. **Admissions Analytics**
4. **Facilities Analytics**
5. **Staff Analytics**
6. **Treatment Analytics**
7. **Geographic Performance**
8. **Insights & Recommendations**

---

# 1. 🏥 Executive Dashboard

The Executive Dashboard provides a high-level view of hospital operations.

### Main areas

- Patient activity
- Admissions
- Treatments
- Facilities
- Beds
- Department performance
- Monthly admission activity
- Patient distribution
- Gender distribution

The page acts as the starting point for management-level exploration.

---

# 2. 👤 Patient Analytics

The Patient Analytics page focuses on patient-level demographic and registration information.

### Analysis

- Patient count
- Age
- Gender
- City
- Registration activity
- Patient distribution

### Main filters

- Gender
- City
- Date

---

# 3. 🏥 Admissions Analytics

The Admissions Analytics page focuses on hospital admission and discharge activity.

### Analysis

- Admissions
- Admission type
- Department
- Admission date
- Discharge date
- Length of stay
- Monthly admission activity
- Patient movement

### Main filters

- Admission type
- Department
- Admission date
- Discharge date

---

# 4. 🏢 Facilities Analytics

The Facilities Analytics page focuses on hospital facilities and bed capacity.

### Analysis

- Total facilities
- Total beds
- Facility type
- Facility name
- City
- Bed capacity
- Facility comparisons

### Main filters

- Facility type
- City
- Facility

---

# 5. 👨‍⚕️ Staff Analytics

The Staff Analytics page focuses on workforce utilization.

### Analysis

- Staff distribution
- Staff by department
- Staff by role
- Assigned shifts
- Worked shifts
- Staff efficiency
- Department workforce comparison

### Main filters

- Department
- Role

---

# 6. 💊 Treatment Analytics

The Treatment Analytics page focuses on healthcare service demand and treatment completion.

### Analysis

- Total treatments
- Treatment type
- Treatment status
- Completed treatments
- Pending treatments
- Cancelled treatments
- Monthly treatment activity
- Department-level treatment demand

### Main filters

- Treatment status
- Treatment type
- Department
- Date

---

# 7. 🌍 Geographic Performance

The Geographic Performance page uses the city information available in the final Power BI model.

### Analysis

- Patients by city
- Facilities by city
- Facility bed capacity by city
- Admissions by city
- Geographic comparisons

### Filters

- City
- Department
- Date

This page helps compare patient activity and healthcare capacity across locations represented in the dashboard.

---

# 8. 💡 Insights & Recommendations

The final page converts the dashboard analysis into management-oriented observations and recommendations.

## Bed Utilization

The dashboard reports **63.9% bed occupancy**, indicating that hospital bed capacity is being utilized while some capacity remains available.

## Patient Stay

The operational analysis reports an **average length of stay of 7.58 days**.

## Workforce Performance

The dashboard reports **84.34% staff efficiency**, providing a view of workforce utilization.

## Treatment Completion

The dashboard reports approximately **75.1% treatment completion**.

---

# 📌 Operational Findings

The Power BI analysis identifies the following department-level observations:

- **Neurology** recorded the highest overall workload in the operational analysis.
- **Orthopedics** recorded the lowest overall workload.
- Neurology's workload signal was **540**.
- **Consultation** was the highest-volume treatment type.
- Neurology recorded a treatment completion rate of **78.35%**.
- Dermatology recorded a treatment completion rate of **68.85%**.
- Dermatology recorded the highest pending treatment rate at **24.59%**.

These findings are based on the analytical values represented in the project dashboard.

---

# ⚠️ Operational Areas Requiring Attention

The dashboard analysis highlights areas that can be monitored by hospital management:

### Capacity

Monitor bed utilization and available capacity against admission demand.

### Patient Flow

Monitor length of stay, admissions and discharge activity to identify possible delays.

### Workforce

Review assigned versus worked shifts and department-level staff efficiency.

### Treatment

Monitor pending and cancelled treatments, particularly in departments with lower completion.

### Geographic Performance

Compare patient activity and facility capacity across cities.

---

# 🎯 Management Recommendations

## 1. Optimize Bed Allocation

Use bed status, department, facility and city information to monitor capacity and support better allocation.

## 2. Improve Patient Flow

Monitor admission activity, discharge activity and length of stay to identify areas where patient flow may require attention.

## 3. Balance Workforce

Use assigned shifts, worked shifts and staff efficiency to support workforce and shift planning.

## 4. Improve Treatment Completion

Monitor treatment status by department and treatment type to identify areas with higher pending or cancelled activity.

## 5. Monitor Geographic Demand

Use city-level patient, admission and facility information to compare demand and capacity across locations.

---

# 🔄 Project Workflow

```text
Healthcare Data
      ↓
Data Preparation
      ↓
Data Integration
      ↓
Power BI Data Model
      ↓
DAX Measures
      ↓
Interactive Visualizations
      ↓
Operational Analysis
      ↓
Insights
      ↓
Recommendations
      ↓
Management Decision Support
```

---

# 🛠️ Tools & Technologies

### Data & Analysis

- Python
- Pandas
- NumPy
- Jupyter Notebook

### Business Intelligence

- Microsoft Power BI

### Version Control

- Git
- GitHub

---

# 📁 Final Project Structure

A recommended repository structure is:

```text
Medical-Operations-Intelligence-Dashboard/
│
├── README.md
│
├── data/
│   └── original / processed project datasets
│
├── notebooks/
│   └── EDA and analysis notebooks
│
├── dashboard/
│   └── Hospital_Management_Dashboard by harshada-2.pbix
│
├── presentation/
│   └── project presentations
│
└── screenshots/
    └── Power BI dashboard screenshots
```

> Keep the original dataset unchanged. If a processed dataset is required for the project workflow, keep it as a separate file rather than overwriting the original source.

---

# 🤝 Team Collaboration

The project was developed collaboratively using Git/GitHub.

Typical workflow:

```text
Create / Update Work
        ↓
Git Branch
        ↓
Development
        ↓
Commit
        ↓
Push
        ↓
Pull Request
        ↓
Review
        ↓
Merge
```

Team activities may include:

- Data preparation
- Data analysis
- Power BI development
- Dashboard visualization
- DAX measures
- Resource analysis
- Geographic analysis
- Documentation
- Presentation

---

# 👥 Member-Wise Contribution

Replace the placeholders below with the **actual names and actual responsibilities of your team members**.

| Team Member | Actual Contribution |
|---|---|
| **Member 1 – [Shambhavi]** | Data collection, preprocessing and data cleaning |
| **Member 2 – [Harshada]** | Power BI dashboard development and visualizations |
| **Member 3 – [Khushi]** | Resource utilization, capacity and workforce analysis |

---

# 📋 Project Completion

| Component | Status |
|---|---|
| Data Preparation | ✅ Completed |
| Data Integration | ✅ Completed |
| Power BI Data Model | ✅ Completed |
| DAX Measures | ✅ Completed |
| Patient Analytics | ✅ Completed |
| Admissions Analytics | ✅ Completed |
| Facilities Analytics | ✅ Completed |
| Staff Analytics | ✅ Completed |
| Treatment Analytics | ✅ Completed |
| Geographic Performance | ✅ Completed |
| Insights & Recommendations | ✅ Completed |
| Final Power BI Dashboard | ✅ Completed |

---

# 🔐 Data Authenticity & Integrity

This documentation is intended to represent the *###  Development of a Healthcare Operations Intelligence Dashboard with Decision Analytics Group 2 *final project as implemented**.

### Data handling principles

- The original dataset should remain unchanged.
- No artificial records are added to the source data.
- No dashboard values are manually fabricated for documentation.
- Dashboard metrics should be taken from the Power BI model/visuals.
- Table names and fields in this README correspond to the final Power BI model shown in the project.
- Any future transformation should be stored separately from the original source.

---

# 🏁 Final Outcome

The **** provides an integrated Power BI environment for analyzing:

- Patients
- Admissions
- Treatments
- Staff
- Beds
- Facilities
- Departments
- Dates
- Cities
- Operational KPIs

The final model combines fact tables, dimension tables and a dedicated measures table to support interactive healthcare operations analysis.

The solution helps users move from raw operational information to:

```text
Data
 ↓
Data Model
 ↓
Measures
 ↓
Dashboard
 ↓
Analysis
 ↓
Insights
 ↓
Recommendations
```

---

## 📌 Final Project Statement

**Medical Operations Intelligence Dashboard** is a Power BI-based healthcare analytics solution that integrates patient, admission, treatment, staff, bed and facility information into an interactive decision-support dashboard.

The project focuses on understanding hospital operations through actual dashboard data while maintaining the integrity of the original dataset.

---

**Project:** ###  Development of a Healthcare Operations Intelligence Dashboard with Decision Analytics Group 2
**Batch:** 2 / Team A  
**Platform:** Microsoft Power BI  
**Final Report File:** `Hospital_Management_Dashboard by harshada-2.pbix`
