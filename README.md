## Car Sales Analysis for a business ##

### Project Overview
To understand and analyse the sales of cars by the company

<br>

---
#### Business Objectives
- To understand which make and models of car are the best-selling
- To understand the total sales of cars from different years
- To ascertain the top 10 most expensive and least expensive cars being sold
- To ascertain the average selling price of the cars in the company

#### Tools:
- SQL
- Excel

  <br>

  ---
#### Key Metrics
- The average selling price of cars in the company
- The most sold car make and model
- What are the top 10 most and lest expensive cars being sold
- Compare the sales of cars depending on the year of the car


### Code and insights

-- Car year sales

SELECT 
    "Car Year",
    SUM("Sale Price") AS Total_Sales
FROM CarSalesProject
GROUP BY "Car Year";

-- Top 10 most expensive selling Cars

SELECT DISTINCT("Car Make"), ("Car Model"),("Sale Price")
FROM CarSalesProject
ORDER BY ("Sale Price") DESC
Limit 10;

-- Number of each car make sold

SELECT "Car Make", COUNT("Car Make") as total_number
FROM CarSalesProject
GROUP BY ("Car Make")
ORDER BY ("Car Make") DESC

-- Average price of all cars sold

SELECT AVG("Sale Price")
FROM CarSalesProject

-- Looking at all the different unique cars sold

SELECT DISTINCT ("Car Make"),("Car Model")
FROM "CarSalesProject"

-- 10 cheapest cars for sale

SELECT DISTINCT("Car Make"), ("Car Model"),("Sale Price")
FROM CarSalesProject
ORDER BY ("Sale Price") 
Limit 10;

-- Best selling car make

SELECT "Car Make", COUNT("Car Make") AS Total_sold
FROM CarSalesProject
GROUP BY "Car Make"
ORDER BY Total_sold DESC
LIMIT 1;

-- Best selling car model

SELECT "Car Model", COUNT("Car Model") AS Total_sold
FROM CarSalesProject
GROUP BY "Car Model"
ORDER BY Total_sold DESC
LIMIT 1;


