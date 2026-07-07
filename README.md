# Uber_Analytics

# 🚖 Uber Analytics Dashboard | Power BI

An interactive Power BI dashboard that transforms raw Uber ride-booking data into actionable business insights — covering booking performance, revenue, operational efficiency, and customer experience.


## 🎯 Overview

This project simulates a real-world business analytics scenario for a ride-hailing platform (Uber). The goal was to design and build an interactive, stakeholder-ready Power BI dashboard that converts raw ride-booking data into meaningful insights — enabling faster, data-driven decisions around bookings, revenue, operations, and customer satisfaction.

The dashboard is built end-to-end: from raw data ingestion and cleaning (Power Query) to KPI design and DAX calculations, culminating in a polished, interactive report.

---

## 🎯 Business Objective

Ride-hailing platforms generate massive volumes of transactional data every day. Without a structured reporting layer, it's difficult for stakeholders to answer basic but critical questions:

- How many bookings are completed vs. lost, and why?
- Which vehicle types and locations generate the most revenue?
- How is performance trending month-over-month and quarter-over-quarter?
- How satisfied are riders and drivers?

**Objective:** Build a single source of truth — an interactive dashboard — that answers these questions at a glance and supports monitoring, trend identification, and decision-making across the business.

---

## 📂 Dataset

| Attribute | Details |
|---|---|
| **Domain** | Ride-hailing / Mobility |
| **Granularity** | Individual booking/trip level |
| **Key Fields** | Booking ID, Date/Time, Customer ID, Vehicle Type, Pickup Location, Drop Location, Booking Status, Distance, Fare/Revenue, Rider Rating, Driver Rating |
| **Format** | CSV / Excel (raw), transformed via Power Query |

> ⚠️ *Note: Add details here about whether this is a public/sample dataset (e.g., Kaggle "Uber Ride Analytics" dataset) or synthetically generated data, along with a link/source citation and file size/row count.*

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| **Power BI** | Dashboard design, visualization, interactivity |
| **Power Query (M)** | Data extraction, cleaning, and transformation |
| **DAX** | Custom measures, calculated columns, KPIs |
| **Excel** | Initial data exploration and validation |

---

## 📊 Dashboard Highlights

### ✅ Executive KPI Overview
A snapshot view of overall business health:
- Completed Bookings
- Lost / Cancelled Bookings
- Total Revenue
- Total Distance Travelled
- Average Trip Distance

### ✅ Time-Based Analysis
Trend tracking to monitor growth and seasonality:
- Monthly Booking Trends
- Monthly Revenue Trends
- Quarterly Performance Comparison

### ✅ Operational Insights
Deeper visibility into how the business operates:
- Revenue by Vehicle Type
- Top Pickup & Drop Locations
- Vehicle-wise Performance Comparison

### ✅ Customer Experience
Service quality tracking:
- Average Rider Rating
- Average Driver Rating

### ✅ Interactive Features
Self-service exploration for end users:
- Vehicle Type Filter
- City / Drop Location Filter
- Customer ID Filter (slicer/search)

---

## 📈 Key KPIs & Metrics

| KPI | Description |
|---|---|
| **Total Bookings** | Total number of rides booked in the selected period |
| **Completed Bookings** | Rides successfully completed |
| **Lost/Cancelled Bookings** | Rides cancelled by customer, driver, or not completed |
| **Total Revenue** | Sum of fares collected across completed rides |
| **Total Distance Travelled** | Aggregate distance covered across all trips |
| **Average Trip Distance** | Mean distance per trip |
| **Average Rider Rating** | Mean rating given by riders |
| **Average Driver Rating** | Mean rating given to drivers |
| **Booking Success Rate** | Completed Bookings ÷ Total Bookings |

---

## 🧹 Data Cleaning & Transformation

Using **Power Query**, the following steps were performed before modeling:

1. Removed duplicate and null records
2. Standardized date/time formats for time-intelligence calculations
3. Corrected data types (numeric fields, categorical fields)
4. Created calculated columns (e.g., Month, Quarter, Year) for time-based analysis
5. Categorized booking statuses (Completed / Cancelled / Lost) into a consistent taxonomy
6. Handled outliers in fare and distance fields

> 💡 *Add specific transformation steps you performed here, e.g., "Removed 1,200 duplicate rows," "Handled 3% missing values in Driver Rating by exclusion," etc. — recruiters love specifics.*

---
---
## 🧮 DAX Measures

Example measures used to power the KPIs (replace with your actual formulas):
## Measure :
## 1. Avg_Distance:
Avg_Distance = AVERAGE(Uber[Ride Distance])

