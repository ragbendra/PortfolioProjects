# Hospital Management Database

## Overview
This project is a simple SQL database for a hospital management system. It helps keep track of patients, doctors, appointments, medical records, and schedules in an organized way. Think of it as a digital filing system for a hospital.

## Purpose
The goal is to create a database that makes it easy to store and manage hospital information, like who the patients are, which doctors are available, when appointments happen, and what medical treatments are needed.

## What’s in the Database
The database is called `hospital_management` and includes a few tables to store different kinds of information. There’s also a mention of a `user_login` table from another system (`online_retail_app`), which might be used for user accounts.

### Tables
1. **user_login** (from `online_retail_app`)
   - Keeps user account details like ID, password, name, sign-up date, and email.
   
2. **patient**
   - Stores patient info like email, password, name, address, and gender.

3. **medical_history**
   - Tracks a patient’s medical past, like dates, health conditions, surgeries, and medicines.

4. **doctor**
   - Holds doctor details like email, gender, password, and name.

5. **appointment**
   - Manages appointment info, including date, start time, end time, and status (e.g., "Scheduled").

6. **patient_visits**
   - Records details of patient visits, like the patient’s email, appointment ID, concerns, and symptoms.

7. **schedule**
   - Stores general schedules, like what times and days are available, including break times.

8. **patients_history**
   - Links patients to their medical history records.

9. **diagnose**
   - Saves diagnoses and prescriptions from appointments, tied to a doctor and appointment.

10. **doctor_schedules**
    - Connects doctors to their specific schedules.

11. **doctor_view_history**
    - Tracks which doctors have looked at a patient’s medical history.

## How to Set It Up
1. **Get a Database Tool**: Use a tool like PostgreSQL to run the database.
2. **Run the SQL Code**:
   - Copy the SQL code into your database tool.
   - Run it to create the `hospital_management` database and all the tables.
   - Note: The `user_login` table is part of another system (`online_retail_app`). If you don’t need it, you can skip that part or create that schema first.
3. **Check the Tables**: Make sure all tables are created correctly.
4. **Add Some Data**: Try adding sample data to test it out.

## How to Use It
- **Add Patients**: Store patient details in the `patient` table.
- **Manage Doctors**: Add doctor info to the `doctor` table and set their schedules in `doctor_schedules`.
- **Book Appointments**: Use the `appointment` table to schedule visits and link them to patients in `patient_visits`.
- **Track Medical Info**: Save diagnoses in `diagnose` and medical histories in `medical_history`.
- **Monitor Access**: Use `doctor_view_history` to see which doctors check patient records.

## Example Actions
1. **Add a Patient**:
   ```sql
   INSERT INTO hospital_management.patient (email, password, name, address, gender)
   VALUES ('jane.smith@example.com', 'abc123', 'Jane Smith', '456 Oak St', 'Female');
   ```

2. **Book an Appointment**:
   ```sql
   INSERT INTO hospital_management.appointment (appointment_id, date, start_time, end_time, status)
   VALUES (1, '2025-06-01', '10:00:00', '10:30:00', 'Scheduled');
   ```

3. **Record a Patient Visit**:
   ```sql
   INSERT INTO hospital_management.patient_visits (patient, appt, concerns, symptoms)
   VALUES ('jane.smith@example.com', 1, 'Cough', 'Sore throat');
   ```

## Summary
This hospital management database is a simple way to organize hospital data. It helps manage patients, doctors, appointments, and medical records, making it easier to run a hospital smoothly. It’s a great starting point for building a full hospital management system!