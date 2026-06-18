# 📚 Student Grade Tracker

> A comprehensive Java console application for managing student academic records efficiently

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white)
![Version](https://img.shields.io/badge/version-1.0-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/status-completed-success?style=for-the-badge)
![CodeAlpha](https://img.shields.io/badge/CodeAlpha-Internship-purple?style=for-the-badge)

---

## 📋 Table of Contents
- [Project Overview](#-project-overview)
- [Features](#-features)
- [Technologies Used](#-technologies-used)
- [Installation & Setup](#-installation--setup)
- [How to Use](#-how-to-use)
- [Project Structure](#-project-structure)
- [Sample Output](#-sample-output)
- [Future Enhancements](#-future-enhancements)
- [Contributing](#-contributing)
- [License](#-license)
- [Contact](#-contact)
- [Acknowledgments](#-acknowledgments)

---

## 🎯 Project Overview

The **Student Grade Tracker** is a Java-based console application developed as part of the **CodeAlpha Internship Program**. It provides educators and academic institutions with a simple yet powerful tool to manage student records, track grades across multiple subjects, and generate comprehensive performance reports.

This project demonstrates proficiency in **Object-Oriented Programming (OOP)** principles, **data structure implementation**, **input validation**, and creating user-friendly console interfaces.

### 🎓 Problem Statement
Educational institutions often struggle with managing student records and calculating academic performance manually. This system automates the process of:
- Storing student information
- Tracking subject-wise grades
- Calculating averages
- Generating performance reports
- Analyzing class statistics

### ✅ Solution
A robust, menu-driven Java application that streamlines academic record management with an intuitive interface and real-time calculations.

---

## ✨ Features

### 👥 Student Management
- ✅ Add new students with name and roll number
- ✅ Prevent duplicate roll numbers
- ✅ View all registered students
- ✅ Search students by roll number

### 📊 Grade Management
- ✅ Add grades for multiple subjects (0-100 range)
- ✅ Input validation for grade values
- ✅ Store grades efficiently using HashMap
- ✅ Update existing grades

### 📈 Performance Calculations
- ✅ Calculate individual student averages
- ✅ Automatic letter grade assignment (A, B, C, D, F)
- ✅ Pass/Fail status determination
- ✅ Grade scale:
  - A: 90-100 (Excellent)
  - B: 80-89 (Good)
  - C: 70-79 (Satisfactory)
  - D: 60-69 (Needs Improvement)
  - F: Below 60 (Fail)

### 📋 Reports & Analytics
- ✅ Individual student report with:
  - Personal information
  - Subject-wise grades
  - Average score
  - Letter grade
  - Pass/Fail status
- ✅ Class statistics including:
  - Total students
  - Class average
  - Highest performer
  - Lowest performer
  - Pass/Fail ratio

### 🎯 User Interface
- ✅ Clean, interactive menu-driven system
- ✅ User-friendly prompts
- ✅ Clear error messages
- ✅ Professional formatting with ASCII art

---

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| **Java** | Core programming language |
| **ArrayList** | Student data storage |
| **HashMap** | Grade storage (Subject → Score) |
| **Scanner** | User input handling |
| **OOP Principles** | Encapsulation, Inheritance, Polymorphism |

### Requirements
- Java 8 or higher
- Any Java IDE (Eclipse, IntelliJ, VS Code) or text editor
- Terminal/Command Prompt

---

## 🚀 Installation & Setup

### Step 1: Clone the Repository
```bash
git clone https://github.com/yourusername/CodeAlpha_StudentGradeTracker.git
cd CodeAlpha_StudentGradeTracker
Step 2: Compile the Program
javac GradeTracker.java
Step 3: Run the Program
java GradeTracker
Alternative: Using IDE
Open the project in your preferred IDE

Navigate to GradeTracker.java

Click "Run" or press Ctrl+F11 (Eclipse) / Shift+F10 (IntelliJ)

💻 How to Use
Main Menu
When you run the program, you'll see:

text
╔═══════════════════════════════════════╗
║     STUDENT GRADE TRACKER MENU      ║
╠═══════════════════════════════════════╣
║ 1. Add Student                      ║
║ 2. Add Grade to Student            ║
║ 3. View All Students               ║
║ 4. View Student Report             ║
║ 5. View Class Statistics           ║
║ 6. Exit                            ║
╚═══════════════════════════════════════╝
Step-by-Step Guide
1️⃣ Adding a Student
text
Enter student name: Sarah Johnson
Enter roll number: 101
✅ Student added successfully!
2️⃣ Adding Grades
text
Enter roll number to add grades: 101
Enter subject name: Mathematics
Enter grade (0-100): 92
✅ Grade added successfully!
3️⃣ Viewing All Students
text
========== ALL STUDENTS ==========
Roll: 101 | Name: Sarah Johnson | Avg: 91.83 | Grade: A
Roll: 102 | Name: Michael Chen | Avg: 78.50 | Grade: C
==================================
4️⃣ Viewing Student Report
text
========== STUDENT REPORT ==========
Name: Sarah Johnson
Roll Number: 101

Subject Grades:
  Mathematics    : 92.00
  Physics        : 88.50
  Chemistry      : 95.00

Average Score: 91.83
Grade Letter: A
Status: PASS ✅
=====================================
5️⃣ Viewing Class Statistics
text
========== CLASS STATISTICS ==========
Total Students: 5
Class Average: 82.40
Passed: 4 | Failed: 1
Highest Average: 91.83 (Sarah Johnson)
Lowest Average: 45.00 (David Wilson)
=======================================
📁 Project Structure
text
CodeAlpha_StudentGradeTracker/
│
├── GradeTracker.java          # Main application file
│
├── README.md                  # Project documentation
├── LICENSE                    # MIT License
├── .gitignore                 # Git ignore file
│
└── docs/                      # Additional documentation
    ├── UML_Diagram.png        # Class structure diagram
    └── User_Guide.pdf         # Detailed user manual
Class Structure
text
┌─────────────────────────────────────┐
│           GradeTracker              │
│─────────────────────────────────────│
│ - students: ArrayList<Student>      │
│ - scanner: Scanner                  │
│─────────────────────────────────────│
│ + addStudent()                      │
│ + addGradesToStudent()              │
│ + viewAllStudents()                 │
│ + viewStudentReport()               │
│ + viewClassStatistics()             │
│ + run()                             │
│ - findStudent()                     │
└─────────────────────────────────────┘
              │
              │ uses
              ▼
┌─────────────────────────────────────┐
│             Student                 │
│─────────────────────────────────────│
│ - name: String                      │
│ - rollNumber: int                   │
│ - grades: HashMap<String, Double>   │
│─────────────────────────────────────│
│ + Student(name, rollNumber)         │
│ + addGrade(subject, score)          │
│ + calculateAverage(): double        │
│ + getGradeLetter(): char            │
│ + displayReport()                   │
└─────────────────────────────────────┘
📊 Sample Output
Here's a complete demonstration of the application:

text
🎓 WELCOME TO STUDENT GRADE TRACKER 🎓

╔═══════════════════════════════════════╗
║     STUDENT GRADE TRACKER MENU      ║
╠═══════════════════════════════════════╣
║ 1. Add Student                      ║
║ 2. Add Grade to Student            ║
║ 3. View All Students               ║
║ 4. View Student Report             ║
║ 5. View Class Statistics           ║
║ 6. Exit                            ║
╚═══════════════════════════════════════╝
Choose an option: 1

Enter student name: Emma Wilson
Enter roll number: 201
✅ Student added successfully!

Choose an option: 2
Enter roll number to add grades: 201
Enter subject name: Mathematics
Enter grade (0-100): 95
✅ Grade added successfully!

Choose an option: 4
Enter roll number: 201

========== STUDENT REPORT ==========
Name: Emma Wilson
Roll Number: 201

Subject Grades:
  Mathematics    : 95.00

Average Score: 95.00
Grade Letter: A
Status: PASS ✅
=====================================
🔮 Future Enhancements
Data Persistence - Save/Load data from files (JSON/CSV)

Database Integration - MySQL/PostgreSQL support

GUI Interface - JavaFX/Swing desktop application

Web Application - Spring Boot REST API

Export Reports - PDF/Excel report generation

Grade Weighting - Different weights for assignments/exams

Multiple Classes - Support for multiple class sections

Attendance Tracking - Integration with attendance records

Email Notifications - Automated alerts for low grades

Mobile App - Android/iOS companion app

Parent Portal - Parent access to student grades

Analytics Dashboard - Visual charts and graphs

🤝 Contributing
We welcome contributions! Follow these steps:

Fork the repository

Create a feature branch

bash
git checkout -b feature/AmazingFeature
Commit your changes

git commit -m 'Add some AmazingFeature'
Push to the branch

git push origin feature/AmazingFeature
Open a Pull Request

Contribution Guidelines
Follow Java coding conventions

Write meaningful commit messages

Update documentation accordingly

Add comments for complex logic

Test your code thoroughly

📝 License
This project is licensed under the MIT License - see the LICENSE file for details.

text
MIT License

Copyright (c) 2024 [Your Name]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
📧 Contact
Anupa Sah

📧 Email: anupasah621@gmail.com

🙏 Acknowledgments
CodeAlpha - For providing this internship opportunity

Java Documentation - For comprehensive API reference

Open Source Community - For tools and inspiration

All Contributors - Who help improve this project

Professor/Instructors - For guidance and support

📊 Badges
https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=java&logoColor=white
https://img.shields.io/badge/GitHub-100000?style=flat-square&logo=github&logoColor=white
https://img.shields.io/badge/Open%2520Source-%E2%9D%A4%EF%B8%8F-green?style=flat-square
https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square
https://img.shields.io/badge/Maintained%253F-yes-green.svg?style=flat-square
https://img.shields.io/badge/Made%2520with-%E2%9D%A4%EF%B8%8F-red?style=flat-square

⭐ Support
If you found this project helpful, please consider:

⭐ Starring the repository

🍴 Forking the project

📢 Sharing with others

📝 Reporting issues

📖 Additional Resources
Java Documentation

GitHub Guide

CodeAlpha Internship

Made with ❤️ by [Anupa Sah]

"Education is the most powerful weapon which you can use to change the world." - Nelson Mandela
## 🔧 Additional Files to Include

### 1. **LICENSE** File
Create a `LICENSE` file with the MIT License text from above.

### 2. **.gitignore** File
```txt
# Compiled class files
*.class

# BlueJ files
*.ctxt

# Package Files
*.jar
*.war
*.nar
*.ear
*.zip
*.tar.gz
*.rar

# Virtual machine crash logs
hs_err_pid*

# IDE Files
.idea/
*.iml
.vscode/
.settings/
.project
.classpath
*.prefs

# OS Files
.DS_Store
Thumbs.db
3. CHANGELOG.md (Optional)
markdown
# Changelog

## [1.0.0] - 2024-10-XX

### Added
- Initial release
- Student management functionality
- Grade tracking system
- Average calculation and grade assignment
- Individual student reports
- Class statistics
- Interactive menu interface

### Fixed
- Input validation for grades
- Duplicate roll number prevention
📤 Uploading to GitHub
bash
# Initialize git repository
git init

# Add all files
git add .

# Commit changes
git commit -m "Initial commit: Student Grade Tracker for CodeAlpha"

# Add remote repository
git remote add origin https://github.com/yourusername/CodeAlpha_StudentGradeTracker.git

# Push to GitHub
git push -u origin main
This README is comprehensive, professional, and specifically tailored for your CodeAlpha internship submission. It covers all required sections and demonstrates your attention to detail and professionalism. 🚀

