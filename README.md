# AI Interview Preparation Platform

An AI-powered interview preparation application that analyzes a candidate's resume, profile description, and target job description to generate a tailored interview preparation report.

## Features

- User registration and login with JWT-based authentication
- Resume upload for profile context
- AI-generated interview reports using Google's Gemini API
- Technical and behavioral interview questions with suggested answers
- Skill-gap analysis with severity levels
- Day-wise interview preparation plan
- PDF generation for generated resume/report content

## Tech Stack

**Frontend**
- React 19
- Vite
- React Router
- Sass
- Axios

**Backend**
- Node.js
- Express 5
- MongoDB and Mongoose
- JWT authentication and bcryptjs
- Google GenAI SDK
- Multer for file uploads
- Puppeteer and pdf-parse

## Project Structure

```text
AI-Interview-Preparation-Platform/
├── Backend/
│   ├── src/
│   │   ├── config/
│   │   ├── controllers/
│   │   ├── middlewares/
│   │   ├── models/
│   │   ├── routes/
│   │   └── services/
│   ├── server.js
│   ├── package.json
│   └── .env.example
├── Frontend/
│   ├── public/
│   ├── src/
│   ├── package.json
│   └── vite.config.js
├── .gitignore
└── README.md
```

## Prerequisites

- Node.js (LTS recommended)
- npm
- MongoDB instance (local or hosted)
- Google GenAI API key

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/aman07052005/AI-Interview-Preparation-Platform.git
cd AI-Interview-Preparation-Platform
```

### 2. Configure the backend

```bash
cd Backend
npm install
```

Create a `.env` file in the `Backend` directory using `.env.example` as a reference, then set your own values:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_long_random_secret
GOOGLE_GENAI_API_KEY=your_google_genai_api_key
```

Start the backend:

```bash
npm run dev
```

### 3. Configure the frontend

Open a second terminal:

```bash
cd Frontend
npm install
npm run dev
```

Vite will print the local development URL in the terminal.

## Environment Variables

| Variable | Description |
|---|---|
| `PORT` | Backend server port |
| `MONGO_URI` | MongoDB connection string |
| `JWT_SECRET` | Secret used to sign and verify JWTs |
| `GOOGLE_GENAI_API_KEY` | API key for Google GenAI |

Never commit your real `.env` file or API keys. Use `.env.example` for documenting required variables.

## Notes

- The backend expects MongoDB to be reachable using `MONGO_URI`.
- AI report generation requires a valid Google GenAI API key.
- Configure the frontend API base URL to point to your running backend if it differs from the project's current configuration.
- Puppeteer may require additional system libraries in some Linux deployment environments.

## Future Improvements

- Add automated backend and frontend tests
- Add deployment configuration and production environment documentation
- Improve upload validation, error handling, and API documentation
- Add CI checks for linting and production builds

## Author

**Aman Yadav**

GitHub: [@aman07052005](https://github.com/aman07052005)
