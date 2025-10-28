# 🚴‍♂️ Seoul Smart Mobility  
### Weather Impact and Bike Rental Trend Analysis  

---

## 📘 Project Overview  

This Power BI project focuses on analyzing the Seoul Bike Sharing dataset to identify key patterns, trends, and factors influencing bike rentals.
The dataset contains hourly data of rented bikes, weather conditions, and operational details.
Through data cleaning, transformation, and visualization, this report helps understand how temperature, humidity, rainfall, and time patterns affect user behavior.

The dashboard provides **interactive insights**, **seasonal patterns**, and **data-driven visuals** to support better decision-making for **urban mobility planning**.

---

## 🎯 Objectives  

- Analyze the relationship between bike rentals and weather parameters.  
- Identify **peak rental hours, days, and seasons**.  
- Examine how **temperature, humidity, and rainfall** impact demand.  
- Build an **interactive Power BI dashboard** showcasing KPIs and advanced visuals.  
- Enable insights for **resource optimization** and **smart city decisions**.  

---

## 🧩 Dataset Description  

| Column Name | Description |
|--------------|-------------|
| Date | Date when rentals were recorded |
| Bike_Count | Number of bikes rented during that hour |
| Hour | Hour of the day (0–23) |
| Temperature_C | Air temperature (°C) |
| Humidity | Relative humidity (%) |
| Wind_Speed_mps | Wind speed (m/s) |
| Visibility_10m | Visibility measured in 10 meters |
| DewPoint_C | Dew point temperature (°C) |
| Rainfall_mm | Rainfall in millimeters |
| Season | Season of the year (Winter, Spring, Summer, Autumn) |
| Holiday | Indicates if the day was a holiday |
| Functioning_Day | Whether the rental system was operational (Yes/No) |
| Day_Name | Extracted day name from Date |
| Month_Name | Extracted month name from Date |
| Year | Extracted year |
| Weekday_Weekend | Classified as Weekday or Weekend |

- **Source:** Seoul Bike Sharing Dataset (CSV Format)  
- **Rows:** 8,760 (Hourly data for one year)  
- **Imported Using:** Excel → Power BI  

---

## 🧹 Data Cleaning Summary (Power Query Steps)  

| Step | Description |
|------|-------------|
| 1 | Imported CSV dataset into Power BI |
| 2 | Removed duplicates, blanks, and error rows |
| 3 | Removed unnecessary columns (like Snowfall) |
| 4 | Added calculated columns: Day_Name, Month_Name, Year, Weekday_Weekend |
| 5 | Fixed data types for all fields |
| 6 | Verified consistency for Functioning Days |
| 7 | Created new calculated column: `Weather_Type = IF([Rainfall_mm] > 0, "Rainy", "Clear")` |

---

## ⚙️ Data Transformation and Wrangling  

| Column | Transformation Applied |
|---------|------------------------|
| Snowfall (cm) | Removed |
| Day_Name | Extracted from Date |
| Month_Name | Extracted from Date |
| Year | Extracted from Date |
| Weekday_Weekend | Classified based on Day_Name |
| Weather_Type | Derived from Rainfall values |

These transformations ensured **clean, analyzable, and meaningful data** for visualization.

---

## 💡 Key KPIs (Performance Indicators)  

| KPI | Description | Formula |
|-----|--------------|----------|
| **Total Bike Rentals** | Total number of rentals | `SUM(Bike_Count)` |
| **Average Temperature (°C)** | Mean temperature across all days | `AVERAGE(Temperature_C)` |
| **Average Humidity (%)** | Mean humidity | `AVERAGE(Humidity)` |
| **Total Rainfall (mm)** | Sum of rainfall | `SUM(Rainfall_mm)` |
| **Functioning Days** | Days when system was operational | `DISTINCTCOUNT(Date)` with `Functioning_Day = "Yes"` |

---

## 📊 Dashboard Visuals  

### **Page 1: Overview Dashboard**
- 📈 Line Chart – Bike Rentals over Time  
- 🌤️ Column Chart – Rentals by Season  
- 📅 Bar Chart – Rentals by Day of Week  
- ☀️ Scatter Plot – Temperature vs Bike Rentals  
- 💧 Pie Chart – Rentals by Weather Type (Rainy / Clear)  
- 🕓 Area Chart – Hourly Rentals showing morning & evening peaks  

---

### **Page 2: Advanced Analysis**
- 🔥 **Season + Temperature Heatmap** – Best temperature range per season  
- ⏰ **Hour vs Day Heatmap** – Identifies weekly peak hours  
- 💨 **Scatter (Correlation)** – Humidity vs Bike Count (with Temperature & Rainfall tooltips)  
- ⚙️ **Clustered Bar Chart** – Functioning vs Non-Functioning Day comparison  

---

## 🧭 Filters and Slicers Used  

| Filter | Description |
|---------|-------------|
| Season | Filter data by season |
| Month | Filter by Month_Name |
| Holiday | Filter by holiday type |
| Functioning Day | Filter by operational status |

These slicers make the dashboard fully **interactive** and **user-friendly** for deeper insights.

---

## 🧠 Insights & Findings  

1. **Summer and Autumn** record the highest bike rentals, while **Winter** has the lowest.  
2. **Peak hours** are 8–9 AM and 5–7 PM — matching daily office commute times.  
3. **Ideal temperature range** (20–28°C) shows maximum rentals.  
4. **Rainy days** significantly reduce rentals.  
5. **High humidity** correlates negatively with rental count.  
6. **Functioning days** show consistent operations, confirming data stability.  

---

## 🏁 Conclusion  

This project demonstrates the power of **Power BI** in converting raw data into **insightful visual narratives**.  
It reveals how **weather and time factors** directly influence public bike usage in Seoul.  

By combining **clean data**, **calculated measures**, and **interactive visuals**, this analysis empowers **data-driven transport planning** and **smart mobility decisions**.

---

## 🛠️ Tools and Technologies Used  

- **Power BI Desktop** – Data cleaning, transformation & visualization  
- **Microsoft Excel** – Initial review & structure checking  
- **Power Query Editor** – Data wrangling & custom column creation  
- **CSV Dataset** – Source file format  

---

## 📷 Dashboard Previews  

- **Figure 1:** KPI & Overview Dashboard  
<img width="1378" height="786" alt="Screenshot 2025-10-27 220626" src="https://github.com/user-attachments/assets/ee271f6f-36ca-46d8-b88f-eb6d11e91d6b" />

- **Figure 2:** Advanced Analysis Dashboard  
<img width="1382" height="785" alt="Screenshot 2025-10-27 220539" src="https://github.com/user-attachments/assets/05b335e9-65be-44b5-8d7c-19b1a182042a" />


---

## 🙏 Acknowledgement  

Special thanks to the **Seoul Bike Sharing Dataset (Open Data)** for providing an excellent real-world dataset.  
This project was created as part of a **Data Analytics learning journey** using **Power BI**.  

---

## 📎 Author  

**👤 Name:** Prafull Wahatule  
**📧 Email:** [prafullwahatule@gmail.com](mailto:prafullwahatule@gmail.com)  
**💻 GitHub:** [prafullwahatule](https://github.com/prafullwahatule)  

---

⭐ *If you found this project helpful, don’t forget to star the repository!* ⭐
