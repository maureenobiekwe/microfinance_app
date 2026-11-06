<h1 align="center">Microfinance Loan Management System</h1>

<p align="center">
  A full-stack MERN application for submitting, reviewing and tracking microfinance loan requests.
</p>

<p align="center">
  <a href="https://microfinance-app.netlify.app"><strong>Live Demo</strong></a>
</p>

---

## Overview

Borrowers register, sign in and submit loan applications. Administrators review each request from a dedicated dashboard and approve or reject it. Borrowers can follow the status of every application they have submitted.

## Features

- **Authentication** – JWT-based registration and login
- **Role-based access** – separate views and permissions for borrowers and administrators
- **Loan applications** – request form with input validation on submission
- **Admin dashboard** – review, approve or reject pending requests
- **Status tracking** – each loan shows as Pending, Approved or Rejected
- **Responsive UI** – built with Tailwind CSS for desktop and mobile
- **Protected REST API** – authentication middleware on all secured routes

## Tech Stack

| Layer      | Technologies                                 |
| ---------- | -------------------------------------------- |
| Frontend   | React, Vite, Tailwind CSS, React Router      |
| Backend    | Node.js, Express.js, JSON Web Tokens         |
| Database   | MongoDB Atlas                                |
| Deployment | Netlify (frontend), Vercel (backend)         |

## Getting Started

### Prerequisites

- Node.js v16 or higher
- npm or yarn
- A MongoDB Atlas cluster (or a local MongoDB instance)
- Git

### 1. Clone the repository

```bash
git clone https://github.com/maureenobiekwe/microfinance_app.git
cd microfinance_app
```

### 2. Install dependencies

```bash
cd Backend && npm install
cd ../Frontend && npm install
```

### 3. Configure environment variables

Copy the sample file in each folder and fill in your own values.

```bash
cp Backend/.env.sample Backend/.env
cp Frontend/.env.sample Frontend/.env
```

**Backend** (`Backend/.env`)

| Variable     | Description                               | Example                       |
| ------------ | ----------------------------------------- | ----------------------------- |
| `MONGO_URI`  | MongoDB connection string                 | `mongodb+srv://...`           |
| `PORT`       | Port the API listens on                   | `3000`                        |
| `JWT_SECRET` | Secret used to sign auth tokens           | any long random string        |
| `Email`      | Admin account email                       | `admin@example.com`           |
| `Password`   | Admin account password                    | choose a strong password      |

**Frontend** (`Frontend/.env`)

| Variable            | Description          | Example                 |
| ------------------- | -------------------- | ----------------------- |
| `VITE_API_BASE_URL` | Base URL of the API  | `http://localhost:3000` |

### 4. Run the app

Start the backend:

```bash
cd Backend
node server.js
```

The API runs at `http://localhost:3000`.

In a second terminal, start the frontend:

```bash
cd Frontend
npm run dev
```

The app runs at `http://localhost:5173`.

## Admin Access

The admin account is created from the `Email` and `Password` values in `Backend/.env`. Sign in with those credentials to open the admin dashboard.

For the live demo, use:

- **Email:** `admin@gmail.com`
- **Password:** `admin@123`

> **Note:** These demo credentials are for evaluation only. Set your own values before deploying, and never commit a real `.env` file.

## Project Structure

```
microfinance_app/
├── Frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── context/        # React context providers
│   │   ├── pages/          # Application pages
│   │   ├── routes/         # Route configuration
│   │   ├── utils/          # Helper functions
│   │   ├── App.jsx         # Root component
│   │   ├── index.css       # Global styles
│   │   └── main.jsx        # Entry point
│   ├── .env.sample
│   ├── package.json
│   └── vite.config.js
├── Backend/
│   ├── controllers/        # Request handlers
│   ├── db/                 # Database connection
│   ├── middlewares/        # Auth and custom middleware
│   ├── models/             # Mongoose schemas
│   ├── routes/             # API routes
│   ├── utils/              # Backend helpers
│   ├── .env.sample
│   ├── package.json
│   ├── server.js           # API entry point
│   └── vercel.json         # Vercel deployment config
└── README.md
```

## Author

**Maureen Obiekwe**
[GitHub](https://github.com/maureenobiekwe) · [Portfolio](https://maureenobiekwe.com)# microfinance_app
