# PrimeAi
:Frontend Developer Task
Overview
This application is a scalable web app with a Next.js frontend and an Express backend. It features JWT authentication, a user dashboard, and a Task management system.

Features
**Authentication**: Register and Login with JWT.
**Dashboard:** Protected route displaying user profile.
**Task Management:** CRUD operations for tasks (Create, Read, Update, Delete).
**Filtering:** Filter tasks by status (All, Pending, Completed).
**UI Redesign:** Modern split-screen Auth pages and elegant Dashboard with card layout.
**Security:** Strong password validation and email case insensitivity.


Setup Guide (For New Users)
If you have downloaded this project, follow these steps to set it up on your local machine.

Prerequisites
Node.js: Install from nodejs.org.
MongoDB: Install locally or have a MongoDB Atlas connection string ready.
1. Clone/Download the Repository
   
--git clone <repository-url>
--cd <repository-folder>

3. Backend Setup
The backend runs on port **5000**.

Navigate to the server directory:

--cd server
Install dependencies:
--npm install

Configure Environment Variables:
Create a .env
 file in the server directory.
Add the following:

  PORT=5000
  MONGODB_URI=mongodb://localhost:27017/webapp
  JWT_SECRET=your_super_secret_key
(Replace MONGODB_URI with your actual connection string if different)
Start the server:
npm start
3. Frontend Setup
The frontend runs on port 3000.

Open a new terminal (keep the backend running).

Navigate to the webapp directory:
--cd webapp
Install dependencies:
--npm install
Start the development server:
--npm run dev
Open your browser and visit http://localhost:3000.

Verification Steps
Prerequisites
MongoDB: Ensure MongoDB is running locally or update .env
 in server with your URI.
 
Ports: Ensure ports 3000 (Frontend) and 5000 (Backend) are free.
1. Start the Backend
cd server
npm start
Expected Output: Server running on port 5000 and MongoDB Connected.

2. Start the Frontend
cd webapp
npm run dev
Expected Output: Next.js server starts on http://localhost:3000.

3. User Flow Verification
Register: Go to http://localhost:3000/register. Enter Name, Email, Password. Click Register.
Result: Redirects to Dashboard.
Dashboard: Verify "Welcome, [Name]" and Profile details.
Add Task: Enter "Test Task" and click Add.
Result: Task appears in the list.
Complete Task: Click "Complete".
Result: Task status changes (visual indicator).
Filter: Select "Completed".
Result: Only completed tasks show.
Delete Task: Click "Delete".
Result: Task is removed.
Logout: Click "Logout".
Result: Redirects to Login.

**API Endpoints**
POST /api/auth/register: Register user.
POST /api/auth/login: Login user.
GET /api/auth/user: Get current user.
GET /api/tasks: Get all tasks.
POST /api/tasks: Create task.
PUT /api/tasks/:id: Update task.
DELETE /api/tasks/:id: Delete task.
