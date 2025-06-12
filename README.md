# Student Management System
Student Management System is a simple database application that lets schools store and manage student records, courses, and enrollments. It has three main parts which is Students to add, remove or edit student details like name and email.Courses to manage course names and credits. Enrollments to assign students to courses. The system uses a database to store data and lets users easily update information. It’s designed for small teams, with each member working on one part. The goal is to make school record-keeping easier without unnecessary complexity

# ✨ Features
✅ User Authentication
Secure login functionality for both students and deans
Session management to restrict unauthorized access

✅ Role-Based Access Control
Student: View/edit profile, manage course enrollments
Dean: View/manage all students and courses, assign/remove students from courses, create new student accounts

🎓 Student Management
Profile viewing and updating
Password update functionality
Course overview and enrollment management

🏫 Course Management
Deans can view all available courses
Assign or remove students from specific courses
Add or delete courses (admin-side)

📄 Account Creation
Deans can register new student accounts using ID, name, email, phone number, and password

🛢 Database Integration
MySQL database stores students, courses, and enrollment data
Foreign key constraints to maintain data integrity

# 🛠 Setup Instructions
🔧 Prerequisites
Java (JDK 8 or higher)
Apache Tomcat (for running the application)
MySQL or MariaDB

#🚀 Steps to Run Locally
Clone the Repository:
git clone [(https://github.com/Ikmalharz/CSA3023-GP16)]

Set up the Database:
Import the provided SQL file into MySQL/MariaDB:
Database Name: universityss
Tables: students, courses, enrollments
Use the provided universityss.sql file to initialize your database.

Configure the Database Connection:

In the project directory, update your database connection strings in DBConnection.java:
String url = "jdbc:mysql://localhost:3306/universityss";
String username = "root";
String password = "";

Deploy the Application:
Copy the project to the webapps folder in Apache Tomcat.
Start Tomcat on port 8080.

Access the Application:
Open your browser and go to:
http://localhost:8080/student-management-system

# 🧰 Technologies Used
Java (JSP, Servlets)
MySQL / MariaDB
Apache Tomcat
HTML/CSS (Basic frontend styling)

#📊 Database Schema (Simplified)
students Table
Column	Type
id	VARCHAR(20)
name	VARCHAR(100)
email	VARCHAR(100)
phone	VARCHAR(15)
password	VARCHAR(255)

courses Table
Column	Type
course_id	VARCHAR(10)
course_name	VARCHAR(100)
instructor	VARCHAR(100)

enrollments Table
Column	Type
student_id	VARCHAR(20)
course_id	VARCHAR(10)

# 📦 Sample Data
INSERT INTO students (id, name, email, password, phone) VALUES
('S69922', 'Ikmal Hariz', 'S69922@ocean.umt.edu.my', '12345678', '0107133240'),
('S71785', 'Iqmal Hadi', 'S71785@ocean.umt.edu.my', '12345678', '01125620056'),
('S71905', 'Kamal Arif', 'S71905@ocean.umt.edu.my', '12345678', '01162211247');

💬 Contributing
Contributions are welcome! If you want to improve this system or fix issues, feel free to fork the repo, make changes, and submit a pull request.

📄 License
This project is licensed under the MIT License.
