# 📦 Subscription Management System API

A **production-ready backend API** built with **Node.js**, **Express**, and **MongoDB** for managing real-world subscriptions, users, and payments. This system supports authentication with JWT, automated email workflows, robust security, and scalable architecture.

---

## 🚀 Features

- ✅ **JWT Authentication** – Signup, Login, Secure access
- 📬 **Email Reminders** – Smart reminders using Upstash workflows
- 🛡️ **Advanced Rate Limiting & Bot Protection** – Powered by Arcjet
- 📚 **MongoDB + Mongoose ORM** – Well-structured schemas and relationships
- 🔄 **Subscription CRUD Operations** – Create, update, and cancel plans
- ⚙️ **Global Error Handling** – Middleware-driven clean error responses
- 🪵 **Logging System** – Debug and monitor with structured logs
- 🧩 **Scalable Code Architecture** – Clean folder and module separation

---

## 🛠️ Tech Stack

- **Node.js**
- **Express.js**
- **MongoDB**
- **Mongoose**
- **JWT for Authentication**
- **Upstash for Workflows**
- **Arcjet for Bot Protection**

---

## 🔐 Authentication

All protected routes require an `Authorization` header with a valid JWT token:

## API Endpoints

### Auth

| Method | Endpoint                  | Description         | Auth Required |
|--------|--------------------------|---------------------|--------------|
| POST   | `/api/v1/auth/sign-up`   | Register a new user | No           |
| POST   | `/api/v1/auth/sign-in`   | User login          | No           |
| POST   | `/api/v1/auth/sign-out`  | User logout         | No           |

---

### Subscriptions

| Method | Endpoint                              | Description                | Auth Required |
|--------|---------------------------------------|----------------------------|--------------|
| POST   | `/api/v1/subscriptions/`              | Create a subscription      | Yes          |
| GET    | `/api/v1/subscriptions/user/:id`      | Get user's subscriptions   | Yes          |

---

### Users

| Method | Endpoint                  | Description              | Auth Required |
|--------|--------------------------|--------------------------|--------------|
| GET    | `/api/v1/users/`         | List all users           | No           |
| GET    | `/api/v1/users/:id`      | Get user details         | Yes          |
| POST   | `/api/v1/users/`         | Create a new user (stub) | No           |
| PUT    | `/api/v1/users/:id`      | Update user (stub)       | No           |
| DELETE | `/api/v1/users/:id`      | Delete user (stub)       | No           |

---

### Workflow

| Method | Endpoint                                   | Description                   | Auth Required |
|--------|--------------------------------------------|-------------------------------|--------------|
| POST   | `/api/v1/workflow/subscription/reminder`   | Send subscription reminders   | No           |

---

## Middleware

- **authorize**: Protects routes that require authentication (JWT-based).

---
## General Note

This API is designed to be modular and scalable, making it easy to extend with new features and endpoints.  
Feel free to contribute, report issues, or suggest improvements. Your feedback is highly appreciated!

