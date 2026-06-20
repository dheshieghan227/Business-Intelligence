# Weather Impact on US Flight Delays (2016)
## Business Intelligence & Data Analytics Project

This project explores the correlation between weather events and US domestic flight delays/cancellations during the year 2016. By integrating millions of weather event data points with flight records across 267 airports, we uncover patterns in flight disruptions caused by meteorological changes.

---

## 📊 Project Overview
Weather disruptions cost the aviation industry billions of dollars annually and cause massive inconvenience to passengers. This project utilizes a complete Business Intelligence pipeline (ETL + Data Modeling + Visualization) to analyze:
- How different weather types (Rain, Snow, Fog, Storm, etc.) impact flight delays.
- Which airports and geographic areas are most vulnerable to weather-induced delays.
- Monthly and seasonal operational trends.

---

## 🛠️ Tech Stack & Workflow
The analysis is structured around two main stages:

### 1. Data Prep & ETL (Alteryx)
- **Workflow file**: Located in `/workflows/Weather_Flight_Delay_BI_Workflow.yxmd`
- **Processes**:
  - Ingests raw flight logs (`2016.csv`), weather event logs (`WeatherEvents.csv`), and airport geographical metadata (`airports.csv`).
  - Cleans and formats date/time records.
  - Normalizes and joins datasets based on airport codes and timestamps.
  - Outputs an optimized dataset (`Final_Weather_Flight_All_Enhanced.yxdb`) for reporting.

### 2. Visualization & Dashboarding (Power BI)
- **Report file**: Located in `/dashboards/Weather_Impact_on_US_Flight_Delays_2016.pbix.zip`
- **Dashboards**:
  - **Geographic & KPI Overview**: High-level KPIs showing 267 US airports, 20M weather events, 6M weather delay minutes, and 115K cancellations.
  - **Weather vs. Flight Delays Storyboard**: Explores the frequency of weather events (Rain represents 74.15%, Fog 11.76%, Snow 11.59%) and parses the correlation between rainfall precipitation levels and average departure delay times.
  - **Operational Trends & Risk Analysis**: Highlights seasonal trends (monthly weather delays vs. weather event counts) and profiles the top 15 busiest airports by weather activity.

---

## 📂 Repository Structure
The project files are organized as follows:
```text
├───dashboards
│       Weather_Impact_on_US_Flight_Delays_2016.pbix.zip   # Power BI Dashboard Storyboards
│
├───reports
│       BI_Talk_Document.pdf                              # Presentation slides & talk outline
│       Project_BI_Phase_1.pdf                             # Phase 1: Planning and requirement analysis
│       Project_BI_Phase_3.pdf                             # Phase 3: Final reporting and deployment notes
│
└───workflows
        Weather_Flight_Delay_BI_Workflow.yxmd             # Alteryx ETL workflow file
```

---

## 🔍 Key Insights & Findings
- **Dominant Disruptor**: Rainfall is the most frequent weather event (74.15% of all events), but Snow and Fog cause higher average delay durations per occurrence.
- **Top Vulnerable Hubs**: Busiest airports such as Atlanta (ATL), Chicago (ORD), and Dallas-Fort Worth (DFW) register the highest cumulative delay minutes due to their high traffic volumes compounding weather delays.
- **Precipitation Correlation**: Flight delay minutes scale exponentially during heavy rainfall events exceeding critical precipitation thresholds.
