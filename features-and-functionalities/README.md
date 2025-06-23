# 🏡 Airbnb Clone - Backend

Welcome to the **Airbnb Clone Backend** repository! This project replicates the backend architecture of the Airbnb platform, including user authentication, property management, bookings, payments, and more. It is designed to be scalable, secure, and modular — ideal for full-stack learning and portfolio building.

---

## 📌 Project Overview

This backend system powers a rental marketplace web app where:
- Hosts can list their properties.
- Guests can search and book accommodations.
- Admins can manage users, bookings, and payments.
- The system ensures secure logins, manages sessions, processes payments, and handles notifications.

---

## 📂 Tech Stack

| Layer            | Technology               |
|------------------|---------------------------|
| **Language**     | Node.js, TypeScript (or JavaScript) |
| **Framework**    | Express.js                |
| **Database**     | PostgreSQL or MySQL       |
| **ORM**          | Sequelize / Prisma        |
| **Authentication** | JWT + OAuth 2.0          |
| **Payments**     | Stripe / PayPal           |
| **File Storage** | AWS S3 / Cloudinary       |
| **Testing**      | Jest / Supertest / Postman |
| **Email**        | SendGrid / Mailgun        |

---

## ⚙️ Features & Functionalities

### 🔐 User Management
- Secure registration and login for hosts and guests.
- OAuth integration (Google, Facebook).
- Role-based access control (guest, host, admin).
- Profile editing and photo upload.

### 🏠 Property Listings
- Add, update, and delete listings.
- Manage availability, amenities, and pricing.
- Upload multiple images per property.

### 🔍 Search & Filtering
- Search by location, price range, amenities, and capacity.
- Support for pagination and sorting.

### 📅 Booking System
- Book property for specific dates.
- Conflict prevention with date validation.
- View and cancel bookings based on policies.
- Booking lifecycle: pending → confirmed → completed/cancelled.

### 💳 Payment Integration
- Stripe or PayPal gateway.
- Guest payments and automated host payouts.
- Multi-currency support.

### ⭐ Reviews & Ratings
- Leave and respond to reviews.
- Ensure only verified bookings can leave feedback.

### 📢 Notifications
- Email notifications for confirmations, cancellations, and payment updates.
- Optional in-app notification support.

### 🛠️ Admin Dashboard
- Manage users, properties, bookings, and transactions.
- View system statistics and logs.

---

## 🧱 Database Schema Overview

- **Users**: id, name, email, password, role, profile_image
- **Properties**: id, title, description, location, price, amenities, host_id
- **Bookings**: id, user_id, property_id, start_date, end_date, status
- **Payments**: id, booking_id, amount, currency, status
- **Reviews**: id, booking_id, rating, comment
- **Notifications**: id, user_id, type, message, read_status

---

## 🔐 Authentication & Authorization

- JWT-based secure token handling.
- OAuth 2.0 for third-party logins.
- Middleware-based role control for route access.

---

## 🚀 API Design

Follows **RESTful API** principles:
- `GET /properties`, `POST /bookings`, `PATCH /users/:id`
- Uses consistent status codes (`200`, `201`, `400`, `401`, `403`, `500`)
- JSON-based request/response bodies

---

## 🧪 Testing

- Unit and integration tests with **Jest** or **Mocha**.
- API testing using **Postman** collections or **Supertest**.

---

## 🧰 Getting Started

```bash
# Clone the repo
git clone https://github.com/RachidJedata/alx-airbnb-project-documentation.git

# Install dependencies
cd airbnb-clone-backend
npm install

# Setup environment variables
cp .env.example .env

# Start development server
npm run dev
