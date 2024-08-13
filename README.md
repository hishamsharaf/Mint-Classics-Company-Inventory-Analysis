# Introduction
Dive intp Mint Classic (a retailer of classic model cars and other vehicles) sales data, to provide suggestions and recommendations for reorganizing or reducing inventory. Also, they need to close on of thier storage facilities if possible to reduce expences.

# Background
To support a data-based business decision, the company wants to have insights about thier inventory and if they need inventory reducing. They want to have answers to the questions like:
1. Where are items stored and if they were rearranged, could a warehouse be eliminated?
2. How are inventory numbers related to sales figures? Do the inventory counts seem appropriate for each item?

# Project Objectives
1. Explore products currently in inventory.
2. Determine important factors that may influence inventory reorganization/reduction.
3. Provide analytic insights and data-driven recommendations.

# Tools I used
To can dive into the company data and analyze it, I used:
1. SQL: The main tool of my analysis, to can query the data and find insights.
2. MYSQL: The chosen database management.
3. Tableau: For Data Visualization.

# The Analysis
Total quantity in stock for each storage facilities.
```sql
select
	wh.warehouseName,
  sum(p.quantityInStock) as t_in_stock
FROM
    products AS p
LEFT JOIN
    warehouses AS wh ON p.warehouseCode = wh.warehouseCode
GROUP BY
    wh.warehouseName
ORDER BY
    t_in_stock DESC;
```
![Total quantity]()



