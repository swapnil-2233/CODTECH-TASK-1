# CODTECH-TASK-1 
NAME-SWAPNIL BALAJI YEREWAD
TASK NAME-PERFORM INNER, LEFT, RIGHT, AND FULL JOINS ON TABLES TO COMBINE DATA MEANINGFULLY.DELIVERABLE: A SET OF JOIN QUERIES AND THEIR OUTPUTS.
FEATURES-It sounds like you're looking for an explanation of how to perform various types of joins (INNER, LEFT, RIGHT, and FULL) on tables to combine data meaningfully, likely as part of an internship or training. Let me break it down for you:

Joins in SQL
Joins are used to combine rows from two or more tables based on a related column between them. Here's a short description of the four main types of joins:

INNER JOIN:

Combines only the rows where there is a match in both tables.

If a row in one table does not have a corresponding row in the other table, it is excluded.

Example: Get customers and their orders where they have placed at least one order.

sql
Copy
SELECT customers.name, orders.order_id
FROM customers
INNER JOIN orders ON customers.customer_id = orders.customer_id;
LEFT JOIN (or LEFT OUTER JOIN):

Returns all rows from the left table and the matching rows from the right table.

If there is no match, NULL values are returned for columns from the right table.

Example: Get all customers and their orders, including customers who haven't placed any orders.

sql
Copy
SELECT customers.name, orders.order_id
FROM customers
LEFT JOIN orders ON customers.customer_id = orders.customer_id;
RIGHT JOIN (or RIGHT OUTER JOIN):

Similar to the LEFT JOIN, but it returns all rows from the right table and the matching rows from the left table.

If there is no match, NULL values are returned for columns from the left table.

Example: Get all orders and the customers who placed them, including orders without customers.

sql
Copy
SELECT customers.name, orders.order_id
FROM customers
RIGHT JOIN orders ON customers.customer_id = orders.customer_id;
FULL JOIN (or FULL OUTER JOIN):

Returns all rows when there is a match in one of the tables.

If there is no match, NULL values are returned for columns from the table with no match.

Example: Get all customers and all orders, whether or not there is a match between them.

sql
Copy
SELECT customers.name, orders.order_id
FROM customers
FULL JOIN orders ON customers.customer_id = orders.customer_id;
