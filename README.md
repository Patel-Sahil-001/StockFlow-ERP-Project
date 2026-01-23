# StockFlow ERP

## About
StockFlow ERP is a system designed to help businesses manage their inventory and sales efficiently. It allows users to track products, generate bills, and view sales analytics.

## Key Features
- **Inventory Tracking**: Monitor stock levels in real-time.
- **Sales Management**: Create bills and track sales history.
- **User Roles**: Secure login for admins and staff.
- **Reports**: View simple graphs for sales and inventory.

## Tech Stack
- **Frontend**: React, Tailwind CSS
- **Backend**: Node.js, Express, MongoDB
- **Authentication**: Google OAuth & JWT

## How to Run

### 1. Backend (Server)
The backend handles the database and API.

```bash
cd backend
npm install
npm run dev
```
*Note: Ensure you have a `.env` file with your credentials (PORT, MONGO_URI, etc).*

### 2. Frontend (UI)
The frontend allows you to interact with the system.

```bash
cd frontend
npm install
npm run dev
```

## API Highlights
*   **POST** `/api/users/login` - Log in to the app
*   **GET** `/api/products` - View all products
*   **POST** `/api/sales` - Create a new sale
*   **GET** `/api/reports` - Get dashboard data

## License
Educational Project.
