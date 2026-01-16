# Smart Campus  

Live Demo 👾  
https://smart-campus-v32n.onrender.com

---

## Overview
Smart Campus is a system for classroom availability, reservations, and infrastructure issue management in an academic campus.

The system allows students and lecturers to report classroom issues, enables maintenance staff to manage and resolve reports, and provides lecturers with smart classroom reservation capabilities based on real availability.

> **Note:**  
> This project was developed as part of an academic **team project**.  
> The technologies and system architecture were learned and implemented through extensive self-driven learning beyond the course material.

---

## Project Description
Smart Campus is an academic campus management system focused on classroom infrastructure and room reservations.

The system supports:
- Reporting classroom issues by students and lecturers
- Centralized issue handling and status management by maintenance staff
- Smart classroom reservations based on real availability

The availability logic takes into account both:
- Existing reservations  
- A fixed weekly schedule  

This provides a unified and reliable interface for managing physical campus resources.

The project was developed as part of an academic course, with emphasis on:
- Proper database design
- Separation of responsibilities between system components
- Writing and maintaining unit tests

---

## System Goals
- Streamline the classroom issue reporting process
- Prevent duplicate reports for identical issues
- Enable smart classroom availability management
- Ensure data reliability using automated tests
- Work with the database in a safe and isolated manner

---

## User Roles 👨‍🎓👨‍🏫👨‍💻
- **Student** – Report classroom issues and reserve classrooms
- **Lecturer** – Report issues and reserve classrooms
- **Maintenance Staff** – Handle reports and manage issue statuses

---

## Core Functionality

### User Management & Authentication
- User creation based on predefined roles
- Password-based authentication
- Prevention of unauthorized role creation

### Issue Reporting Management
- Creation of new issue reports with room, category, and description
- Persistent storage of reports in the database
- Initial report status set to `open`
- Automatic grouping and closure of identical reports  
  (same room, same category, same time window)
- Manual status updates to `done`

### Classroom Reservation Management
- Availability checks by date and time range
- Creation of reservations only when classrooms are available
- Cancellation of existing reservations and status updates
- Prevention of overlapping reservations

### Classroom Availability Queries
- Retrieval of available classrooms within a given time range
- Consideration of both existing reservations and weekly schedules
- Display of detailed classroom information  
  (room type, projector availability, seating capacity)
- Calculation of maximal free time windows per classroom

---

## Architecture & Technologies 👾
- **Programming Language:** Python  
- **Backend:** Flask  
- **Database:** SQLite  
- **Version Control:** Git & GitHub  
- **Testing:** pytest  

---

## Unit Testing 📝
The system includes comprehensive unit tests covering core functionality, including:
- User authentication and authorization
- Issue report creation and management
- Classroom availability and reservations
- Complex database queries

Each test runs on an isolated, temporary database created at runtime to prevent interference with real data and to ensure reliable test results.

---

## Running Tests
Tests are executed using `pytest` and validate that all core functions behave as expected, including edge cases.

---

## Requirements ‼️
- Flask  
- python-dotenv  
- openai  
- tzdata  

---

## Notes 📌
- The system was designed with future extensibility in mind  
  (additional roles, enhanced UI, integration with external systems).
- The code emphasizes readability, maintainability, and separation of concerns.
- Before running the application, the `seed.py` file should be executed via the terminal to seed initial demo data.

