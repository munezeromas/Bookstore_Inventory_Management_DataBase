#  Bookstore Inventory Management Database

This project provides a relational database schema for managing a bookstore's inventory, customer information, and orders. It is built using PostgreSQL and follows standard database normalization principles.

##  Project Overview

The **Bookstore Inventory Management** system enables efficient tracking of:
- Books in stock
- Customer details
- Order records

The design ensures data integrity and supports scalability for future features such as purchase history, inventory alerts, and sales analytics.



## Technologies Used

- **PostgreSQL 17**
- **SQL (DDL & DML)**
- **IntelliJ IDEA** (with JDBC integration)
- **Git & GitHub** for version control



## Books Table
Stores information about books available in the store.

| Column          | Data Type     | Description               |
|-----------------|---------------|---------------------------|
| book_id         | SERIAL        | Primary Key               |
| title           | VARCHAR(100)  | Title of the book         |
| author          | VARCHAR(100)  | Author of the book        |
| genre           | VARCHAR(50)   | Genre/category            |
| price           | DECIMAL(6, 2) | Price of the book         |
| stock_quantity  | INT           | Available quantity in stock |


### Customers Table
Contains details of customers.

| Column       | Data Type     | Description             |
|--------------|---------------|-------------------------|
| customer_id  | SERIAL        | Primary Key             |
| first_name   | VARCHAR(50)   | First name              |
| last_name    | VARCHAR(50)   | Last name               |
| email        | VARCHAR(100)  | Customer's email        |
| phone        | VARCHAR(20)   | Contact number          |

---

###  Orders Table
Logs all customer orders.

| Column        | Data Type       | Description                     |
|---------------|------------------|---------------------------------|
| order_id      | SERIAL           | Primary Key                     |
| customer_id   | INT              | Foreign Key → Customers         |
| order_date    | TIMESTAMP        | Date & time of the order        |
| total_amount  | DECIMAL(8, 2)    | Total cost of the order         |

