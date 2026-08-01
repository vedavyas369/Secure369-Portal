# 🚀 Secure369 Intern & Employee Management Portal

A complete web-based **Intern and Employee Management System** built using **Python Flask** and modern DevOps technologies.

The Secure369 Intern & Employee Management Portal is designed to manage the complete lifecycle of interns and employees — from intern registration and training to full-time employee conversion, attendance, projects, performance, and employment records.

This project is also a hands-on DevOps learning project covering:

**Python → Flask → Git → GitHub → Docker → Jenkins → Terraform → AWS → Nginx**

---

# 📌 Project Status

🚧 **Currently Under Development**

The application is being developed step by step while learning and implementing each technology practically.

---

# 🎯 Project Objectives

The main objectives of this project are:

- Build a real-world web application using Flask
- Manage interns
- Manage employees
- Automatically generate Intern IDs
- Automatically generate Employee IDs
- Convert successful interns into full-time employees
- Preserve complete internship history after conversion
- Manage attendance
- Manage training
- Manage projects
- Manage performance reviews
- Manage employee records
- Build an Admin/HR dashboard
- Implement secure authentication
- Store information in a database
- Use Git and GitHub for version control
- Containerize the application using Docker
- Build CI/CD using Jenkins
- Provision AWS infrastructure using Terraform
- Deploy the application on AWS
- Configure Nginx as a reverse proxy
- Learn the complete DevOps lifecycle

---

# 🔄 Intern to Employee Lifecycle

One of the main features of this application is managing the complete journey from internship to full-time employment.

```text
Candidate
    │
    ▼
Intern Selected
    │
    ▼
Intern Registration
    │
    ▼
Automatic Intern ID
INT-2026-0001
    │
    ▼
Internship
    │
    ├── Attendance
    ├── Training
    ├── Projects
    ├── Performance
    ├── Reviews
    └── Documents
    │
    ▼
Internship Completion
    │
    ├─────────────────────────┐
    │                         │
    ▼                         ▼
Internship Completed      Selected for
Only                      Full-Time Employment
                              │
                              ▼
                      Convert to Employee
                              │
                              ▼
                     Automatic Employee ID
                        EMP-2026-0001
                              │
                              ▼
                       Active Employee
                              │
                              ├── Attendance
                              ├── Projects
                              ├── Performance
                              ├── Department
                              ├── Designation
                              └── Employment History
```

The internship record will **not be deleted** when an intern becomes an employee.

The system will preserve the complete history.

---

# 🆔 Automatic ID Generation

Every intern and employee will receive a unique ID generated automatically by the application.

## 👨‍🎓 Intern ID

Example:

```text
INT-2026-0001
INT-2026-0002
INT-2026-0003
```

Format:

```text
INT-YEAR-SEQUENCE
```

Example:

```text
INT-2026-0025
```

This represents Intern Number 25 created during 2026.

The Intern ID will automatically be generated when HR/Admin registers a new intern.

---

# 👨‍💼 Employee ID

Every employee will receive a unique Employee ID.

Example:

```text
EMP-2026-0001
EMP-2026-0002
EMP-2026-0003
```

Format:

```text
EMP-YEAR-SEQUENCE
```

If an intern becomes an employee, the Employee ID will remain linked to their previous Intern ID.

Example:

```text
Name: Rahul Kumar

Intern ID:
INT-2026-0015

        ↓

Converted to Employee

        ↓

Employee ID:
EMP-2027-0008
```

---

# 🔑 Internal Database IDs

The visible Intern ID and Employee ID will not be used as the internal database primary keys.

The database will maintain separate internal IDs.

Example:

```text
Database ID: 147
Intern ID: INT-2026-0025
```

Employee example:

```text
Database ID: 203
Employee ID: EMP-2027-0008
Previous Intern ID: INT-2026-0025
```

This provides a cleaner and more maintainable database design.

---

# ✨ Main Application Features

The application will contain the following major modules:

- Authentication
- Admin Dashboard
- Intern Management
- Employee Management
- Intern-to-Employee Conversion
- Attendance Management
- Training Management
- Project Management
- Performance Reviews
- Document Management
- Reports
- Certificate Management
- User Management

---

# 🔐 Authentication & Authorization

The system will include secure authentication.

Features:

