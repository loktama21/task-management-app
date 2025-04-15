# 📋 Task Management Application Documentation

## 🧾 Table of Contents
1. [Overview](#overview)
2. [Features](#features)
3. [Tech Stack](#tech-stack)
4. [System Architecture](#system-architecture)
5. [Setup Instructions](#setup-instructions)
6. [API Endpoints](#api-endpoints)
7. [Database Schema](#database-schema)
8. [Authentication & Authorization](#authentication--authorization)
9. [Usage Guide](#usage-guide)
10. [Testing](#testing)
11. [Deployment](#deployment)
14. [License](#license)

---

## 🔍 Overview
A full-stack Task Management App that allows users to sign up, create, edit, delete, and manage their daily tasks.

---

## ✅ Features
- User registration & login
- Create, read, update, delete (CRUD) tasks
- Set due dates and task status
- Filter tasks (e.g., completed, pending)
- Secure authentication with JWT

---

## 🧰 Tech Stack
- **Frontend:** React + Tailwind CSS
- **Backend:** FastAPI (Python)
- **Database:** PostgreSQL
- **Auth:** JWT (JSON Web Tokens)
- **Hosting:** Heroku

---

## 🏗️ System Architecture

Authentication handled via JWT tokens in headers.

---

## 🛠️ Setup Instructions

### Prerequisites
- Node.js
- Python 3.9+
- PostgreSQL

### Steps
1. Clone the repo
2. Set up `.env` files for backend and frontend
3. Install dependencies
4. Run backend & frontend servers

---

## 📡 API Endpoints

| Method | Endpoint             | Description          | Auth Required |
|--------|----------------------|----------------------|---------------|
| POST   | /register            | Register new user    | No            |
| POST   | /login               | Authenticate user    | No            |
| GET    | /tasks               | Get all tasks        | Yes           |
| POST   | /tasks               | Create task          | Yes           |
| PUT    | /tasks/{id}          | Update task          | Yes           |
| DELETE | /tasks/{id}          | Delete task          | Yes           |

---

## 🗃️ Database Schema

### Users
- `id` (PK)
- `username`
- `email`
- `password_hash`

### Tasks
- `id` (PK)
- `title`
- `description`
- `status` (e.g., pending/completed)
- `due_date`
- `user_id` (FK to Users)

---

## 🔐 Authentication & Authorization
- JWT tokens are issued at login
- Token must be included in the `Authorization` header for protected routes

---

## 🧑‍💻 Usage Guide
1. Register a new user
2. Log in to receive a JWT token
3. Use token to interact with tasks (CRUD)
4. UI allows task creation, editing, filtering

---

## 🚀 Deployment
- Backend: Deploy with Heroku
- Frontend: Netlify
- Database: Use RDS

---

## 📄 License
MIT License – free to use and modify.

