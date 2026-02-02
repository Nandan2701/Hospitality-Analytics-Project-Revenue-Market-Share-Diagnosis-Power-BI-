# 🏨 Hospitality Revenue & Market Share Analysis (Power BI)

## 📌 Project Overview

This project analyzes operational and booking data from a hotel chain that was experiencing a decline in revenue and market share.  
The objective was to understand performance issues using hospitality KPIs and to derive actionable business insights through data analysis and visualization.

The project focuses on:

- Revenue behavior  
- Room utilization  
- Pricing strategy  
- Customer impact on occupancy  

---

## 🎯 Business Objective

To identify:

- Why revenue was not growing despite stable demand  
- Which operational and pricing decisions were limiting performance  
- What data-backed actions could improve revenue and occupancy  

---

## 📊 Key Hospitality Metrics Used

- **Revenue:**  
  Total money earned from room bookings  

- **RevPAR (Revenue per Available Room):**  
  `Revenue ÷ Total available rooms`

- **ADR (Average Daily Rate):**  
  `Revenue ÷ Booked rooms`

- **Occupancy %:**  
  `Utilized rooms ÷ Booked rooms`

- **DSRN (Daily Sellable Room Nights):**  
  Total room capacity per day  

- **DBRN (Daily Booked Room Nights):**  
  Rooms booked per day  

- **DURN (Daily Utilized Room Nights):**  
  Rooms actually used  

- **Realisation %:**  
  `Utilized bookings ÷ Total bookings`

- **Cancellation %:**  
  `Cancelled bookings ÷ Total bookings`

---

## 📅 Business Definitions

- **Weekend:** Friday & Saturday  
- **Weekday:** Sunday to Thursday  

## 📁 Dataset

The dataset follows a star-schema–style structure with dimension and fact tables.  
Only the following tables were present in the raw data:

---

### 📐 Dimension Tables

**dim_date**
- date  
- day_type (weekday / weekend)  
- mmm yy  
- week_no  

**dim_hotels**
- property_id  
- property_name  
- city  
- category  

**dim_room**
- room_id  
- room_class  

---

### 📊 Fact Tables

**fact_aggregated_bookings**
- property_id  
- room_category  
- check_in_date  
- capacity  
- successful_bookings  

**fact_bookings**
- booking_id  
- booking_date  
- check_in_date  
- checkout_date  
- booking_platform  
- booking_status  
- property_id  
- no_guests  
- ratings_given  
- revenue_generated  
- revenue_realized  

---

All business KPIs (ADR, RevPAR, Occupancy %, DSRN, DBRN, DURN, Realisation %, Cancellation %) were not present in the raw data and were computed using DAX measures.

---

## 🧹 Data Preparation

Main steps:

- Built relationships between dimension and fact tables  
- Standardized column naming for analysis  
- Created calculated measures for hospitality KPIs using DAX  
- Validated calculated metrics by cross-checking with raw aggregates  
- Ensured consistency between booking, revenue, and capacity data  

## 📈 Analysis & Insights

### 1. Weekday vs Weekend Pricing

ADR difference between weekdays and weekends was minimal despite higher weekend demand.  
This indicated that weekends were being treated like business days.

**Business implication:**  
Opportunity to increase revenue by applying differential weekend pricing.

---

### 2. Platform-Level Realisation

Realisation percentage was around 70%, indicating high post-booking cancellations.  
Inconsistency in pricing and expectations across platforms likely contributed to this.

**Business implication:**  
Standardize pricing and presentation across platforms to reduce cancellations.

---

### 3. Ratings vs Occupancy

Properties with lower ratings showed lower occupancy.  
Higher-rated properties consistently achieved better room utilization.

**Business implication:**  
Improving service quality and expectation management can directly raise occupancy and revenue.

---

## 📊 Dashboard Features

The Power BI dashboard includes:

- Revenue, RevPAR, ADR, Occupancy KPIs  
- Weekday vs Weekend performance comparison  
- Platform-wise realization analysis  
- Property-level performance table  
- Time-based trends  
- Interactive filters for city, room type, and time period  

---

## 📤 Output

- Power BI interactive dashboard  
- DAX measures for hospitality KPIs  
- Insight-driven business recommendations  

---

## 🎓 Key Learning Outcomes

- Learned hospitality industry KPIs and revenue logic  
- Practiced translating business problems into analytical questions  
- Built end-to-end Power BI solutions with calculated metrics  
- Improved ability to derive operational insights from dashboards  

---

## ⚠️ Limitations

- Analysis is descriptive, not predictive  
- Dataset represents a fixed time period  
- Insights are based only on available operational metrics  