- Admin Login
- HR Login
- Logout
- Password Hashing
- Session Management
- Protected Routes
- Role-Based Access
- Unauthorized Access Protection

Possible roles:

```text
Admin
HR
Manager
Employee
Intern
```

Different users can receive different permissions.

---

# 📊 Admin / HR Dashboard

The dashboard will provide an overview of the organization.

Example:

```text
┌────────────────────┐
│ Total Interns      │
│        25          │
└────────────────────┘

┌────────────────────┐
│ Active Interns     │
│        18          │
└────────────────────┘

┌────────────────────┐
│ Total Employees    │
│        12          │
└────────────────────┘

┌────────────────────┐
│ Active Employees   │
│        11          │
└────────────────────┘

┌────────────────────┐
│ Intern → Employee  │
│         5          │
└────────────────────┘
```

The dashboard will also show:

- Recent Interns
- Recent Employees
- Interns Completing Soon
- Attendance Summary
- Project Status
- Training Status
- Recent Conversions
- Performance Reviews
- Recent Activities

---

# 👨‍🎓 Intern Management

HR/Admin will be able to:

- Add Intern
- Automatically Generate Intern ID
- View Interns
- Search Interns
- View Intern Profile
- Edit Intern
- Update Internship Status
- Track Internship Duration
- Assign Department
- Assign Mentor
- Manage Attendance
- Assign Training
- Assign Projects
- Add Performance Reviews
- Manage Documents
- Complete Internship
- Convert Intern to Employee

Intern information may include:

```text
Intern ID
Full Name
Email
Phone Number
Date of Birth
Address
College
Degree
Specialization
Graduation Year
Skills
Certificates
Department
Mentor
Internship Start Date
Internship End Date
Internship Duration
Internship Status
```

Possible statuses:

```text
Active
Completed
Discontinued
Converted to Employee
```

---

# 👨‍💼 Employee Management

HR/Admin will be able to:

- Add Employee
- Automatically Generate Employee ID
- Convert Intern to Employee
- View Employees
- Search Employees
- Edit Employee
- View Employee Profile
- Assign Department
- Assign Designation
- Set Employment Type
- Manage Attendance
- Assign Projects
- Add Performance Reviews
- Manage Documents
- Update Employment Status

Employee information may include:

```text
Employee ID
Previous Intern ID
Full Name
Email
Phone
Department
Designation
Joining Date
Employment Type
Manager
Employment Status
```

Possible employment types:

```text
Full-Time
Part-Time
Contract
Temporary
```

Possible employee statuses:

```text
Active
Probation
Notice Period
Resigned
Terminated
Inactive
```

---

# 🔄 Convert Intern to Employee

One of the core application features will be:

```text
Convert to Employee
```

Example:

```text
Intern Profile
────────────────────────────

Name:
Rahul Kumar

Intern ID:
INT-2026-0015

Department:
SOC

Internship Status:
Completed


[ Convert to Employee ]
```

After conversion:

```text
Employee Profile
────────────────────────────

Name:
Rahul Kumar

Employee ID:
EMP-2027-0008

Previous Intern ID:
INT-2026-0015

Department:
SOC

Designation:
SOC Analyst

Employment Type:
Full-Time

Status:
Active
```

During conversion, the system will:

- Generate Employee ID
- Preserve Intern ID
- Preserve Personal Information
- Preserve Internship Attendance
- Preserve Training History
- Preserve Projects
- Preserve Performance Reviews
- Preserve Documents
- Record Employee Joining Date
- Set Department
- Set Designation
- Set Employment Type
- Update Internship Status to `Converted to Employee`

---

# 📜 Complete Person History

The application will maintain the complete history of each person.

Example:

```text
PERSON PROFILE
────────────────────────────

Name:
Rahul Kumar


CURRENT EMPLOYMENT
────────────────────────────

Employee ID:
EMP-2027-0008

Designation:
SOC Analyst

Department:
SOC

Employment Status:
Active


PREVIOUS INTERNSHIP
────────────────────────────

Intern ID:
INT-2026-0015

Internship Period:
01-Jul-2026 → 31-Dec-2026

Internship Status:
Converted to Employee

Attendance:
94%

Projects Completed:
4

Training Completed:
8
```

---

# 📅 Attendance Management

