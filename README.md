# UPSC-2025-registration-system-using-python
The UPSC Registration System is a lightweight, educational application implemented in Python with a MySQL backend.  The project is designed as a learning prototype to practice problem solving, programming fundamentals, and database connectivity.
# UPSC Registration System (Python + MySQL)

A simple Python-based UPSC Registration System using MySQL for storing and retrieving candidate information.

Author: Pranav Pathak  
Registration No.: 25BCE10975  
VIT Bhopal University — 1st Semester, 1st Year  
Flipped Course Project: Problem Solving and Programming

---

## Project Overview

This project provides a basic command-line UPSC registration system that demonstrates how to collect, store, retrieve, update, and delete candidate information using Python as the application layer and MySQL as the database backend. It is intended as a learning project for database connectivity, CRUD operations, and basic input validation.

Key features:
- Add new candidate records
- View all candidates
- Search candidate by registration ID or name
- Update candidate information
- Delete candidate records
- Uses MySQL to persist data
- Simple, modular Python code suitable for extension

---

## Tech Stack

- Python 3.x
- MySQL (or MariaDB)
- mysql-connector-python (or an equivalent MySQL driver)

---

## Prerequisites

Make sure you have the following installed on your system:

- Python 3.8+
- MySQL Server
- Python package: mysql-connector-python (or mysqlclient/pymysql if you prefer and adjust code accordingly)

Install the Python package with:

pip install mysql-connector-python

---

## Database Setup

1. Start your MySQL server.
2. Create a database (example name: upsc_registration) and a user, or use an existing one.

Example SQL to create the database and table:

CREATE DATABASE IF NOT EXISTS upsc_registration;
USE upsc_registration;

CREATE TABLE IF NOT EXISTS candidates (
    reg_id INT AUTO_INCREMENT PRIMARY KEY,
    full_name VARCHAR(255) NOT NULL,
    dob DATE NOT NULL,
    email VARCHAR(255),
    phone VARCHAR(20),
    address TEXT,
    applied_exam VARCHAR(100),
    registration_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

Adjust the table schema to match fields used in the Python code.

3. Update the database connection settings in the Python configuration or the script (host, user, password, database).

---

## Running the Application

1. Clone the repository:

git clone https://github.com/prapathaknavnirman-talentx/upsc-registration-system-using-python-and-mysql.git
cd upsc-registration-system-using-python-and-mysql

2. Ensure the database is created and the table exists (see Database Setup).

3. Edit the configuration or connection constants in the main Python file (e.g., db_config or connection parameters).

4. Run the main script:

python main.py

Follow the command-line prompts to add, view, search, update, or delete candidate records.

---

## Project Structure (example)

- main.py              - Entry point and CLI menu
- db.py                - Database connection utilities
- models.py            - Candidate model and CRUD operations
- config.py            - Database connection configuration
- README.md
- PROJECT_REPORT.md    - Formal project report

Your repository may vary; adjust according to your specific file names.

---

## Notes & Extensions

This project is designed for learning. Suggested improvements:
- Add form validation and stronger input sanitization
- Implement a GUI (Tkinter, PyQt) or a web interface (Flask/Django)
- Add role-based access or authentication
- Add export/import (CSV) and reporting features
- Use ORM (SQLAlchemy) for more portability

---

## License

This project is for educational purposes. Feel free to reuse or modify the code for learning and coursework, but consult your institution's rules for academic submissions.

---

## Author & Course Information

Pranav Pathak  
Registration No.: 25BCE10975  
VIT Bhopal University — 1st Semester, 1st Year  
Flipped Course Project: Problem Solving and Programming

If you need the README tailored to specific filenames or code snippets from your repo, send the file names and I will insert exact usage instructions.
