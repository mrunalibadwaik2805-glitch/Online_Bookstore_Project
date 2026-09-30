# 📚 Online Bookstore SQL Project

## 📌 Project Overview

The **Online Bookstore SQL Project** is a PostgreSQL database project designed to manage and analyze an online bookstore's data.

The project contains information about **books, customers, and orders** and uses SQL queries to answer common business questions such as sales performance, customer spending, book popularity, stock availability, and revenue.

This project demonstrates practical knowledge of **SQL, PostgreSQL, database design, joins, aggregation, filtering, grouping, and business data analysis**.

---

## 🛠️ Tools & Technologies

* **Database:** PostgreSQL
* **SQL Tool:** pgAdmin 4
* **Language:** SQL
* **Data Source:** CSV files
* **Database Concepts:** Relational Database, Primary Keys, Foreign Keys

---

## 🗂️ Database Structure

The project contains three main tables:

### 1. Books

Stores information about books available in the bookstore.

| Column         | Description           |
| -------------- | --------------------- |
| Book_ID        | Unique ID of the book |
| Title          | Book title            |
| Author         | Book author           |
| Genre          | Book genre            |
| Published_year | Year of publication   |
| Price          | Book price            |
| Stock          | Available stock       |

### 2. Customers

Stores customer information.

| Column      | Description           |
| ----------- | --------------------- |
| Customer_ID | Unique customer ID    |
| Name        | Customer name         |
| Email       | Customer email        |
| Phone       | Customer phone number |
| City        | Customer city         |
| Country     | Customer country      |

### 3. Orders

Stores information about customer orders.

| Column       | Description             |
| ------------ | ----------------------- |
| Order_ID     | Unique order ID         |
| Customer_ID  | ID of the customer      |
| Book_ID      | ID of the ordered book  |
| Order_Date   | Date of order           |
| Quantity     | Number of books ordered |
| Total_Amount | Total order amount      |

---

## 🔗 Database Relationships

The database uses **primary keys and foreign keys** to establish relationships between tables.

```text
Customers
    |
    | Customer_ID
    ↓
 Orders
    |
    | Book_ID
    ↓
 Books
```

* `Customers.Customer_ID` → `Orders.Customer_ID`
* `Books.Book_ID` → `Orders.Book_ID`

---

## 📊 SQL Analysis Performed

### Basic SQL Queries

The project includes queries to:

1. Retrieve books from the **Fiction** genre.
2. Find books published after **1950**.
3. Find customers from **Canada**.
4. Retrieve orders placed in **November 2023**.
5. Calculate the total stock of books.
6. Find the most expensive book.
7. Find orders containing more than one book.
8. Find orders with a total amount greater than `$20`.
9. List all available book genres.
10. Find the book with the lowest stock.
11. Calculate total revenue generated from orders.

---

## 🚀 Advanced SQL Analysis

The project also includes advanced business-oriented queries:

### 1. Books Sold by Genre

Calculates the total number of books sold for each genre using:

* `JOIN`
* `SUM()`
* `GROUP BY`

### 2. Average Fantasy Book Price

Calculates the average price of books belonging to the Fantasy genre using:

* `AVG()`
* `WHERE`

### 3. Customers With At Least 2 Orders

Identifies customers who have placed two or more orders using:

* `COUNT()`
* `GROUP BY`
* `HAVING`
* `JOIN`

### 4. Most Frequently Ordered Book

Identifies the book that appears most frequently in the orders using:

* `COUNT()`
* `GROUP BY`
* `ORDER BY`
* `LIMIT`
* `JOIN`

### 5. Top 3 Most Expensive Fantasy Books

Finds the three most expensive books in the Fantasy genre.

### 6. Books Sold by Author

Calculates the total quantity of books sold by each author.

### 7. Cities of Customers Spending Over $30

Identifies cities where customers placed orders worth more than `$30`.

### 8. Customer With Highest Spending

Identifies the customer who has spent the most based on total order value.

### 9. Remaining Stock After Orders

Calculates the remaining stock of each book after considering fulfilled orders.

