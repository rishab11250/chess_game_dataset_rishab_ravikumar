# Chess Match Analytics API — Backend

A robust RESTful backend system built to store, analyze, and serve chess match data. This API provides comprehensive endpoints for match management, player profiles, opening theory, analytics, and advanced searching.

## 🚀 Tech Stack

- **Runtime:** Node.js (v20+)
- **Framework:** Express.js
- **Database:** MongoDB with Mongoose ODM
- **Auth:** JWT (jsonwebtoken + bcryptjs)
- **Validation:** express-validator
- **Logging:** morgan
- **Rate Limiting:** express-rate-limit

## 📁 Project Structure

```
server/
├── src/
│   ├── config/          # Database and environment configurations
│   ├── controllers/     # Request handlers (MVC)
│   ├── middlewares/     # Custom middlewares (auth, error, logger, etc.)
│   ├── models/          # Mongoose schemas
│   ├── routes/          # API route definitions
│   ├── scripts/         # DB seeding and utility scripts
│   ├── services/        # Business logic
│   ├── utils/           # Helper functions and standardized responses
│   ├── app.js           # Express app setup
│   └── server.js        # Entry point
├── .env.example         # Template for environment variables
├── package.json         # Project dependencies and scripts
└── README.md            # Project documentation
```

## 🛠️ Setup & Installation

1. **Clone the repository**
2. **Navigate to the server directory:**
   ```bash
   cd server
   ```
3. **Install dependencies:**
   ```bash
   pnpm install
   ```
4. **Environment Configuration:**
   - Copy `.env.example` to `.env`
   - Fill in your MongoDB URI and JWT secrets.
5. **Database Seeding:**
   - Ensure your MongoDB is running.
   - Run the seed script to import the chess match dataset:
     ```bash
     pnpm run seed
     ```
6. **Start the server:**
   - Development mode: `pnpm run dev`
   - Production mode: `pnpm start`

## ✨ Core Features

- **Authentication:** Secure registration and login with JWT and refresh token support.
- **Match Management:** Full CRUD operations for chess matches with soft-delete and archiving.
- **Player Analytics:** Detailed statistics for players including win rates, rating history, and opening preferences.
- **Opening Theory:** Categorized openings with win-rate analytics and complexity levels.
- **Advanced Search:** Multi-filter search functionality with fuzzy matching and autocomplete.
- **Aggregation Pipelines:** High-performance analytics powered by MongoDB's aggregation framework.
- **Admin Panel:** Specialized routes for user management and system health monitoring.

## 🔑 Environment Variables

Required variables in `.env`:
- `PORT`: Server port (default: 5000)
- `MONGODB_URI`: MongoDB connection string
- `JWT_SECRET`: Secret key for access tokens
- `JWT_REFRESH_SECRET`: Secret key for refresh tokens
- `NODE_ENV`: development / production
