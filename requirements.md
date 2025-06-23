# 📑 Backend Requirement Specifications – Airbnb Clone

This document specifies the detailed functional and technical requirements for three key backend features: User Authentication, Property Management, and Booking System. Each section includes API endpoints, input/output formats, validation rules, and performance criteria.

---

## 🔐 1. User Authentication

### Objective
Allow users to register, log in, and manage sessions securely using JWT.

### API Endpoints

| Method | Endpoint          | Description             | Auth Required |
|--------|-------------------|-------------------------|---------------|
| POST   | `/api/auth/register` | Register a new user     | ❌            |
| POST   | `/api/auth/login`    | Authenticate and return token | ❌        |
| GET    | `/api/auth/profile`  | Fetch user profile      | ✅            |

### Input Specifications

**POST /api/auth/register**
```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "password": "Secret123!"
}
