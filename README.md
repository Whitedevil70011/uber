Uber Clone — Frontend & Backend

A simple Uber-style ride-hailing application containing separate frontend/ (client) and Backend/ (server) directories.

📁 Project Structure
uber/
├─ Backend/        # Node.js / Express backend
│  ├─ src/
│  ├─ package.json
│  └─ .env.example
├─ frontend/       # JavaScript frontend (React or similar)
│  ├─ src/
│  └─ package.json
└─ README.md

🚀 Features

User authentication (JWT)

Passenger & Driver modes

Create, cancel, and accept rides

Real-time ride updates (Socket.IO or similar)

Map integration (Google Maps / Mapbox)

Driver live location updates

REST API for all operations

📦 Requirements

Node.js (v16+)

npm or yarn

MongoDB (local or Atlas)

Map API key (Google/Mapbox)

Optional: Redis for socket scaling

🔧 Backend Setup

Navigate to backend directory:

cd Backend
npm install


Create a .env file:

PORT=5000
MONGO_URI=mongodb://localhost:27017/uber-clone
JWT_SECRET=your_jwt_secret
GOOGLE_MAPS_API_KEY=your_key
SOCKET_ORIGIN=http://localhost:3000


Start backend:

npm run dev

🎨 Frontend Setup

Navigate to frontend directory:

cd frontend
npm install


Create a .env file:

VITE_API_URL=http://localhost:5000/api
VITE_MAPS_KEY=your_map_api_key


Start frontend:

npm run dev

🔌 API Overview (Sample)
Auth

POST /api/auth/register

POST /api/auth/login

Users / Drivers

GET /api/users/me

GET /api/drivers?lat=&lng=&radius=

Rides

POST /api/rides

POST /api/rides/:id/cancel

POST /api/rides/:id/accept

GET /api/rides/:id

Real-Time (Sockets)

ride:created

ride:accepted

driver:location

ride:updated

🧪 Testing

Backend uses Jest/Supertest (if implemented).
Frontend uses React Testing Library (if implemented).

🚀 Deployment

Frontend → Vercel / Netlify

Backend → Render / Railway / AWS

Database → MongoDB Atlas

Ensure HTTPS, CORS, environment variables, and production builds.

❗ Troubleshooting

CORS errors: add frontend URL to backend CORS config

Socket not connecting: verify backend URL & port

Map not loading: check API key / billing
