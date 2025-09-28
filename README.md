# Library Management System Database

## Overview

This relational database supports a simple Library Management System. It manages authors, books, members, and book loans.

The design ensures data integrity with:

- Proper primary and foreign keys
- Unique constraints to eliminate duplicates
- Relationships supporting one-to-many cardinality

## Database Schema

### Tables:

- **Authors**: Stores author details.
- **Books**: Stores book details, linked to Authors.
- **Members**: Stores library members' information.
- **Loans**: Records loans of books to members including loan and return dates.

### Relationships:

1. **One-to-Many: Authors to Books**
   - An author can write many books.
2. **One-to-Many: Members to Loans**
   - A member can have multiple active or past loans.
3. **One-to-Many: Books to Loans**
   - A book can be loaned many times but only once at a time.

## ER Diagram Description

- **Authors** (AuthorID PK)  
  └───<writes>───► **Books** (BookID PK, AuthorID FK)

- **Members** (MemberID PK)  
  └───<borrows>───► **Loans** (LoanID PK, MemberID FK, BookID FK)

- **Books** (BookID PK)  
  └───<loaned in>───► **Loans** (LoanID PK, BookID FK, MemberID FK)

## Running the SQL Script

To create the database and tables, run the provided `LibraryDB.sql` file in your MySQL environment.

# Library-Management-System

Make sure to replace `Vikhtaryan` with your MySQL user.

---

## Contact

For questions or suggestions, contact victornjoro1368@gmail.com.