This query uses:

* `LEFT JOIN`
* `SUM()`
* `COALESCE()`
* `GROUP BY`
* Calculated columns

---

## 🧠 SQL Concepts Demonstrated

This project demonstrates the following PostgreSQL/SQL concepts:

* `CREATE DATABASE`
* `CREATE TABLE`
* `DROP TABLE`
* `PRIMARY KEY`
* `FOREIGN KEY`
* `SERIAL`
* `VARCHAR`
* `NUMERIC`
* `DATE`
* `COPY`
* `SELECT`
* `WHERE`
* `BETWEEN`
* `DISTINCT`
* `ORDER BY`
* `LIMIT`
* `SUM()`
* `AVG()`
* `COUNT()`
* `GROUP BY`
* `HAVING`
* `JOIN`
* `LEFT JOIN`
* `COALESCE()`
* Aggregate functions
* Calculated columns
* Relational database concepts

---

## 📁 Project Files

```text
Online-Bookstore-SQL/
│
├── Online_Bookstore.sql
│
├── Books.csv
├── Customers.csv
├── Orders.csv
│
└── README.md
```

### File Description

**Online_Bookstore.sql**
Contains database creation, table creation, CSV data import commands, and SQL analysis queries.

**Books.csv**
Contains book information.

**Customers.csv**
Contains customer information.

**Orders.csv**
Contains order information.

**README.md**
Contains project documentation.

---

## ▶️ How to Run the Project

### Step 1: Install PostgreSQL

Install PostgreSQL and open **pgAdmin 4** or use the PostgreSQL Query Tool.

### Step 2: Create the Database

Run:

```sql
CREATE DATABASE OnlineBookstore;
```

Connect to the `OnlineBookstore` database.

### Step 3: Create the Tables

Run the table creation section from:

```text
Online_Bookstore.sql
```

### Step 4: Import CSV Data

Update the CSV file paths in the SQL file according to the location on your computer.

Example:

```sql
COPY Books(Book_ID, Title, Author, Genre, Published_year, Price, Stock)
FROM 'D:\PostgreSQL\ST - SQL ALL PRACTICE FILES-2\All Excel Practice Files\Books.csv'
CSV HEADER;
```

Do the same for `Customers.csv` and `Orders.csv`.

### Step 5: Run the Analysis Queries

Execute the SQL queries provided in the project to analyze bookstore data.

---

## 📈 Business Questions Answered

This project answers practical business questions such as:

* Which genres have the highest book sales?
* What is the average price of Fantasy books?
* Which customers place multiple orders?
* Which book is ordered most frequently?
* Which authors sell the most books?
* Which customers spend the most money?
* What is the total bookstore revenue?
* How much stock remains after fulfilling orders?
* Which customers spend more than $30?
* Which books are the most expensive?

---

## 🎯 Project Objective

The main objective of this project is to demonstrate how **SQL and PostgreSQL can be used to store, manage, analyze, and extract meaningful insights from bookstore data**.

The project focuses on converting raw transactional data into useful information that can support business analysis and decision-making.

---

## 💡 Key Learning Outcomes

Through this project, I practiced:

* Designing relational database tables
* Creating primary and foreign key relationships
* Importing CSV data into PostgreSQL
* Writing SQL queries for data retrieval
* Performing data aggregation
* Using joins to combine multiple tables
* Filtering and grouping data
* Analyzing customer purchasing behavior
* Calculating revenue and sales metrics
* Performing inventory analysis
* Solving real-world business questions using SQL

---

## 👩‍💻 Author

**Mrunali Badwaik**

Aspiring **AI-Powered Full Stack Developer | Data Analytics Learner**

### Skills Demonstrated

`SQL` `PostgreSQL` `Data Analysis` `Database Management` `Joins` `Aggregation` `Business Analysis`

---

## ⭐ Project Highlights

This project demonstrates practical SQL skills through a real-world **Online Bookstore database**, including customer analysis, sales analysis, revenue calculation, book popularity, and inventory tracking.

If you find this project useful, feel free to ⭐ the repository.
