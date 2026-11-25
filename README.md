# WorkDesk – Employee, Task & Support Management System

A full-stack web application for managing employees, tasks, leave requests, performance reviews, and workplace support operations through a centralized platform.

## Overview

WorkDesk is a role-based employee management system designed to simplify day-to-day organizational activities.

It provides separate functionalities for administrators and employees, helping organizations manage employee information, assign and track tasks, process leave requests, monitor performance, and handle support tickets.

## Key Features

### Authentication & Authorization
- Employee registration and login
- JWT-based authentication
- Role-based access control
- Protected application routes

### Employee Management
- Add, view, update, and delete employee records
- Search and filter employee information

### Task Management
- Create and assign tasks
- Track task progress and status
- Manage task priorities and deadlines
- Task workload and recommendation functionality

### Leave Management
- Submit leave requests
- View leave records
- Approve or reject leave requests
- Track leave status

### Support Ticket Management
- Raise support tickets
- Manage ticket priorities and statuses
- Assign tickets to administrators
- Exchange messages through support tickets

### Performance Management
- Create employee performance reviews
- View performance ratings and remarks
- Track employee performance statistics

### Dashboard & Analytics
- Admin dashboard with management statistics
- Employee dashboard with personal task and support information
- Workload and performance statistics

## Technology Stack

| Layer | Technologies |
|---|---|
| Frontend | React 18, TypeScript |
| Styling | Tailwind CSS |
| Routing | React Router |
| Backend | Node.js, Express.js |
| Database | MySQL |
| Authentication | JWT, bcryptjs |
| API Communication | Axios, REST APIs |
| Development Tools | Vite, Nodemon |
| API Testing | Postman |
| Version Control | Git, GitHub |

## System Architecture

WorkDesk follows a three-layer architecture:

1. **Frontend:** React and TypeScript provide the user interface and handle user interactions.
2. **Backend:** Node.js and Express.js handle API requests, authentication, authorization, and business logic.
3. **Database:** MySQL stores and manages application data.

### Application Flow

```text
        User
         |
         v
 React Frontend
         |
         | HTTP Requests (Axios)
         v
 Express REST APIs
         |
         v
 Authentication & Business Logic
         |
         v
    MySQL Database
```

## Database Design

The application uses MySQL with the following tables:

- roles
- users
- tasks
- leaves
- tickets
- ticket_messages
- performance_reviews
- contact_messages

## Project Structure

```text
WorkDesk/
├── frontend/
│   ├── src/
│   │   ├── api/
│   │   ├── components/
│   │   ├── context/
│   │   ├── pages/
│   │   ├── types/
│   │   └── utils/
│   └── package.json
│
├── backend/
│   ├── config/
│   ├── controllers/
│   ├── database/
│   ├── middleware/
│   ├── routes/
│   ├── utils/
│   ├── app.js
│   └── package.json
│
├── .gitignore
└── README.md
```

## Installation & Setup

### Prerequisites

- Node.js and npm
- MySQL Server 8
- Git

### 1. Clone the Repository

```bash
git clone https://github.com/Anjali163/WorkDesk-employee-management-system.git
cd WorkDesk-employee-management-system
```

### 2. Configure the Database

1. Open MySQL Workbench.
2. Execute the SQL script:

```text
backend/database/schema.sql
```

**Important:** The schema script drops an existing database named `workdesk` before recreating it. Back up existing data before executing it.

### 3. Configure and Run the Backend

```bash
cd backend
npm install
```

Configure the backend environment variables in a local `.env` file.

Run the seed script if required:

```bash
npm run seed
```

Start the backend:

```bash
npm run dev
```

Backend URL: `http://localhost:5000`

### 4. Configure and Run the Frontend

Open another terminal:

```bash
cd frontend
npm install
```

Configure the frontend environment variables if required.

Start the frontend:

```bash
npm run dev
```

Frontend URL: `http://localhost:5173`

*Note: Use the environment variable names and npm scripts defined in the respective project files.*

## API Documentation

API endpoints, HTTP methods, and access permissions are documented in:

`backend/API.md`

## Screenshots

Application screenshots will be added here to demonstrate the user interface and major functionalities.

## Future Enhancements

- Advanced employee search and filtering
- Improved dashboard analytics
- Automated testing
- Cloud deployment
- Enhanced reporting functionality

## Author

**Anjali Nanavare**

Full-Stack Development Project

[GitHub Profile](https://github.com/Anjali163)

---

If you find this project interesting, feel free to explore the repository and its implementation.