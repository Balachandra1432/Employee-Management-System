📂 Employee Management System (SQL Project)
📌 Project Overview

This project is a SQL-based Employee Management Database designed to simulate a company’s HR system. It includes multiple interconnected tables such as regions, countries, locations, departments, jobs, employees, and dependents, along with sample data and queries.

The project demonstrates database design, normalization, foreign key constraints, and SQL queries for retrieving meaningful insights.

🏗️ Database Schema

Main Entities:

Regions – Defines geographical regions (Europe, Americas, Asia, etc.)

Countries – Countries belonging to regions

Locations – Office addresses tied to countries

Departments – Departments within company locations

Jobs – Job roles with salary ranges

Employees – Employee details with job, department, and manager relationships

Dependents – Family dependents of employees


🔑 Features Implemented

Created normalized relational schema with PK, FK, and cascading constraints.

Inserted sample company data (employees, jobs, departments, etc.).

Wrote SQL queries for:

Fetching employee details and salaries.

Joining employees with their departments and jobs.

Filtering employees by salary, job title, or department.

Displaying dependents of specific employees.

📊 Sample Queries
1. Retrieve all employee names and their salaries
```
SELECT first_name, last_name, salary 
FROM employees;
```
2. Show job title and salary range of each job
```
SELECT job_title, min_salary, max_salary 
FROM jobs;
```
3. List employees working in the IT department
```
SELECT e.first_name, e.last_name, d.department_name 
FROM employees e
JOIN departments d ON e.department_id = d.department_id
WHERE d.department_name = 'IT';
```
4. Find employees earning more than 10,000
```
SELECT * FROM employees 
WHERE salary > 10000;
```
🛠️ Tech Stack

Database: MySQL / SQL

Concepts Used: DDL, DML, Joins, Primary Key, Foreign Key, Cascade Constraints, Normalization

🚀 How to Run

Clone this repository:

git clone https://github.com/YourUsername/employee-management-sql.git


Open MySQL Workbench / SQL CLI.

Run the script:

SOURCE company_database.sql;


Explore tables and queries.

📌 Author

👤 Bala Chandra

📧 pasupulabalachandra1432@gmail.com
