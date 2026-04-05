# Zorvyn-Finance-Data-Processing-and-Access-Control-Backend
This project is a backend system for a finance dashboard where different users interact with financial records based on their role.

Name: Kanishka Mandrawliya
Email ID: kanshka0628@gmail.com
Linkedin: https://www.linkedin.com/in/kanishka-m-2a17a8229/
Phone no: 8408973870


# Finance Data Processing and Access Control Backend

A backend API for a finance dashboard system with role-based access control, financial record management, dashboard analytics, JWT authentication, and SQLite persistence.


## Overview

This project was built as a backend assignment for a finance dashboard system where different users interact with financial records based on their assigned role.

The system supports:

- User and role management
- Active/inactive user status
- Financial record CRUD operations
- Record filtering
- Dashboard summary and analytics APIs
- Role-based access control
- Input validation and error handling
- Persistent storage using SQLite

In addition to the core requirements, the project also includes optional enhancements such as JWT authentication, Swagger API documentation, seed data, and basic automated tests.

---

## Tech Stack

- **Language:** Python
- **Framework:** FastAPI
- **Database:** SQLite
- **ORM:** SQLAlchemy
- **Validation:** Pydantic
- **Authentication:** JWT
- **Testing:** Pytest
- **Documentation:** Swagger UI / OpenAPI

---

## Why This Stack

### FastAPI
FastAPI was chosen because it provides:
- clean and fast REST API development
- built-in validation with Pydantic
- automatic Swagger/OpenAPI docs
- readable and maintainable structure

### SQLite
SQLite was used because:
- it is lightweight
- it requires no separate installation
- it is ideal for local development and assignment evaluation
- it keeps setup simple

### SQLAlchemy
SQLAlchemy was used to:
- define models cleanly
- manage database operations through ORM
- keep the data layer organized and extensible

### JWT Authentication
JWT was added to support:
- token-based authentication
- secure access to protected APIs
- role-based access control at backend level

---

## Features Implemented

- User and role management
- Demo user seeding
- Active/inactive user status handling
- JWT-based authentication
- Financial record creation, reading, updating, and deletion
- Record filtering by type, category, and date
- Dashboard summary APIs
- Category-wise totals
- Recent activity endpoint
- Monthly trend endpoint
- Role-based access control
- Input validation and structured error handling
- SQLite database persistence
- Swagger API documentation
- Basic automated tests

---

## Role Model

The project supports the following roles:

### Viewer
- Can view allowed data
- Can access dashboard information
- Cannot create, update, or delete records
- Cannot manage users

### Analyst
- Can read financial records
- Can access dashboard insights and summaries
- Cannot manage users
- Cannot perform full administrative actions

### Admin
- Full access to user management
- Full access to record management
- Can create, update, and delete records
- Can create users and update user status

### Inactive User
- Marked inactive in the database
- Blocked from protected backend actions

---

## Project Structure

```text
finance_backend_assignment/
├── app/
│   ├── __init__.py
│   ├── auth.py
│   ├── db.py
│   ├── dependencies.py
│   ├── main.py
│   ├── models.py
│   ├── schemas.py
│   ├── seed.py
│   └── routes/
│       ├── dashboard.py
│       ├── records.py
│       └── users.py
├── tests/
│   └── test_app.py
├── finance_dashboard.db
├── requirements.txt
└── README.md
