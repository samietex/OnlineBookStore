## Online Bookstore Database Documentation

![](./Bookstore%20Database%20Cover.png)

### Introduction
The Online Bookstore Database is designed to manage information related to books, authors, customers, orders, and reviews for an online bookstore. This documentation outlines the database schema, constraints, and provides sample SQL queries to perform various tasks.

### Database Schema
![The All About Online Bookstore Database ERD](Database%20ERD.png)



The database consists of the following tables:

**1. Books:**
    
* Attributes: ISBN, title, publication year, price, genre
* Relationships: Multiple authors per book

**2. Authors:**
    
* Attributes: Author ID, name, biography

**3. Customers:**

* Attributes: Customer ID, name, email, address

**4. Orders:**

* Attributes: Order ID, customer ID, order date, total price
* Relationships: Multiple books per order

**5. Reviews:**

* Attributes: Review ID, customer ID, book ISBN, rating, comments

### Constraints

* **Primary Keys:**
  * Each table has a primary key (e.g., Book ISBN, Author ID, Customer ID, etc.).
* **Foreign Keys:**
  * Relationships between tables are established using foreign keys (e.g., Customer ID in Orders references Customers).
* **Unique Constraints:**
  * Ensure uniqueness of attributes (e.g., unique ISBN for each book).
* **Not Null Constraints:**
  * Essential attributes cannot be null (e.g., book title, author name).
* **Check Constraints:**
  * Validate data (e.g., rating must be between 1 and 5).

### Sample Data
* Insert sample data into the tables to populate them.
* Use SQL `INSERT INTO` statements to add records.

### SQL Queries

**1. Update Book Prices:**

* Use UPDATE statements to modify book prices.

**2. Retrieve Books Published in a Specific Year:**

* Use SELECT with a WHERE clause to filter by publication year.

**3. Retrieve Orders by a Particular Customer:**

* Join Orders and Customers tables using customer ID.

**4. Calculate Total Amount Spent by Each Customer:**

* Aggregate total price per customer using SUM.

**5. Retrieve Highest-Rated Book:**
* Use MAX to find the highest rating.

**6. Authors by Genre:**
* Join Books and Authors tables to filter by genre.

**7. Customers with Most Reviews:**

* Count reviews per customer and sort.

**8. Average Rating by Author:**

* Group by author and calculate average rating.

**9. Books with Price Higher Than Genre Average:**

* Compare book prices with average genre price.

**10. Customers Ordering Specific Author’s Books:**
* Join Orders, Customers, and Books tables.

**11. Books with Ratings Higher Than Yearly Average:**
* Compare book ratings with average for the same year.
