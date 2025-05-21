# Uber Analytics: An Exploratory Data Analysis Using Power BI

### Table of Contents
- [Project Overview](#project-overview)
- [Objectives](#objectives)
- [Landing Page and Methodology](#landing-page-and-methodology)
- [Data Source](#data-source)
- [Tools and Techniques Used](#tools-and-techniques-used)
- [Type of Analysis](#type-of-analysis)
- [Key Performance Indicators](#key-performance-indicators)
- [Data Analysis and Results](#data-analysis-and-results)
- [Key Insights](#key-insights)
- [Recommendations](#recommendations)

### Project Overview
This project analyzes Uber ride data to uncover key insights regarding trip patterns, total fares, distances traveled, and night shift distributions. The goal is to create an interactive Power BI dashboard that helps visualize trip trends based on location, time, and payment type.
![Uber Analytics Dashboard edited](https://user-images.githubusercontent.com/123456789/yourimage.jpg)

### Objectives
- Develop a dashboard to track key ride metrics (trips, fares, duration, and distance).
- Identify trends in Uber rides across different times and locations.
- Analyze payment methods used by customers.
- Provide recommendations for optimizing Uber services.

### Landing Page and Methodology
The dataset consists of two tables:
- Location Table (CSV file) – Contains trip location details.
- Trip Details Table (Excel file) – Contains trip metadata, including timestamps, fares, and distances.

### Key Column Descriptions
- Trip ID – Unique identifier for each trip.
- Pickup Time & Drop-off Time – Start and end time of each ride.
- Trip Distance – Distance covered during the ride.
- Fare Amount & Surge Fee – Base fare and any surge pricing applied.
- Total Fare – Sum of fare amount and surge fee.
- Payment Type – Method used to pay for the trip (e.g., card, cash).

### Data Source
- The Location Table dataset (CSV file) was obtained from [DataWolfs](https://drive.google.com/file/d/1r9FvSg3No1apwp_7k4OHIQzpQxrx9eJL/view?usp=drive_link)
- The Trip Details dataset (Excel file) was obtained from [DataWolfs](https://docs.google.com/spreadsheets/d/1gSR39464gWsXKlEXC7sk1jVnOjtid91j/edit?usp=drive_link&ouid=111270115836829077910&rtpof=true&sd=true)

### Tools and Techniques Used
- Tools: Power BI, Microsoft Excel
- Techniques: Data Cleaning, Data Transformation, Data Visualization, and DAX calculations

### Type of Analysis
Exploratory Data Analysis (EDA) – Identifying patterns, trends, and anomalies in Uber ride data.

### Key Performance Indicators
- Total Trips: Number of trips within a selected timeframe.
- Total Fare: Total revenue generated from trips.
- Total Distance: Total distance covered across all trips.
- Night Trip Percentage: Percentage of trips occurring during nighttime.
- Trip Distribution by Location: Identifies popular pickup locations.

### Data Analysis and Results
- A Date Table was created to facilitate time-based filtering.
- A Shift Column was created to categorize trips as Day (6 AM - 9 PM) or Night (9 PM - 6 AM).
- Relationships were established between Trip Details, Location Table, and Date Table to enhance dashboard interactivity.
- KPIs were calculated using DAX measures, such as:
Total Trips = COUNT('Trip Details'[Trip ID])
Total Fare = SUM('Trip Details'[Fare])
Night Shift% % = 
VAR Nightcount = CALCULATE([Total Trips], 'Trip Details'[Shift] = "Night")
RETURN DIVIDE(Nightcount, [Total Trips], 0)

### Key Insights
1. Total Trips & Revenue
- Total Trips: 117K rides recorded in the dataset.
- Total Fare Revenue: $1.8M in total earnings.
- Total Distance Traveled: 393.9K miles covered by Uber rides.

2. Peak Ride Times
- The most pickups occur between 6 AM and 9 AM and 5 PM and 8 PM, indicating peak commuting hours.
- A noticeable trip dip is observed between 10 AM and 4 PM, likely due to lower demand.

3. Night Shift Trends
- 39.6% of Uber rides happen during nighttime (9 PM - 6 AM), showing a strong late-night demand.
- Demand surges between 10 PM - 2 AM, which aligns with nightlife and late-hour work shifts.

4. Trip Distribution by Location (Top 5 busiest pickup locations)
- Penn Station
- Upper East Side
- Lenox Hill
- Clifton
- Upper West Side
These areas account for many Uber trips, suggesting high commuter activity.

5. Trip Distribution by Day
- Friday and Saturday see the highest trip volumes, likely due to social outings.
- Wednesdays record the lowest trips, suggesting midweek slumps in ride demand.

6. Payment Preferences
- Credit/Debit Card payments dominate at 87.5%, while Cash payments account for 12.5% of transactions.
- Digital payment adoption is high, reinforcing Uber’s cashless transaction model.

7. Trip Duration & Distance
- Total trip duration: 1.9 million minutes (~31,667 hours).
- Average trip distance: ~3.37 miles per ride.

8. Demand Patterns by Pickup Time
- The highest number of rides occurs around 7:00 AM and 6:00 PM, reinforcing peak work commute times.
- A minor spike in pickups happens around 11:00 PM, aligning with late-night travel needs.

### Recommendations
- Surge Pricing Optimization: Increase pricing during peak hours to maximize revenue and encourage more drivers to be available.
- Driver Allocation: Assign more drivers to high-demand locations based on historical trends to reduce wait times and improve customer satisfaction.
- Improved Night Safety Measures: With nearly 40% of trips occurring at night, Uber should enhance safety protocols for both riders and drivers, such as emergency assistance features, background checks, and better driver-rider matching.
- Incentives for Nighttime Drivers: Offer incentives such as higher commissions, bonuses, or fuel subsidies to encourage more drivers to work night shifts, reducing long wait times during those hours.
- Enhanced Payment Method Options: If cash or specific payment methods are underutilized, Uber should explore adding more local payment options to improve accessibility for a wider range of customers.
- Optimized Route Planning: Leverage AI-driven route optimization to reduce travel time, fuel consumption, and driver fatigue, leading to a better ride experience.
- Targeted Marketing Campaigns: Run promotions or discounts for specific customer segments based on ride frequency, location, or time of day to encourage repeat business.
- Reduce Cancellations & No-shows: Introduce penalties or flexible ride options for customers who frequently cancel trips, minimizing disruptions for drivers.
- Improve Fare Transparency: Provide a detailed fare breakdown (distance, time, surge pricing, fees) before trip confirmation to enhance customer trust and reduce fare disputes.
- Dynamic Driver Scheduling: Use predictive analytics to adjust driver availability based on demand patterns, ensuring that drivers are where they’re needed most.






