### Event Management System - MERN Stack
🚀 Features
✅ Create, view, update, and delete events

🎨 Simple and intuitive user interface

📱 Responsive design

🔄 RESTful API backend

### 🛠 Technologies Used
Frontend:

React.js

React Router

Axios

Backend:

Node.js

Express.js

Database:

MongoDB

Styling:

Plain CSS

### 📋 Prerequisites
Node.js (v14 or higher)

npm or yarn

MongoDB (local instance or cloud)

### 🖥 Setup Guide
🔧 Backend Installation
1. Navigate to backend folder
cd backend
2. Install dependencies
npm install
3. Environment Setup
Create .env file in backend folder with:

env
MONGO_URI=mongodb://localhost:27017/eventmanager
PORT=5000
4. Start the server
npm start
For development with auto-restart:
npm run dev
### 🎨 Frontend Installation
1. Navigate to frontend folder
bash
cd frontend
2. Install dependencies
bash
npm install
3. Start the application
bash
npm start

### 🔌 API Endpoints
Method	Endpoint	Description
GET	/api/events	Get all events
POST	/api/events	Create new event
GET	/api/events/:id	Get single event
PUT	/api/events/:id	Update event
DELETE	/api/events/:id	Delete event
### ⚙ Available Commands
Backend:

bash
npm start    # Start production server
npm run dev  # Start dev server (with nodemon)
Frontend:

bash
npm start    # Run dev server
npm test     # Run tests
npm run build # Create production build


### 🔮 Future Improvements
🔐 User authentication

📝 Form validation

🛑 Error notifications

💅 UI improvements with CSS framework

🔍 Search & filtering

📖 Pagination

🤝 Contributing
Pull requests welcome! For major changes, please open an issue first.

### 📜 License
MIT

💡 Tip: Make sure MongoDB is running before starting the backend server!
🚨 Note: The frontend will run on port 3000, backend on port 5000 by default.
