"# database-assignment-3" 
Security and accountability are essential in any library system to ensure proper record-keeping of
member activities and inventory management. Imagine a library that manages its operations using a
SQL database.To maintain an audit trail for transparency and record-keeping, the library requires an
auditing system. To implement this, add a new entity called Audit_Log. The Audit_Log table will
store key details, such as the timestamp, the action performed (e.g., Register, Borrow, Return,
Update), and the staff member responsible for the action. Each time a library staff member performs
an operation on member or book records, an entry should automatically be saved to the Audit_Log
table.
A sample dataset is provided in the attached Excel file. Based on this data, complete the following
tasks

Part#1 – Design (35 Marks)

1. Design SQL Schema for the given dataset. Identify the Entities/Tables and corresponding
columns, constraints, and primary keys. Also, identify the relationships between different
Entities and map them through foreign keys correctly. [15Marks]
2. Using SQL queries perform following operations [20 Marks]
a. Create Database and Tables. Define Constraints, Primary Keys and Foreign Keys
b. Identify the relationships between different Entities and map them through foreign
keys correctly.

Fall 2024
Database System

FAST NUCES Islamabad
Assignment-3

Part#2 – Insertions (20 Marks)

Download the provided dataset and load it into the created tables. You can use any utility for this
purpose. Using individual insert queries for each row is not allowed (and possible) for the given
dataset. You have to understand the type of data in a column while designing the schema. You
can assume empty cells as NULL. Generate data for Audit_Log table while uploading your data
using triggers.

Part#3 – Queries (75 Marks)
Write SQL Queries to Perform Following Operations
Creating Triggers [15+20+15 Marks]
1. Insert Trigger on Members Table [15 Marks]
Create an INSERT trigger on the Members table. When a new member registers, an entry
should be saved in the Audit_Log table to record the insertion. Include details such as the
member_id, action (e.g., 'INSERT'), and a timestamp.
2. Insert and Delete Triggers on Borrowing Table [20 Marks]
Create INSERT and DELETE triggers on the Borrowing table to log book borrowing and
return actions in the Audit_Log table. Each action (borrow or return) should save details
like the borrowing_id, action (e.g., 'BORROW' or 'RETURN'), book_id, and a
timestamp.
3. Update Trigger on Books Table [15 Marks]
Create an UPDATE trigger on the Books table to log any changes to book availability in the
Audit_Log table. When a book’s availability is updated, save an entry with the book_id,
old_status, new_status, action ('UPDATE'), and a timestamp.
Operations [5+5+5+10 Marks]
1. Add a New Library Member and Assign a Library Card [5 Marks]
Add a new member to the Members table and assign them a library card. Check the
Audit_Log table to confirm that an entry was recorded. Include a snapshot of the
Audit_Log table in your report.
2. Record 4 Book Borrowing Actions for the Member [5 Marks]
Execute four different book borrowing actions by this member in the Borrowing table.
After each transaction, check the Audit_Log table to ensure each action was recorded.
Include snapshots of the Audit_Log table in your report.
3. Update Book Availability Status [5 Marks]
Update the status of a book (e.g., from available to not available) in the Books table. Check
the Audit_Log table to verify that this update was logged. Include a snapshot of the
Audit_Log table in your report.
4. Display All Borrowing Transactions for the Member [10 Marks]
Write a query to display all borrowing transactions for the specified member. The result
should include member_id, member_name, book_title, borrow_date, return_date,
status, and timestamp.
