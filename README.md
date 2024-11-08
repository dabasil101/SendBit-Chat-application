#Sendbit Chat Application
Sendbit is a real-time chat application built with React, Express, MongoDB, and Socket.io. Users can create accounts, join chat rooms, and communicate with each other in real-time. Messages are stored in MongoDB, allowing users to view previous messages when they log back in.

#Table of Contents
Features
Technologies Used
Installation
Usage
Folder Structure
API Endpoints
Environment Variables
Contributing
License
Features
Real-time messaging powered by Socket.io
User authentication (signup and login)
Chat rooms with message history
User presence indicator to show online users
Persistent message storage with MongoDB
Responsive design for mobile and desktop
Technologies Used
Frontend: React, Socket.io-client
Backend: Express, Socket.io, MongoDB
Database: MongoDB
Communication: Socket.io for real-time messaging
Installation
To run Sendbit locally, follow these steps:

#Prerequisites
Node.js
MongoDB
Git
Steps
Clone the Repository

bash
Copy code
git clone https://github.com/yourusername/sendbit.git
cd sendbit
Install Dependencies

For both server and client:

bash
Copy code
# In the root directory
npm install
cd client
npm install
Environment Variables

Create a .env file in the root directory with the following variables:

plaintext
Copy code
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
Run MongoDB

Start your MongoDB server if it isn’t already running:

bash
Copy code
mongod
Run the Application

Open two terminals to start both the server and the client:

Server:

bash
Copy code
npm run server
Client:

bash
Copy code
cd client
npm start
The client will start on http://localhost:3000 and the server on http://localhost:5000.

Usage
Sign Up: Create a new account.
Log In: Use your account credentials to log in.
Chat: Select a user to start chatting. The chat window updates in real-time.
Logout: Log out from the application to end your session.
Folder Structure
graphql
Copy code
sendbit/
├── client/                  # React frontend
│   ├── public/
│   ├── src/
│   │   ├── components/      # Reusable components (ChatWindow, Login, Signup, etc.)
│   │   ├── services/        # Services for API requests
│   │   ├── App.js           # Main React component
│   │   └── index.js         # Entry point for React
├── server/
│   ├── controllers/         # Request handlers
│   ├── models/              # Mongoose schemas
│   ├── routes/              # API routes
│   ├── index.js             # Entry point for Express server
│   └── socket.js            # Socket.io server logic
└── README.md
API Endpoints
User Authentication

POST /api/auth/signup - Register a new user
POST /api/auth/login - Log in an existing user
Messages

POST /api/messages/add - Add a new message
GET /api/messages/get - Retrieve messages between users
Users

GET /api/users - Get all connected users
Environment Variables
Variable	Description
PORT	Port for the server
MONGO_URI	MongoDB connection URI
JWT_SECRET	Secret key for JWT tokens
Contributing
Contributions are welcome! Feel free to open a pull request or submit issues.
