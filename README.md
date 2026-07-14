# 🎬 QuickShow - Movie & Event Booking Platform

<p align="center">
  <img src="https://img.shields.io/badge/React-19-blue?logo=react" />
  <img src="https://img.shields.io/badge/Node.js-Express-green?logo=node.js" />
  <img src="https://img.shields.io/badge/MongoDB-Database-green?logo=mongodb" />
  <img src="https://img.shields.io/badge/Stripe-Payments-635BFF?logo=stripe" />
  <img src="https://img.shields.io/badge/Clerk-Authentication-purple" />
  <img src="https://img.shields.io/badge/Inngest-Background_Jobs-black" />
  <img src="https://img.shields.io/badge/License-MIT-blue" />
</p>

## 🚀 Live Demo

🌐 **Website:** https://quick-show-frontend-tau.vercel.app/

---

# 📖 Overview

**QuickShow** is a modern full-stack **Movie & Event Ticket Booking Platform** inspired by BookMyShow. It provides a seamless booking experience with **real-time seat management, secure authentication, Stripe payments, QR ticket generation, automated seat release, waitlist management, and organizer/admin dashboards.**

The application is built using a scalable MERN architecture and demonstrates production-level concepts such as:

- Secure Authentication
- Concurrent Seat Booking Prevention
- Payment Processing
- Background Event Scheduling
- Email Notifications
- QR Ticket Generation
- Real-Time Seat Availability
- Admin & Organizer Management

---

# ✨ Features

## 👤 Customer Features

- User Registration & Login
- Browse Movies & Events
- Search and Filter Shows
- View Event Details
- Interactive Seat Selection
- Real-Time Seat Availability
- Temporary Seat Hold (Configurable TTL)
- Secure Stripe Payments
- Booking Confirmation
- QR Code Ticket via Email
- Booking History
- Booking Cancellation
- Join Waitlist for Sold-Out Shows

---

## 🎭 Organizer Features

- Register & Login
- Create Movies/Events
- Add Venue, Date & Time
- Configure Seat Categories
- Set Pricing per Category
- View Revenue Analytics
- Booking Summary Dashboard

---

## 🛠 Admin Features

- Manage Movies
- Manage Shows
- Manage Venues
- Configure Seat Layouts
- Configure Seat Categories
- Manage Users
- View All Bookings

---

## 🎟 Smart Booking System

- Real-Time Seat Status
    - ✅ Available
    - 🟡 Held
    - 🔴 Booked

- Configurable Seat Hold Timer (e.g. 10 Minutes)

- Automatic Hold Expiry

- Real-Time Seat Release

- Prevents Double Booking

- Booking Confirmation

- QR Ticket Generation

---

## ⏳ Waitlist Management

When an event becomes sold out:

- Customer can join waitlist
- Waitlist is maintained by seat category
- On cancellation:
    - Seat is offered to next customer
    - Email notification sent
    - Time-limited booking link generated
- If customer does not complete payment:
    - Seat automatically moves to next person

---

## 💳 Payment Integration

- Stripe Payment Gateway
- Secure Checkout
- Payment Intent
- Webhook Verification
- Booking Confirmation after Successful Payment

---

## 📧 Email Notifications

Automatic emails are sent for:

- Registration
- Booking Confirmation
- QR Ticket
- Waitlist Notification
- Seat Availability
- Booking Cancellation

---

# 🏗 Tech Stack

## Frontend

- React
- React Router
- Tailwind CSS
- Axios
- Clerk Authentication
- React Hot Toast

---

## Backend

- Node.js
- Express.js
- MongoDB
- Mongoose
- Clerk Authentication
- Stripe
- Inngest
- Nodemailer
- QR Code Generator

---

## APIs & Services

- TMDB API
- Stripe
- Clerk
- Inngest
- SMTP Email Service

---

# 📂 Project Structure

```text
quickshow/
│
├── client/                     # Frontend React application
│   ├── src/
│   │   ├── components/         # Reusable UI components
│   │   │   ├── admin/          # Admin-specific components
│   │   │   └── ...
│   │   ├── pages/              # Page components
│   │   │   ├── admin/          # Admin pages
│   │   │   └── ...
│   │   ├── context/            # React Context providers
│   │   ├── lib/                # Utility functions
│   │   └── assets/             # Static assets
│   ├── public/                 # Public assets
│   └── package.json
│
├── server/                     # Backend Node.js application
│   ├── controllers/            # Route controllers
│   ├── models/                 # MongoDB models
│   ├── routes/                 # API routes
│   ├── middleware/             # Custom middleware
│   ├── configs/                # Configuration files
│   ├── inngest/                # Background job handlers
│   └── package.json
│
└── README.md
```

