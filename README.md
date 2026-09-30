# ScamShield 🛡️

ScamShield is a full-stack digital threat intelligence platform designed to help users report suspected online scams and provide a structured way to manage and analyze scam-related information.

## 🌐 Live Demo

**[ScamShield – Live Demo](https://scam-shield-tan.vercel.app)**

**[GitHub Repository](https://github.com/codeby-kanishka/ScamShield)**

---

## 📌 Problem Statement

Online scams are becoming increasingly common, while users often face difficulty identifying, documenting, and reporting suspicious activities.

ScamShield provides a centralized platform where users can submit information about suspected scams, while authorized administrators can review and manage submitted reports.

---

## 🚀 Features

- User registration and login
- JWT-based authentication
- Secure password hashing
- Scam report submission
- Scam report management
- Protected API routes
- Role-based authorization
- Admin functionality
- Location-based scam information
- Threat visualization and map functionality
- RESTful API architecture
- MongoDB database integration
- Responsive React frontend

---

## 🛠️ Tech Stack

### Frontend

- React.js
- JavaScript
- HTML5
- CSS3
- Vite

### Backend

- Node.js
- Express.js
- REST APIs
- JWT Authentication
- bcrypt.js

### Database

- MongoDB
- MongoDB Atlas
- Mongoose

### Deployment

- Vercel
- MongoDB Atlas

---

## 🏗️ Project Architecture

```text
ScamShield/
│
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── assets/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── api.js
│   │   ├── App.jsx
│   │   ├── App.css
│   │   ├── index.css
│   │   └── main.jsx
│   ├── index.html
│   ├── package.json
│   ├── vite.config.js
│   └── vercel.json
│
├── backend/
│   ├── src/
│   │   ├── config/
│   │   ├── controllers/
│   │   ├── middleware/
│   │   ├── models/
│   │   ├── routes/
│   │   ├── services/
│   │   ├── utils/
│   │   └── server.js
│   ├── package.json
│   └── package-lock.json
│
├── README.md
└── .gitignore
