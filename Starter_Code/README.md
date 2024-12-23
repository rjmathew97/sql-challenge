# Module 9 Challenge: SQL Employee Database

## **Overview**
This project involves creating and analyzing an employee database using SQL. The challenge covers:
1. Data modeling to design an Entity Relationship Diagram (ERD) for the database
2. Data engineering to create table schemas, define constraints and import data from CSV files.
3. Data analysis to answer questions using SQL queries.

## **Technologies Used**
- SQL (PostgreSQL and PgAdmin)
- QuickDBD for ERD creation
- CSV files of data input

sql-challenge/
    EmployeeSQL/
│       Data/               # CSV files for data import
│       challengeschema.sql # SQL script for creating database schema
│       queries.sql         # SQL queries for data analysis
│       README.md           # Project documentation (this file)
│       ERD/                # ERD diagram image

## **Entity Relationship Diagram (ERD)**
The ERD illustrates the relationships between the tables in the database. It includes:
- `employees`
- `titles`
- `salaries`
- `departments`
- `dept_manager`
- `dept_emp`

![ERD] /Users/Rosy/Desktop/Class_Requirements/Bootcamp Assignment/gitSqlChallenge/sql-challenge/Starter_Code/data/QuickDBD-export.png

## **Setup Instructions**
1. **Clone the Repository:**
   ```bash
   git clone https://github.com/rjmathew97/sql-challenge.git
   cd sql-challenge/EmployeeSQL

2. **Create the Database:**
CREATE DATABASE Mod09ChallengeDB;

3. **Run the Schema Script:** 
\i challengeschema.sql

3. **Import the Data:** 
COPY titles (title_id, title)
FROM '/Users/Rosy/Desktop/Class_Requirements/Bootcamp Assignment/gitSqlChallenge/sql-challenge/Starter_Code/data/titles.csv'
DELIMITER ',' CSV HEADER;

COPY employees (emp_no, emp_title_id, birth_date, first_name, last_name, sex, hire_date)
FROM '/Users/Rosy/Desktop/Class_Requirements/Bootcamp Assignment/gitSqlChallenge/sql-challenge/Starter_Code/data/employees.csv'
DELIMITER ',' CSV HEADER;

COPY departments (dept_no, dept_name)
FROM '/Users/Rosy/Desktop/Class_Requirements/Bootcamp Assignment/gitSqlChallenge/sql-challenge/Starter_Code/data/departments.csv'
DELIMITER ',' CSV HEADER;

COPY dept_manager (dept_no, emp_no)
FROM '/Users/Rosy/Desktop/Class_Requirements/Bootcamp Assignment/gitSqlChallenge/sql-challenge/Starter_Code/data/dept_manager.csv'
DELIMITER ',' CSV HEADER;

COPY dept_emp (emp_no, dept_no)
FROM '/Users/Rosy/Desktop/Class_Requirements/Bootcamp Assignment/gitSqlChallenge/sql-challenge/Starter_Code/data/dept_emp.csv'
DELIMITER ',' CSV HEADER;

COPY salaries (emp_no, salary)
FROM '/Users/Rosy/Desktop/Class_Requirements/Bootcamp Assignment/gitSqlChallenge/sql-challenge/Starter_Code/data/salaries.csv'
DELIMITER ',' CSV HEADER;

5. **Run Queries:** 
Run the queries in queries.sql to analyze the data.













