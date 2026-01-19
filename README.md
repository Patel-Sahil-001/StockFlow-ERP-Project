# StockFlow ERP

A full-stack ERP system for inventory and sales management.

## 🛠 Tech Stack

- **Frontend**: React, Vite, Tailwind CSS, Redux
- **Backend**: Node.js, Express.js, MongoDB
- **Auth**: Passport.js (Google OAuth), JWT
- **Tools**: Cloudinary (Image Upload), Nodemailer (Email), Vercel (Deployment)

## 🚀 Getting Started

### Prerequisites

- Node.js (v18+)
- MongoDB URI
- Cloudinary & Google OAuth credentials

### Installation

1.  **Clone the repository**
    ```bash
    git clone https://github.com/yourusername/StockFlow-ERP-Project.git
    cd StockFlow-ERP-Project
    ```

2.  **Backend Setup**
    ```bash
    cd backend
    npm install
    
    # Create .env file with:
    # PORT=5000
    # MONGO_URI=your_mongo_uri
    # JWT_SECRET=your_secret
    # CLOUDINARY_*, EMAIL_*, GOOGLE_* credentials
    
    npm run dev
    ```

3.  **Frontend Setup**
    ```bash
    cd frontend
    npm install
    
    # Create .env file with:
    # VITE_API_URL=http://localhost:5000/api
    
    npm run dev
    ```

## 📚 API Overview

| Method | Endpoint | Description |
| :--- | :--- | :--- |
| **Auth** | `/api/users/login` | User login |
| **Products** | `/api/products` | Manage inventory |
| **Sales** | `/api/sales` | Create & view orders |
| **Reports** | `/api/reports/sales` | Analytics data |

## 📄 License

This project is for educational purposes.
