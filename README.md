# StockFlow ERP

A comprehensive Enterprise Resource Planning (ERP) system for inventory and sales management, built with modern web technologies. Designed as a 6th semester university project.



## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Configuration](#configuration)
- [Running the Application](#running-the-application)
- [API Documentation](#api-documentation)
- [Database Schema](#database-schema)
- [Contributors](#contributors)

## 🎯 Overview

StockFlow is a full-stack ERP application that streamlines inventory management, sales tracking, and business reporting. It provides real-time insights into stock levels, automated restock alerts, and comprehensive sales analytics.

## ✨ Features

### Inventory Management
- Real-time product inventory tracking
- Automated restock notifications
- Category-based product organization
- Cloudinary-based image storage for products

### Sales Management
- Sales order creation and tracking
- Automated bill generation (PDF)
- Sales history and analytics
- Multi-user sales support

### User Management
- Role-based authentication (Passport.js)
- Password reset and recovery
- User profile management
- JWT token-based API authentication

### Notifications & Alerts
- Real-time restock alerts
- Email notifications for critical events
- Notification history and management

### Analytics & Reporting
- Sales reports and metrics
- Inventory insights
- Audit logs for compliance
- Comprehensive data visualization

## 🛠 Tech Stack

### Backend
- **Runtime**: Node.js
- **Framework**: Express.js
- **Database**: MongoDB with Mongoose ODM
- **Authentication**: Passport.js, JWT
- **Email**: Nodemailer
- **Task Scheduling**: node-cron
- **File Upload**: Cloudinary

### Frontend
- **Framework**: React with Vite
- **State Management**: Redux
- **Styling**: Tailwind CSS
- **Build Tool**: Vite
- **HTTP Client**: Axios (inferred from structure)

### DevOps
- **Backend Deployment**: Vercel (configured)
- **Frontend Deployment**: Vercel
- **Version Control**: Git

## 📁 Project Structure

```
StockFlow-ERP-Project/
├── backend/
│   ├── app.js              # Express app initialization
│   ├── package.json        # Backend dependencies
│   ├── api/                # API aggregation
│   ├── config/             # Configuration files (DB, Passport, Cloudinary)
│   ├── controller/         # Business logic for each feature
│   ├── db/                 # Database connection
│   ├── jobs/               # Cron jobs and scheduled tasks
│   ├── middlewares/        # Custom middleware (auth, error handling)
│   ├── migrations/         # Data migrations
│   ├── models/             # Mongoose schemas
│   ├── responses/          # Standardized response handlers
│   ├── routes/             # API route definitions
│   ├── scripts/            # Utility scripts (DB cleanup)
│   ├── seeds/              # Data seeding scripts
│   ├── src/                # Core utilities (billing, email)
│   └── utils/              # Helper functions (JWT, audit logging, etc.)
│
└── frontend/
    ├── package.json        # Frontend dependencies
    ├── vite.config.js      # Vite configuration
    ├── tailwind.config.js  # Tailwind CSS setup
    ├── index.html          # Entry HTML
    └── src/
        ├── App.jsx         # Main app component
        ├── main.jsx        # React entry point
        ├── components/     # Reusable UI components
        ├── hooks/          # Custom React hooks
        ├── layouts/        # Page layout templates
        ├── pages/          # Page components
        └── redux/          # Redux store and slices
```

## 🚀 Installation

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local or Atlas)
- npm or yarn package manager

### Backend Setup

```bash
cd backend
npm install
```

### Frontend Setup

```bash
cd frontend
npm install
```

## ⚙️ Configuration

### Backend Environment Variables

Create a `.env` file in the `backend/` directory:

```env
# Server
PORT=5000
NODE_ENV=development

# Database
MONGO_URI=mongodb+srv://username:password@cluster.mongodb.net/dbname

# JWT
JWT_SECRET=your_jwt_secret_key

# Email (Nodemailer)
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_app_password

# Cloudinary
CLOUDINARY_NAME=your_cloudinary_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

# Passport
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
```

### Frontend Environment Variables

Create a `.env` file in the `frontend/` directory:

```env
VITE_API_URL=http://localhost:5000/api
VITE_APP_NAME=StockFlow
```

## ▶️ Running the Application

### Start Backend Server

```bash
cd backend
npm start
# or for development with auto-reload
npm run dev
```

The backend will run on `http://localhost:5000`

### Start Frontend Development Server

```bash
cd frontend
npm run dev
```

The frontend will run on `http://localhost:5173`

### Build for Production

**Backend:**
```bash
cd backend
npm run build
```

**Frontend:**
```bash
cd frontend
npm run build
```

## 📚 API Documentation

### Key API Endpoints

#### User Management
- `POST /api/users/register` - Register new user
- `POST /api/users/login` - User login
- `GET /api/users/profile` - Get user profile
- `PUT /api/users/profile` - Update user profile

#### Products
- `GET /api/products` - Get all products
- `POST /api/products` - Create product
- `PUT /api/products/:id` - Update product
- `DELETE /api/products/:id` - Delete product

#### Sales
- `POST /api/sales` - Create sales order
- `GET /api/sales` - Get sales history
- `GET /api/sales/:id` - Get sales details

#### Categories
- `GET /api/categories` - Get all categories
- `POST /api/categories` - Create category

#### Reports
- `GET /api/reports/sales` - Sales analytics
- `GET /api/reports/inventory` - Inventory insights

#### Notifications
- `GET /api/notifications` - Get user notifications
- `POST /api/notifications/:id/read` - Mark as read

## 🗄️ Database Schema

Key collections:
- **Users** - User accounts and profiles
- **Products** - Product inventory
- **Categories** - Product categories
- **Sales** - Sales transactions
- **Notifications** - System notifications
- **AuditLogs** - System activity tracking
- **RestockLogs** - Inventory restock history

## 👥 Contributors

- Your Name / Student ID

## 📝 License

This project is created for educational purposes as part of a university curriculum.

## 📧 Support

For questions or issues, please contact the project maintainer or create an issue in the repository.