## 2. Booking_count:
Booking_Count = DISTINCTCOUNT(Uber[Booking ID])

## 3. Booking_Value:
Booking_value = SUM(Uber[Booking Value])

## 4. Booking_Remove_Status_Filter:
Bookings_Remove_Status_Filter = CALCULATE([Booking_Count],ALL(Uber[Booking Status]))

## 5. Booking_completed:
Completed_Bookings = CALCULATE([Booking_Count],Uber[Booking Status]="Completed")

## 6. Lost_Booking:
Lost_Bookings = CALCULATE([Booking_Count],Uber[Booking Status]<>"Completed")

## 7. Total_Distance:
Total_Distance = SUM(Uber[Ride Distance])

---

## 🖼️ Dashboard Preview


<img width="1370" height="773" alt="image" src="https://github.com/user-attachments/assets/1654e963-6b9e-47b1-86d0-b36bf553efc6" />
<img width="1373" height="782" alt="image" src="https://github.com/user-attachments/assets/2c1f5d00-1033-4ad5-a6c2-b3782ea434e1" />
<img width="1374" height="773" alt="image" src="https://github.com/user-attachments/assets/4c5efc3e-8e8d-489a-8885-4b642a558102" />
<img width="1373" height="779" alt="image" src="https://github.com/user-attachments/assets/1d1e6e51-7d80-47af-b270-76853f094016" />
<img width="1375" height="776" alt="image" src="https://github.com/user-attachments/assets/ec6324d7-3c88-4970-9ab5-a08c9fe256da" />
<img width="1371" height="770" alt="image" src="https://github.com/user-attachments/assets/a9cfc107-2d1a-4948-9c91-a56f3c120242" />
<img width="1371" height="779" alt="image" src="https://github.com/user-attachments/assets/d70c6a33-9b6f-4d62-85e3-4c6c1d1b0d77" />
<img width="1375" height="777" alt="image" src="https://github.com/user-attachments/assets/958fb169-5b9a-438e-9be9-5a721864f583" />


📹 **Video Walkthrough:** *Add a link to your recording (YouTube/LinkedIn/Loom) here.*

---

## 🔍 Insights & Findings

> Replace these with your actual data-driven findings — this section is what makes a README stand out.

- Example: *"XX% of bookings were completed, while lost bookings were primarily driven by [reason], concentrated in [location/vehicle type]."*
- Example: *"Revenue peaked in [month/quarter], driven by higher demand for [vehicle type]."*
- Example: *"[Location] consistently ranks as the top pickup point, suggesting potential for driver allocation optimization."*
- Example: *"Average driver ratings remained stable at X.X, while rider ratings showed a slight decline in [period], warranting further investigation."*

---


---

## 📁 Project Structure

```
uber-analytics-dashboard/
│
├── data/
│   └── uber_bookings_raw.csv        # Raw dataset (or link/source if not included)
│
├── dashboard/
│   └── Uber_Analytics_Dashboard.pbix # Power BI dashboard file
│
├── images/
│   └── screenshots/                  # Dashboard screenshots for README
│
├── docs/
│   └── data_dictionary.md            # Field definitions and descriptions
│
└── README.md
```

---

## 🧠 Skills Applied

- Data Cleaning & Transformation
- Business Requirement Analysis
- KPI Design
- Data Visualization
- Dashboard Design Principles
- Interactive Reporting
- Business Storytelling with Data

---

## 📚 What I Learned

This project strengthened my understanding of both **data analytics** and **business analysis** by helping me:

- Convert business requirements into analytical dashboards
- Design meaningful KPIs for business stakeholders
- Identify booking and revenue trends
- Analyze operational performance across vehicle categories
- Build interactive dashboards for better decision-making
- Present complex data in a simple, actionable format

---

## 🚀 Future Improvements

- [ ] Integrate SQL as the backend data source instead of static files
- [ ] Add predictive analytics (e.g., demand forecasting) using Python
- [ ] Build a real-time/near-real-time data refresh pipeline
- [ ] Add driver-side operational metrics (idle time, utilization rate)
- [ ] Deploy dashboard to Power BI Service with row-level security

---

## 🤝 Connect With Me

I'm continuously improving my skills in **SQL, Python, Power BI, and Business Analytics** through real-world projects like this one. Feedback and suggestions are always welcome!

- 💼 LinkedIn: 
- 📧 Email: prasennimje100@gmail.com


---

⭐ **If you found this project useful or interesting, consider giving it a star!**

#PowerBI #DataAnalytics #BusinessAnalytics #DataAnalyst #BusinessAnalyst #Dashboard #DataVisualization #DAX #PowerQuery #Analytics #SQL #Python #PortfolioProject
