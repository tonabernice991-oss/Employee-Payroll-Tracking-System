# Employee Payroll Tracking System

## 📌 Project Overview
The **Employee Payroll Tracking System** is designed to manage employee information, salary structures, and monthly payroll records within an organization.  
Many companies struggle with payroll errors, delayed payments, and poor record management when using manual or spreadsheet-based systems.  

This project focuses on designing and implementing a **relational database using MySQL** to accurately calculate, store, and track employee payroll data.

## 🛠️ Tools & Technologies
- **MySQL** – Database engine
- **SQL (Structured Query Language)** – Query language
- **MySQL Workbench** – Database design and management
- **GitHub** – Version control and collaboration
- **ER Diagram Tool (Draw.io / Lucidchart)** – Database schema visualization

## 📂 Repository Structure
-  → Documentation, ER diagrams, schema design notes
-  → SQL scripts for table creation, sample data, and queries
-  → Example database configuration file
-  → Payroll calculation logic and stored procedures

## ⚙️ Features
- Employee information management (ID, name, department, role)
- Salary structure definition (basic pay, allowances, deductions)
- Monthly payroll calculation and record storage
- Error reduction through relational database design
- Easy retrieval of payroll history

## ❗ Problem Statement
Organizations must ensure that employees are paid accurately and on time.  
Without a structured payroll database, companies face:
- Salary miscalculations  
- Inconsistent payroll records  
- Difficulty tracking deductions and allowances  
- Limited payroll reporting  

This project aims to create a **reliable payroll tracking system** that eliminates these challenges.

Here is a **clean explanation you can post directly in your GitHub README** under a section like **📚 Project Explanation**. It is written in a **clear academic style teachers expect** but still simple.

---

# 📚 Project Questions / Tasks Explanation

## 1️⃣ Database Model

### Why a Relational Database is Suitable 

A **relational database** is suitable for an employee payroll system because it organizes data into structured tables that are connected through relationships. This structure makes it easy to store, retrieve, and manage payroll information efficiently.

In a payroll system, different types of data must be managed, such as employee information, salary details, and payment records. A relational database allows these different types of data to be stored in separate tables while maintaining connections between them.

Using a relational database also provides several advantages:

* ✔️ Reduces data redundancy
* ✔️ Improves data consistency
* ✔️ Makes payroll calculations more accurate
* ✔️ Allows efficient data retrieval using SQL queries
* ✔️ Ensures better data organization

Relational databases such as **MySQL** are widely used in organizations because they support structured data management and strong data integrity.

### How Tables, Relationships, and Constraints Ensure Payroll Accuracy

#### Tables

Tables are used to store different categories of information.
For example:

* **Employees table** → stores employee personal details
* **Salary table** → stores salary structure information
* **Payroll table** → stores salary payment records

Separating data into tables helps avoid duplication and makes the database easier to manage.

#### Relationships

Relationships connect tables using **primary keys** and **foreign keys**.

Example:

* One employee can have **many payroll records**
* Payroll records must reference a **valid employee**

These relationships ensure that payroll records always belong to a valid employee.

#### Constraints

Constraints are rules that maintain the accuracy and reliability of data.

Common constraints include:

* **Primary Key** → uniquely identifies each record
* **Foreign Key** → ensures valid relationships between tables
* **NOT NULL** → prevents missing important data
* **UNIQUE** → prevents duplicate entries

### Attributes of Each Entity

#### Employee Entity

Attributes:

* Employee_ID (Primary Key)
* First_Name
* Last_Name
* Department
* Position
* Hire_Date
* Email
* Phone_Number

#### Salary Entity

Attributes:

* Salary_ID (Primary Key)
* Employee_ID (Foreign Key)
* Basic_Salary
* Allowances
* Deductions

#### Payroll Entity

Attributes:

* Payroll_ID (Primary Key)
* Employee_ID (Foreign Key)
* Salary_ID (Foreign Key)
* Pay_Date
* Net_Salary

### Relationships Between Entities

The relationships between the entities are:

* One **Employee** can have **one salary structure**
* One **Employee** can have **many payroll records**

An **Entity Relationship Diagram (ERD)** can be created using tools such as **Draw.io** or **Lucidchart** to visually represent these relationships.

# 3️⃣ Normalization

### Why Normalization Is Required

**Normalization** is the process of organizing database tables to reduce redundancy and improve data integrity.

The main goals of normalization are:

* ✔️ Eliminate duplicate data
* ✔️ Improve database efficiency
* ✔️ Ensure logical data organization
* ✔️ Prevent data anomalies

Normalization divides large tables into smaller related tables.

### First Normal Form (1NF)

A table is in **First Normal Form** when:

* Each field contains **atomic values** (no multiple values in one column)
* Each record can be uniquely identified

Example improvement:

Separate repeating salary entries from employee details.

### Second Normal Form (2NF)

A table is in **Second Normal Form** when:

* It is already in **1NF**
* All non-key attributes depend on the **entire primary key**

To achieve 2NF, employee details are separated from payroll records.

Tables created:

* **Employees Table**
* **Payroll Table**

### Third Normal Form (3NF)

A table is in **Third Normal Form** when:

* It is already in **2NF**
* There are **no transitive dependencies** (non-key attributes should not depend on other non-key attributes)

For example:

Salary details are stored in a separate **Salary table** instead of inside the Payroll table.

Final normalized tables:

* Employees
* Departments
* Payroll

This structure ensures:

✔️ Reduced redundancy
✔️ Better data integrity
✔️ Accurate payroll calculations
✔️ Easier database maintenance

### Here is an example that applies these 9 queries:

1. Create the database employee_payroll_db.
2. Create all tables with proper primary and foreign keys.
3. Insert the sample data into each table.
4. Retrieve all employees from a specific department.
5. Calculate net salary using base salary, allowances, and deductions.
6. Display payroll details for a specific month.
7. Update an employee’s base salary.
8. Delete a payroll record using payroll_id.
9. Use JOINs to display employee names, department names, and net salaries.

👉 **Click here to view the queries for better understanding:https://1drv.ms/w/c/c6767e1f5b535938/IQAuPLMeLNRmR46HtlIrdV8EAaUgKyUJE6wq_rNIxMe9l68?e=sNAsI2**

🧕**Author:**
**TONA**
## THANK YOU







