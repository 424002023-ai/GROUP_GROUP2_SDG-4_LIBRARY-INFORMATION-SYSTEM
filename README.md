Project Title and SDG Goal
Library Management System (LMS) — Supporting SDG 4: Quality Education

This project supports UN Sustainable Development Goal 4 (SDG 4): Quality Education, specifically addressing the challenge of providing equitable access to learning resources, reducing borrowing delays, and enabling data-driven monitoring of library usage.

Project Description

The Library Management System is designed to manage books, members, borrowing transactions, inventory, and reporting operations using a structured RDBMS schema.

This project demonstrates mastery of core DBMS concepts, including:

- Data Definition Language (DDL)

Normalized schema design using 5 core entities (Books, Categories, Members, Inventory, Borrowings)

Constraints: CHECK, PRIMARY KEY, FOREIGN KEY, UNIQUE

Indexing for optimized searching and joins

- Data Manipulation Language (DML)

50+ INSERT statements for books, members, inventory, borrowings, and categories

- Stored Logic (Procedures, Triggers, Views)

Stored Procedure: borrow_book

Automates borrowing with ACID-compliant transaction control

Checks stock availability and updates inventory

Trigger: Prevents negative inventory values

Views:

v_category_demand → Borrowing frequency by category

v_most_borrowed → Top borrowed books

v_overdue_members → Members with overdue books

- Data Control Language (DCL)

User creation and role-based access (librarian vs viewer)

The system ensures that educational institutions can track book usage, prevent over-borrowing, maintain accurate inventory, and generate insights that improve learning resource allocation.

- Installation / Setup Instructions

Follow these steps to set up the database on MariaDB / MySQL:

1. Clone the Repository
git clone https://github.com/your-org/GROUP_NAME_SDG_PROJECT.git
cd GROUP_NAME_SDG_PROJECT

2. Open MySQL or MariaDB
mysql -u root -p

3. Create the Database
CREATE DATABASE library_sdg4;
USE library_sdg4;

4. Run SQL Scripts in Correct Order

Inside the 1_SQL_SCRIPTS folder:

1.1_DDL_Schema.sql – creates tables, constraints

1.2_DML_TestData.sql – inserts sample data

1.3_StoredLogic.sql – procedures, triggers, and views

1.4_DCL_Users.sql – creates DB users and permissions

You may run them via MySQL CLI:

SOURCE 1_SQL_SCRIPTS/1.1_DDL_Schema.sql;
SOURCE 1_SQL_SCRIPTS/1.2_DML_TestData.sql;
SOURCE 1_SQL_SCRIPTS/1.3_StoredLogic.sql;
SOURCE 1_SQL_SCRIPTS/1.4_DCL_Users.sql;


OR via phpMyAdmin / MySQL Workbench (import individually).

- Usage Instructions (Demo CLI Application)

The 2_DEMO_INTERFACE folder contains the CLI app that demonstrates the system’s main features.



1. Expected Output Examples

When borrowing a book:

Automatic transaction control

Inventory decrement

Error message if no copies available

When checking overdue books:

List returned using SQL view

The CLI acts as a simulation of basic librarian functions for the project demonstration.

2. Contributors
Member Name	Role / Contribution
Ardales, Ma. Jaslene O Normalization 3NF/BCNF (MIDTERM)
Gabriel, Sam Jared G. Trigger (FINALS)
Manalac, John Paul ERD (MIDTERM)
Nabayat, CharisseComplex DQL (PRELIM) Rabino, Ezekiel Kent A
Stored Procedure (FINALS)
