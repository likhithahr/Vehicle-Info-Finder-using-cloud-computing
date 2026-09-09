# 🚗 Vehicle Info Finder

### ☁️ Cloud-Based Vehicle & Insurance Management System

A full-stack web application that helps users manage **vehicle information, insurance and PUC expiry details, automated reminders, and insurance renewal** through a cloud-based architecture.

The application is built using the **MERN stack** and deployed using **AWS S3 and AWS EC2**, with **MongoDB Atlas** as the cloud database.

---

## 🌟 Overview

Vehicle Info Finder provides a centralized platform where users can:

- 🔐 Register and log in
- 🚘 Store and manage vehicle information
- 📋 Track insurance and PUC expiry dates
- 📧 Receive automated expiry reminder emails
- 💳 Renew insurance using a UPI QR-based payment flow
- 🧾 Generate and store payment receipts
- ☁️ Access the application through cloud-hosted services

The system follows a layered architecture where the React frontend communicates with the Node.js and Express backend through REST APIs, while the backend communicates with MongoDB Atlas for data storage.

---

## ✨ Key Features

### 🔐 User Authentication

- User registration and login
- Backend-based authentication
- Authentication data stored in MongoDB Atlas

### 🚘 Vehicle Management

- Add and manage vehicle information
- Store vehicle number, make, model, and year
- Track insurance and PUC expiry dates

### 📧 Automated Expiry Reminders

- Scheduled backend jobs check upcoming expiry dates
- Reminder emails are triggered when an expiry is approaching
- Reminder history can be maintained in the database

### 💳 Insurance Renewal

- Enter vehicle and insurance details
- Generate a UPI QR code
- Make payment using supported UPI applications
- Confirm the transaction
- Store payment information
- Generate a receipt

### ☁️ Cloud Deployment

- React frontend hosted using AWS S3
- Node.js + Express backend deployed on AWS EC2
- MongoDB Atlas used as the cloud database

---

# 🏗️ System Architecture

```text
                         👤 USER
                           │
                           ▼
                  ┌──────────────────┐
                  │ React Frontend   │
                  │    AWS S3        │
                  └────────┬─────────┘
                           │
                     HTTPS / REST API
                           │
                           ▼
                  ┌──────────────────┐
                  │ Node.js + Express│
                  │    AWS EC2       │
                  └────────┬─────────┘
                           │
                           ▼
                  ┌──────────────────┐
                  │  MongoDB Atlas   │
                  │  Cloud Database  │
                  └──────────────────┘
```

---

# 🛠️ Technology Stack

### Frontend

- **React.js** — User interface and frontend development

### Backend

- **Node.js** — Backend JavaScript runtime
- **Express.js** — REST API and backend framework

### Database

- **MongoDB Atlas** — Cloud-hosted database

### Cloud Services

- **AWS S3** — React frontend hosting
- **AWS EC2** — Node.js backend hosting
- **AWS IAM** — AWS access and permissions

### Other Technologies

- **NodeMailer** — Email notifications
- **Cron Jobs** — Scheduled expiry checks
- **JWT** — Authentication
- **UPI QR** — Insurance renewal payment flow

---

# 🔄 Major Workflows

## 🔐 Registration & Login

```text
User
 ↓
Signup / Login
 ↓
React Frontend
 ↓
Express API
 ↓
MongoDB Atlas
 ↓
Authentication
 ↓
Dashboard
```

---

## 🚘 Vehicle Information

```text
User enters vehicle details
          ↓
     React Frontend
          ↓
       REST API
          ↓
   Node.js + Express
          ↓
     MongoDB Atlas
          ↓
   Vehicle information
          ↓
    Displayed to user
```

---

## 📧 Automated Expiry Reminder

The application uses scheduled backend jobs to check vehicle expiry information.

```text
MongoDB Atlas
      ↓
   Cron Job
      ↓
Check expiry dates
      ↓
Expiry approaching?
      ↓
     YES
      ↓
   NodeMailer
      ↓
Email Notification
      ↓
     User
```

The reminder system checks upcoming vehicle expiry information and triggers an email when an expiry is within the configured reminder period.

---

## 💳 Insurance Renewal

```text
Insurance Page
      ↓
Enter vehicle + insurance details
      ↓
Generate UPI QR
      ↓
Scan using UPI application
      ↓
Complete payment
      ↓
User confirms payment
      ↓
Store payment details
      ↓
Generate receipt
```

> **Note:** The current implementation uses user confirmation for payment completion rather than live payment-gateway verification.

---

