# 🚀 AI Resume Builder - Backend API

A robust, high-performance RESTful API built with **Node.js**, **Express**, and **MongoDB**. This backend powers the AI Resume Builder application, providing secure authentication, resume management, and real-time AI content generation using **Groq (Llama 3)**.

## 🌟 Key Features

-   **Custom Authentication:** Secure Signup/Login using **JWT (JSON Web Tokens)** and **Bcrypt** for password hashing.
-   **AI Integration (Groq LPU):** 
    -   Utilizes Groq SDK for ultra-fast inference (sub-2s response time).
    -   Generates Professional Summaries, Bullet Points, and Interview Questions.
    -   **Robust JSON Parsing:** Implemented Regex-based fallback strategies to handle unstructured AI responses and prevent server crashes.
-   **Resume Management:** Full CRUD operations for Resumes (Personal Info, Experience, Education, Skills).
-   **Database:** Modeled using **Mongoose** schemas with embedded sub-documents for optimized read performance.
-   **Secure Architecture:** 
    -   MVC Pattern (Model-View-Controller).
    -   Middleware for route protection and error handling.
    -   Environment variable management with `dotenv`.

---

## 🛠️ Tech Stack

-   **Runtime:** [Node.js](https://nodejs.org/)
-   **Framework:** [Express.js](https://expressjs.com/)
-   **Database:** [MongoDB](https://www.mongodb.com/) (Atlas) + [Mongoose ODM](https://mongoosejs.com/)
-   **AI Service:** [Groq SDK](https://groq.com/) (Llama 3 / Mixtral models)
-   **Authentication:** `jsonwebtoken`, `bcryptjs`
-   **Utilities:** `cors`, `dotenv`, `nodemon`

---

## 📂 Project Structure

The project follows a modular **Service-Controller-Route** architecture to ensure separation of concerns:


## 🚀 Getting Started

### Prerequisites
-   Node.js (v18+)
-   MongoDB (Local or Atlas URL)
-   Groq API Key

### 1. Clone the Repository
```bash
git clone https://github.com/iamyash07/AI-Resume-Builder-Backend.git
cd AI-Resume-Builder-Backend

### 2. Install Dependencies
npm install

3. Configure Environment Variables
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_super_secret_jwt_key
GROQ_API_KEY=your_groq_api_key

4. Run the Server
# Development Mode (with Nodemon)
npm run dev

# Production Mode
npm start

folder Structure

AI Resume Builder/
├── backend/
│   ├── config/
│   │   └── db.js
│   ├── controllers/
│   │   ├── auth.controller.js
│   │   ├── resume.controller.js
│   │   ├── ai.controller.js
│   │   └── job.controller.js
│   ├── middleware/
│   │   └── auth.middleware.js
│   ├── models/
│   │   ├── User.model.js
│   │   ├── Resume.model.js
│   │   └── JobApplication.model.js
│   ├── routes/
│   │   ├── auth.routes.js
│   │   ├── resume.routes.js
│   │   ├── ai.routes.js
│   │   └── job.routes.js
│   └── utils/
│       └── aiHelper.js
├── .env
├── .gitignore
├── package.json
└── server.js          


All backend APIs

✅ 1.  GET    /                           Health Check
✅ 2.  POST   /api/auth/register          Register
✅ 3.  POST   /api/auth/login             Login
✅ 4.  GET    /api/auth/profile           Get Profile
✅ 5.  POST   /api/resume                 Create Resume
✅ 6.  GET    /api/resume                 Get All Resumes
✅ 7.  GET    /api/resume/:id             Get Single Resume
✅ 8.  PUT    /api/resume/:id             Update Resume
✅ 9.  DELETE /api/resume/:id             Delete Resume
✅ 10. POST   /api/ai/generate-summary    AI Summary
✅ 11. POST   /api/ai/generate-bullets    AI Bullets
✅ 12. POST   /api/ai/review-resume       AI Review
✅ 13. POST   /api/ai/match-job           AI Job Match
✅ 14. POST   /api/ai/interview-questions AI Interview Qs
✅ 15. POST   /api/jobs                   Create Job App
✅ 16. GET    /api/jobs                   Get All Jobs
✅ 17. PUT    /api/jobs/:id               Update Job
✅ 18. DELETE /api/jobs/:id               Delete Job


What I built:
├── ✅ MongoDB Atlas Database
├── ✅ JWT Authentication System
├── ✅ Resume CRUD APIs
├── ✅ 5 AI Features (Groq/Llama 3.3)
├── ✅ Job Application Tracker
├── ✅ Security (bcrypt + JWT)
└── ✅ Clean MVC Architecture