# Seoul Smart Mobility
### Weather Impact and Rental Trend Analysis


## 📘 Project Overview

This Power BI project focuses on analyzing the Seoul Bike Sharing dataset to identify key patterns, trends, and factors influencing bike rentals.
The dataset contains hourly data of rented bikes, weather conditions, and operational details.
Through data cleaning, transformation, and visualization, this report helps understand how temperature, humidity, rainfall, and time patterns affect user behavior.

The dashboard provides interactive insights, seasonal comparisons, and advanced visuals for data-driven decision-making.

## 🎯 Objectives

To analyze the relationship between bike rentals and weather parameters.

To identify peak rental hours, days, and seasons.

To understand how rainfall, temperature, and humidity affect rental demand.

To develop an interactive Power BI dashboard showcasing both summary KPIs and advanced insights.

To improve decision-making for urban mobility and resource optimization.

## 🧩 Dataset Description

- Source: Seoul Bike Sharing Dataset (CSV Format)
- Total Records: 8,760 rows (Hourly data for one year)
- File Type: CSV
- Imported Using: Microsoft Excel → Power BI

Column Name	Description
Date	Date when the rentals were recorded
Bike_Count	Number of bikes rented during that hour
Hour	Hour of the day (0–23)
Temperature_C	Air temperature (°C)
Humidity	Relative humidity (%)
Wind_Speed_mps	Wind speed (m/s)
Visibility_10m	Visibility measured in 10 meters
DewPoint_C	Dew point temperature (°C)
Rainfall_mm	Rainfall in millimeters
Season	Season of the year (Winter, Spring, Summer, Autumn)
Holiday	Whether it was a holiday or not
Functioning_Day	Indicates if the rental system was operating (Yes/No)
Day_Name	Extracted day name from date
Month_Name	Extracted month name
Year	Extracted year
Weekday_Weekend	Classifies day as Weekday or Weekend
🧹 Data Preparation and Cleaning

## Performed in Power Query Editor (Power BI)

Step	Description
1	Imported CSV file into Power BI
2	Removed duplicate, blank, and error rows
3	Removed unwanted columns like “Snowfall (cm)”
4	Added new columns – Day_Name, Month_Name, Year, Weekday_Weekend
5	Ensured correct data types (Date, Numeric, Text)
6	Verified consistent data for Functioning Days
7	Created calculated columns like Weather_Type = IF([Rainfall_mm] > 0, "Rainy", "Clear")

## ⚙️ Data Transformation and Wrangling
Column	Transformation Applied
Snowfall (cm)	Removed (Not required)
Day_Name	Added using Date column
Month_Name	Added using Date column
Year	Extracted from Date
Weekday_Weekend	Classified based on Day_Name

These transformations helped in building meaningful visuals and filters for detailed analysis.

##💡 Key KPIs (Performance Indicators)
### KPI	Description	Formula
Total Bike Rentals	Overall rental count	SUM(Bike_Count)
Average Temperature (°C)	Average temperature over all days	AVERAGE(Temperature_C)
Average Humidity (%)	Average humidity value	AVERAGE(Humidity)
Total Rainfall (mm)	Total rainfall during the period	SUM(Rainfall_mm)
Functioning Days	Count of days when system was active	DISTINCTCOUNT(Date) with Functioning_Day = Yes

## 📊 Dashboard Visuals
### Page 1: Overview Dashboard

- 📈 Line Chart: Bike rentals over time

- 🌤️ Column Chart: Rentals by Season

- 📅 Bar Chart: Rentals by Day of Week

- ☀️ Scatter Plot: Temperature vs Bike Rentals

- 💧 Pie Chart: Rentals by Weather Type (Rainy / Clear)

- 🧭 Area Chart: Hourly rentals to show morning & evening peaks

### Page 2: Advanced Analysis

- 🔥 Season + Temperature Heatmap: Shows which temperature range performs best per season

- ⏰ Hour vs Day Heatmap: Identifies peak hours for each day

- 💨 Scatter (Correlation): Humidity vs Bike Count (with Temperature & Rainfall tooltips)

- ⚙️ Clustered Bar Chart: Functioning vs Non-Functioning Days comparison

## 🧭 Filters and Slicers Used
Filter	Field Used
Season	Season column
Month	Month_Name
Holiday	Holiday column
Functioning Day	Functioning_Day column

These filters allow users to analyze bike rental trends for specific seasons, holidays, or operational days.

## 🧠 Insights & Findings

1. Rentals are highest during Summer and Autumn, and lowest in Winter.

2. Peak hours are 8–9 AM and 5–7 PM, matching office commute times.

3. Moderate temperatures (20–28°C) result in the highest rentals.

4. Rainy days have significantly lower rentals.

5. A negative correlation exists between Humidity and Bike Count.

Functioning days show consistent operations with minimal downtime.

## 🏁 Conclusion

This project demonstrates how Power BI can transform raw data into meaningful visual stories.
Through the Seoul Bike Sharing dataset, we discovered that temperature, weather, and time are the main drivers of rental demand.

By creating interactive dashboards, users can easily explore how environmental conditions and user behavior change throughout the year.
The project achieves its main goal of providing clear, data-driven insights for better planning and decision-making in urban transport systems.

## 🛠️ Tools and Technologies Used

- Power BI Desktop – Data cleaning, transformation, visualization

- Microsoft Excel – Pre-analysis & structure checking

- CSV Dataset – Source file format

- Power Query Editor – Used for data wrangling and transformation

## 📷 Dashboard Previews

Figure 1: KPI and Overview Dashboard
Figure 2: Advanced Analysis Dashboard

## 🙏 Acknowledgement

Special thanks to open datasets like the Seoul Bike Sharing Data, which provided a great opportunity to explore real-world weather-based analysis.
This project was created as part of a learning journey in Data Analytics and Power BI.

##📎 Author

👤 Prafull Wahatule
📧 Email: [prafullwahatule@gmail.com]
💻 GitHub: prafullwahatule