---

# 🔄 Booking Workflow

```text
Browse Event
      │
      ▼
Select Seats
      │
      ▼
Seats Held for 10 Minutes
      │
      ▼
Stripe Payment
      │
      ▼
Booking Confirmed
      │
      ▼
QR Ticket Generated
      │
      ▼
Email Sent
```

---

# 🔐 Environment Variables

## Server (.env)

```env
# 🌐 Database
MONGODB_URI=mongodb://localhost:27017/quickshow

# 🔐 Clerk Authentication
CLERK_PUBLISHABLE_KEY=your-clerk-publishable-key
CLERK_SECRET_KEY=your-clerk-secret-key

# ⚙️ Inngest Event Scheduling
INNGEST_EVENT_KEY=your-inngest-event-key
INNGEST_SIGNING_KEY=your-inngest-signing-key

# 🎬 TMDB API
TMDB_API_KEY=your-tmdb-api-key

# 💳 Stripe
STRIPE_PUBLISHABLE_KEY=your-stripe-publishable-key
STRIPE_SECRET_KEY=your-stripe-secret-key
STRIPE_WEBHOOK_SECRET=your-stripe-webhook-secret

# 📧 Email
SENDER_EMAIL=your-sender@example.com
SMTP_USER=your-smtp-username
SMTP_PASS=your-smtp-password
```

---

## Client (.env)

```env
# Currency
VITE_CURRENCY=$

# Clerk
VITE_CLERK_PUBLISHABLE_KEY=your-clerk-publishable-key

# Backend URL
VITE_BASE_URL=http://localhost:3000

# TMDB Images
VITE_TMDB_IMAGE_BASE_URL=https://image.tmdb.org/t/p/original
```

---

# ⚙ Installation

Clone the repository

```bash
git clone https://github.com/yourusername/quickshow.git
```

Go to project

```bash
cd quickshow
```

Install Backend

```bash
cd server
npm install
```

Install Frontend

```bash
cd ../client
npm install
```

---

# ▶ Running the Project

### Terminal 1

```bash
cd server
npm run dev
```

### Terminal 2

```bash
cd client
npm run dev
```

---

# 🌍 Application URLs

| Service | URL |
|----------|-----|
| Frontend | http://localhost:5173 |
| Backend API | http://localhost:5000 |

---

# 👨‍💼 Admin Access

- Create an Admin account through the API or directly in MongoDB.
- Access the Admin Dashboard:

```
/admin
```

---

# 🧪 Testing

### Client

```bash
cd client
npm run test
```

### Server

```bash
cd server
npm run test
```

---

# 📚 API Documentation

## Authentication

| Method | Endpoint | Description |
|---------|----------|-------------|
| POST | `/api/users/register` | Register User |
| POST | `/api/users/login` | Login User |
| GET | `/api/users/profile` | Get Profile |
| PUT | `/api/users/profile` | Update Profile |

---

## Movies & Shows

| Method | Endpoint |
|---------|----------|
| GET | `/api/shows` |
| GET | `/api/shows/:id` |
| POST | `/api/admin/shows` |
| PUT | `/api/admin/shows/:id` |
| DELETE | `/api/admin/shows/:id` |

---

## Bookings

| Method | Endpoint |
|---------|----------|
| POST | `/api/bookings` |
| GET | `/api/bookings/user` |
| GET | `/api/admin/bookings` |
| PUT | `/api/bookings/:id` |

---

## Payments

| Method | Endpoint |
|---------|----------|
| POST | `/api/bookings/create-payment-intent` |
| POST | `/api/webhooks/stripe` |

---

# 📌 Future Improvements

- 🎭 Multiple Venue Support
- 📱 Progressive Web App (PWA)
- 📍 Google Maps Integration
- 🎟 Coupon & Discount System
- 📊 Advanced Analytics Dashboard
- ⭐ User Reviews & Ratings
- 🤖 AI-based Movie Recommendations
- 🌙 Dark Mode
- 📲 Mobile Application

---

# 👨‍💻 Author

**Gajanan Tongale**

📧 Email: **gajutongale@gmail.com**

💼 LinkedIn:
https://www.linkedin.com/in/gajanan-tongale/

🌐 Live Project:
https://quick-show-frontend-tau.vercel.app/

---

# ⭐ Support

If you found this project helpful, consider giving it a **⭐ Star** on GitHub. It helps others discover the project and motivates future improvements.

---

## 📄 License

This project is licensed under the **MIT License**.

---

<p align="center">
Made with ❤️ by <strong>Gajanan Tongale</strong>
</p>
