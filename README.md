# Task Management App Backend

## Overview
This is the backend implementation of the Task Management App. It provides APIs for user authentication, task management, and a manager role with enhanced permissions.

## Features
- **User Authentication**: Signup, login, and secure authentication.
- **Task Management**: Users can add, edit, and delete tasks.
- **Manager Role**: Managers can add users and manage everything.
- **Database Connection**: Successfully connected to a database for persistent storage.

## Technologies Used
- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Authentication**: JWT (JSON Web Token)
- **Authorization**: Role-based access control (User & Manager)

## Installation

1. Clone the repository:
   ```sh
   git clone [repository_link]
   cd task-management-backend
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Set up environment variables in a `.env` file:
   ```env
   PORT=5000
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret
   ```
4. Run the server:
   ```sh
   npm start
   ```

## API Endpoints

### Authentication
- **POST /api/auth/signup** - Register a new user
- **POST /api/auth/login** - Login and get a token

### Task Management
- **POST /api/tasks** - Create a new task (User & Manager)
- **GET /api/tasks** - Retrieve all tasks
- **PUT /api/tasks/:id** - Update a task (Owner or Manager)
- **DELETE /api/tasks/:id** - Delete a task (Owner or Manager)

### Manager Features
- **POST /api/managers/add-user** - Managers can add new users
- **GET /api/managers/users** - Get a list of all users
- **DELETE /api/managers/users/:id** - Managers can remove users

## Future Enhancements
- Implement notifications for task updates.
- Add real-time collaboration features using WebSockets.
- Improve user interface and integrate with a React Native frontend.

## Contribution
Feel free to fork this repository and submit pull requests for improvements.

## License
This project is open-source and available under the [MIT License](LICENSE).
