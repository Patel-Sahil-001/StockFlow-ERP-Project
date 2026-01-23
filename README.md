# StockFlow ERP

![StockFlow Logo](frontend/public/logo.png)


> A comprehensive Enterprise Resource Planning (ERP) system for efficient inventory tracking, sales management, and business analytics.

StockFlow ERP is a robust full-stack web application designed to streamline business operations. It empowers users to manage products, generate professional invoices, analyze sales trends through interactive charts, and secure data with role-based access control.

## 🚀 Key Features

*   **📦 Smart Inventory Management**: Real-time tracking of stock levels, product categories, and low-stock alerts.
*   **🧾 Sales & Invoicing**: Create detailed bills and automatically generate downloadable PDFs for transactions.
*   **📊 Analytics Dashboard**: Visualize sales performance and inventory distribution with dynamic charts (powered by Chart.js).
*   **🔐 Secure Authentication**: Integrated Google OAuth and JWT-based authentication for secure user sessions.
*   **☁️ Cloud Integration**: Seamless image uploads and media management using Cloudinary.
*   **📧 Email Notifications**: Automated emails for system alerts and reports via Nodemailer.
*   **🛡️ Role-Based Access**: Distinct permissions for Admins and Staff members to ensure data security.

## 🛠️ Tech Stack

### Frontend
*   **Framework**: [React](https://reactjs.org/) (with [Vite](https://vitejs.dev/))
*   **State Management**: [Redux Toolkit](https://redux-toolkit.js.org/)
*   **Styling**: [Tailwind CSS](https://tailwindcss.com/)
*   **Visualization**: [Chart.js](https://www.chartjs.org/) & [React-Chartjs-2](https://react-chartjs-2.js.org/)
*   **Forms**: [Formik](https://formik.org/) & [Yup](https://github.com/jquense/yup)
*   **HTTP Client**: [Axios](https://axios-http.com/)

### Backend
*   **Runtime**: [Node.js](https://nodejs.org/) & [Express.js](https://expressjs.com/)
*   **Database**: [MongoDB](https://www.mongodb.com/) (Mongoose ODM)
*   **Authentication**: [Passport.js](https://www.passportjs.org/) (Google Strategy) & JWT
*   **File Storage**: [Cloudinary](https://cloudinary.com/)
*   **Utilities**: [PDFKit](https://pdfkit.org/) (PDF Generation), [Nodemailer](https://nodemailer.com/)

## ⚙️ Installation & Setup

Follow these steps to set up the project locally.

### Prerequisites
*   Node.js (v18+)
*   MongoDB (Compass or Atlas URL)
*   Cloudinary Account (Cloud Name, API Key, API Secret)
*   Google Cloud Console Project (Client ID, Client Secret)

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/StockFlow-ERP-Project.git
cd StockFlow-ERP-Project
```

### 2. Backend Setup
Navigate to the backend directory and install dependencies.
```bash
cd backend
npm install
```

Create a `.env` file in the `backend` folder with the following variables:
```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
EMAIL_USER=your_email_address
EMAIL_PASS=your_email_password
```

Start the backend server:
```bash
npm run dev
# Server will run on http://localhost:5000
```

### 3. Frontend Setup
Open a new terminal, navigate to the frontend directory, and install dependencies.
```bash
cd frontend
npm install
```

Create a `.env` file in the `frontend` folder (if required by your config, though Vite typically uses `import.meta.env`):
```env
VITE_API_URL=http://localhost:5000/api
```

Start the frontend development server:
```bash
npm run dev
# or
npm start
```

## 📡 API Endpoints Overview

| Method | Endpoint | Description |
| :--- | :--- | :--- |
| **POST** | `/api/users/auth/google` | Google OAuth Login |
| **POST** | `/api/users/login` | Email/Password Login |
| **GET** | `/api/products` | Fetch all inventory items |
| **POST** | `/api/products` | Add new product (with image) |
| **GET** | `/api/sales/stats` | Get sales analytics data |
| **POST** | `/api/sales/invoice` | Generate sale invoice PDF |

## 🤝 Contributing

Contributions are welcome! Please fork the repository and create a pull request with your changes.

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

## 📄 License

This project is for educational purposes.
