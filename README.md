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






SELECT 
    "Car Year",
    SUM("Sale Price") AS Total_Sales
FROM CarSalesProject
GROUP BY "Car Year";
