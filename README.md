# ScamShield 🛡️

ScamShield is a full-stack digital threat intelligence platform designed to help users report suspected online scams and provide a structured way to manage and analyze scam-related information.


## 📌 Problem Statement

Online scams are becoming increasingly common, including fake customer-care calls, phishing attempts, fraudulent websites, payment scams, and social engineering attacks.

Users often face difficulty identifying, documenting, and reporting suspicious activities.

ScamShield provides a centralized platform where users can submit information about suspected scams, while authorized administrators can review and manage submitted reports.

---

## 🎯 Project Objectives

- Provide a centralized platform for reporting suspected scams.
- Allow authenticated users to submit scam reports.
- Store and organize scam-related information.
- Provide administrators with tools to manage submitted reports.
- Display scam-related information in an organized manner.
- Provide location-based visualization of reported threats.
- Build a foundation for future threat-intelligence features.

---

## 🚀 Features

### User Features

- User registration and login
- JWT-based authentication
- Secure password hashing
- Submit scam reports
- View scam-related information
- Location-based scam information
- Threat visualization

### Security Features

- JWT authentication
- Protected API routes
- Authentication middleware
- Role-based authorization
- Password hashing using bcrypt
- Environment variables for sensitive credentials

### Admin Features

- Admin authentication
- Role-based access control
- View submitted scam reports
- Manage submitted reports
- Access protected administrative functionality

### Platform Features

- RESTful API architecture
- MongoDB database integration
- Map/location-based visualization
- React-based frontend
- Express.js backend

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

## 🏗️ System Architecture

```text
                         ScamShield
                              │
              ┌───────────────┴───────────────┐
              │                               │
       React Frontend                    Express Backend
              │                               │
          Components                         Routes
              │                               │
            Pages                         Middleware
              │                               │
           api.js                         Controllers
              │                               │
              └───────────────┬───────────────┘
                              │
                          Utilities
                              │
                         Mongoose Models
                              │
                              ▼
                       MongoDB Atlas
```

---

## 📁 Project Structure

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
│   │   ├── utils/
│   │   └── server.js
│   ├── package.json
│   └── package-lock.json
│
├── README.md
└── .gitignore
```

---

## 🔄 Application Flow

The overall application flow is:

```text
User
  │
  ▼
React Frontend
  │
  ▼
User Authentication
  │
  ▼
JWT Token
  │
  ▼
Protected API Request
  │
  ▼
Express.js Backend
  │
  ├── Authentication Middleware
  │
  ├── Authorization Middleware
  │
  ▼
Controllers
  │
  ▼
Utilities
  │
  ▼
Mongoose Models
  │
  ▼
MongoDB Atlas
  │
  ▼
Response
  │
  ▼
React Frontend
```

### Scam Report Flow

```text
User
  ↓
Fills Scam Report Form
  ↓
Frontend Request
  ↓
REST API
  ↓
Authentication Check
  ↓
Backend Controller
  ↓
Data Processing
  ↓
MongoDB
  ↓
Report Stored
  ↓
Response
  ↓
Frontend Updates
```

---

## 🔐 Authentication Flow

ScamShield uses JWT-based authentication to secure protected resources.

```text
User
  ↓
Login / Registration
  ↓
Backend validates credentials
  ↓
Password verification
  ↓
JWT generated
  ↓
Token returned to client
  ↓
Client sends token with protected requests
  ↓
Authentication middleware verifies token
  ↓
Request allowed / rejected
```

### Authentication Process

1. The user registers or logs into the application.
2. The backend validates the provided credentials.
3. Passwords are securely hashed using bcrypt.
4. After successful authentication, a JWT is generated.
5. The authenticated client uses the token for protected requests.
6. Authentication middleware verifies the token.
7. Authorized requests continue to the appropriate controller.
8. Unauthorized requests are rejected.

---

## 🛡️ Authorization Flow

ScamShield uses role-based authorization for administrative functionality.

```text
Request
   ↓
JWT Verification
   ↓
User Identified
   ↓
Role Checked
   ↓
Admin?
 ┌───────┴───────┐
 │               │
Yes              No
 │               │
 ▼               ▼
Allow          Reject
Request        Request
```

**Authentication** determines who the user is.

**Authorization** determines what the user is allowed to access.

---

## 📡 REST API Architecture

The backend follows a RESTful API architecture.

```text
React Frontend
      ↓
HTTP Request
      ↓
Express Router
      ↓
Middleware
      ↓
Controller
      ↓
Utilities
      ↓
Mongoose
      ↓
MongoDB
      ↓
HTTP Response
      ↓
React Frontend
```

The API handles functionality such as:

- User registration
- User authentication
- Scam report creation
- Scam report retrieval
- Scam report management
- Protected resources
- Administrative operations

---

## 🗄️ Database

ScamShield uses **MongoDB Atlas** as its cloud database.

**Mongoose** is used as the Object Data Modeling (ODM) library for interacting with MongoDB.

The database stores application information such as:

- User information
- Authentication-related data
- User roles
- Scam reports
- Report-related information

---

## 🔒 Security

Security considerations implemented in ScamShield include:

- JWT-based authentication
- Password hashing using bcrypt
- Protected API routes
- Role-based authorization
- Environment variables for sensitive configuration
- Separation of frontend and backend responsibilities

Sensitive credentials such as database connection strings and JWT secrets are stored using environment variables and are not committed to the repository.

---

## ⚙️ Running the Project Locally

### 1. Clone the Repository

```bash
git clone https://github.com/codeby-kanishka/ScamShield.git
cd ScamShield
```

### 2. Run the Backend

Open a terminal:

```bash
cd backend
npm install
npm start
```

Create a `.env` file inside the `backend` directory.

Example:

```env
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
```

### 3. Run the Frontend

Open another terminal:

```bash
cd frontend
npm install
npm run dev
```

The frontend will run using the Vite development server.

---

## 🔑 Environment Variables

Sensitive credentials are stored using environment variables.

Example:

```env
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
```

**Never commit real database credentials, JWT secrets, API keys, or other sensitive information to GitHub.**

---

## 🎯 Project Goals

ScamShield aims to provide a structured platform for:

- Reporting suspected scams
- Organizing scam-related information
- Managing submitted reports
- Providing visibility into reported digital threats
- Helping administrators review and manage scam reports

---

## 🔮 Future Scope

The project can be further enhanced with:

- Automated scam classification using machine learning
- Real-time scam alerts and notifications
- Advanced analytics and threat dashboards
- Integration with external threat-intelligence sources
- Community-based scam verification and reporting

---

## 🔗 Links

**Live Demo:**  
https://scam-shield-tan.vercel.app

**GitHub Repository:**  
https://github.com/codeby-kanishka/ScamShield

---

## 👩‍💻 Author

**Kanishka**

GitHub:  
https://github.com/codeby-kanishka
