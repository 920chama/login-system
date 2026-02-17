# Login System

A full-stack login system with JWT authentication built with Express.js and React.js.

## Features

- JWT-based authentication
- Secure password hashing with bcrypt
- Modern and responsive UI
- Form validation and error handling
- RESTful API architecture

## Tech Stack

### Backend
- Node.js
- Express.js
- JWT (jsonwebtoken)
- bcrypt for password hashing
- MongoDB with Mongoose

### Frontend
- React.js
- Axios for API calls
- Modern CSS styling

## Getting Started

### Prerequisites

- Node.js (v14 or higher)
- MongoDB (local installation or Atlas account)

**📋 MongoDB Setup Required:** See [MONGODB_SETUP.md](MONGODB_SETUP.md) for detailed MongoDB installation and configuration instructions.

### Backend Setup

1. Navigate to the backend directory:
   ```bash
   cd backend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Set up MongoDB:
   - **Quick option:** Use [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) (free cloud database)
   - **Local option:** Install MongoDB locally
   - **See detailed guide:** [MONGODB_SETUP.md](MONGODB_SETUP.md)

4. Create a `.env` file based on `.env.example`:
   ```bash
   cp .env.example .env
   ```

5. Update the `.env` file with your MongoDB connection string:
   ```
   MONGODB_URI=mongodb://localhost:27017/login-system
   # OR for MongoDB Atlas:
   # MONGODB_URI=mongodb+srv://username:password@cluster.xxxxx.mongodb.net/login-system
   ```

6. Start the server:
   ```bash
   npm start
   ```

The backend will run on `http://localhost:5000`

### Frontend Setup

1. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm start
   ```

The frontend will run on `http://localhost:3000`

## API Endpoints

### Authentication

- `POST /api/auth/register` - Register a new user
- `POST /api/auth/login` - Login user
- `GET /api/auth/verify` - Verify JWT token
- `GET /api/auth/profile` - Get user profile (protected)

## Project Structure

```
login-system/
├── backend/
│   ├── config/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── server.js
│   └── package.json
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   ├── services/
│   │   ├── App.js
│   │   └── index.js
│   └── package.json
└── README.md
```

## Security Features

- Passwords are hashed using bcrypt
- JWT tokens for stateless authentication
- Protected routes with authentication middleware
- CORS configuration
- Environment variables for sensitive data

## License

MIT

