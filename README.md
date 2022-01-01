# College-Management-System
A college management system built using the Django framework. It is designed for interactions between students and teachers. Features include attendance, marks and time table.

## Installation

Python needs to be installed. Install the dependencies with

```bash
pip install -r requirements.txt
```

## Usage

Go to the project folder and run

```bash
python manage.py runserver
```

Then go to the browser and enter the url **http://127.0.0.1:8000/**

## Login

The login page is common for students and teachers.

The django admin page is at **http://127.0.0.1:8000/admin**. Create an admin user with

```bash
python manage.py createsuperuser
```

## Users

New students and teachers can be added through the add student / add teacher forms or through the admin page. Login credentials are generated automatically:

| User    | Username                                   | Password                                  |
|---------|--------------------------------------------|-------------------------------------------|
| Student | firstname + `_` + last 3 digits of USN     | firstname + `_` + year of birth (YYYY)    |
| Teacher | firstname + `_` + teacher ID               | firstname + `_` + year of birth (YYYY)    |
The admin page is used to modify all tables such as Students, Teachers, Departments, Courses, Classes etc.

**For more details regarding the system and features please refer the reports included.**

## Resetting Attendance

The attendance time range can be reset from Django Admin -> Attendance (http://127.0.0.1:8000/admin/info/attendanceclass/).

- Start Date: Start Date of Attendance period
- End Date: End Date of Attendance period

This will delete all present attendance data and create new attendance objects for the given time range.