# ☁️ AWS Cloud Deployment

## Frontend — AWS S3

The React application is built and hosted as a static website using Amazon S3.

```text
React Application
       ↓
   npm build
       ↓
   Build Folder
       ↓
    AWS S3
       ↓
Static Website Hosting
       ↓
    Public URL
```

### Deployment Steps

1. Build the React application.
2. Create an S3 bucket.
3. Enable static website hosting.
4. Upload the generated build files.
5. Configure the required bucket access policy.
6. Access the frontend through the generated AWS public URL.

---

## Backend — AWS EC2

The Node.js and Express backend is deployed on an AWS EC2 virtual server.

```text
Node.js + Express
       ↓
     AWS EC2
       ↓
   Backend APIs
       ↓
 MongoDB Atlas
```

The backend was developed and tested locally before being deployed to AWS EC2.

---

# 🗄️ Database

The application uses **MongoDB Atlas** as the cloud database.

```text
MongoDB Atlas
│
├── Users
│   └── Authentication information
│
├── Vehicles
│   ├── Vehicle number
│   ├── Owner information
│   ├── Insurance details
│   └── PUC expiry
│
├── Email Logs
│   └── Reminder history
│
└── Insurance Payments
    └── Payment confirmation details
```

---

# 📁 Project Structure

```text
Vehicle-Info-Finder
│
├── vehicleproject-backend/
│   │
│   ├── models/
│   │   ├── Vehicle
│   │   ├── User
│   │   └── Payment
│   │
│   ├── routes/
│   │   ├── auth
│   │   ├── vehicles
│   │   └── insurance
│   │
│   ├── middleware/
│   │
│   ├── configuration/
│   │
│   └── uploads/
│       └── receipts
│
├── vehicleproject-frontend/
│   │
│   ├── components/
│   │   ├── Navbar
│   │   └── Input Forms
│   │
│   ├── pages/
│   │   ├── Login
│   │   ├── Signup
│   │   ├── Dashboard
│   │   └── Insurance
│   │
│   ├── App.js
│   └── App.css
│
└── README.md
```

---

# 🔌 REST API

The frontend communicates with the backend through REST APIs.

### Example API Endpoint

```http
GET /vehicles/:number
```

### API Flow

```text
React Frontend
      ↓
HTTP Request
      ↓
Express Route
      ↓
MongoDB Query
      ↓
JSON Response
      ↓
React Frontend
      ↓
Display Result
```

---

# 🧪 Development & Testing

The application was developed and tested locally before cloud deployment.

### Frontend

```text
React.js
localhost:3000
```

### Backend

```text
Node.js + Express.js
localhost:5001
```

The backend was connected to MongoDB Atlas during local testing to verify API operations and database communication before deployment to AWS EC2.

---

# 🎯 Project Objectives

- Build a cloud-based vehicle management platform
- Simplify vehicle information management
- Track insurance and PUC expiry dates
- Automate expiry notifications
- Provide a digital insurance renewal workflow
- Demonstrate full-stack MERN development
- Deploy application components using AWS cloud services

---

# ⚠️ Current Limitations

- Vehicle details are entered manually.
- UPI payment confirmation currently depends on user acknowledgment.
- There is no live payment-gateway verification.
- Email reminders depend on the backend server and scheduled jobs being available.
- No two-factor or biometric authentication.
- The current system is designed for individual users rather than large-scale fleet management.

---

# 🚀 Future Improvements

- 🔗 Integrate RTO / government vehicle databases
- 💳 Integrate a secure payment gateway
- ✅ Add automatic payment verification
- 🔐 Implement two-factor authentication
- 📱 Improve mobile responsiveness
- 🚛 Add fleet-management functionality
- 📊 Add advanced vehicle analytics
- ☁️ Improve production scalability and monitoring

---

# 💡 What I Learned

Through this project, I gained practical experience in:

- Full-stack MERN development
- REST API design
- Frontend-backend integration
- MongoDB Atlas
- AWS EC2 deployment
- AWS S3 static hosting
- Cloud-based application architecture
- Authentication and middleware
- Automated backend tasks
- Email automation
- UPI-based payment workflows
- Database integration

---

# 📌 Project Information

**Project:** Vehicle Info Finder using Cloud Computing

**Project Type:** Team Mini Project

**Domain:** Cloud Computing & Full-Stack Web Development

**Architecture:** MERN + AWS

---

<p align="center">

### 🚗 Vehicle Info Finder

**Manage your vehicle. Track your insurance. Stay informed.**

☁️ Built with MERN + AWS

</p>
