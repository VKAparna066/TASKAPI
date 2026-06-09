# Scalable REST API with Authentication & Role-Based Access

## Overview

This project is a full-stack application built to demonstrate secure and scalable backend development practices. It includes JWT-based authentication, role-based authorization, CRUD operations for tasks, API documentation, validation, and a simple React frontend for interacting with the APIs.

## Features

### Backend

* User Registration
* User Login
* Password Hashing using bcrypt
* JWT Authentication
* Role-Based Access Control (User/Admin)
* CRUD Operations for Tasks
* API Versioning (`/api/v1`)
* Request Validation
* Global Error Handling
* Swagger API Documentation
* MongoDB Database Integration
* Structured Project Architecture
* Logging and Security Middleware

### Frontend

* User Registration Page
* User Login Page
* Protected Dashboard
* Create Task
* View Tasks
* Update Task
* Delete Task
* API Response Notifications

---

## Technology Stack

### Backend

* Node.js
* Express.js
* MongoDB Atlas
* Mongoose
* JWT
* bcryptjs
* express-validator
* Swagger UI

### Frontend

* React.js
* Vite
* Axios
* React Router

---

## Project Structure

```text
project-root/

backend/
├── src/
│   ├── config/
│   ├── controllers/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── validators/
│   └── server.js
├── .env
├── package.json

frontend/
├── src/
│   ├── components/
│   ├── pages/
│   ├── services/
│   └── App.jsx
├── package.json

README.md
```

## Installation

### Clone Repository

```bash
git clone <repository-url>
cd project-root
```

### Backend Setup

```bash
cd backend
npm install
```

Create a `.env` file:

```env
PORT=5000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
JWT_EXPIRES_IN=1d
```

Run backend:

```bash
npm run dev
```

Server runs on:

```text
http://localhost:5000
```

### Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

Frontend runs on:

```text
http://localhost:5173
```

---

## API Endpoints

### Authentication

#### Register User

```http
POST /api/v1/auth/register
```

#### Login User

```http
POST /api/v1/auth/login
```

### Tasks

#### Get All Tasks

```http
GET /api/v1/tasks
```

#### Get Task By ID

```http
GET /api/v1/tasks/:id
```

#### Create Task

```http
POST /api/v1/tasks
```

#### Update Task

```http
PUT /api/v1/tasks/:id
```

#### Delete Task

```http
DELETE /api/v1/tasks/:id
```

---

## Authentication

Protected routes require a JWT token in the Authorization header:

```http
Authorization: Bearer <token>
```

---

## Role-Based Access

### User

* Register
* Login
* Manage own tasks

### Admin

* View all users
* Manage all tasks
* Access admin-only routes

---

## Swagger Documentation

API documentation is available at:

```text
http://localhost:5000/api-docs
```

---

## Validation and Security

* Password hashing with bcrypt
* JWT authentication
* Request validation using express-validator
* Protected routes
* Role-based authorization
* Error handling middleware
* Input sanitization

---

## Scalability Considerations

The application is designed to support future scaling:

1. API versioning (`/api/v1`)
2. Modular folder structure
3. Stateless JWT authentication
4. Database indexing
5. Redis caching integration (future enhancement)
6. Docker containerization support
7. Load balancing support
8. Migration to microservices architecture when required

---

## Future Improvements

* Refresh Token Authentication
* Redis Caching
* Docker Deployment
* Rate Limiting
* Email Verification
* Password Reset
* CI/CD Pipeline
* Unit and Integration Testing

---

## Author

Developed as part of the Backend Developer Internship Assignment.
