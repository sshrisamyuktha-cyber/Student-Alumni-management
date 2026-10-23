# Alumni Management System

## Brief Overview

The Alumni Management System is a menu-driven application designed to facilitate and enhance engagement between educational institutions and their alumni. It provides a centralised platform for managing alumni records, organising events, and fostering meaningful connections between graduates and their institutions.

The system features two interfaces: one for administrators and another for alumni. Administrators can manage student and alumni records, create and update events, search for information, and communicate with alumni. Alumni can register, update their details, explore upcoming events, register for activities, and search for other alumni.

Developed using Python and MySQL, the application incorporates authentication, input validation, database management, and email functionality. Its aim is to streamline administrative processes, maintain accurate records, and encourage alumni participation in institutional activities.

## Objectives and Scope

The primary objective of this project is to simplify alumni data management and improve engagement between educational institutions and their graduates.

The system aims to:

- Simplify student and alumni registration and profile management.
- Maintain accurate and organised alumni records.
- Facilitate event creation, registration, and attendance management.
- Enable alumni to connect with other graduates.
- Improve communication through email notifications.
- Provide administrators with efficient search and data retrieval tools.
- Support secure and consistent database operations.

### Future Enhancements

The system can be extended to improve its functionality, scalability, and accessibility through the following features:

- Maintain logs of administrator and alumni activities for accountability.
- Migrate the application and database to the cloud.
- Develop a web-based interface for easier access.
- Automate email and SMS notifications for event reminders, updates, and cancellations.
- Collect post-event feedback and analyse event success using attendance, feedback, and cost-efficiency metrics.
- Track alumni activities and generate engagement reports.
- Integrate OTP or email-based verification to strengthen authentication.

## System Workflow and Features

### 1. User Authentication

- **Admin Login:** Administrators log in using a username and password validated against the database.
- **Login Attempt Limit:** The system restricts login attempts to three to enhance security.
- **Password Input:** The `getpass` library is used to accept passwords without displaying them in the terminal.

### 2. Student Management

#### Student Registration

Administrators can register students by entering details such as:

- Name and class
- Date of birth
- Contact number and email address
- Passing year and academic stream
- Location
- Employment status and related details

The system validates inputs, including date of birth and email format, before storing the information.

#### Student Search

Administrators can search and filter student records based on:

- Name
- Passing year
- Academic stream
- Employment status

Search results are displayed in a structured tabular format.

#### Student Record Updates

Administrators can update selected student details, including class, contact number, email address, employment status, professional domain, and company.

### 3. Event Management

#### Event Creation

Administrators can create events by specifying:

- Event name and description
- Event date
- Event type, such as a workshop or seminar
- Venue
- Number of available seats
- Event status

The system validates event dates to ensure that events are scheduled at least two weeks in advance.

#### Event Updates

Administrators can modify event information, including its name, description, date, venue, and other relevant details.

#### Event Search and Status Management

Events can be searched and categorised according to their status:

- Active
- Completed
- Postponed
- Cancelled

### 4. Communication

The system includes email functionality to facilitate communication between administrators and alumni.

- Send emails containing announcements, updates, and notifications.
- Validate email addresses before sending.
- Use SMTP to send messages through a configured email account.

### 5. Alumni Registration

#### Verification Against Student Records

Alumni registration is validated against existing student records to ensure that only eligible former students can register.

#### Duplicate Registration Prevention

The system checks whether an individual is already registered in the alumni database to prevent duplicate entries.

#### Alumni Database Updates

Verified student information is transferred to the alumni database. Alumni can also provide updated details, such as contact information and employment status.

### 6. Alumni Event Participation

#### View Events

Alumni can browse events categorised as:

- Upcoming (Active)
- Completed
- Postponed
- Cancelled

#### Event Registration

- Display active events with available seats.
- Allow alumni to register for events.
- Update seat availability in the database following registration.

### 7. Alumni Search

Registered alumni can search for other alumni using:

- Name
- Email address
- Passing year

Search results are presented in a structured table to improve readability.

### 8. Integration Between Admin and Alumni Features

The alumni interface works alongside the administrator interface. Events and records created or updated by administrators are made available to alumni through the relevant menus.

This integration supports consistent information management and enables alumni to interact with institution-led activities.

### 9. Usability and Navigation

The application uses menu-driven interfaces to provide straightforward navigation.

Users can:

- Register or update relevant information.
- View and search events.
- Register for events.
- Search alumni records.
- Return to the main menu or exit the program.

Input validation and error handling help manage invalid menu selections, email addresses, and numeric values.

### 10. Secure Database Interaction

The application uses MySQL to store and retrieve student, alumni, and event information.

Database operations include:

- Retrieving event information.
- Registering alumni for events.
- Verifying alumni details against student records.
- Creating and updating student and alumni records.
- Managing event registrations and seat availability.

SQL queries are designed to use parameterised inputs to reduce the risk of SQL injection and support data integrity.

### 11. Main Menu and Exit Options

The system provides menu options that allow users to navigate between available features, return to previous menus, or exit the application.

### 12. MySQL Integration

MySQL serves as the database management system for storing and maintaining student, alumni, event, and registration records.

The Python application connects to MySQL through `mysql.connector` to perform database operations.

## Hardware and Software Requirements

### Hardware

- A personal computer (PC)

### Software

- Python (IDLE, Visual Studio Code, or another Python IDE)
- MySQL Command-Line Client
- MySQL Workbench
- MySQL Connector for Python

## Python Libraries and Modules

| Library / Module | Purpose |
|---|---|
| `PrettyTable` | Displays student records, alumni search results, and event listings in readable tables. |
| `datetime` | Handles dates and times for age validation, event scheduling, and registration records. |
| `getpass` | Accepts administrator passwords without displaying them in the terminal. |
| `smtplib` | Sends emails through an SMTP server. |
| `mysql.connector` | Connects Python to MySQL and performs database operations. |
| `re` | Uses regular expressions to validate email formats and other input patterns. |
| `sys` | Supports program termination and command-line-related operations. |
| `utils` (custom module) | Provides reusable functions for input handling, email validation, login, and other utility operations. |

## Project Goals

The Alumni Management System aims to provide an organised and accessible way to manage alumni information and institutional events. By combining student record management, alumni registration, event participation, and communication features, the project supports stronger relationships between institutions and their graduates.

