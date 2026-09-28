# Interview AI

Interview AI is a full-stack application that helps users prepare for interviews by generating interview reports from their resume, job description, and self-description.

## Features

- User registration, login, logout, and protected routes
- Resume upload for interview preparation
- AI-generated interview reports
- Interview report history
- Resume PDF generation

## Tech Stack

- Frontend: React, Vite, React Router, Axios, Sass
- Backend: Node.js, Express, MongoDB, Mongoose
- Authentication: JWT stored in an HTTP cookie
- AI: Google GenAI

## Project Structure

```text
Backend/     Express API and MongoDB models
Frontend/    React + Vite client
```

## Prerequisites

- Node.js 18 or newer
- MongoDB running locally or a MongoDB Atlas connection
- Google GenAI API key

## Environment Setup

Create `Backend/.env` with:

```env
MONGO_URI=mongodb://127.0.0.1:27017/interview-ai
JWT_SECRET=replace-with-a-long-random-secret
GOOGLE_GENAI_API_KEY=your-google-genai-api-key
```

Never commit `.env` files or API keys to GitHub.

## Installation

Install backend dependencies:

```powershell
cd Backend
npm install
```

Install frontend dependencies:

```powershell
cd ..\Frontend
npm install
```

## Running Locally

Start the backend in one terminal:

```powershell
cd Backend
npm run dev
```

The API runs at `http://localhost:3000`.

Start the frontend in a second terminal:

```powershell
cd Frontend
npm run dev
```

Open the Vite URL shown in the terminal, usually `http://localhost:5173`.

## Available Scripts

### Backend

- `npm run dev` - Start the API with Nodemon

### Frontend

- `npm run dev` - Start the Vite development server
- `npm run build` - Create a production build
- `npm run lint` - Run ESLint
- `npm run preview` - Preview the production build locally

## API Routes

- `POST /api/auth/register` - Register a user
- `POST /api/auth/login` - Log in a user
- `GET /api/auth/logout` - Log out the current user
- `GET /api/auth/get-me` - Get the current user
- `POST /api/interview/` - Generate an interview report
- `GET /api/interview/` - Get the user's interview reports
- `GET /api/interview/report/:interviewId` - Get one interview report
- `POST /api/interview/resume/pdf/:interviewReportId` - Generate a resume PDF

## GitHub Setup

After creating a GitHub repository, connect and push this project with:

```powershell
git remote add origin https://github.com/YOUR_USERNAME/interview-ai.git
git push -u origin master
```
