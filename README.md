🔄 Application Workflow
🚘 Vehicle Information Flow


📧 Automated Insurance Reminder

The system checks vehicle insurance expiry information through a scheduled background task. When the expiry date is within the configured reminder period, an email notification is sent to the user.

💳 Insurance Renewal Flow

The current implementation uses user confirmation after the UPI transaction rather than live payment-gateway verification.

☁️ AWS Deployment
Frontend Deployment — AWS S3

The React frontend is deployed using AWS S3 static website hosting.

Backend Deployment — AWS EC2

The Node.js and Express.js backend is hosted on an AWS EC2 instance.

🗄️ Database

The application uses MongoDB Atlas as its cloud-hosted database.

The system stores information related to:

👤 Users
🚘 Vehicles
🛡️ Insurance
📄 PUC expiry
💳 Insurance payments
📧 Email reminder logs
Main Backend Models
🔌 REST API

The frontend communicates with the backend through REST APIs.

Example:

The backend receives the vehicle number, searches MongoDB Atlas, and returns the corresponding vehicle information as a JSON response.

🔐 Authentication

The application includes user authentication.

The backend uses authentication middleware to protect relevant routes.

📧 Email Notification System

The project uses NodeMailer for sending email notifications.

The system combines:

Cron Jobs → Schedule and trigger the check
NodeMailer → Send the email
🗂️ Backend Project Structure
🧪 Development & Testing

The application was first developed and tested locally before cloud deployment.

Frontend
Backend

The backend was connected to MongoDB Atlas during local development to verify API operations and database communication.

🎯 Project Objectives
Provide an easy-to-use platform for managing vehicle information.
Track insurance and PUC expiry dates.
Reduce the possibility of missing insurance renewal deadlines.
Provide automated email reminders.
Provide a convenient digital insurance renewal flow.
Demonstrate full-stack development with cloud deployment.
Use AWS services to host application components.


💡 Why Cloud Computing?

Cloud computing allows the application to be accessed remotely without depending on a single local machine.

The project uses:

This separation allows the frontend, backend, and database to perform their respective roles independently.

⚠️ Current Limitations
Vehicle information is entered manually.
UPI payment confirmation is based on user acknowledgment.
No live payment gateway verification is currently implemented.
Email reminders depend on the backend server and scheduled jobs being available.
No two-factor or biometric authentication.
The current system is designed primarily for individual users rather than large fleet management.
🚀 Future Enhancements
🔗 Integration with government/RTO vehicle databases
🏛️ Integration with RTO or mParivahan APIs
💳 Integration with secure payment gateway APIs
✅ Automatic payment verification
🔐 Two-factor authentication
📱 Improved mobile responsiveness
🚛 Fleet management functionality
📊 Advanced vehicle analytics
📈 Improved monitoring and scalability
☁️ Production-level cloud optimization




🌟 Advantages
✔️ Cloud-based application
✔️ Accessible from different devices
✔️ Centralized vehicle information
✔️ Automated expiry reminders
✔️ Digital insurance renewal
✔️ Downloadable receipts
✔️ MERN-based full-stack architecture
✔️ AWS-based deployment
✔️ Cloud-hosted database
📚 What I Learned

Through this project, I gained practical understanding of:

Full-stack MERN development
React frontend development
Node.js backend development
Express.js REST APIs
MongoDB Atlas
AWS S3
AWS EC2
AWS IAM
Authentication and middleware
Cron Jobs
NodeMailer
Cloud deployment
Frontend-backend-database integration
Digital payment workflows
👩‍💻 Project Details

Project Name: Vehicle Info Finder using Cloud Computing

Project Type: Team Mini Project

Domain: Cloud Computing & Full-Stack Web Development

Architecture: Layered Cloud-Based Architecture

Technology Stack: MERN + AWS + MongoDB Atlas

⭐ Project Highlights
<p align="center"> <b>🚗 Vehicle Info Finder</b><br> Making vehicle and insurance management simpler through cloud technology. </p> ```