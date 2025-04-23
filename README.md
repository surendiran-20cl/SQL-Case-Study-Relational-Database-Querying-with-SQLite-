# SQL Case Study 2 – Relational Database Querying with SQLite in Google Colab

This repository contains the full implementation of SQL Case Study 2 using SQLite in a Google Colab environment. The project replicates a relational database schema and performs end-to-end SQL operations including table creation, data insertion, and complex querying.

## Overview

The project demonstrates:

- Creation of normalized tables representing employees, jobs, departments, and locations.
- Data manipulation using basic SQL statements.
- Advanced querying techniques including:
  - **WHERE** filters and pattern matching
  - **ORDER BY** sorting
  - **GROUP BY** aggregation with **HAVING** filters
  - **INNER JOINs** across related tables
  - **Conditional logic** using `CASE` expressions
  - **Scalar and correlated subqueries**
- Practical examples of SQL logic used in enterprise-level data systems.

## Technologies Used

- **SQLite** (via Python's `sqlite3` module)
- **Google Colab** (for Jupyter-style interactive querying)
- **Pandas** (for tabular result display)

## Database Schema

Four tables were defined and populated as per the case study:

1. **LOCATION**  
   - `Location_ID` (Primary Key)  
   - `City`

2. **DEPARTMENT**  
   - `Department_Id` (Primary Key)  
   - `Name`  
   - `Location_Id` (Foreign Key → LOCATION)

3. **JOB**  
   - `Job_ID` (Primary Key)  
   - `Designation`

4. **EMPLOYEE**  
   - `Employee_Id` (Primary Key)  
   - `First_Name`, `Last_Name`, `Middle_Name`  
   - `Job_Id` (Foreign Key → JOB)  
   - `Hire_Date`, `Salary`, `Comm`, `Department_Id` (Foreign Key → DEPARTMENT)

## Project Sections

The project is organized into the following logical sections:

### 1. Table Creation and Data Insertion
- Schema creation for all tables using `CREATE TABLE` statements
- Sample records inserted using `INSERT INTO` and `executemany`

### 2. Simple Queries
- `SELECT` statements to retrieve complete and partial records
- Use of aliases and string concatenation

### 3. Filtering with WHERE Clause
- Logical operators: `=`, `BETWEEN`, `IN`, `LIKE`, `IS NULL`
- Range and pattern-based filtering

### 4. Sorting with ORDER BY
- Single and multi-column ordering
- Ascending and descending sorts

### 5. Aggregation with GROUP BY and HAVING
- Use of `COUNT`, `AVG`, `MAX`, `MIN`, and `SUM`
- Filtering grouped records using `HAVING`

### 6. Joins
- `INNER JOIN` between EMPLOYEE, DEPARTMENT, LOCATION, and JOB
- Cross-table querying for detailed relational insights

### 7. Conditional Statements
- Salary-based grading using `CASE`
- Grouping by conditional values

### 8. Subqueries
- Scalar and nested subqueries
- Correlated subqueries comparing row-level metrics (e.g., departmental salary average)
- `UPDATE` with subquery-driven logic

## How to Use

1. Open the provided notebook (`.ipynb`) in [Google Colab](https://colab.research.google.com/)
2. Execute all cells sequentially
3. Modify or extend queries for additional practice

## Use Cases

- SQL learning and practice for data science and analytics roles
- Interview preparation for relational database concepts
- Academic or training program assignments

## License

This project is developed as part of the Intellipaat SQL Certification Program. All sample data and structure are for educational purposes only.

---

**Author:** Surendiran   
**Platform:** Intellipaat Certification Project  
**Environment:** Google Colab (Python + SQLite)

