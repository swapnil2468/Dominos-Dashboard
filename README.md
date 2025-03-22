# 📊 Domino's Sales Dashboard

## 🗂 Introduction
This Power BI dashboard analyzes Domino's pizza sales data, providing key insights into revenue, order trends, and customer preferences. The dataset includes details on order transactions, pizza categories, and pricing information.

### 📌 Key Dataset Columns:
- **order_id**: Unique identifier for each order.
- **pizza_name**: Name of the pizza ordered.
- **quantity**: Number of pizzas in the order.
- **order_date** & **order_time**: Timestamp of the order.
- **price**: Total price of the order.
- **pizza_category**: Category of the pizza (e.g., Veggie, Classic, Chicken, Supreme).
- **pizza_sizes**: Available sizes (S, M, L, XL, XXL).

---

## 🔢 DAX Queries
Below are the DAX queries used for key calculations in the dashboard:

```DAX
Total Revenue = SUM('Dataset'[price])
```
Calculates the total revenue generated from pizza sales.

```DAX
Total no of order = DISTINCTCOUNT('Dataset'[order_id])
```
Counts the number of distinct orders placed.

```DAX
Total Pizza Sold = SUM('Dataset'[quantity])
```
Determines the total number of pizzas sold.

```DAX
Avg Order Value = DIVIDE([Total Revenue],[Total no of order])
```
Computes the average revenue per order.

```DAX
Avg Pizza per Order = DIVIDE([Total Pizza Sold],[Total no of order])
```
Finds the average number of pizzas per order.

---
![DASHBOARD](Dominos Dashboard.pdf)
## 📊 Dashboard Breakdown
The dashboard consists of the following key sections:

1. **Total Metrics**
   - Displays **Total Revenue, Total Orders, Avg Order Value, Total Pizzas Sold, and Avg Pizzas per Order**.
   
2. **Order by Weekday**
   - Bar chart showing total orders for each day of the week.
   
3. **Order Peak Time**
   - Histogram displaying order trends by time of the day.
   
4. **Total Revenue by Pizza Category**
   - Pie chart visualizing revenue distribution across different pizza categories.
   
5. **Top & Bottom Selling Pizzas**
   - List of the best and least-performing pizzas based on revenue.
   
6. **Pizza Size Preferences**
   - Pie chart showing the distribution of orders across different pizza sizes.

---

## 📈 Key Insights
- **Total Revenue**: ₹24.06M from **21K** orders.
- **Average Order Value**: ₹1.13K per order.
- **Total Pizzas Sold**: 50K with an **Avg of 2 pizzas per order**.
- **Peak Order Time**: Highest orders observed around **2:00 PM - 3:00 PM**.
- **Most Popular Pizza Size**: **Large (L) with 45.75% of orders**.
- **Revenue Breakdown**:
  - Classic (26.9%)
  - Supreme (25.5%)
  - Chicken (23.88%)
  - Veggie (23.72%)

---

## 📌 Conclusion
This dashboard provides valuable insights into sales trends, customer preferences, and order patterns, helping optimize inventory and marketing strategies. 🚀
