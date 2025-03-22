# Domino's Sales Analysis Dashboard

## 1. Introduction
The dataset used for this Power BI dashboard contains order details of Domino's pizzas, including revenue, number of orders, quantity sold, and various categorical breakdowns. The key metrics analyzed include:

- **Total Revenue**: The total earnings from all pizza orders.
- **Total Number of Orders**: The count of distinct orders placed.
- **Average Order Value**: The average revenue per order.
- **Total Pizza Sold**: The total quantity of pizzas ordered.
- **Average Pizza per Order**: The average number of pizzas per order.

## 2. DAX Queries
Below are the DAX formulas used to compute key metrics:

```DAX
Avg Order Value = DIVIDE([Total Revenue],[Total no of order])
Avg Pizza per Order = DIVIDE([Total Pizza Sold],[Total no of order])
Total no of order = DISTINCTCOUNT('Dataset'[order_id])
Total Pizza Sold = SUM('Dataset'[quantity])
Total Revenue = SUM('Dataset'[price])
```

## 3. Dashboard Breakdown
The Power BI dashboard includes:

- **KPI Cards** displaying:
  - Total Revenue: **24.06M**
  - Total Orders: **21K**
  - Avg Order Value: **1.13K**
  - Total Pizza Sold: **50K**
  - Avg Pizza per Order: **2**

- **Visualizations**:
  - **Order by Weekday**: A bar chart showing the number of orders by weekday, with the highest on **Wednesday (3.5K orders)**.
  - **Order Peak Time**: A histogram showing peak order times, with spikes around **10 AM - 2 PM**.
  - **Total Revenue by Pizza Category**: A pie chart showing revenue share among categories:
    - Classic: **26.9%**
    - Supreme: **25.5%**
    - Chicken: **23.88%**
    - Veggie: **23.72%**
  - **Bottom 5 Selling Pizzas** and **Top 5 Selling Pizzas** with revenue breakdown.
  - **Pizza Sizes' Order Distribution**: A pie chart showing distribution among L, M, S, XL, and XXL sizes, with L being the most ordered (45.75%).

## 4. Insights
- **Peak Sales Days**: Wednesdays have the highest orders, while Fridays have the lowest.
- **Best-selling Pizza**: The **Barbecue Chicken Pizza** has the highest revenue (**1.25M**).
- **Worst-selling Pizza**: The **Brie Carre Pizza** has the lowest revenue (**340K**).
- **Order Timing**: Most orders happen around lunchtime (10 AM - 2 PM).
- **Category Performance**: Classic pizzas generate the most revenue, followed by Supreme.

## 5. Dashboard Output
For a visual representation, refer to the full Power BI dashboard output:

[Domino's Dashboard Output (PDF)](../mnt/data/Dominos%20Dashboard.pdf)
