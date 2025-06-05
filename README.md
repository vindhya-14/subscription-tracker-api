
```markdown
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

```

Authorization: Bearer <your-token>

````

---

# 🔌 API Routes – Subscription Management System

This backend exposes a set of organized RESTful APIs for authentication, user management, subscriptions, and workflows (email reminders). Each router is modular and versioned under `/api/v1/`.

---

## 📁 Route Overview

| Module         | Route Prefix           | Description                            |
|----------------|------------------------|----------------------------------------|
| Auth           | `/api/v1/auth`         | Signup, Login, Logout                  |
| Users          | `/api/v1/users`        | User CRUD & profile fetching           |
| Subscriptions  | `/api/v1/subscriptions`| Subscription CRUD for authenticated users |
| Workflows      | `/api/v1/workflows`    | Trigger email reminder workflows       |

---

## 🔐 Auth Routes – `/api/v1/auth`

| Method | Endpoint      | Description        |
|--------|---------------|--------------------|
| POST   | `/sign-up`    | Register a new user |
| POST   | `/sign-in`    | Authenticate and return JWT |
| POST   | `/sign-out`   | Logout user (e.g. token blacklist) |

---

## 👤 User Routes – `/api/v1/users`

| Method | Endpoint       | Description            |
|--------|----------------|------------------------|
| GET    | `/`            | Get all users          |
| GET    | `/:id`         | Get a specific user (🔒 Protected) |
| POST   | `/`            | Create a new user (demo placeholder) |
| PUT    | `/:id`         | Update user (demo placeholder) |
| DELETE | `/:id`         | Delete user (demo placeholder) |

---

## 📦 Subscription Routes – `/api/v1/subscriptions`

| Method | Endpoint             | Description                        |
|--------|----------------------|------------------------------------|
| POST   | `/`                  | Create a new subscription (🔒 Protected) |
| GET    | `/user/:id`          | Get subscriptions by user (🔒 Protected) |

> 🚧 Additional routes like `PUT /:id`, `DELETE /:id`, or `GET /:id` can be uncommented/implemented as needed.

---

## 🔁 Workflow Routes – `/api/v1/workflows`

| Method | Endpoint                      | Description                      |
|--------|-------------------------------|----------------------------------|
| POST   | `/subscription/reminder`      | Trigger reminder emails workflow |

---

## 🔐 Authentication Middleware

Routes marked with **(🔒 Protected)** require a valid **JWT** in the `Authorization` header:

```http
Authorization: Bearer <your_token>


