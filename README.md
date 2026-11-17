Smart Student Management System
A web-based system to manage students, teachers, courses, attendance, marks and assignments in one place. The system has three role-based modules: Student, Teacher and Admin.

Features
Student Module
View dashboard (attendance %, GPA, upcoming assignments)
View and update own profile
View enrolled courses
Check course-wise attendance
View marks, grades and results
View and submit assignments
View class timetable
Teacher Module
Dashboard with today's classes and pending work
View assigned classes and student lists
Mark attendance
Upload and update marks
Create assignments, view submissions and grade them
Admin Module
Dashboard with total students, teachers and courses
Add, edit, delete and search students and teachers
Create courses and assign teachers
Enroll students in courses
Generate attendance and result reports
Post announcements
Shared
Single login with role-based redirect (Admin / Teacher / Student)
JWT authentication and role-based route protection
Tech Stack
Layer	Technology
Frontend	React, React Router,
Backend	Node.js, Express.js
Database	SQLite
Project Structure
smart-student-management-system/
├── backend/
│   ├── server.js
│   ├── config/db.js
│   ├── middleware/        # auth.js, role.js
│   ├── routes/            # auth, student, teacher, admin
│   ├── controllers/       # auth, student, teacher, admin
│   └── models/            # User, Student, Teacher, Course, Attendance, Marks, Assignment
└── frontend/
    └── src/
        ├── App.jsx
        ├── api/axios.js
        ├── context/AuthContext.jsx
        ├── components/    # Navbar, Sidebar, Table, ProtectedRoute
        └── pages/
            ├── Login.jsx
            ├── student/
            ├── teacher/
            └── admin/
Database Tables
users, students, teachers, courses, enrollments, attendance, marks, assignments, submissions, announcements

Installation and Setup
Prerequisites
Node.js (v18 or later)
npm
Backend
cd backend
npm install
npm start
The server runs on http://localhost:5000.

Frontend
cd frontend
npm install
npm run dev
The app runs on http://localhost:5173.

Environment Variables
Create a .env file in backend/:

PORT=5000
JWT_SECRET=your_secret_key
User Roles
Role	Access
Admin	Manage students, teachers, courses, reports, notices
Teacher	Attendance, marks, assignments for assigned classes
Student	Own profile, courses, attendance, results, assignments
Group Members
Arusa (Student Module)
Maryam (Teacher Module)
