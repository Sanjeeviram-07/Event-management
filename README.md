Event Management System - MERN Stack
A simple CRUD (Create, Read, Update, Delete) event management system built with the MERN stack (MongoDB, Express.js, React, Node.js).

Features
Create, view, update, and delete events

Simple and intuitive user interface

Responsive design

RESTful API backend

Technologies Used
Frontend: React.js, React Router, Axios

Backend: Node.js, Express.js

Database: MongoDB

Styling: Plain CSS

Prerequisites
Node.js (v14 or higher)

npm or yarn

MongoDB (local instance or cloud)

Installation
Backend Setup
Navigate to the backend folder:

bash
cd backend
Install dependencies:

bash
npm install
Create a .env file in the backend folder with the following content:

MONGO_URI=mongodb://localhost:27017/eventmanager
PORT=5000
Start the backend server:

bash
npm start
# or for development with nodemon
npm run dev
Frontend Setup
Navigate to the frontend folder:

bash
cd frontend
Install dependencies:

bash
npm install
Start the React application:

bash
npm start
Project Structure
event-management/
├── backend/               # Backend server code
│   ├── models/            # MongoDB models
│   ├── routes/            # API routes
│   ├── .env               # Environment variables
│   ├── package.json       # Backend dependencies
│   └── server.js          # Express server setup
│
└── frontend/             # Frontend React app
    ├── public/           # Static files
    ├── src/
    │   ├── components/    # React components
    │   ├── App.js         # Main App component
    │   └── index.js       # React entry point
    └── package.json      # Frontend dependencies
API Endpoints
GET /api/events - Get all events

POST /api/events - Create a new event

GET /api/events/:id - Get a single event

PUT /api/events/:id - Update an event

DELETE /api/events/:id - Delete an event

Available Scripts
In both the backend and frontend directories, you can run:

Backend
npm start - Starts the backend server

npm run dev - Starts the server with nodemon (auto-restart on changes)

Frontend
npm start - Runs the app in development mode

npm test - Launches the test runner

npm run build - Builds the app for production

Screenshots
(You can add screenshots of your application here)

Future Improvements
Add user authentication

Implement form validation

Add error handling notifications

Improve UI with a CSS framework

Add search and filtering functionality

Implement pagination

Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

License
MIT
