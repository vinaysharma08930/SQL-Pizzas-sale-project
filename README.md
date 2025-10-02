# SQL Pizza Sale Project:

## Overview:
This project simulates a *Pizza Sale database* using SQL. The database is designed to manage pizza sales, customers, orders, and inventory. 

## Features:
- Manage *Customers, **Orders, **Pizzas, and **Categories*.
- Perform *CRUD operations* on all tables.
- Generate *sales reports* and insights.
- Learn *JOINs, GROUP BY, and aggregation functions*.
- Analyze *category-wise distribution* of pizza sales.

## Database Structure:

### Tables:
1. *Customers*:
   - CustomerID (Primary Key)
   - Name
   - Email
   - Phone
   - Address

2. *Pizzas*:
   - PizzaID (Primary Key)
   - Name
   - CategoryID (Foreign Key)
   - Price

3. *Categories*:
   - CategoryID (Primary Key)
   - CategoryName

4. *Orders*:
   - OrderID (Primary Key)
   - CustomerID (Foreign Key)
   - OrderDate
   - TotalAmount

5. *OrderDetails*:
   - OrderDetailID (Primary Key)
   - OrderID (Foreign Key)
   - PizzaID (Foreign Key)
   - Quantity
   - Price

## Sample Queries:
- View *all pizzas* with category:
```sql
SELECT Pizzas.Name, Categories.CategoryName, Pizzas.Price
FROM Pizzas
JOIN Categories ON Pizzas.CategoryID = Categories.CategoryID;

Total sales per pizza:


SELECT Pizzas.Name, SUM(OrderDetails.Quantity) AS TotalSold
FROM OrderDetails
JOIN Pizzas ON OrderDetails.PizzaID = Pizzas.PizzaID
GROUP BY Pizzas.Name;

Customer order history:


SELECT Customers.Name, Orders.OrderID, Orders.OrderDate, Orders.TotalAmount
FROM Orders
JOIN Customers ON Orders.CustomerID = Customers.CustomerID;


### Installation & Setup:

1. Clone the repository:

git clone <https://github.com/vinaysharma08930/SQL-Pizzas-sale-project/tree/main>

2. Open your SQL client (MySQL, PostgreSQL, etc.).


3. Run the provided schema.sql to create tables.


4. Run data.sql to populate sample data.


5. Start practicing SQL queries.


### Insights & Analysis.

Identify top-selling pizzas.

Check category-wise pizza distribution.

Analyze customer order patterns.

Generate monthly/weekly sales reports.

### Tools Used:
SQL (MySQL )
