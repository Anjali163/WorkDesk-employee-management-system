# WorkDesk – Employee, Task & Support Management System

A full-stack web application designed to simplify employee management, task allocation, leave management and workplace support operations.

## Overview

WorkDesk is a role-based management application that provides a centralized platform for administrators and employees.

Administrators can manage employees, assign tasks, review performance and handle support requests, while employees can manage their tasks, apply for leaves and raise support tickets.

## Key Features

### Authentication & Authorization
- Employee registration and login
- JWT-based authentication
- Role-based access control (Admin and Employee)
- Protected application routes

### Employee Management
- Add new employees
- View employee records
- Update employee information
- Delete employee records
- Search and filter employees

### Task Management
- Create and assign tasks
- Track task progress
- Manage task priorities and deadlines
- Update task status
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
- Exchange messages on support tickets

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

## Project Architecture

The application follows a three-layer architecture:

1. **Frontend:** React and TypeScript provide the user interface and communicate with backend APIs.
2. **Backend:** Node.js and Express handle API requests, authentication, authorization and application logic.
3. **Database:** MySQL stores employee, task, leave, ticket and performance information.

Frontend → REST API → Backend → MySQL Database

## Database Design

The project uses MySQL with the following tables:

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
├── screenshots/
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
git clone https://github.com/YOUR_USERNAME/workdesk-employee-management-system.git
cd workdesk-employee-management-system
```

### 2. Configure the Database

Open MySQL Workbench and execute:

`backend/database/schema.sql`

**Note:** The schema script drops an existing database named `workdesk` before recreating it. Back up any existing data before executing it.

### 3. Configure the Backend

```bash
cd backend
npm install
```

Copy `.env.example` to `.env` and configure your MySQL credentials and JWT secret.

Run the seed script once:

```bash
npm run seed
```

Start the backend:

```bash
npm run dev
```

Backend URL: `http://localhost:5000`

### 4. Configure the Frontend

Open another terminal:

```bash
cd frontend
npm install
```

Copy `.env.example` to `.env` if you need to configure a different API URL.

Start the frontend:

```bash
npm run dev
```

Frontend URL: `http://localhost:5173`

## Demo Login

After successfully running the database seed script:

| Role | Email | Password |
|---|---|---|
| Admin | admin@workdesk.com | Password@123 |
| Employee | riya@workdesk.com | Password@123 |

These are local demonstration credentials only. Do not use them for a deployed application.

## API Documentation

Detailed API endpoints, HTTP methods and access permissions are documented in:

`backend/API.md`

## Screenshots


## Future Enhancements

- Advanced employee search and filtering
- Improved dashboard analytics
- Automated testing
- Cloud deployment
- Enhanced reporting functionality

## Author

**Anjali Nanavare**

Full-Stack Development Project

GitHub: https://github.com/Anjali163

---

If you find this project useful, feel free to explore the code and its implementation.