Attendance will be available for interns and employees.

Attendance statuses:

```text
P   - Present
A   - Absent
L   - Leave
WFH - Work From Home
OD  - On Duty
```

Features:

- Mark Daily Attendance
- Edit Attendance
- View Attendance
- Attendance History
- Monthly Attendance
- Attendance Percentage
- Intern Attendance
- Employee Attendance
- Attendance Reports

---

# 📚 Training Management

Training modules can be assigned to interns and employees.

Possible training topics:

- Linux
- Networking
- Git
- GitHub
- AWS
- Docker
- Jenkins
- Terraform
- Cybersecurity
- SOC
- SIEM
- Splunk
- Wazuh
- VAPT
- DevOps
- Cloud Security

Features:

- Create Training
- Assign Training
- Training Date
- Trainer
- Attendance
- Completion Status
- Training Remarks

---

# 📁 Project Management

The application will support project management.

Features:

- Create Project
- Assign Project
- Assign Intern
- Assign Employee
- Project Start Date
- Project End Date
- Project Description
- Project Status
- Progress Tracking
- Project Remarks
- Completed Projects

Possible project statuses:

```text
Not Started
In Progress
On Hold
Completed
Cancelled
```

---

# ⭐ Performance Reviews

Managers/HR will be able to review interns and employees.

Features:

- Performance Rating
- Technical Skills
- Communication
- Attendance
- Teamwork
- Task Completion
- Learning Ability
- Manager Feedback
- HR Feedback
- Final Remarks

Performance information can help HR decide whether an intern should be converted into an employee.

---

# 📄 Document Management

The system can maintain references to important documents.

Intern documents may include:

- Government ID
- College ID
- Resume
- NDA
- Internship Agreement
- No Objection Letter
- Certificates

Employee documents may include:

- Government ID
- Resume
- Offer Letter
- Appointment Letter
- NDA
- Education Certificates
- Experience Documents

Sensitive documents and secrets must not be stored directly in the public Git repository.

---

# 🏆 Certificate Management

Planned features:

- Internship Completion Certificate
- Certificate Number
- Intern Name
- Intern ID
- Internship Duration
- Department
- Completion Date
- Certificate Generation
- Certificate Download

---

# 📈 Reports

The portal will eventually support reports such as:

- Intern Report
- Employee Report
- Attendance Report
- Monthly Attendance Report
- Project Report
- Training Report
- Internship Completion Report
- Intern-to-Employee Conversion Report
- Performance Report

---

# 🛠️ Technology Stack

| Category | Technology |
|---|---|
| Frontend | HTML5 |
| Styling | CSS3 |
| UI Framework | Bootstrap 5 |
| Frontend Logic | JavaScript |
| Backend | Python |
| Web Framework | Flask |
| Template Engine | Jinja2 |
| Database | SQLite |
| Version Control | Git |
| Source Code Management | GitHub |
| Containerization | Docker |
| CI/CD | Jenkins |
| Infrastructure as Code | Terraform |
| Cloud Platform | AWS |
| Cloud Server | AWS EC2 |
| Reverse Proxy | Nginx |

---

# 📂 Project Structure

```text
Secure369-Portal/
│
├── app/
│   ├── app.py
│   │
│   └── templates/
│       └── index.html
│
├── static/
│   ├── css/
│   ├── js/
│   └── images/
│
├── database/
│
├── terraform/
│
├── nginx/
│
├── docs/
│
├── tests/
│
├── Dockerfile
├── Jenkinsfile
├── requirements.txt
├── README.md
└── .gitignore
```

The project structure will expand as new modules are developed.

---

# 🗄️ Planned Database Design

The database will eventually contain tables such as:

```text
users
people
interns
employees
departments
attendance
projects
project_assignments
training
training_assignments
performance_reviews
documents
certificates
activity_logs
```

---

# 👤 People Table

Common personal information can be stored separately.

Example:

```text
people

id
first_name
last_name
email
phone
date_of_birth
address
created_at
updated_at
```

---

# 👨‍🎓 Interns Table

Example:

```text
interns

id
person_id
intern_id
department_id
mentor_id
start_date
end_date
status
created_at
updated_at
```

Example Intern ID:

```text
INT-2026-0001
```

---

# 👨‍💼 Employees Table

Example:

