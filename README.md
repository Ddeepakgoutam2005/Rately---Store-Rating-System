# Rately - Store Rating System

A full-stack application for rating and reviewing stores.

## Deployment Guide

This guide will help you deploy the application using MongoDB Atlas for the database, Render for the backend, and Vercel for the frontend.

### 1. MongoDB Atlas Setup (Database)

1.  **Create an account:** Go to [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) and sign up.
2.  **Create a Cluster:** Follow the prompts to create a free shared cluster.
3.  **Network Access:** In the "Network Access" tab, click "Add IP Address" and select "Allow Access From Anywhere" (0.0.0.0/0) for initial setup, or add your Render server's IP if you want more security.
4.  **Database User:** In "Database Access", create a user with a username and password. Remember these!
5.  **Get Connection String:** Click "Connect" -> "Drivers" -> Select Node.js. Copy the connection string. It will look like:
    `mongodb+srv://<username>:<password>@cluster0.xxxx.mongodb.net/?retryWrites=true&w=majority`
    *Replace `<username>` and `<password>` with the credentials you created.*

### 2. Backend Deployment (Render)

1.  **Prepare for Render:**
    *   Ensure your code is pushed to a GitHub repository.
2.  **Create a New Web Service:**
    *   Log in to [Render](https://render.com/).
    *   Click "New" -> "Web Service".
    *   Connect your GitHub repository.
3.  **Configure Web Service:**
    *   **Name:** `rately-backend` (or your choice).
    *   **Root Directory:** `backend`
    *   **Environment:** `Node`
    *   **Build Command:** `npm install`
    *   **Start Command:** `npm start`
4.  **Add Environment Variables:**
    *   `MONGO_URI`: (Your MongoDB connection string)
    *   `JWT_SECRET`: (A random strong string)
    *   `CLIENT_URL`: (Your future Vercel URL, e.g., `https://rately.vercel.app`)
    *   `NODE_ENV`: `production`
5.  **Deploy:** Click "Create Web Service". Once deployed, copy the Render URL (e.g., `https://rately-backend.onrender.com`).

### 3. Frontend Deployment (Vercel)

1.  **Prepare for Vercel:**
    *   Ensure your code is pushed to the same GitHub repository.
2.  **Create a New Project:**
    *   Log in to [Vercel](https://vercel.com/).
    *   Click "Add New" -> "Project".
    *   Import your GitHub repository.
3.  **Configure Project:**
    *   **Framework Preset:** `Create React App`
    *   **Root Directory:** `frontend`
4.  **Add Environment Variables:**
    *   `REACT_APP_API_URL`: (Your Render Backend URL + `/api`, e.g., `https://rately-backend.onrender.com/api`)
5.  **Deploy:** Click "Deploy".

---

## Local Development

### Backend
1.  `cd backend`
2.  `npm install`
3.  Create a `.env` file based on `.env.example`.
4.  `npm run dev`

### Frontend
1.  `cd frontend`
2.  `npm install`
3.  `npm start`

## Tech Stack
- **Frontend:** React, Tailwind CSS, Axios
- **Backend:** Node.js, Express, MongoDB, Mongoose
- **Auth:** JWT (JSON Web Tokens)
