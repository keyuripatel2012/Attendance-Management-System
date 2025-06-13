# Attendance-Management-System | JAVA Spring Boot

## 📘 Overview

Attendance Management System (AMS) is a robust, integrated, and scalable system built to streamline and digitize student attendance tracking, internal assessments, event scheduling, and academic reporting for educational institutions. Developed using modern full-stack technologies, AMS is designed for faculty, students, and administrators to enhance transparency, efficiency, and accuracy in academic processes.

---

## ✨ Key Features

- **Student Attendance Tracking** – Real-time daily attendance records with automated calculations and graphical summaries.
- **Timetable Management** – Dynamic and customizable timetable generation based on faculty, subjects, and institutional requirements.
- **Exam and Result Management** – Online internal exam results with downloadable performance reports.
- **Fee Payment Integration** – Multiple payment modes (UPI, Card, Wallet) with secure transaction logging.
- **Role-Based Access** – Secure access for Admin, Faculty, Students, and Management with custom privileges.
- **Analytics and Reporting** – Visual dashboards for performance tracking, attendance insights, and academic progress.
- **Multi-Device Compatibility** – Responsive web app usable on desktops, tablets, and mobile devices.
- **Event Scheduling** – Centralized event calendar with registration, notifications, and participation tracking.

---

## 🛠 Technology Stack (Simplified)

| Part              | Tools Used                                                      |
|-------------------|------------------------------------------------------------------|
| **Frontend**      | HTML, CSS, Bootstrap, JavaScript – for designing the interface.  |
| **Backend**       | Java with Spring Boot – handles all server-side logic.           |
| **Database**      | MySQL – stores student, attendance, exam, and user data.         |
| **Build Tool**    | Maven – for building and managing dependencies.                  |
| **IDE**           | Eclipse – used for development.                                  |
| **Operating System** | Windows 11 – development and testing environment.             |

---

## 📂 Database Schema

AMS uses a normalized relational schema. Key tables include:

- `faculty`
- `department`
- `semester`
- `program`
- `subject`
- `student` (admission)
- `teacher` (registration)
- `admin`
- `user`, `role`, `user_role`

Each table includes metadata for audit trails (`createdon`, `createdby`, `updatedon`, `modifiedby`) and logical deletion control (`active` bit).

> See the full data dictionary in the `/docs/data_dictionary.md`.

---

## 🖥️ System Requirements

### Minimum Hardware:
- **Processor**: Intel Core i3  
- **RAM**: 8 GB  
- **Storage**: 256 GB SSD

### Software Environment:
- Windows 11  
- Java JDK 11+  
- MySQL 8.x  
- Apache Maven 3.8+  
- Eclipse IDE (or any preferred IDE)

---

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/attendance-management-system.git
cd attendance-management-system
```

### 2. Setup the MySQL Database
- Create a database named `ams_db`.
- Import the SQL schema from `docs/schema.sql`.

### 3. Configure Spring Boot (`application.properties`)
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/ams_db
spring.datasource.username=root
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update
```

### 4. Build and Run the Application
```bash
mvn clean install
mvn spring-boot:run
```

### 5. Access the Web Interface
Visit: [http://localhost:8080](http://localhost:8080)

---

## 📊 User Roles & Access

| Role     | Access Permissions                               |
|----------|--------------------------------------------------|
| Admin    | Full control (users, roles, data)                |
| Faculty  | Manage attendance, exams, and results            |
| Student  | View timetable, attendance, and results          |
| Manager  | View analytics and institution-level reports     |

---

## 📈 System Flow (UML)

- Use Case Diagram: `/docs/use_case_diagram.png`
- Class Diagram: `/docs/class_diagram.png`
- Activity Diagram: `/docs/activity_diagram.png`

---

## 📄 License

This project is developed as part of MCA Semester-3 final submission under Gujarat Vidyapith. Not intended for commercial distribution.
