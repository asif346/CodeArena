# CodeArena - A Leetcode Clone

A full-stack coding platform inspired by LeetCode, built with React on the frontend and Express + MongoDB + Redis on the backend. The app supports user authentication, problem browsing, code submissions, AI-powered doubt solving, and uploaded solution videos.

## Features

- User signup/login with JWT-based authentication
- Problem listing and individual problem pages
- Code submission handling and submission history
- AI-powered DSA tutor using Groq
- Video-based solution uploads with Cloudinary
- Admin tools for managing problems and videos
- Redis-backed token validation

## Tech Stack

- Frontend: React, Vite, Redux Toolkit, React Router
- Backend: Node.js, Express
- Database: MongoDB with Mongoose
- Cache/Auth validation: Redis
- AI: Groq SDK
- Media: Cloudinary

## Project Structure

Leetcode_clone/
├── Backend/
│   ├── src/
│   ├── package.json
│   └── .env.example (add your own env file)
├── frontend/
│   ├── src/
│   ├── package.json
│   └── vite.config.js
├── README.md
└── .gitignore

## Prerequisites

Before running the app, make sure you have:
- Node.js 18+
- npm or pnpm
- MongoDB running locally or a MongoDB Atlas connection string
- Redis running locally or a remote Redis instance
- Cloudinary account for video uploads
- Groq API key for the AI tutor

## Backend Setup

1. Open a terminal and go to the backend folder:
cd Backend

2. Install dependencies:
npm install

3. Create a `.env` file in the `Backend` folder with the following values:
env
PORT=3000
DB_CONNECTION_STRING=mongodb://localhost:27017/leetcode_clone
JWT_KEY=your_super_secret_jwt_key

REDIS_HOST=localhost
REDIS_PORT=6379
REDIS_PASSWORD=

GROQ_API_KEY=your_groq_api_key
RAPIDAPI_KEY=your_rapidapi_key

CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret


> Note: the backend code also accepts `DB_CONNCECTION_STRING` as a fallback, but `DB_CONNECTION_STRING` is the preferred variable name.

4. Start the backend server:
node src/index.js
The backend server should run on `http://localhost:3000`.

## Frontend Setup

1. Open a new terminal and go to the frontend folder:
cd frontend

2. Install dependencies:
npm install


3. Start the Vite dev server:
npm run dev

The frontend will typically run at:
http://localhost:5173

## Running the Full App

- Start MongoDB
- Start Redis
- Start the backend from `Backend`
- Start the frontend from `frontend`
- Open the frontend in the browser and log in or sign up

## Common Notes

- The frontend is configured to call the backend at `http://localhost:3000`.
- Cookies are used for authentication, so the backend and frontend must be running on the expected localhost ports.
- If you are using Cloudinary or Groq features, make sure the corresponding API keys are valid.
