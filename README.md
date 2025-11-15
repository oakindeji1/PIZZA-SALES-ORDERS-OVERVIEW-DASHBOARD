# PIZZA-SALES-ORDERS-OVERVIEW-DASHBOARD

# Problem Statement

## Step 1: Import the file into SQL
### 🔍 Step 2: Understand the Dataset
### Firstly, I’ll took a quick look at the structure of your SQL file — specifically:

    What sheets are present.
    What columns exist (e.g., Pizza Id, Order id, Quantity, Order Date, Order Time, Unit Price, Total Price, pizza Category,etc.) 
	with 48,620 rows.
    This will allow me to map the data fields to your KPIs.
     
### Software Used
    • MS SQL Server
	• MS Office/Excel
    	
## KPI’s Requirement
## We need to analyse key indicators for our pizza sales data to gain insights into our business performance.
### Specifically, we want to calculate the following metrics:

Table  format
<img width="1919" height="1022" alt="image" src="https://github.com/user-attachments/assets/8243fe73-34cd-49c7-bd01-59079a866b17" />


   ###  1)	Total Revenue: The sum of the total price of all pizza orders.
   
<img width="1807" height="671" alt="image" src="https://github.com/user-attachments/assets/6c84e99f-9f4c-4d08-bc22-17e85f5811cf" />


   ### 2)	Average Order values: The average amount spent per order, calculated by dividing the total revenue by the total number of orders.
   
<img width="1529" height="606" alt="image" src="https://github.com/user-attachments/assets/bad22088-f3b3-4772-a282-36e275916728" />


   ### 3)	Total Pizza sold: The sum of the quantities of all pizzas sold

   <img width="1115" height="603" alt="image" src="https://github.com/user-attachments/assets/c1088e49-f87b-437c-9e7b-fcb908fda891" />

	
  ###  4)	Total Orders: The total number of orders placed.

  <img width="1375" height="556" alt="image" src="https://github.com/user-attachments/assets/ab8d393d-fa6b-4e90-b10f-9d8d797688b7" />

	
  ###  5)	Average Pizzas per Order: The average number of pizzas sold per order, calculated by dividing the total number of pizzas sold by the total number of orders.

  <img width="1294" height="601" alt="image" src="https://github.com/user-attachments/assets/3adca883-0690-45ff-99d4-a87ff9910498" />

	
### Chart Requirement
#### We would like to visualize various aspects our pizza sales data to gain insights and understanding key trends. We have identified the following requirements for creating charts:

 ###  1)	Daily Trend for Total Orders
 
<img width="1642" height="675" alt="image" src="https://github.com/user-attachments/assets/5f1fa557-1077-49bf-8d34-4a9ed78740bf" />


 ###     Create a bar chart that displays the daily trend of total orders over a specific time period.
 
 ### 2)	Monthly Trends for Total Orders:
 
<img width="1698" height="789" alt="image" src="https://github.com/user-attachments/assets/88955332-905d-4a80-8e32-29d5634aa0a3" />


  ###    Create a line chart that illustrates the hourly trend of total orders throughout the day,
  
  ### 3)	Percentage of sales by Pizza Category
  
   <img width="1521" height="710" alt="image" src="https://github.com/user-attachments/assets/a4effec9-4225-4636-b8be-f593bc0310c4" />


  ###    Create a pie chart that shows the distribution of sales across different pizza categories
 ### 4)	Percent of sales by Pizza Size:
 
  <img width="1483" height="662" alt="image" src="https://github.com/user-attachments/assets/10c2e805-b1f0-4436-bcc6-56eb13cd29b0" />

 ###     Generate a pie chart that represents the percentage of sales attributed to different pizza sizes.
###  5)	Total Pizza Sold by Pizza Category

<img width="1609" height="670" alt="image" src="https://github.com/user-attachments/assets/fcb84820-96a0-4bd0-bd5b-5dce3018597a" />

 ###     Create a funnel chart that presents the total number of pizza sold for each pizza category

 ### 6)	Top 5 Best Sellers by Revenue

<img width="1427" height="786" alt="image" src="https://github.com/user-attachments/assets/4d3990d0-d116-4e3c-b38c-638d57ebcbc2" />


 ###     Create a bar chart highlighting the top 5 Best Sellers by Revenue, Total Quantity, Total order
 
 ### 7)	Bottom 5 Worst Seller Revenue
 
<img width="1273" height="748" alt="image" src="https://github.com/user-attachments/assets/420efe35-bb75-4643-b3af-567b7f290f4b" />


 ###   Create a bar chart highlighting the top 5 worst Sellers by Revenue, Total Quantity, Total order
 
 ### 8)	Top 5 Best Sellers by Total Quantity

<img width="1342" height="692" alt="image" src="https://github.com/user-attachments/assets/f6fc8c71-7e86-4521-bc54-cc79a5317aaa" />

 ###     Create a bar chart highlighting the top 5 Best Sellers by Revenue, Total Quantity, Total order
 
 ### 9)	Bottom 5 Worst Seller by Total Quantity

<img width="1431" height="764" alt="image" src="https://github.com/user-attachments/assets/292bc1e1-5661-4cd7-9e4e-18e7c59d6348" />

	 
###    Create a bar chart highlighting the top 5 worst Sellers by Revenue, Total Quantity, Total order
	
###  10)	Top 5 Best Sellers by Total order

<img width="1373" height="744" alt="image" src="https://github.com/user-attachments/assets/df155d87-b685-490f-a720-8933b984ddce" />

 ###      Create a bar chart highlighting the top 5 Best Sellers by Revenue, Total Quantity, Total order
	  
###  11)	Bottom 5 Worst Seller by Total order
      
<img width="1344" height="785" alt="image" src="https://github.com/user-attachments/assets/8ff6010c-3217-437b-b654-31c8fe8874eb" />


### Create a bar chart highlighting the top 5 worst Sellers by Total order



Now I imported the sql file in Excel file:
<img width="1703" height="897" alt="image" src="https://github.com/user-attachments/assets/b18fd3dc-8325-4d5c-bb17-35e8d5e68bce" />

and the imported file as below:

<img width="1886" height="939" alt="image" src="https://github.com/user-attachments/assets/dbfc8baa-e0cb-46d2-9c14-7bbdd9c82b4b" />

Cleeaned the data by 
Getting the Total Order using 
       =1/COUNTIF(B:B,[@[order_id]])
extrating days, Months and Year from the dates Using the below formulae:
          =TEXT(B2,"MMM")
		  =TEXT(B2,"DDD")
          =TEXT(B2,"YYYY")
And Hour as 
=TEXT([@[order_time]],"HH")

The Unit Price and Total Price Column was formated as currency 

Then Replace L, S,M, XL, XXL to Large, Small,Medium, XLarge and, XXLarge

### Step 2: Dashboard Metrics Design


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
