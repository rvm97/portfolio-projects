# Hotel Data Analytics Project

This repository contains the complete Power BI analytics solution for hotel performance monitoring, forecasting, and guest behavior analysis. It integrates simulated booking data with real-time KPIs and provides a modular, scalable dashboard experience.

---

## 📁 Contents

- `PowerBI/` — Power BI Desktop (.pbix) dashboard file
- `BigQuery/` — SQL scripts and views used in the data warehouse
- `Simulations/` — Python scripts to generate synthetic booking/guest data
- `Documentation/` — Project Summary, Data Dictionary, and KPI Definitions

---

## 🧩 Project Overview

The goal of this project is to deliver a unified dashboard that tracks hotel KPIs such as revenue, occupancy, ADR, and RevPAR, while supporting segmentation by guest type, booking channel, room type, and time periods (LN, MTD, YTD, etc.).

---

## 🧠 Key Modules

### 1. **Daily Performance Summary**
- Net Room Revenue, Occupancy %, ADR, RevPAR
- Dynamic panels for Last Night, MTD, YTD
- Built-in vs Target and vs Last Year comparisons

### 2. **Today's Guest Movements**
- Expected Arrivals, Departures, and Stayovers
- Drill-down by room type and guest profile

### 3. **7-Day Forecast**
- Forecasted Occupancy by room type
- ADR, Booking Count, and Room Availability
- Pickup trends with visual alerts

### 4. **Historical & Market Analysis**
- Year-over-year performance trends
- Segmentation by source, guest culture, nationality
- Repeat guest analysis and visit tracking

### 5. **Booking & Channel Insights**
- Booking patterns by lead time, LoS, weekend stays
- Channel mix (Direct vs OTA) with cancellation analysis

---

## 🔍 Dataset Overview

### BookingDetails Table (Fact)
- `booking_id`, `check_in_date`, `check_out_date`, `guest_count`
- `room_type`, `gross_final_rate`, `vat_amount`, `net_final_rate`
- `cancellation_flag`, `no_show_flag`, `visit_number`, `guest_id`

### Lookup Tables
- `HotelCalendar`: Dates, flags for MTD, YTD, etc.
- `AvailableRooms`: Daily room capacity per type
- `BookingSource`: Source categorization and contract rates
- `VAT`: Country-specific VAT rate
- `Targets`: KPI targets by date

---

## ⚙️ BigQuery Views

Main view: `vw_kpi_summary_by_date`  
- Includes flags: `isLastNight`, `isMTD`, `isYTD`, etc.  
- Used for all dashboard filters and aggregation logic

Other views:
- `vw_forecast_by_date`
- `vw_occupancy_by_room_type`
- `vw_booking_channel_summary`
- `vw_guest_repeat_behavior`

---

## 📌 Setup Instructions

1. Clone this repository and open the Power BI .pbix file.
2. Update your BigQuery data source credentials in Power BI.
3. Refresh visuals (queries are optimized via views).
4. Optional: Regenerate simulation data with the provided Python scripts.

---

## 🧠 AI Commentary Logic

Each KPI includes AI-generated commentary based on:
- ADR vs Target ADR
- RevPAR vs ADR (yield vs occupancy)
- ADR vs Base Rate (discounting evaluation)

---

## 🔒 Data Privacy & Ethics

All data is fully synthetic. Guest names, nationalities, booking patterns, and room behavior are simulated using randomized but realistic distributions.

---

## 🛠️ Future Enhancements

- Event-Based Pricing Adjustments
- Competitor Rate Benchmarking
- Automated daily export to email/PDF/Teams
- Voice-enabled insights via Power BI + Azure

---

## 📬 Contact

Created by Robert [Your Last Name]  
Business Intelligence & Hotel Analytics Professional  
Connect via LinkedIn | GitHub | Email

---

