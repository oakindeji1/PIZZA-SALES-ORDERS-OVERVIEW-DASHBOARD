# PIZZA-SALES-ORDERS-OVERVIEW-DASHBOARD

# Problem Statement

## KPI’s Requirement
## We need to analyse key indicators for our pizza sales data to gain insights into our business performance.
### Specifically, we want to calculate the following metrics:

   ###  1)	Total Revenue: The sum of the total price of all pizza orders.
   
	<img width="287" height="131" alt="image" src="https://github.com/user-attachments/assets/6ed7c8fc-42c6-45c2-a708-1bf25169ff0a" />

   ### 2)	Average Order values: The average amount spent per order, calculated by dividing the total revenue by the total number of orders.
	<img width="305" height="133" alt="image" src="https://github.com/user-attachments/assets/40ae47e4-dfb2-4529-becf-5413e22c274c" />

   ### 3)	Total Pizza sold: The sum of the quantities of all pizzas sold
	<img width="311" height="135" alt="image" src="https://github.com/user-attachments/assets/13e23d14-4ad0-4325-85f0-fffe065be6fe" />

  ###  4)	Total Orders: The total number of orders placed.
	<img width="315" height="128" alt="image" src="https://github.com/user-attachments/assets/00de21e3-0f26-46f1-89ce-98b88bfd1b01" />

  ###  5)	Average Pizzas per Order: The average number of pizzas sold per order, calculated by dividing the total number of pizzas sold by the total number of orders.
	<img width="325" height="141" alt="image" src="https://github.com/user-attachments/assets/df0337b7-d31b-429b-a1e9-1e8164fa9932" />

### Chart Requirement
#### We would like to visualize various aspects our pizza sales data to gain insights and understanding key trends. We have identified the following requirements for creating charts:

 ###  1)	Daily Trend for Total Orders
 
     <img width="367" height="325" alt="image" src="https://github.com/user-attachments/assets/34a592c3-6e80-4235-b422-3d4e46c4f970" />

 ###     Create a bar chart that displays the daily trend of total orders over a specific time period.
 
 ### 2)	Monthly Trends for Total Orders:
 
     <img width="400" height="475" alt="image" src="https://github.com/user-attachments/assets/f193b809-478e-4299-8e74-f08c4dc3a011" />

  ###    Create a line chart that illustrates the hourly trend of total orders throughout the day,
  
  ### 3)	Percentage of sales by Pizza Category
  
    <img width="601" height="275" alt="image" src="https://github.com/user-attachments/assets/35a88b30-168c-4881-8bc9-f0d6cd6b060a" />

  ###    Create a pie chart that shows the distribution of sales across different pizza categories
 ### 4)	Percent of sales by Pizza Size:
  	<img width="549" height="318" alt="image" src="https://github.com/user-attachments/assets/33d02fba-7cf1-48f3-b914-4071b5902392" />

 ###     Generate a pie chart that represents the percentage of sales attributed to different pizza sizes.
###  5)	Total Pizza Sold by Pizza Category
      <img width="565" height="271" alt="image" src="https://github.com/user-attachments/assets/a5d293f1-7b38-467d-b79b-eed6d22f54fd" />

 ###     Create a funnel chart that presents the total number of pizza sold for each pizza category

 ### 11)	Top 5 Best Sellers by Revenue
      <img width="516" height="242" alt="image" src="https://github.com/user-attachments/assets/5eb16410-1637-4534-91fc-71ad5b124b9e" />

 ###     Create a bar chart highlighting the top 5 Best Sellers by Revenue, Total Quantity, Total order
 ### 13)	Bottom 5 Worst Seller Revenue
      <img width="560" height="211" alt="image" src="https://github.com/user-attachments/assets/fbd4410b-1342-4a00-b6af-2c882f1c5d3e" />

 ###   Create a bar chart highlighting the top 5 worst Sellers by Revenue, Total Quantity, Total order
 ### 11)	Top 5 Best Sellers by Total Quantity
      <img width="716" height="283" alt="image" src="https://github.com/user-attachments/assets/82a1b1f8-d0ec-4a8e-869b-4809d2406f13" />

 ###     Create a bar chart highlighting the top 5 Best Sellers by Revenue, Total Quantity, Total order
 ### 13)	Bottom 5 Worst Seller by Total Quantity
     <img width="667" height="305" alt="image" src="https://github.com/user-attachments/assets/85e8a013-bcb8-4a38-ad72-0b26fea4e264" />

###    Create a bar chart highlighting the top 5 worst Sellers by Revenue, Total Quantity, Total order
	
###  11)	Top 5 Best Sellers by Total order
       <img width="516" height="264" alt="image" src="https://github.com/user-attachments/assets/07727706-f191-4ec5-b721-a693b9e8fc8c" />
 ###      Create a bar chart highlighting the top 5 Best Sellers by Revenue, Total Quantity, Total order
	  
###  13)	Bottom 5 Worst Seller by Total order
       <img width="508" height="215" alt="image" src="https://github.com/user-attachments/assets/01842d00-f8d1-4b7c-8e26-f131beef8c65" />

### Create a bar chart highlighting the top 5 worst Sellers by Total order

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
