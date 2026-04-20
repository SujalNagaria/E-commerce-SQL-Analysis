# E-commerce-SQL-Analysis
Leveraged SQL to analyze an E-commerce dataset, building queries to uncover insights on customer behavior, product demand, and revenue patterns.

The main purpose of making this project was to analyse how well can I structure a query to get the desired output and what insights can I derive from the output to help make better decisions.

**Tables Involved**

1) Customers
2) Products
3) Orders
4) Order_Items

**Questions Solved**

Q1) What were the total revenue per customer?
- <img width="467" height="138" alt="Screenshot 2026-04-20 154623" src="https://github.com/user-attachments/assets/25a9f135-ddb6-424f-ae90-5385c7061142" />
To retrieve this output, I first identified which tables can I use and tried to find out the correlation between them. Once I decided to go with tables: Order_Items and CustomerID, I looked forward to calculate total revenue using the help of (Quantity*Price) from the Order_Items table.
I proceeded with joining these tables using INNER JOIN (Which retrieves matching values from both the table) on CustomerID. Last step was to group by the output by the Customer details in order to get individual total revenue for each one of them.
<img width="454" height="377" alt="Screenshot 2026-04-20 153249" src="https://github.com/user-attachments/assets/5ddd059e-1f4f-4595-9f1e-dfb9cff8f6b4" />
