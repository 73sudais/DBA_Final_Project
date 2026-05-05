# DBA_Final_Project
Personal Expense Tracker is a SQL-based project that manages user expenses with categories, budgets, and transactions. It uses normalized tables (3NF), primary/foreign keys, sequences, triggers, views, joins, and aggregation to track and analyze spending efficiently in Oracle SQL.

## 💰 Personal Expense Tracker (SQL Project)
### 📌 Overview

The Personal Expense Tracker is a database project designed to manage and analyze user expenses. It helps track income and spending by organizing data into users, categories, transactions, and budgets.

This project is built using Oracle SQL with proper normalization, relationships, and advanced SQL features like joins, views, triggers, and aggregation.

## 🛠️ Technologies Used

Oracle SQL
SQL Developer
PL/SQL (Triggers & Sequences)

## 📊 Features
👤 User management system
🏷️ Category-based expense tracking
💸 Transaction recording system
📅 Monthly budget management
📈 Expense summary and reporting
🔗 Relational database design (3NF)

## 🧱 Database Structure

Tables
Users
Categories
Transactions
Budgets
Key Concepts Used
Primary Keys (PK)
Foreign Keys (FK)
Sequences
Triggers
Views
Joins
Aggregation (SUM, GROUP BY)

## 🔗 Relationships

One user → Many transactions
One category → Many transactions
One user → Many budgets
One category → Many budgets

## 📊 Example Query

SELECT 
    c.category_name,
    SUM(t.amount) AS spent,
    b.limit_amount
FROM transactions t
JOIN categories c ON t.category_id = c.category_id
LEFT JOIN budgets b ON b.category_id = c.category_id
GROUP BY c.category_name, b.limit_amount;

## 🚀 How to Run

Open Oracle SQL Developer
Create a new database connection
Run SQL scripts in order:
Table creation
Sequences & triggers
Insert data
Views & queries

## 🎯 Learning Outcomes

Database design in 3NF
Writing complex SQL queries
Understanding relationships between tables
Practical use of PL/SQL triggers and sequences
