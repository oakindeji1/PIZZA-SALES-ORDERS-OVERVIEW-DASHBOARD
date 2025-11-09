# PIZZA-SALES-ORDERS-OVERVIEW-DASHBOARD

# Problem Statement

## KPI’s Requirement
## We need to analyse key indicators for our pizza sales data to gain insights into our business performance.
### Specifically, we want to calculate the following metrics:
    1)	Total Revenue: The sum of the total price of all pizza orders.
    2)	Average Order values: The average amount spent per order, calculated by dividing the total revenue by the total number of orders.
    3)	Total Pizza sold: The sum of the quantities of all pizzas sold
    4)	Total Orders: The total number of orders placed.
    5)	Average Pizzas per Order: The average number of pizzas sold per order, calculated by dividing the total number of pizzas sold by the total number of orders.
### Chart Requirement
#### We would like to visualize various aspects our pizza sales data to gain insights and understanding key trends. We have identified the following requirements for creating charts:
  1)	Daily Trend for Total Orders:
      Create a bar chart that displays the daily trend of total orders over a specific time period.
  2)	Monthly Trends for Total Orders:
      Create a line chart that illustrates the hourly trend of total orders throughout the day,
  3)	Percentage of sales by Pizza Category
      Create a pie chart that shows the distribution of sales across different pizza categories
  4)	Percent of sales by Pizza Size:
      Generate a pie chart that represents the percentage of sales attributed to different pizza sizes.
  5)	Total Pizza Sold by Pizza Category
      Create a funnel chart that presents the total number of pizza sold for each pizza category
  6)	Top 5 Best Sellers by Revenue, Total Quantity, Total order
      Create a bar chart highlighting the top 5 Best Sellers by Revenue, Total Quantity, Total order
  7)	Bottom 5 Worst Seller Revenue, Total Quantity, Total order
    Create a bar chart highlighting the top 5 worst Sellers by Revenue, Total Quantity, Total order

### Software Used
    •	MS Office/Excel
    •	MS SQL Server


### 🔍 Step 1: Understand the Dataset
### Firstly, I’ll took a quick look at the structure of your Excel file — specifically:
     What sheets are present.
     What columns exist (e.g., Year, Month, Accident_Severity, Vehicle_Type, Casualties, Road_Type, etc.).
     This will allow me to map the data fields to your KPIs.
     Cleeaned the data by extrating days, Months and Year from the dates Using the below formulae:
          =TEXT(B2,"DD")
          =TEXT(B2,"MMM")
          =TEXT(B2,"YYYY")

### Step 2: Dashboard Metrics Design
### Primary KPIs
     Total Casualties
     Formula: =SUM(Casualties)
### Card visualization
     Casualties by Accident Severity
     Severity categories: Fatal, Serious, Slight
     Show total and % of total using:
     =F9/($F$9 +$F$10) i.e (Casualties by Severity) / (Total Casualties)

### Max Casualties by Vehicle Type
     Pivot Table: Vehicle Type vs SUM of Casualties
     Highlight maximum value.
     Visualization: Pie chart 

### Secondary KPIs
     Total Casualties by Vehicle Type
     Visualization: Pie chart

### Step 3: Trends and Comparisons
     Monthly Trend Comparison (2021 vs 2022)
     Pivot: Month as Axis, SUM(Casualties) as Values, Year as Legend.
     Visualization: Line chart with two lines (2021 and 2022)

### Step 4: Contextual Insights
     Max Casualties by Road Type
     Pivot: Road Type by count(Casualties) using Calculated items
     Visualization: Bar Chart.

	 Distribution by Road Surface
     Pivot: Road Surface × count(Casualties)
     Visualization: Hierarachy Chart.
     Casualties by Area and Time (Day/Night)

	Pivot: Rows → Area/Location; Columns → Day/Night; Values → SUM(Casualties)
	Visualization: Pie Chart

### Dashboard
																
<img width="1868" height="785" alt="image" src="https://github.com/user-attachments/assets/94799f7b-c52b-48bd-95b5-bd3eb4229c32" />

### Insight

🚦 Casualty Overview Dashboard Summary

	1)	Total Casualties: 197,644
	2)	Fatal: 2,486 (1.3%)
	3)	Serious: 25,685 (13%)
	4)	Slight: 169,473 (86%)

🚗 Casualties by Vehicle Type
#### Cars: 157,248 (80% of total vehicle casualties)
#### Cars remain the dominant contributor to overall road casualties, highlighting the need for continued focus on car safety and driver awareness initiatives.

📅 Casualty Trend by Month
#### Higher in Jan & Dec 2021 than Jan & Dec 2022
#### Seasonal peaks suggest increased risk during winter months, likely linked to weather and travel patterns.

🛣️ Casualties by Road Type & Condition
#### Highest by Road Type: Single Carriageway – 148,543
#### Highest by Surface Condition: Dry Roads – 135,403
#### Despite favorable surface conditions, dry roads saw the most casualties - possibly due to higher traffic volume and speed.

📍 Casualties by Location & Time
#### Urban areas: Higher than rural
#### Daylight: Higher than night-time
#### Urban density and daytime activity continue to drive higher incident rates.
