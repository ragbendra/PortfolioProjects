# Student Management Database

## Overview
This project is a simple SQL database for managing a school’s student information. It organizes details about students, parents, teachers, classes, subjects, and who teaches what, making school administration easier.

## Purpose
The goal is to create a database that helps schools keep track of important information, like student and teacher details, class assignments, and subject tutors, in one organized place.

## What’s in the Database
The database is called `student_management` and contains several tables to store different types of school data. Here’s a quick look at what each table does:

### Tables
1. **user_login**
   - Stores user account details for the system, like ID, password, name, sign-up date, and email.

2. **parent_details**
   - Keeps information about students’ parents, including names, emails, phone numbers, and jobs for both father and mother.

3. **teachers**
   - Holds teacher details like ID, name, date of birth, email, contact number, registration date, and a unique registration ID.

4. **class_details**
   - Manages class information, including a class ID, the class teacher, and the school year.

5. **student_details**
   - Stores student info like ID, name, date of birth, class, roll number, email, parent ID, registration date, and a unique registration ID.

6. **subject**
   - Tracks subjects offered, including a subject ID, name, class year, and the teacher in charge (subject head).

7. **subject_tutors**
   - Links teachers to the subjects and classes they teach, with a unique row ID for each connection.

## How to Set It Up
1. **Get a Database Tool**: Use a tool like PostgreSQL to run the database.
2. **Run the SQL Code**:
   - Copy the SQL code into your database tool.
   - Run it to create the `student_management` database and all the tables.
3. **Check the Tables**: Make sure all tables are created with the right columns.
4. **Add Sample Data**: Try adding some data to test how it works.

## How to Use It
- **Add Students**: Store student details in the `student_details` table and link them to parents in `parent_details`.
- **Manage Teachers**: Add teacher info to the `teachers` table.
- **Set Up Classes**: Use the `class_details` table to create classes and assign class teachers.
- **Track Subjects**: Add subjects to the `subject` table and assign subject heads.
- **Assign Tutors**: Use `subject_tutors` to connect teachers to the subjects and classes they teach.

## Example Actions
1. **Add a Student**:
   ```sql
   INSERT INTO student_management.student_details (student_id, first_name, last_name, date_of_birth, class_id, roll_no, email_id, parent_id, registration_date, registration_id)
   VALUES ('S001', 'Emma', 'Brown', '2010-03-15', 'C001', '01', 'emma.brown@example.com', 'P001', '2025-01-10', 'REG001');
   ```

2. **Add a Teacher**:
   ```sql
   INSERT INTO student_management.teachers (teacher_id, first_name, last_name, date_of_birth, email_id, contact, registration_date, registration_id)
   VALUES ('T001', 'Sarah', 'Wilson', '1985-06-20', 'sarah.wilson@example.com', '555-1234', '2025-01-05', 'TREG001');
   ```

3. **Assign a Subject Tutor**:
   ```sql
   INSERT INTO student_management.subject_tutors (subject_id, teacher_id, class_id)
   VALUES ('SUB001', 'T001', 'C001');
   ```

## Summary
This student management database is a simple way to organize school data. It helps track students, parents, teachers, classes, and subjects, making it easier to manage a school. It’s a great starting point for building a full school management system!