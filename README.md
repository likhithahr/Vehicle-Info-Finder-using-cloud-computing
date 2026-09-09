# 🚗 Vehicle Info Finder

### ☁️ Cloud-Based Vehicle & Insurance Management System

A full-stack web application that helps users manage their **vehicle information, insurance and PUC expiry details, automated reminders, and insurance renewal** through a cloud-based architecture.

The application is built using the **MERN stack** and deployed using **AWS S3 and AWS EC2**, with **MongoDB Atlas** as the cloud database.

---

## 🌟 Overview

Vehicle Info Finder provides a centralized platform where users can:

- 🔐 Register and securely log in
- 🚘 Store and manage vehicle information
- 📋 Track insurance and PUC expiry dates
- 📧 Receive automated expiry reminder emails
- 💳 Renew insurance using a UPI QR-based payment flow
- 🧾 Generate and store payment receipts
- ☁️ Access the application through cloud-hosted services

The system follows a layered architecture where the React frontend communicates with the Node.js/Express backend through REST APIs, while the backend communicates with MongoDB Atlas for data storage.

---

## ✨ Key Features

### 🔐 User Authentication
- User registration and login
- Backend-based authentication
- Authentication data stored in MongoDB Atlas

### 🚘 Vehicle Management
- Add and manage vehicle information
- Store vehicle number, make, model and year
- Track insurance and PUC expiry dates

### 📧 Automated Expiry Reminders
- Scheduled backend jobs check upcoming expiry dates
- Reminder emails are triggered when an expiry is approaching
- Reminder history can be maintained in the database

### 💳 Insurance Renewal
- Enter insurance and vehicle details
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

'''text

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



#🛠️ Technology Stack
Technology	Purpose
⚛️ React.js	Frontend user interface
🟢 Node.js	Backend JavaScript runtime
🚂 Express.js	REST API and backend framework
🍃 MongoDB Atlas	Cloud database
☁️ AWS S3	React frontend hosting
☁️ AWS EC2	Backend server hosting
🔐 AWS IAM	AWS access and permissions
📧 NodeMailer	Email notifications
⏰ Cron Jobs	Scheduled expiry checks
💳 UPI QR	Insurance renewal payment flow
🔑 JWT	Authentication


#🔄 Major Workflows
🔐 Registration & Login
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

#🚘 Vehicle Information
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
  
#📧 Automated Expiry Reminder

The application uses scheduled backend jobs to check vehicle expiry information.

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

The reminder system checks upcoming insurance expiry dates and triggers an email when the expiry is within the configured reminder period.

#💳 Insurance Renewal
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

Note: The current implementation uses user confirmation for payment completion rather than live payment-gateway verification.



#☁️ AWS Cloud Deployment
Frontend — AWS S3

The React application is built and hosted as a static website using Amazon S3.

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

#Deployment Steps
Build the React application.
Create an S3 bucket.
Enable static website hosting.
Upload the generated build files.
Configure the required bucket access policy.
Access the frontend through the generated public URL.
Backend — AWS EC2

The Node.js and Express backend is deployed on an AWS EC2 virtual server.

Node.js + Express
       ↓
     AWS EC2
       ↓
   Backend APIs
       ↓
 MongoDB Atlas

The backend was first developed and tested locally before being deployed to EC2.



#🗄️ Database

The application uses MongoDB Atlas, a cloud-hosted MongoDB service.

Major data areas include:

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


#⚠️ Current Limitations
Vehicle details are entered manually.
UPI payment confirmation currently depends on user acknowledgment.
There is no live payment-gateway verification.
Email reminders depend on the backend server and scheduled jobs being available.
No two-factor or biometric authentication.
The current system is designed for individual users rather than large-scale fleet management.



#🚀 Future Improvements
🔗 Integrate RTO / government vehicle databases
💳 Integrate a secure payment gateway
✅ Add automatic payment verification
🔐 Implement two-factor authentication
📱 Improve mobile responsiveness
🚛 Add fleet-management functionality
📊 Add advanced vehicle analytics
☁️ Improve production scalability and monitoring

#<p align="center">
🚗 Vehicle Info Finder

Manage your vehicle. Track your insurance. Stay informed.

☁️ Built with MERN + AWS

</p> ```



