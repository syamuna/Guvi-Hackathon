# 🏥 Hospital Operations & Analytics Dashboard (Power BI)

## 📌 Overview
This project is an end-to-end **Hospital Operations Analytics Dashboard** developed using **Power BI** for a mid-sized, multi-specialty hospital network in India.

The dashboard enables hospital leadership, operations teams, and administrators to **monitor performance, optimize capacity, control costs, and improve patient outcomes** using intuitive and non-technical visual analytics.

The solution is designed to support both:
- **Short-term operational decisions** (staffing, bed availability, peak hours)
- **Long-term planning** (capacity, cost efficiency, quality improvement)

---

## 🛠️ Technology Stack
- **BI Tool:** Power BI Desktop
- **Data Source:** CSV files (synthetic hospital data)
- **Database (conceptual):** PostgreSQL / MySQL
- **Deployment:** On-premise / internal private infrastructure
- **Export Formats:** CSV, Excel, PDF

> ❗ No third-party healthcare APIs or EMR integrations were used.

---

## 📊 Dashboard Pages & Key Features

### 1️⃣ Executive Overview
Provides high-level KPIs for leadership.

**KPIs**
- Average Length of Stay (ALOS)
- Bed Occupancy %
- Cost per Discharge

**Visuals**
- Admissions by Branch (Bar Chart)

**Global Slicers**
- Date
- Branch
- Department

---

### 2️⃣ Operations & Capacity
Focuses on patient flow and operational bottlenecks.

**Visuals**
- Admissions vs Discharges Trend (Line Chart)
- Hour vs Department Heatmap  
  *(Matrix with conditional formatting)*
- Emergency vs Scheduled Admissions (Stacked Bar Chart)

**Insights**
- Peak admission hours
- Discharge delays
- Emergency load distribution

---

### 3️⃣ Clinical Utilization
Analyzes doctor workload and clinical demand.

**Visuals**
- Doctor Utilization by Department  
  *(Drill-down: Department → Doctor)*
- Admissions by Department (Procedure Proxy)

**KPIs**
- Doctor Utilization %

---

### 4️⃣ Financial Performance
Tracks cost drivers and financial efficiency.

**Visuals**
- Billing Breakdown (Room, Pharmacy, Procedure)
- Cost per Patient Trend (Line Chart)

**Slicer**
- Insurance Type

---

### 5️⃣ Outcomes & Quality
Monitors quality of care and patient outcomes.

**Visuals**
- Outcome Distribution (Donut Chart)
- Readmission Trend (30-day logic)
- ALOS vs Outcome (Table)

**Metrics**
- Readmission Rate
- Outcome-based LOS comparison

---

## 📁 Dataset Description

| File Name | Description |
|----------|-------------|
| `patients.csv` | Patient demographics & insurance |
| `admissions.csv` | Admission & discharge records |
| `billing.csv` | Cost & billing details |
| `doctor_utilization.csv` | Doctor schedules & workload |
| `outcomes.csv` | Patient outcome classification |
| `date_dim.csv` | Date dimension for time analysis |

**Data Granularity:**  
- Daily (admissions, discharges, costs)  
- Hourly (admission time analysis)

## 🧠 Key Metrics & Logic

- **ALOS:**  
  Average of (Discharge Date − Admission Date)

- **Bed Occupancy %:**  
  Occupied Beds / Total Beds

- **Doctor Utilization %:**  
  Booked Hours / Available Hours

- **Cost per Patient:**  
  Total Cost / Distinct Patients

- **Readmission Flag:**  
  Patient re-admitted within **30 days** of previous admission

---

## 📈 Business Value
- Identifies operational bottlenecks
- Improves staffing & capacity planning
- Enhances financial transparency
- Supports quality-of-care monitoring
- Enables branch and department comparison

---

## ▶️ How to Use
1. Download the `.pbix` file
2. Open using **Power BI Desktop**
3. Place all CSV files in the same folder
4. Refresh data
5. Use slicers to explore insights

---

## 📌 Assumptions
- Total bed capacity is fixed (configurable)
- Admissions act as a proxy for procedure volume
- Readmission window is set to 30 days
- Dashboard is designed for **non-technical users**

---

## 📜 Disclaimer
This dashboard uses **synthetic hospital data** for educational and demonstration purposes only.  
No real patient, clinical, or hospital data is included.

---

## 👤 Author
Created by: YAMUNA S  
