# CBT Exam Web Application

## Overview
The CBT Exam Web Application is a modern, scalable web-based system designed to conduct computer-based tests for students and provide administrators with tools to manage exams, questions, and results.
The system follows a React + API Gateway + Backend Services architecture to support scalability, performance, and security.

## System Architecture
The application is built using a client–server model with separated frontend and backend services.

Client (Browser)
    ↓
React Frontend
    ↓
API Gateway
    ↓
Backend Services
    ↓
PostgreSQL Database

## User Roles
The system supports two primary user roles:
- Student
- Administrator

## Functional Features
### Authentication & Authorization
- User registration and login
- JWT-based authentication
- Role-based route protection
- Secure logout mechanism

## Student Features

- View available exams
- Start and take exams
- Timed exam sessions
- Multiple-choice questions
- Automatic submission when time expires
- Automatic score calculation
- View exam results

## Admin Features

- Create, update, and delete exams
- Add, edit, and remove questions
- Set exam duration
- Publish or unpublish exams
- View student submissions
- Access exam results and statistics

## Exam Management

- Support for multiple exams
- Support for multiple questions per exam
- Each question contains multiple options with one correct answer
- Exam visibility control (published/unpublished)

## Non-Functional Requirements
⚡ Performance

Supports concurrent users

Fast loading of exam questions

🔒 Security

All API endpoints are protected

HTTPS enforced for data transmission

Password hashing before storage

Unauthorized access is denied

📈 Scalability

Modular backend services

Horizontal scalability support

🧩 Reliability

Prevents loss of exam data during submission

Graceful error handling

🧰 Tech Stack
Frontend

HTML5

CSS3

JavaScript (ES6+)

React.js

React Router

Axios / Fetch API

Backend

Node.js

Express.js

RESTful API

JWT Authentication

Middleware-based architecture

Database

PostgreSQL

ORM: Prisma or Sequelize

Infrastructure

API Gateway

Nginx (Reverse Proxy)

Environment variables (.env)

CI/CD with GitHub Actions

🔌 API Endpoints
Authentication
POST /api/auth/register
POST /api/auth/login

Exams
GET    /api/exams
GET    /api/exams/{id}
POST   /api/admin/exams
PUT    /api/admin/exams/{id}
DELETE /api/admin/exams/{id}

Submissions & Results
POST /api/exams/{id}/submit
GET  /api/student/results
GET  /api/admin/results

🗄️ Database Design
Entities

Users

Exams

Questions

Options

Results

Relationships

A user can take multiple exams

An exam contains multiple questions

A question has multiple options

Each result belongs to one user and one exam

🌍 Deployment

Frontend deployed on a CDN-enabled platform

Backend deployed on a cloud server

PostgreSQL hosted on a managed database service

All services communicate over HTTPS

🧑‍💻 Development Workflow

Version control using Git

GitHub repository hosting

Branching strategy (main, develop)

Code linting and formatting

Unit and integration testing

🔮 Future Enhancements

Question randomization

Anti-cheating mechanisms

Real-time exam monitoring

Advanced analytics dashboard

📄 License

This project is licensed under the MIT License.
