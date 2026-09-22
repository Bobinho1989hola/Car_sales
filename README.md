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

<> Markdown

### Results

Car year | Total_sales
---------|------------
2016     | 2422877745
2017     | 2439544778
2018     | 2419835114
2019     | 2422945771
2020     | 2420677424
2021     | 2401486049
2022     | 2411756970


-- Top 10 most expensive selling Cars

SELECT DISTINCT("Car Make"), ("Car Model"),("Sale Price")
FROM CarSalesProject
ORDER BY ("Sale Price") DESC
Limit 10;

<> Markdown

### Results
Car Make | Car Model | Cost
---------|-----------|------
Nissan   | F-150     | 50000
Chevrolet| Altima    | 50000
Honda    | Civic     | 50000
Chevrolet| Silverado | 50000
Chevrolet| Corolla   | 50000
Nissan   | Silverado | 50000
Ford     | Civic     | 50000
Ford     | Altima    | 50000
Toyota   | F-150     | 50000

-- Number of each car make sold

SELECT "Car Make", COUNT("Car Make") as total_number
FROM CarSalesProject
GROUP BY ("Car Make")
ORDER BY ("Car Make") DESC

<> Markdown

### Results

Toyota	209315
Nissan	209114
Honda	210101
Ford	210074
Chevrolet	209971

-- Average price of all cars sold

SELECT AVG("Sale Price")
FROM CarSalesProject

### Results
 Average sales price: 30018.3739255656

-- Looking at all the different unique cars sold

SELECT DISTINCT ("Car Make"),("Car Model")
FROM "CarSalesProject"

### Results

Nissan	Altima
Nissan	F-150
Ford	Civic
Ford	Altima
Honda	Silverado
Honda	F-150
Ford	Corolla
Toyota	Silverado
Toyota	F-150
Chevrolet	Altima
Honda	Corolla
Nissan	Silverado
Toyota	Civic
Nissan	Civic
Chevrolet	F-150
Chevrolet	Silverado
Ford	Silverado
Toyota	Altima
Chevrolet	Civic
Chevrolet	Corolla
Honda	Civic
Nissan	Corolla
Toyota	Corolla
Ford	F-150
Honda	Altima


-- 10 cheapest cars for sale

SELECT DISTINCT("Car Make"), ("Car Model"),("Sale Price")
FROM CarSalesProject
ORDER BY ("Sale Price") 
Limit 10;

### Results

Nissan	Altima	10000
Nissan	Silverado	10000
Nissan	Civic	10000
Toyota	Civic	10000
Toyota	Altima	10000
Honda	Corolla	10000
Chevrolet	Civic	10000
Ford	Corolla	10000
Chevrolet	F-150	10000
Nissan	F-150	10000


-- Best selling car make

SELECT "Car Make", COUNT("Car Make") AS Total_sold
FROM CarSalesProject
GROUP BY "Car Make"
ORDER BY Total_sold DESC
LIMIT 1;

### Results
Car  | Quantity sold
-----|-------------
Honda|	210101


-- Best selling car model

SELECT "Car Model", COUNT("Car Model") AS Total_sold
FROM CarSalesProject
GROUP BY "Car Model"
ORDER BY Total_sold DESC
LIMIT 1;

### Results

Silverado	210257



