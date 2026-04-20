# E-commerce-SQL-Analysis
Leveraged SQL to analyze an E-commerce dataset, building queries to uncover insights on customer behavior, product demand, and revenue patterns.

The main purpose of making this project was to analyse how well can I structure a query to get the desired output and what insights can I derive from the output to help make better decisions.

**TABLES INVOLVED**

1) Customers
2) Products
3) Orders
4) Order_Items

**QUESTIONS SOLVED**

**Q1) What were the total revenue per customer?**

**Output**

<img width="466" height="135" alt="Screenshot 2026-04-20 160037" src="https://github.com/user-attachments/assets/f01d3047-515a-44da-af8f-abcc3c4e5ec9" />


To retrieve this output, I first identified which tables can I use and tried to find out the correlation between them. Once I decided to go with tables: Order_Items and CustomerID, I looked forward to calculate total revenue using the help of (Quantity*Price) from the Order_Items table.

I proceeded with joining these tables using INNER JOIN (Which retrieves matching values from both the table) on CustomerID. Last step was to group by the output by the Customer details in order to get individual total revenue for each one of them.
Using Order By was crucial to gain insights from the output.

**Query**

<img width="478" height="364" alt="Screenshot 2026-04-20 155938" src="https://github.com/user-attachments/assets/351911b9-7e6b-476b-9c19-cf9047967772" />


**Data Driven Insights**

The results indicate that Pranali Pandey is the highest-spending customer, whereas Shreya Singh contributes relatively low revenue. This distinction helps identify high-value customers and provides insight into purchasing behavior and product preferences.



**Q2) How many number of orders are there per Customer. Also, Provide customer details.**

**Output**

<img width="529" height="132" alt="Screenshot 2026-04-20 160628" src="https://github.com/user-attachments/assets/bf8f1c6d-99ab-45e3-9977-01086ce0cc00" />


To retrieve this output, I first identified the relevant tables: Orders and Customers and established their relationship using CustomerID.

I then used an INNER JOIN to combine both tables, ensuring only customers with orders were included. Next, I applied COUNT(OrderID) to calculate the total number of orders per customer and used GROUP BY on customer details to aggregate the results correctly.

Finally, I used ORDER BY TotalOrders DESC to rank customers based on their order count, making it easier to identify the most active customers.

**Query**

<img width="704" height="401" alt="Screenshot 2026-04-20 162227" src="https://github.com/user-attachments/assets/1f7a419e-df67-4018-a219-715e5c3a4e2e" />



**Data Driven Insights**

The output reveals that Sujal Nagaria leads in total orders, but only by a small margin. This suggests limited differentiation in customer engagement and indicates potential to enhance product quality or customer experience to increase purchase frequency.

**Q3) Who are the Top 3 highest speniding Customers?**

**OUTPUT**

<img width="579" height="112" alt="Screenshot 2026-04-20 162711" src="https://github.com/user-attachments/assets/7a293343-c0ee-47b6-a79b-21786d917d30" />

To retrieve this output, I used the Orders, Order_Items, and Customers tables and joined them using OrderID and CustomerID to connect transaction-level data with customer details. This allowed me to combine purchase information with customer attributes like name and city.

I then calculated the total amount spent by each customer using SUM(Quantity * Price), ensuring the revenue is derived from detailed order-level data. After that, I grouped the results by customer details to aggregate their total spending.

Finally, I used ORDER BY to rank customers based on their spending in descending order and applied TOP 3 to extract the highest-spending customers.

**QUERY**

<img width="531" height="436" alt="Screenshot 2026-04-20 162455" src="https://github.com/user-attachments/assets/0f743378-2e7a-4d93-aa25-e16739d68828" />