```text
employees

id
person_id
employee_id
previous_intern_id
department_id
designation
joining_date
employment_type
status
created_at
updated_at
```

Example Employee ID:

```text
EMP-2027-0008
```

---

# 🔗 Database Relationship Concept

A person can start as an intern and later become an employee.

```text
PERSON
  │
  ├───────────────┐
  │               │
  ▼               ▼
INTERN         EMPLOYEE

INT-2026-0015  EMP-2027-0008
```

Both records belong to the same person.

This allows the application to preserve the complete history.

---

# 🎓 What I Will Learn & Implement

This project provides hands-on experience across application development, DevOps, Infrastructure as Code, and cloud deployment.

---

# 🐍 Python

Python will be used to:

- Build Backend Logic
- Create Functions
- Create Modules
- Process User Input
- Validate Data
- Generate Intern IDs
- Generate Employee IDs
- Connect to Database
- Perform CRUD Operations
- Handle Application Errors
- Implement Business Logic

---

# 🌐 Flask

Flask will be used to:

- Build the Web Application
- Create Routes
- Handle HTTP Requests
- Return HTTP Responses
- Render HTML Templates
- Use Jinja2
- Process Forms
- Implement Authentication
- Manage Sessions
- Protect Routes
- Connect to Database
- Build Admin Dashboard
- Build Intern Management
- Build Employee Management
- Implement Intern-to-Employee Conversion
- Build Attendance Management
- Build Project Management

---

# 🎨 HTML, CSS, Bootstrap & JavaScript

Frontend technologies will be used to:

- Build Web Pages
- Create Navigation
- Create Forms
- Create Tables
- Create Dashboard Cards
- Build Responsive Pages
- Create Login Screens
- Create Intern Profiles
- Create Employee Profiles
- Add Interactive Features
- Make the Application Mobile-Friendly

---

# 🗄️ Database

SQLite will initially be used during development.

The application will learn and implement:

- Tables
- Columns
- Rows
- Primary Keys
- Foreign Keys
- Relationships
- Constraints
- Queries
- CRUD Operations

CRUD means:

```text
Create
Read
Update
Delete
```

---

# 📂 Git & GitHub

Git and GitHub will be used for source code management.

I will learn and use:

```text
git status
git add
git commit
git push
git pull
git branch
git switch
git merge
```

Development workflow:

```text
VS Code
   │
   ▼
Git
   │
   ▼
GitHub
```

---

# 🐳 Docker

Docker will be used to containerize the application.

I will learn:

- Dockerfile
- Docker Images
- Docker Containers
- Docker Build
- Docker Run
- Docker Ports
- Docker Volumes
- Docker Networks
- Container Logs
- Container Management

Application flow:

```text
Flask Application
       │
       ▼
Docker Image
       │
       ▼
Docker Container
       │
       ▼
AWS EC2
```

---

# ⚙️ Jenkins

Jenkins will be used for CI/CD automation.

I will learn:

- Jenkins Installation
- Jenkins Configuration
- Jenkins Plugins
- Jenkins Pipeline
- Jenkinsfile
- GitHub Integration
- Automated Testing
- Docker Builds
- Automated Deployment

Planned pipeline:

```text
GitHub
   │
   ▼
Jenkins
   │
   ├── Checkout Code
   ├── Install Dependencies
   ├── Run Tests
   ├── Build Docker Image
   ├── Deploy Application
   └── Verify Deployment
```

---

# 🏗️ Terraform

Terraform will be used for Infrastructure as Code.

Instead of manually creating all AWS infrastructure, Terraform configuration files will automate infrastructure provisioning.

I will learn:

- Providers
- Resources
- Variables
- Outputs
- Terraform State
- Infrastructure Planning
- Infrastructure Deployment

Important commands:

```bash
terraform init
terraform fmt
terraform validate
terraform plan
terraform apply
terraform destroy
```

Terraform will eventually provision:

```text
AWS
│
├── VPC
├── Public Subnet
├── Internet Gateway
├── Route Table
├── Security Group
└── EC2 Instance
```

---

# ☁️ AWS

AWS will host the application.

The project will use free or Free Tier eligible resources wherever practical while monitoring usage to avoid unnecessary charges.

I will learn:

