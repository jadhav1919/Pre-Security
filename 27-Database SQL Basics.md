# Databases Basics - Concepts

## What is Data?

Data is information stored by a computer.

Examples:

* Names
* Prices
* Dates
* Orders
* User accounts

Data becomes useful when it is organized and easy to search.

 

# What is a Database?

A database is a structured collection of data stored electronically.

It allows computers to:

* Store information
* Search information
* Update information
* Retrieve information quickly

A database can be thought of as a digital notebook that never runs out of pages.

 

# Why Use Databases?

Without databases:

* Information becomes difficult to manage
* Searching takes longer
* Large amounts of data become confusing

Databases solve these problems by organizing data efficiently.

 

# Tables

Data inside a database is stored in tables.

A table is similar to a spreadsheet.

Example:

| ID | Drink  | Price |
| -- | ------ | ----- |
| 1  | Coffee | 3     |
| 2  | Tea    | 2     |

Each table stores information about a specific topic.

 

# Columns

Columns define the type of information stored.

Examples:

| id | drink | price |
| -- | ----- | ----- |

Columns:

* id
* drink
* price

Each column stores one type of data.

 

# Rows

A row represents one complete record.

Example:

| id | drink  | price |
| -- | ------ | ----- |
| 1  | Coffee | 3     |

This entire line is one row.

Key Idea:

* Column = one type of information
* Row = one complete record

 

# Record

A record is another name for a row.

Example:

| id | drink | price |
| -- | ----- | ----- |
| 5  | Latte | 4     |

This row is one record.

 

# SQL (Structured Query Language)

SQL is a language used to communicate with databases.

It allows users to:

* View data
* Search data
* Filter data
* Sort data
* Modify data

SQL works by sending queries to a database.

 

# Query

A query is a request sent to a database.

Examples:

* Show all orders
* Show only coffee orders
* Show cheapest drinks
* Sort drinks by price

The database processes the query and returns results.

 

# SELECT

Used to choose which columns should be displayed.

Syntax:

```sql
SELECT column_name
FROM table_name;
```

Examples:

```sql
SELECT drink FROM Orders;
```

```sql
SELECT drink, price FROM Orders;
```

 

# SELECT *

The * symbol means all columns.

Example:

```sql
SELECT * FROM Orders;
```

Returns every column from the table.

 

# FROM

Specifies which table SQL should use.

Example:

```sql
SELECT * FROM Orders;
```

Here:

```sql
FROM Orders
```

tells SQL to retrieve data from the Orders table.

 

# WHERE

Used to filter rows.

Only rows matching the condition are returned.

Example:

```sql
SELECT * FROM Orders
WHERE drink = 'Coffee';
```

Returns only coffee orders.

---

# ORDER BY

Used to sort results.

Example:

```sql
SELECT * FROM Orders
ORDER BY price;
```

Sorts by price from lowest to highest.

  

# DESC

DESC means descending order.

Example:

```sql
SELECT * FROM Orders
ORDER BY price DESC;
```

Sorts from highest to lowest.
 

# Combining SQL Clauses

SQL statements can combine multiple clauses.

Example:

```sql
SELECT *
FROM Orders
WHERE drink = 'Coffee'
ORDER BY price DESC;
```

Process:

1. Select data from Orders
2. Keep only Coffee rows
3. Sort by price (highest first)

 

# Common SQL Keywords

| Keyword  | Purpose         |
| -------- | --------------- |
| SELECT   | Choose columns  |
| FROM     | Choose table    |
| WHERE    | Filter rows     |
| ORDER BY | Sort results    |
| DESC     | Sort descending |

---
