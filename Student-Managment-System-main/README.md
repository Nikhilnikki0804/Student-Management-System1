# 🎓 StudentVault – Secure Student Portal

## 📌 Overview

StudentVault is a full-stack Java web application developed to securely manage student information through authentication and role-based access control.
The application allows students to register, log in, view their personal details, and update account information. It also provides administrative access where the admin can view and manage all student records.
This project was built to strengthen practical knowledge of Java web development concepts such as Servlets, JSP, JDBC connectivity, session handling, and MVC architecture.

---

## ✨ Features

### 🔐 Secure Authentication
- User registration and login functionality
- Credential validation using JDBC and MySQL

### 👨‍💼 Role-Based Access Control
- Admin access for managing all student records
- Student-specific access to personal information only

### 👩‍🎓 Student Dashboard
- View personal details
- Update account information
- Access personalized dashboard

### 🗄 Database Integration
- Real-time data storage and retrieval using MySQL
- JDBC connectivity for database operations

### 🧩 MVC-Based Architecture
- Structured implementation using Model-View-Controller pattern
- Separation of presentation, business logic, and data access

### 💻 Responsive User Interface
- User-friendly pages designed using JSP, HTML, CSS, and Bootstrap

---

## 🛠 Tech Stack Used

| Layer | Technology |
|------|------------|
| Frontend | JSP, HTML5, CSS3, Bootstrap |
| Backend | Java Servlets, JDBC |
| Database | MySQL |
| Server | Apache Tomcat |
| Version Control | Git & GitHub |
| IDE | Eclipse |

---

## 🏗 System Architecture

This project follows the **MVC (Model-View-Controller)** design pattern.

### Model
Handles student data and database operations.

### View
JSP pages for user interaction.

### Controller
Servlets process requests and control application flow.

---

## 🚀 Application Workflow

### User Flow

1. New users register with valid details
2. Existing users log in using credentials
3. Session is created after successful authentication
4. Users are redirected based on their role

### Admin Access
If the logged-in user's ID is **1**, the system grants administrator access.

Admin can:
- View all registered student details
- Manage student records

### Student Access
Regular students can:
- View their personal information
- Update profile details
- Access individual dashboard

---

## 📂 Project Structure

```bash
StudentVault/
│
├── java/com/
│   └── pentagon/
│       ├── Conn/
│       │   └── Connectors.java
│       │
│       ├── StudentDAO/
│       │   ├── StudentDAO.java
│       │   └── StudentDAOImp.java
│       │
│       ├── StudentDTO/
│       │   └── Student.java
│       │
│       └── student/dynamic/
│           ├── Dashboard.java
│           ├── Forgotpassword.java
│           ├── Login.java
│           ├── Signup.java
│           └── UpdateAccount.java
│
├── webapp/
│   ├── index.jsp
│   ├── login.jsp
│   ├── register.jsp
│   ├── dashboard.jsp
│   ├── forgotpassword.jsp
│   ├── updateAccount.jsp
│   └── viewStudents.jsp
│
├── WEB-INF/
│   └── web.xml
│
└── README.md
```

---

## ⚙️ Installation & Setup

### 1. Clone Repository

```bash
git clone https://github.com/your-username/StudentVault.git
cd StudentVault
```

---

### 2. Configure MySQL Database

Create database:

```sql
CREATE DATABASE student_portal;
```

Create table:

```sql
CREATE TABLE students (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(50),
    email VARCHAR(100),
    password VARCHAR(100),
    course VARCHAR(50)
);
```

---

### 3. Configure JDBC Connection

Update database credentials in:

```java
Connectors.java
```

Example:

```java
private static final String URL = "jdbc:mysql://localhost:3306/student_portal";
private static final String USER = "root";
private static final String PASSWORD = "your_password";
```

---

### 4. Add MySQL JDBC Driver

Download MySQL Connector/J and add it to:

```bash
WEB-INF/lib
```

---

### 5. Deploy on Apache Tomcat

- Import project into Eclipse
- Configure Apache Tomcat Server
- Run project on server

Access application:

```bash
http://localhost:8080/StudentVault/
```

---

## 🧠 Core Concepts Implemented

### Servlet Lifecycle
- Initialization
- Request processing
- Response handling
- Destruction

### Session Management
Used HttpSession for maintaining logged-in user sessions.

### Request Dispatching
Used RequestDispatcher for forwarding requests between resources.

### JDBC Connectivity
Integrated Java application with MySQL database.

### Authentication & Authorization
Implemented secure login verification and role-based access.

---

## 🛑 Challenges Faced

During development, the following challenges were addressed:

- Managing user sessions
- Implementing role-based dashboard access
- Handling database connection exceptions
- Maintaining proper request flow
- Deploying and configuring Tomcat server

---

## 📚 Learning Outcomes

Through this project, I gained practical experience in:

- Java Web Application Development
- JSP and Servlet Integration
- JDBC Programming
- MySQL Database Design
- MVC Architecture
- Session Handling
- Debugging Deployment Errors

---

## 🔮 Future Enhancements

Planned improvements include:

- Password encryption using BCrypt
- Email-based password recovery
- Attendance management module
- File upload support
- REST API integration
- Admin analytics dashboard

---

## 📸 Screenshots

Add project screenshots here:

- Login Page
- Registration Page
- Student Dashboard
- Admin Dashboard

---

## 👨‍💻 Author

**Sarath Babu Endluri**

📧 sarathendluri90@gmail.com  
🔗 Portfolio: https://sarathendluri333.github.io/  
🔗 LinkedIn: https://linkedin.com/in/sarath-endluri-0056242bb

---

## 📄 License

This project is developed for educational and learning purposes.
