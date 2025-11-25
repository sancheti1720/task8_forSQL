# Task 8 – Stored Procedures and Functions

This task teaches how to write **stored procedures** and **functions** in SQL.  
Stored routines help modularize SQL logic and make code reusable.

---

## Objective
- Learn how to create and execute stored procedures  
- Use IN and OUT parameters  
- Create SQL functions  
- Use conditional logic (IF / ELSE)  
- Return scalar values from functions  

---

## Tools Used
- MySQL Workbench / DB Browser for SQLite  
(MySQL recommended because SQLite does not support stored procedures)

---

## Database Used
Simple **Library Management System**:

- authors  
- books  
- issued_books  

These tables help students understand procedures easily.

---

## What Was Created

### ✔ Stored Procedure 1  
**getBooksByAuthor**  
Returns all books written by a specific author.

### ✔ Stored Procedure 2  
**countBooksOfAuthor**  
Uses an OUT parameter to return book count.

### ✔ SQL Function 1  
**calculatePriceWithTax**  
Adds 10% tax and returns final price.

### ✔ SQL Function 2  
**isExpensive**  
Checks whether the book price is greater than 300.

---

## How to Run

### Run a stored procedure:
```sql
CALL getBooksByAuthor('Sudha Murty');
```

### Run procedure with OUT parameter:
```sql
CALL countBooksOfAuthor('Sudha Murty', @res);
SELECT @res;
```

### Use SQL function:
```sql
SELECT title, calculatePriceWithTax(price) FROM books;
```