- EC2
- IAM
- VPC
- Subnets
- Internet Gateway
- Route Tables
- Security Groups
- SSH
- Linux Server Management
- Cloud Deployment

---

# 🌐 Nginx

Nginx will act as the reverse proxy.

Instead of exposing Flask's development port directly:

```text
5000
```

users will access the application through standard web ports:

```text
HTTP  → 80
HTTPS → 443
```

Architecture:

```text
Internet
   │
   ▼
Nginx
   │
   ▼
Flask Application
   │
   ▼
Database
```

---

# 🔐 DevOps & Cloud

Through this project, I will gain hands-on experience with:

- Software Development Lifecycle
- Version Control
- Web Development
- Database Management
- Linux
- Containerization
- CI/CD
- Infrastructure as Code
- AWS
- Cloud Deployment
- Reverse Proxy
- Application Logs
- Monitoring
- Troubleshooting
- Deployment Automation

---

# 🏗️ Current Architecture

Current development architecture:

```text
Browser
   │
   │ HTTP Request
   ▼
Flask
   │
   ▼
Jinja2
   │
   ▼
HTML Template
   │
   ▼
Browser
```

---

# 🚀 Planned Production Architecture

```text
Developer
   │
   │ git push
   ▼
GitHub
   │
   ▼
Jenkins
   │
   ├── Checkout
   ├── Test
   ├── Build
   └── Deploy
         │
         ▼
       AWS EC2
         │
         ▼
       Docker
         │
         ▼
       Nginx
         │
         ▼
       Flask
         │
         ▼
      Database
         │
         ▼
        Users
```

Terraform will manage the AWS infrastructure:

```text
Terraform
   │
   ▼
AWS
   │
   ├── VPC
   ├── Subnet
   ├── Internet Gateway
   ├── Route Table
   ├── Security Group
   └── EC2
```

---

# 🗺️ Complete Development Roadmap

## Phase 1 — Project Setup

- [x] Create Project Folder
- [x] Initialize Git
- [x] Create GitHub Repository
- [x] Connect Local Repository to GitHub
- [x] Create Initial Project Structure
- [x] Install Python
- [x] Install Flask
- [x] Push Initial Code to GitHub
- [x] Create Project README

---

## Phase 2 — Flask Basics

- [x] Create Flask Application
- [x] Start Flask Development Server
- [x] Create Home Route
- [x] Understand Localhost
- [x] Understand Port 5000
- [x] Create HTML Template
- [x] Configure Templates Folder
- [x] Use `render_template()`
- [x] Add Bootstrap
- [x] Build Basic Homepage

---

## Phase 3 — Frontend

- [ ] Create Base Template
- [ ] Professional Navigation Bar
- [ ] Home Page
- [ ] About Page
- [ ] Login Page
- [ ] Contact Page
- [ ] Custom CSS
- [ ] JavaScript
- [ ] Responsive Design

---

## Phase 4 — Database

- [ ] Configure SQLite
- [ ] Create Database
- [ ] Create People Table
- [ ] Create Users Table
- [ ] Create Departments Table
- [ ] Create Interns Table
- [ ] Create Employees Table
- [ ] Create Attendance Table
- [ ] Create Projects Table
- [ ] Create Training Table
- [ ] Create Performance Reviews Table
- [ ] Create Documents Table
- [ ] Create Relationships
- [ ] Implement CRUD Operations

---

## Phase 5 — Authentication & Roles

- [ ] Admin Login
- [ ] HR Login
- [ ] Logout
- [ ] Password Hashing
- [ ] Sessions
- [ ] Protected Routes
- [ ] Role-Based Access Control

---

## Phase 6 — Intern Management

- [ ] Intern Registration
- [ ] Automatic Intern ID Generation
- [ ] Intern List
- [ ] Intern Search
- [ ] Intern Profile
- [ ] Edit Intern
- [ ] Internship Start Date
- [ ] Internship End Date
- [ ] Department Assignment
- [ ] Mentor Assignment
- [ ] Internship Status
- [ ] Internship Completion

---

## Phase 7 — Employee Management

- [ ] Employee Registration
- [ ] Automatic Employee ID Generation
- [ ] Employee List
- [ ] Employee Search
- [ ] Employee Profile
- [ ] Edit Employee
- [ ] Department Assignment
- [ ] Designation
- [ ] Employment Type
- [ ] Joining Date
- [ ] Employee Status

