# 🏡 Airbnb Clone - Backend

This is the **backend service** for the Airbnb Clone project, developed to simulate the server-side operations of a real-world rental platform. It provides APIs for user management, property listings, bookings, reviews, and payment processing.

---

## 📚 Table of Contents

- [Project Overview](#project-overview)
- [Tech Stack](#tech-stack)
- [Features](#features)
- [Installation](#installation)
- [Environment Variables](#environment-variables)
- [API Endpoints](#api-endpoints)
- [Database Schema](#database-schema)
- [Testing](#testing)
- [Security](#security)
- [Deployment](#deployment)
- [License](#license)

---

## 🚀 Project Overview

The goal of this backend is to power a full-stack Airbnb-like application by supporting the following:
- Secure registration & login for users and hosts.
- Property management by hosts.
- Search, filter, and booking system for guests.
- Payment integration using Stripe or PayPal.
- Review and rating system after booking completion.
- Admin tools for system-wide management.

---

## 🛠️ Tech Stack

| Layer         | Technology               |
|---------------|---------------------------|
| Language       | JavaScript / TypeScript   |
| Runtime        | Node.js                   |
| Framework      | Express.js                |
| Database       | PostgreSQL / MySQL        |
| ORM            | Sequelize / Prisma        |
| Authentication | JWT, OAuth 2.0            |
| File Storage   | AWS S3 / Cloudinary       |
| Payments       | Stripe / PayPal           |
| Email          | SendGrid / Mailgun        |
| Caching        | Redis (optional)          |
| Testing        | Jest / Supertest          |

---

## 🌟 Features

### 👤 User Management
- Registration/login via email/password or Google/Facebook OAuth.
- Role-based access: Guest, Host, Admin.
- Profile updates with avatar support.

### 🏠 Property Management
- Hosts can create, update, and delete listings.
- Listings support title, description, location, price, images, and amenities.

### 🔍 Search and Filter
- Filter properties by location, price, guests, and amenities.
- Search results are paginated for performance.

### 📅 Booking System
- Guests can book available properties for specific dates.
- Double-booking protection using date validation.
- Booking statuses: pending, confirmed, cancelled, completed.

### 💳 Payments
- Stripe/PayPal integration.
- Guest payment at booking.
- Host payout after stay completion.
- Multi-currency support.

### ⭐ Reviews
- Only verified users can leave reviews.
- Hosts can respond to reviews.

### 🔔 Notifications
- Email alerts for bookings, payments, cancellations.
- In-app notification system (optional).

### 🛡️ Admin Dashboard
- Monitor users, bookings, properties, and financials.

---

## 🧰 Installation

```bash
git clone https://github.com/your-username/airbnb-clone-backend.git
cd airbnb-clone-backend
npm install
