# 🔥 Project Phoenix: Database Migration Engine

### "Because manual DB management is a disaster waiting to happen."

## 📌 Overview
This project is part of the DevOps Course. It demonstrates how to treat Database Infrastructure as Code (IaC). Instead of creating tables manually, we use Python-based versioned migrations to build and update our SQL Server schema.



## 🛠️ Tech Stack
* **Language:** Python 3.x
* **Database:** Microsoft SQL Server
* **Library:** `pyodbc`
* **Automation:** GitHub Actions (Coming Soon)

## 📁 Project Structure
- `db_scripts/`: Contains versioned SQL migration files (001, 002...).
- `src/migrate.py`: The execution engine that applies scripts to the DB.
- `requirements.txt`: Project dependencies.

## 🚀 Getting Started

### 1. Prerequisites
Make sure you have the **ODBC Driver for SQL Server** installed on your machine.

### 2. Installation
Clone the repo and install dependencies:

pip install -r requirements.txt
3. Configuration
Open src/migrate.py and update the DB_CONFIG dictionary with your local SQL Server credentials:

server: Your server address (e.g., localhost or .\SQLEXPRESS)

database: Your target DB name

user/password: Your credentials

4. Running Migrations
Execute the following command to apply all pending scripts:


python src/migrate.py
⚠️ The "Disaster" Scenario
If the production database is deleted:

Create a new empty database.

Run this project.

Your entire schema (Tables, Indexes, Constraints) will be restored in seconds.