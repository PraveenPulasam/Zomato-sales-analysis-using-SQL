#  Zomato Sales SQL Project

This is a beginner-to-intermediate level SQL project designed for Data Analyst portfolio building. The dataset simulates Zomato's restaurant sales, including customer details, orders, menu items, and restaurant info.

---

## Project Objective

To perform **sales analysis** using SQL by answering 14 real-world business questions related to customer behavior, menu performance, revenue tracking, and restaurant performance.

---

##  Dataset Overview (`/data` folder)

- `customers.csv`: Customer names, contact info, and location
- `orders.csv`: Order details including order date, item, price, quantity, status
- `menu.csv`: Menu items with price and category
- `restaurants.csv`: Restaurant names, location, cuisine, and delivery time

---

##  Business Questions Solved

1. List all customers who placed an order.
2. Find the total number of orders delivered.
3. Show the top 5 most ordered food items.
4. What is the total sales amount per payment method?
5. How many distinct cities are served by Zomato restaurants?
6. Find the average delivery time for each restaurant.
7. Which city had the highest total number of orders?
8. Find customers who placed more than 5 orders.
9. Which menu item generated the highest total revenue?
10. Get total sales and number of orders per day.
11. Rank restaurants by total number of delivered orders using window functions.
12. Find the top 3 most popular cuisines by number of orders.
13. Show customer details with their last order date.
14. Which restaurant has the highest average order value?

---

##  Skills Used

- SQL Joins & Aggregations
- Window Functions
- Group By, Order By
- Date Functions
- Ranking & Filtering

---

##  Sample Query

```sql
-- 3. Top 5 Most Ordered Food Items
SELECT 
    menu_item, 
    COUNT(*) AS order_count
FROM orders
GROUP BY menu_item
ORDER BY order_count DESC
LIMIT 5;
