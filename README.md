# TransitGuard

**Real-time safety intelligence for Chicago public transit.**

TransitGuard is an AI-powered platform that predicts safety incidents across the Chicago Transit Authority (CTA) system. Built as a capstone project for Northwestern University's MS in Data Science program.

![TransitGuard Dashboard](assets/transitguard-dashboard.png)

## The Problem

The CTA serves 950,000+ daily riders across 128 bus routes and 8 rail lines. Crime on the system increased post-pandemic, but incident reporting remains reactive — passengers and transit authorities only know about problems after they happen.

## The Solution

TransitGuard shifts from reactive to predictive. We analyzed 50,000+ CTA-related crime incidents (2014-2024) alongside ridership patterns, streetlight outages, and environmental factors to build models that identify high-risk stations, routes, and time windows *before* incidents occur.

### Components

| Component | Description | Repo |
|-----------|-------------|------|
| **Dashboard** | Real-time safety metrics and hotspot visualization | [transitguard-dashboard](https://github.com/foxintheloop/transitguard-dashboard) |
| **Mobile App** | SMS/push alerts for riders and dispatchers | [transitguard-app](https://github.com/foxintheloop/transitguard-app) |
| **GenAI Chatbot** | Natural language safety queries by location/time | Integrated |
| **Predictive Models** | XGBoost, Logistic Regression, time series forecasting | Integrated |

## Key Findings

- **CTA trains have 3x more incidents than buses** despite lower ridership — environment matters more than volume
- **Theft and battery account for 52%** of all CTA-related crimes
- **Weekday peaks (Tue-Thu) and summer months** show highest incident rates
- **Spatial clustering (DBSCAN)** identified persistent hotspots across the rail network

## Technical Approach

| Goal | Method |
|------|--------|
| Identify hotspots | DBSCAN spatial clustering, KDE |
| Predict incidents | XGBoost, Logistic Regression, time series forecasting |
| Segment risk zones | ZIP code and community area aggregation |
| Surface insights | Real-time dashboard, GenAI chatbot, mobile alerts |

## Data Sources

All data from the [City of Chicago Data Portal](https://data.cityofchicago.org/):

- Crime data (8.29M records, 2001-present)
- CTA ridership (daily boarding totals, L station entries, bus routes)
- 311 reports (streetlight outages, graffiti removal)
- Traffic crashes and fatalities
- Geographic boundaries (community areas, wards, ZIP codes)

## Team

Built by a 5-person team at Northwestern University (MSDS 498 Capstone, 2025):

- Kevin Ou — Dashboards, GenAI
- **Derek Plemons** — GenAI Development, Modeling
- Sergio Valentini — App Development, Modeling
- Summer Xia — Data Cleaning, Visualization, Modeling
- Sophie Xiao — Data Cleaning, Visualization

## Stack

`Python` `XGBoost` `scikit-learn` `Pandas` `Folium` `Streamlit` `React Native`

## License

MIT

---

*Northwestern University — MS in Data Science Capstone Project — April 2025*
