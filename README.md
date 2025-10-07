# MERN Task Management App

A simple full-stack Task Management web application built with the MERN stack (MongoDB, Express, React, Node).
This repo is ready-to-post on GitHub and includes server and client code, environment examples, and deployment notes.

## Features
- User registration and login (JWT authentication)
- Create, Read, Update, Delete tasks (per-user)
- Protected API routes for task operations
- React frontend with login/register and a task dashboard
- Ready for deployment on Render (backend + frontend) and MongoDB Atlas

## Tech Stack
- Frontend: React (create-react-app style)
- Backend: Node.js, Express.js, Mongoose
- Database: MongoDB (Atlas recommended)
- Auth: JSON Web Tokens (JWT)
- Styling: Simple CSS (no external UI framework required)

## Repo Structure
```
/backend    -> Express server, models, routes
/frontend   -> React app (CRA structure)
README.md
.env.example
```

## Quick start (local development)

### Prerequisites
- Node.js v16+ and npm
- MongoDB URI (local or Atlas)

### Backend
```bash
cd backend
cp .env.example .env
# set MONGO_URI and JWT_SECRET in .env
npm install
npm run dev
```
Backend runs at `http://localhost:5000` by default.

### Frontend
```bash
cd frontend
npm install
npm start
```
Frontend runs at `http://localhost:3000` and proxies API requests to the backend.

## Environment variables (.env)
See `.env.example` in each folder for required variables. Important values:
- MONGO_URI - MongoDB connection string
- JWT_SECRET - secret used to sign JWT tokens
- PORT - backend port (optional)

## Deployment
- Use MongoDB Atlas for the database.
- Deploy backend and frontend as separate services on Render, Heroku, or Vercel.
- Ensure environment variables are configured in the cloud provider.
- Set up CORS or proxying as required (the backend cors() is enabled).
