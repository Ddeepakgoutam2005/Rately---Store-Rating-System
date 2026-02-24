# Rately - Store Rating System

Rately is a full-stack platform that allows users to rate and review local businesses, helping others find the best services while providing business owners with valuable feedback and performance insights.

## 🚀 Features

### For Customers (Normal Users)
- **Discover Stores:** Browse a list of local businesses.
- **Rate & Review:** Share shopping experiences with honest ratings and detailed feedback.
- **Track History:** View and manage personal rating history.
- **Personalized Profile:** Manage account settings and preferences.

### For Store Owners
- **Performance Analytics:** Visualize customer satisfaction trends through a dedicated dashboard.
- **Feedback Management:** Read and analyze customer reviews to improve services.

### For System Administrators
- **User Management:** Create, update, and manage all user accounts (Admin, Store Owner, Normal User).
- **Store Management:** Onboard and manage store listings on the platform.
- **System Analytics:** Overview of platform performance and growth statistics.

## 🛠️ Tech Stack

### Frontend
- **React:** Component-based UI development.
- **Tailwind CSS:** Modern, responsive styling.
- **Axios:** API communication with the backend.
- **React Router:** Client-side navigation and protected routing.
- **Context API:** Global state management (Authentication).

### Backend
- **Node.js & Express:** Scalable server-side application framework.
- **MongoDB & Mongoose:** NoSQL database for flexible data storage.
- **JWT (JSON Web Tokens):** Secure authentication and authorization.
- **CORS:** Cross-Origin Resource Sharing configuration for secure API access.
- **Helmet & Rate Limiting:** Security middleware to protect against common vulnerabilities.

## 📂 Project Structure

```
Rately/
├── backend/                # Express API
│   ├── config/             # Database & environment config
│   ├── controllers/        # Business logic for routes
│   ├── middleware/         # Auth & validation logic
│   ├── models/             # Mongoose schemas (User, Store, Rating)
│   ├── routes/             # API endpoint definitions
│   └── server.js           # Entry point
└── frontend/               # React Application
    ├── public/             # Static assets
    ├── src/
    │   ├── components/     # Reusable UI & Layout components
    │   ├── contexts/       # Auth state management
    │   ├── pages/          # View components (Admin, User, Owner)
    │   ├── services/       # API interaction layer
    │   └── App.js          # Root component & Routing
```

## ⚙️ Getting Started

### Prerequisites
- Node.js (v14+)
- MongoDB (Local or Atlas)

### Installation

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd Rately-main
   ```

2. **Backend Setup:**
   ```bash
   cd backend
   npm install
   # Create a .env file based on .env.example and fill in details
   npm run dev
   ```

3. **Frontend Setup:**
   ```bash
   cd frontend
   npm install
   # Create a .env.local file with REACT_APP_API_URL=http://localhost:5000/api
   npm start
   ```

## 🔒 Default Admin Credentials
- **Email:** `admin@rately.com`
- **Password:** `Admin@123`

## 📄 License
This project is licensed under the MIT License.
