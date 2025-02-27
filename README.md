# citibike
# 🚲 Citi Bike Ridership Analysis - NYC & NJ  

![Citi Bike](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e7/Citi_Bike_logo.svg/800px-Citi_Bike_logo.svg.png)  

## 📌 Overview  
This project analyzes **Citi Bike ridership trends** in **New Jersey**, providing insights into:  
✅ **Peak usage times & trip patterns**  
✅ **User behavior differences (members vs. casual riders)**  
✅ **Station popularity & geographic distribution**  
✅ **Trip distances & duration trends**  

🔍 **Goal:** Help city planners, transportation officials, and Citi Bike managers optimize the bike-sharing system.  

---

## 📂 Dataset  
- **Source:** [Citi Bike System Data](https://ride.citibikenyc.com/system-data)  
- **Timeframe:** October – December 2024  
- **Size:** 250,000+ trip records  
- **Key Features:**  
  - 🚲 **Ride Data**: Ride ID, Start/End Time, User Type  
  - 📍 **Geographic Data**: Start/End Station, Latitude/Longitude  
  - ⏱ **Trip Metrics**: Duration, Distance  

---

## 🛠 Technologies Used  
| **Tool**  | **Purpose** |
|-----------|------------|
| 🐍 **Python (Pandas, Geopy)** | Data cleaning, preprocessing, distance calculation |
| 📊 **Tableau Public** | Interactive dashboards & geographic analysis |
| 📍 **Geopy (Haversine Distance)** | Estimating trip distances using lat/lng |
| 🔢 **Jupyter Notebooks** | Exploratory data analysis (EDA) |

---

## 📊 Data Processing & Cleaning  
### ✅ **Step 1: Data Preparation**  
- Merged multiple months of Citi Bike data (Oct–Dec 2024).  
- Converted timestamps (`started_at`, `ended_at`) to **datetime format**.  
- Filled missing values (**unknown stations & missing coordinates**).  

### ✅ **Step 2: Feature Engineering**  
- **Trip Duration (`duration_minutes`)** → Difference between `ended_at` and `started_at`.  
- **Trip Distance (`trip_distance_miles`)** → Calculated using **latitude/longitude** with the **Geopy library**.  
- **Extracted Time Features** → `hour`, `day_of_week`, `month` from `started_at`.  

### ✅ **Step 3: Outlier Handling**  
- Removed **negative or zero-duration trips**.  
- Filtered out **unrealistically long distances (>10 miles)**.  

---

## 📊 Tableau Dashboards  
### **📌 Dashboard 1: Citi Bike Usage Trends**  
🔎 **Focus: When and How People Ride**  
✅ **KPIs** → Total rides, avg. trip duration, total distance.  
✅ **Peak Usage (Line Chart)** → Morning/evening rush hours.  
✅ **Trips by Day (Bar Chart)** → Weekday vs. weekend comparison.  
✅ **Trip Distance (Highlight Table)** → Common ride distances.  
✅ **Top 10 Start Stations (Bar Chart)** → Identifies busiest stations.  

🔗 **[View Dashboard 1 on Tableau Public](#)**  

---

### **📌 Dashboard 2: User Behavior & Station Analysis**  
🔎 **Focus: How Different Users Ride & Where**  
✅ **Member vs. Casual User Trends (Bar Chart)** → Who rides longer?  
✅ **Station Popularity (Treemap)** → Most used stations.  
✅ **Start & End Station Maps** → Citi Bike usage distribution.  

🔗 **[View Dashboard 2 on Tableau Public](#)**  

---

## 📖 Citi Bike Story: Key Takeaways  
This **Tableau Story** presents key insights in an easy-to-follow format.  
📈 **What’s Inside?**  
- **Slide 1:** Citi Bike Usage Trends (Peak times & trip distances)  
- **Slide 2:** User Behavior & Station Analysis  
- **Slide 3:** Summary & Key Takeaways  

🔗 **[View the Full Tableau Story on Tableau Public](#)**  

---

## 📂 Project Structure  