---

## Phase 8 — Intern to Employee Conversion

- [ ] Convert Intern to Employee
- [ ] Generate Employee ID
- [ ] Link Employee to Previous Intern Record
- [ ] Preserve Internship History
- [ ] Preserve Attendance
- [ ] Preserve Training
- [ ] Preserve Projects
- [ ] Preserve Performance Reviews
- [ ] Transfer Personal Information
- [ ] Set Employee Joining Date
- [ ] Set Department
- [ ] Set Designation
- [ ] Set Employment Type
- [ ] Update Intern Status
- [ ] Display Complete Person History

---

## Phase 9 — Attendance Management

- [ ] Daily Attendance
- [ ] Present
- [ ] Absent
- [ ] Leave
- [ ] Work From Home
- [ ] On Duty
- [ ] Attendance History
- [ ] Attendance Percentage
- [ ] Monthly Attendance
- [ ] Attendance Reports

---

## Phase 10 — Training Management

- [ ] Create Training
- [ ] Assign Training
- [ ] Assign Trainer
- [ ] Training Attendance
- [ ] Training Completion
- [ ] Training Remarks
- [ ] Training History

---

## Phase 11 — Project Management

- [ ] Create Projects
- [ ] Assign Interns
- [ ] Assign Employees
- [ ] Project Start Date
- [ ] Project End Date
- [ ] Project Status
- [ ] Progress Tracking
- [ ] Project Remarks
- [ ] Project History

---

## Phase 12 — Performance Management

- [ ] Intern Performance Review
- [ ] Employee Performance Review
- [ ] Ratings
- [ ] Manager Feedback
- [ ] HR Feedback
- [ ] Final Remarks
- [ ] Performance History

---

## Phase 13 — Documents & Certificates

- [ ] Document Management
- [ ] Internship Documents
- [ ] Employee Documents
- [ ] Certificate Number Generation
- [ ] Internship Completion Certificate
- [ ] Certificate Download

---

## Phase 14 — Reports

- [ ] Intern Reports
- [ ] Employee Reports
- [ ] Attendance Reports
- [ ] Training Reports
- [ ] Project Reports
- [ ] Performance Reports
- [ ] Conversion Reports

---

## Phase 15 — Testing

- [ ] Flask Route Tests
- [ ] Database Tests
- [ ] Authentication Tests
- [ ] Intern ID Tests
- [ ] Employee ID Tests
- [ ] Conversion Tests
- [ ] Application Validation

---

## Phase 16 — Docker

- [ ] Create Dockerfile
- [ ] Build Docker Image
- [ ] Run Docker Container
- [ ] Configure Ports
- [ ] Configure Environment Variables
- [ ] Configure Volumes
- [ ] View Docker Logs
- [ ] Containerize Flask Application

---

## Phase 17 — AWS

- [ ] Configure AWS CLI
- [ ] Configure IAM
- [ ] Create VPC
- [ ] Create Public Subnet
- [ ] Create Internet Gateway
- [ ] Create Route Table
- [ ] Create Security Group
- [ ] Launch EC2
- [ ] SSH into EC2
- [ ] Configure Linux Server

---

## Phase 18 — Terraform

- [ ] Configure AWS Provider
- [ ] Create Variables
- [ ] Create Outputs
- [ ] Create VPC
- [ ] Create Subnet
- [ ] Create Internet Gateway
- [ ] Create Route Table
- [ ] Create Security Group
- [ ] Provision EC2
- [ ] Terraform Format
- [ ] Terraform Validate
- [ ] Terraform Plan
- [ ] Terraform Apply
- [ ] Terraform Destroy

---

## Phase 19 — Jenkins CI/CD

- [ ] Install Jenkins
- [ ] Configure Jenkins
- [ ] Install Required Plugins
- [ ] Connect Jenkins to GitHub
- [ ] Create Jenkinsfile
- [ ] Create Pipeline
- [ ] Checkout Source Code
- [ ] Install Dependencies
- [ ] Run Tests
- [ ] Build Docker Image
- [ ] Deploy Application
- [ ] Verify Deployment

---

## Phase 20 — Production Deployment

