Ecommerce Database Backup & Recovery System (PostgreSQL DBA Project)
🧠 Project Overview

This project demonstrates a real-world Database Administration (DBA) workflow using PostgreSQL, focusing on:

Database design and relational schema creation
Data insertion and management
Backup generation using pg_dump
Disaster simulation (data loss scenario)
Database recovery using restore mechanisms
Validation of data integrity after recovery

The goal is to simulate a production-like database environment and demonstrate essential DBA skills such as backup, recovery, and system reliability management.

🎯 Key Objectives
Design a normalized relational database structure
Implement real-world e-commerce schema
Perform full database backup
Simulate accidental data loss
Restore database from backup
Validate system recovery and data consistency
🛠️ Tech Stack
PostgreSQL
SQL (DDL + DML)
pgAdmin 4
Command Line Tools (pg_dump, psql)
Windows OS (development environment)
🧱 Database Schema

The system consists of 4 main relational tables:

👤 users
Stores customer information
📦 products
Stores product inventory details
🧾 orders
Stores customer orders
🔗 order_items
Stores order-product relationships
Relationship Flow:
users → orders → order_items → products

Project Structure
ecommerce-dba-backup-recovery/
│
├── database/
│   ├── schema.sql
│   ├── seed_data.sql
│
├── backup/
│   ├── ecommerce_backup.sql
│   ├── backup_commands.txt
│
├── recovery/
│   ├── disaster_simulation.sql
│   ├── restore_commands.txt
│
├── scripts/
│   ├── full_setup.sql
│   ├── verify_data.sql
│
├── screenshots/
│   ├── tables_created.png
│   ├── data_inserted.png
│   ├── backup_success.png
│   ├── restore_success.png
│
└── docs/
    ├── architecture.md
    ├── rpo_rto_explanation.md

    How to Run This Project
1️⃣ Create Database
CREATE DATABASE ecommerce_db;

Run Schema Script
schema.sql

Insert Sample Data
seed_data.sql

Verify Data
SELECT * FROM users;
SELECT * FROM products;
SELECT * FROM orders;
SELECT * FROM order_items;

Backup Process

Database backup is created using PostgreSQL utility:
pg_dump -U postgres ecommerce_db > ecommerce_backup.sql
This generates a full database dump for recovery purposes.

Disaster Simulation

To simulate a real-world failure scenario:
DROP TABLE orders;
DROP TABLE order_items;
This represents accidental data loss or system failure.

Recovery Process

Database is restored using:
psql -U postgres ecommerce_db < ecommerce_backup.sql
After recovery, all tables and data are restored successfully.

Key DBA Concepts Demonstrated
✔ Backup & Recovery

Ensures data safety and system resilience.

✔ Disaster Simulation

Tests real-world failure scenarios.

✔ Data Integrity

Ensures consistency after recovery.

✔ Relational Database Design

Proper normalization and relationships.

Skills Demonstrated
PostgreSQL Database Management
SQL Schema Design
Data Backup & Restore Operations
Disaster Recovery Planning
Database Integrity Validation
Command Line Database Operations


Project Evidence

Screenshots included in /screenshots folder:
Database schema creation
Data insertion results
Backup success confirmation
Recovery success confirmation


Why This Project Matters

This project simulates real DBA responsibilities found in enterprise environments:

Preventing data loss
Ensuring business continuity
Managing database failures
Maintaining system reliability
It reflects production-level thinking, not just academic SQL practice.

Author

Tania Aktar Zhuma
Aspiring Database Administrator | SQL | PostgreSQL | Data Systems