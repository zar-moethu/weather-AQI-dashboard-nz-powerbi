🌧️ Real-Time Weather & Air Quality Power BI Dashboard - Live Weather Monitoring Across New Zealand


📍 Project Overview: The Framework for Insight

This project provides a real-time dashboard that captures both current conditions and 7-day forecast insights for major cities across New Zealand — including Auckland, Wellington, Christchurch, Tauranga, and Dunedin. Powered by live API integration and developed in Power BI, it visualizes key environmental metrics such as:

- Temperature — with dynamic icons that change based on real-time conditions (e.g., fog, rain, cloud)

- Humidity,  Wind Speed, Visibility, Pressure, Feels Like, and UV Index (current)

- Air Quality (current) — CO, NO₂, SO₂, O₃, PM10, and PM2.5 levels with color categories indicating pollutant thresholds

- Sunrise & Sunset Times with a 7-day forecast overlay

- Chance of Rain with daily breakdowns across the week

- 7-Day Temperature Forecast Trend — temperature and condition breakdowns for each day

🧠 **Business Understanding**
Goal: Deliver a user-friendly dashboard showing live and forecasted weather + air quality for key New Zealand cities.

Value: Helps everyday users, commuters and decision-makers access relevant environmental insights in real time.

Core Feature: Real-time API integration and multi-city breakdown.

**🔄 Data Pipeline: Real-Time ETL Process**

🔹 *Extract* -  Pulled live data via API from: https://www.weatherapi.com/
              - API returned data in JSON format

🔹 *Transform* -After importing JSON into Power BI, cleaned and transformed the data by handling:
- Unit conversions (e.g., wind speed, pressure)
- Null/missing values & duplicates
- Date/time formatting
- Engineered new columns and tables:
- Built additional tables for other cities , taking Auckland’s table as a reference data structure, ensuring other cities are also powered by real-time data.

🔹 Load
- Loaded into Power BI

**📊 Data Modeling & Relationships**

- Built relationships by creating one-to-many across tables between cities and location-level data
- Removed messy relationships created by Power BI and replaced them with a clean, simplified model
- Created necessary reference tables and relationships
- Ensured a clean star schema structure to support efficient dashboard filtering and slicing

**🧮 DAX Calculations**
Built DAX measures for custom logic across visuals:
  - Categorizing AQI into color-coded thresholds (Green, Yellow, Orange, Red, Purple) for circular shape
  - Dynamic weather icon logic based on condition codes (e.g., fog, rain, snow) pulled from the API response and mapped to
    custom visuals
  - Chance of Rain probability is shown as a percentage (e.g., 85%) in the 7-day forecast
  - Unit formatting applied to temperature (°C), wind (Kph), pressure (hPa), and AQI values (µg/m³)
  - Enabled slicers across city-level filtering and built DAX logic to dynamically adjust forecast visuals based on selected      day of the week

**🎨  Visualization: Dashboard Overview**
The final result is a single-page interactive dashboard showing:

- KPI cards for current metrics (temperature, humidity, UV index)
- 7-day forecast visualized using line and column charts
- Dynamic weather icons that update with real-time data
- Color-coded AQI section based on thresholds (e.g., Green → Red)
- Sunrise & Sunset shown alongside the 7-day forecast to help users understand the timing of daylight in relation to upcoming
  temperature patterns
- Slicers to toggle between cities and daily/hourly forecasts

<img width="1430" height="829" alt="image" src="https://github.com/user-attachments/assets/e62a8af9-727d-4786-a7fc-7017ac29853d" />


📂 **Project Files**

- *Power BI Dashboard File* (Click on View Raw):  
  [WeatherDashboard.pbix](https://github.com/zar-moethu/weather-AQI-dashboard-nz-powerbi/blob/main/WeatherReport%20(VF).pbix)
- *Dashboard Overview (PDF Preview)*:  
  [Dashboard Overview (PDF)](https://github.com/zar-moethu/weather-AQI-dashboard-nz-powerbi/blob/main/Dashboard%20Overview.pdf)


  **How to use this project:**
-  Refresh the Power BI dashbord file to pull the latest API data. This ensures you're working with real-time information.
-  Data analysis is an ongoing process and continuous improvement and innovation are key to long-term success. I believe
   every  analyst’s journey is strengthened by an open mindset and a willingness to receive feedback. I welcome your
   thoughts,  suggestions and collaboration on this project.
-  Feel free to download, explore, and adapt it to better understand how real-time data can be modeled and visualized in
    Power BI.
  
    ⚠️ Disclaimer: This dashboard is intended for visual learning and demonstration purposes only — not for business or
    operational use. 