- [ ] Install Docker on EC2
- [ ] Deploy Application Container
- [ ] Install Nginx
- [ ] Configure Reverse Proxy
- [ ] Configure Ports
- [ ] Configure Domain
- [ ] Configure HTTPS
- [ ] Test Production Application

---

## Phase 21 — Monitoring & Maintenance

- [ ] Application Health Checks
- [ ] Docker Logs
- [ ] Nginx Logs
- [ ] Server Logs
- [ ] Basic Monitoring
- [ ] Database Backup
- [ ] Troubleshooting Documentation

---

# 📊 Current Project Progress

```text
Project Setup          ██████████ 100% ✅
Flask Basics           ██████████ 100% ✅
Frontend               ██░░░░░░░░  20% 🚧
Database               ░░░░░░░░░░   0%
Authentication         ░░░░░░░░░░   0%
Intern Management      ░░░░░░░░░░   0%
Employee Management    ░░░░░░░░░░   0%
Attendance             ░░░░░░░░░░   0%
Projects               ░░░░░░░░░░   0%
Docker                 ░░░░░░░░░░   0%
AWS                    ░░░░░░░░░░   0%
Terraform              ░░░░░░░░░░   0%
Jenkins                ░░░░░░░░░░   0%
Production             ░░░░░░░░░░   0%
```

---

# ▶️ Run the Application Locally

Clone the repository:

```bash
git clone https://github.com/vedavyas369/Secure369-Portal.git
```

Enter the project directory:

```bash
cd Secure369-Portal
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Start the Flask application:

```bash
python app/app.py
```

Open the application in the browser:

```text
http://127.0.0.1:5000
```

---

# 🔄 Git Development Workflow

Check changes:

```bash
git status
```

Add changes:

```bash
git add .
```

Commit:

```bash
git commit -m "Describe what was changed"
```

Push:

```bash
git push
```

Workflow:

```text
VS Code
   │
   ▼
Git
   │
   ▼
GitHub
```

Final workflow:

```text
VS Code
   │
   ▼
Git
   │
   ▼
GitHub
   │
   ▼
Jenkins
   │
   ▼
Docker
   │
   ▼
AWS EC2
   │
   ▼
Nginx
   │
   ▼
Flask Application
```

---

# 🏁 Final Project Outcome

After completing this project, I will have built a complete:

## Secure369 Intern & Employee Management Portal

The system will manage the complete lifecycle:

```text
Candidate
    ↓
Intern
    ↓
Training
    ↓
Attendance
    ↓
Projects
    ↓
Performance
    ↓
Internship Completion
    ↓
Employee Conversion
    ↓
Full-Time Employee
    ↓
Employee Management
```

The project will demonstrate practical experience with:

- Python
- Flask
- HTML
- CSS
- Bootstrap
- JavaScript
- Jinja2
- SQLite
- Database Design
- Authentication
- Role-Based Access
- Git
- GitHub
- Docker
- Jenkins
- Terraform
- AWS
- EC2
- Nginx
- CI/CD
- Infrastructure as Code
- Cloud Deployment
- Monitoring
- Troubleshooting

---

# 👨‍💻 Author

**Vedavyas**

Building and learning through hands-on implementation of:

☁️ **AWS** — Cloud infrastructure and application deployment

🐳 **Docker** — Application containerization

⚙️ **Jenkins** — CI/CD pipeline and deployment automation

🏗️ **Terraform** — Infrastructure as Code for AWS

🐍 **Python** — Backend programming and business logic

🌐 **Flask** — Web application development

🗄️ **Database** — Intern, employee, attendance, project and training data

📂 **Git & GitHub** — Version control and source code management

🔐 **DevOps & Cloud** — Development, automation, infrastructure, deployment, monitoring and troubleshooting

---

# 📌 Project Note

This repository documents the complete hands-on development journey of the Secure369 Intern & Employee Management Portal.

The application will be continuously improved as new modules, DevOps tools, AWS infrastructure, automation, security controls, testing and deployment stages are implemented.

The goal is not only to build the application, but also to understand how a real application moves through the complete lifecycle:

```text
Plan
  ↓
Develop
  ↓
Test
  ↓
Version Control
  ↓
Build
  ↓
Containerize
  ↓
Provision Infrastructure
  ↓
Deploy
  ↓
Monitor
  ↓
Improve
```