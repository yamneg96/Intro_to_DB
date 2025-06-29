Apologies for that! Here's the **complete `README.md`** content with everything fully enclosed in proper Markdown code blocks as you asked:

````md
# 📚 ALX Book Store Database Project

Welcome to the **Intro_to_DB** project! This repository demonstrates the design and implementation of a MySQL database for an online bookstore. It includes schema creation, data population, and basic database operations using SQL and Python.

---

## 📁 Project Structure

```plaintext
Intro_to_DB/
│
├── alx_book_store.sql            # Full schema definition with all tables
├── MySQLServer.py                # Python script to create the database
├── task_2.sql                    # Creates all tables in the bookstore schema
├── task_3.sql                    # Lists all tables in the bookstore
├── task_4.sql                    # Prints description of the 'books' table
├── task_5.sql                    # Inserts a single customer record
├── task_6.sql                    # Inserts multiple customer records
└── README.md                     # Project description and instructions
````

---

## 🧱 Database Schema Overview

**Database Name:** `alx_book_store`

### Tables:

* `authors`

  * `author_id` (INT, PK)
  * `author_name` (VARCHAR)

* `books`

  * `book_id` (INT, PK)
  * `title` (VARCHAR)
  * `author_id` (INT, FK → authors)
  * `price` (DOUBLE)
  * `publication_date` (DATE)

* `customers`

  * `customer_id` (INT, PK)
  * `customer_name` (VARCHAR)
  * `email` (VARCHAR)
  * `address` (TEXT)

* `orders`

  * `order_id` (INT, PK)
  * `customer_id` (INT, FK → customers)
  * `order_date` (DATE)

* `order_details`

  * `orderdetailid` (INT, PK)
  * `order_id` (INT, FK → orders)
  * `book_id` (INT, FK → books)
  * `quantity` (DOUBLE)

---

## 🚀 Setup Instructions

### 🐍 Step 1: Create the Database via Python

Run the Python script:

```bash
python3 MySQLServer.py
```

This script connects to MySQL and creates the `alx_book_store` database if it doesn't already exist.

> 🔐 Make sure to replace `"your_password_here"` in the script with your actual MySQL password.

---

### 🗃 Step 2: Create All Tables

Run this SQL script to define all necessary tables:

```bash
mysql -u root -p alx_book_store < task_2.sql
```

---

### 📋 Step 3: List All Tables

```bash
mysql -u root -p alx_book_store < task_3.sql
```

---

### 🔍 Step 4: Describe `books` Table Without DESCRIBE

```bash
mysql -u root -p alx_book_store < task_4.sql
```

---

### ✍️ Step 5: Insert a Single Customer

```bash
mysql -u root -p alx_book_store < task_5.sql
```

---

### 🧑‍🤝‍🧑 Step 6: Insert Multiple Customers

```bash
mysql -u root -p alx_book_store < task_6.sql
```

---

## ✅ Sample Data Added

```sql
-- Customer 1
(1, 'Cole Baidoo', 'cbaidoo@sandtech.com', '123 Happiness Ave.')

-- Customer 2
(2, 'Blessing Malik', 'bmalik@sandtech.com', '124 Happiness Ave.')

-- Customer 3
(3, 'Obed Ehoneah', 'eobed@sandtech.com', '125 Happiness Ave.')

-- Customer 4
(4, 'Nehemial Kamolu', 'nkamolu@sandtech.com', '126 Happiness Ave.')
```

---

## 📌 Notes

* SQL keywords are written in **UPPERCASE** as required.
* All foreign keys are correctly referenced to maintain integrity.
* The project assumes `localhost`, `root` user — modify as needed.
* The scripts are reusable and fail-safe (won’t crash if entities exist).

---

## 🏁 End

Well done on completing your database journey!
Keep querying and keep building 🧠💾✨

```

Let me know if you want a PDF version or to auto-include this in your zipped project!
```
