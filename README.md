# 🚀 WorkFlow – Employee Management & Leave Management System

A modern **full-stack Employee Management and Leave Management System** built with **Django REST Framework, React.js, MySQL, and JWT Authentication**.

WorkFlow provides a centralized platform for managing employees, departments, leave requests, authentication, and administrative operations through secure REST APIs and a responsive React frontend.

---

## ✨ Features

### 🔐 Authentication

* User registration and login
* JWT access and refresh tokens
* Protected routes
* Authentication-based API access
* Logout functionality

### 👨‍💼 Employee Management

* Add employees
* View employee details
* Update employee information
* Delete employees
* Search employees
* Filter employees
* View employees by department
* Manage employee status

### 🏢 Department Management

* Create departments
* View departments
* Update departments
* Delete departments
* View employees belonging to departments

### 📝 Leave Management

Employees can:

* Apply for leave
* View leave history
* Check leave status
* View leave details

Administrators can:

* View all leave requests
* Filter leave requests
* Approve leave requests
* Reject leave requests
* Add reviewer comments

### 📊 Dashboard

* Total Employees
* Total Departments
* Pending Leaves
* Approved Leaves
* Rejected Leaves

### 🔎 API Features

* RESTful APIs
* CRUD operations
* JWT authentication
* Role-based permissions
* Search
* Filtering
* Ordering
* Pagination
* Validation
* Error handling

---

# 🛠️ Tech Stack

## Backend

* 🐍 Python
* 🎯 Django
* 🔌 Django REST Framework
* 🗄️ MySQL
* 🔐 JWT Authentication
* 🌐 Django CORS Headers

## Frontend

* ⚛️ React.js
* 🟨 JavaScript
* 🧭 React Router
* 📡 Axios
* 🎨 Bootstrap
* 💅 Custom CSS
* 🪝 React Hooks

## Tools

* Git
* GitHub
* VS Code
* Postman
* Google Antigravity

---

# 🏗️ Project Architecture

```text
WorkFlow/
│
├── backend/
│   │
│   ├── manage.py
│   ├── requirements.txt
│   ├── .env
│   │
│   ├── config/
│   │   ├── settings.py
│   │   ├── urls.py
│   │   ├── asgi.py
│   │   └── wsgi.py
│   │
│   ├── accounts/
│   │   ├── models.py
│   │   ├── serializers.py
│   │   ├── views.py
│   │   ├── permissions.py
│   │   └── urls.py
│   │
│   ├── employees/
│   │   ├── models.py
│   │   ├── serializers.py
│   │   ├── views.py
│   │   ├── permissions.py
│   │   └── urls.py
│   │
│   ├── departments/
│   │   ├── models.py
│   │   ├── serializers.py
│   │   ├── views.py
│   │   └── urls.py
│   │
│   └── leaves/
│       ├── models.py
│       ├── serializers.py
│       ├── views.py
│       ├── permissions.py
│       └── urls.py
│
└── frontend/
    │
    ├── package.json
    ├── public/
    │
    └── src/
        ├── components/
        ├── pages/
        ├── services/
        ├── hooks/
        ├── context/
        ├── routes/
        ├── assets/
        ├── styles/
        ├── App.jsx
        └── main.jsx
```

---

# 🗄️ Database Models

## Department

```text
Department
├── id
├── name
├── description
├── created_at
└── updated_at
```

## Employee

```text
Employee
├── id
├── employee_id
├── first_name
├── last_name
├── email
├── phone
├── date_of_birth
├── gender
├── address
├── designation
├── department
├── joining_date
├── salary
├── profile_image
├── is_active
├── created_at
└── updated_at
```

## Leave

```text
Leave
├── id
├── employee
├── leave_type
├── start_date
├── end_date
├── reason
├── status
├── applied_at
├── reviewed_at
└── reviewer_comment
```

---

# 🔗 REST API Endpoints

## 🔐 Authentication

| Method | Endpoint                   | Description                |
| ------ | -------------------------- | -------------------------- |
| POST   | `/api/auth/register/`      | Register a new user        |
| POST   | `/api/auth/login/`         | User login                 |
| POST   | `/api/auth/token/refresh/` | Refresh JWT token          |
| GET    | `/api/auth/profile/`       | Get logged-in user profile |

## 👨‍💼 Employee APIs

| Method | Endpoint               | Description               |
| ------ | ---------------------- | ------------------------- |
| GET    | `/api/employees/`      | Get all employees         |
| POST   | `/api/employees/`      | Create employee           |
| GET    | `/api/employees/{id}/` | Get employee              |
| PUT    | `/api/employees/{id}/` | Update employee           |
| PATCH  | `/api/employees/{id}/` | Partially update employee |
| DELETE | `/api/employees/{id}/` | Delete employee           |

## 🏢 Department APIs

| Method | Endpoint                 | Description                 |
| ------ | ------------------------ | --------------------------- |
| GET    | `/api/departments/`      | Get all departments         |
| POST   | `/api/departments/`      | Create department           |
| GET    | `/api/departments/{id}/` | Get department              |
| PUT    | `/api/departments/{id}/` | Update department           |
| PATCH  | `/api/departments/{id}/` | Partially update department |
| DELETE | `/api/departments/{id}/` | Delete department           |

## 📝 Leave APIs

| Method | Endpoint                    | Description            |
| ------ | --------------------------- | ---------------------- |
| GET    | `/api/leaves/`              | Get leave requests     |
| POST   | `/api/leaves/`              | Apply for leave        |
| GET    | `/api/leaves/{id}/`         | Get leave details      |
| PUT    | `/api/leaves/{id}/`         | Update leave           |
| PATCH  | `/api/leaves/{id}/`         | Partially update leave |
| DELETE | `/api/leaves/{id}/`         | Delete leave           |
| PATCH  | `/api/leaves/{id}/approve/` | Approve leave          |
| PATCH  | `/api/leaves/{id}/reject/`  | Reject leave           |

---

# 🔐 Authentication Flow

```text
User
  │
  ▼
Login
  │
  ▼
Django REST API
  │
  ▼
Access Token + Refresh Token
  │
  ▼
React Application
  │
  ▼
Authorization Header
  │
  ▼
Protected API
```

Example authorization header:

```http
Authorization: Bearer <access_token>
```

---

# ⚙️ Installation & Setup

## 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/WorkFlow.git
cd WorkFlow
```

---

# 🐍 Backend Setup

## 2. Navigate to Backend

```bash
cd backend
```

## 3. Create Virtual Environment

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

### Linux / macOS

```bash
python3 -m venv venv
source venv/bin/activate
```

---

## 4. Install Dependencies

```bash
pip install -r requirements.txt
```

---

# 🗄️ MySQL Configuration

Create the database:

```sql
CREATE DATABASE workflow_db;
```

Create a `.env` file inside the backend directory:

```env
SECRET_KEY=your_secret_key
DEBUG=True

DB_NAME=workflow_db
DB_USER=root
DB_PASSWORD=your_mysql_password
DB_HOST=localhost
DB_PORT=3306
```

> ⚠️ Never upload your `.env` file or database password to GitHub.

---

# 🔄 Run Django Migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

---

# 👤 Create Superuser

```bash
python manage.py createsuperuser
```

---

# ▶️ Start Backend Server

```bash
python manage.py runserver
```

Backend:

```text
http://127.0.0.1:8000/
```

---

# ⚛️ Frontend Setup

Open a new terminal and navigate to the frontend:

```bash
cd frontend
```

Install dependencies:

```bash
npm install
```

---

# 🌐 Frontend Environment Variables

Create a `.env` file inside the frontend directory:

```env
VITE_API_URL=http://127.0.0.1:8000/api
```

---

# ▶️ Start React Application

```bash
npm run dev
```

Frontend:

```text
http://localhost:5173/
```

---

# 🔄 Application Architecture

```text
                ┌──────────────────────┐
                │       React.js       │
                │       Frontend       │
                └──────────┬───────────┘
                           │
                         Axios
                           │
                           ▼
                ┌──────────────────────┐
                │   Django REST API    │
                │       Backend        │
                └──────────┬───────────┘
                           │
                      Django ORM
                           │
                           ▼
                ┌──────────────────────┐
                │        MySQL         │
                │       Database       │
                └──────────────────────┘
```

---

# 🧪 API Testing

The APIs can be tested using:

* Postman
* Thunder Client
* Browser
* React frontend

Example login request:

```http
POST /api/auth/login/
```

Request body:

```json
{
  "username": "admin",
  "password": "your_password"
}
```

Example response:

```json
{
  "access": "your_access_token",
  "refresh": "your_refresh_token"
}
```

---

# 📸 Screenshots

Add your application screenshots inside a `screenshots` folder.

## 🔐 Login

```markdown
![Login](screenshots/login.png)
```

## 📊 Dashboard

```markdown
![Dashboard](screenshots/dashboard.png)
```

## 👨‍💼 Employee Management

```markdown
![Employees](screenshots/employees.png)
```

## 🏢 Department Management

```markdown
![Departments](screenshots/departments.png)
```

## 📝 Leave Management

```markdown
![Leaves](screenshots/leaves.png)
```

---

# 📚 What I Learned

Through this project, I strengthened my understanding of:

* Python
* Django
* Django REST Framework
* REST API development
* ModelSerializer
* ViewSets
* DefaultRouter
* Django ORM
* MySQL
* JWT Authentication
* Permissions
* React Components
* React Hooks
* React Router
* Axios
* CRUD Operations
* API Integration
* Search and Filtering
* Pagination
* Responsive UI Development
* Full-Stack Application Architecture
* Git and GitHub

---

# 🚀 Future Enhancements

* 📧 Email notifications
* 🔔 Real-time notifications
* 📊 Advanced analytics
* 📅 Calendar-based leave management
* 📁 Employee document management
* 🖼️ Profile image upload
* 🌙 Dark mode
* ☁️ Cloud deployment
* 🐳 Docker support
* 🔄 CI/CD pipeline
* 📈 Advanced employee reports

---

# 👨‍💻 Author

## Dastagiri Potuganti

**Python Full Stack Developer | Django Developer | React.js Learner**

B.Sc. Computer Science graduate passionate about building full-stack web applications using Python, Django, REST APIs, React.js, and MySQL.

### 🔗 GitHub

[![GitHub](https://img.shields.io/badge/GitHub-Dastagiri--Potuganti-black?style=for-the-badge\&logo=github)](https://github.com/Dastagiri-Potuganti)

### 🔗 LinkedIn

Add your LinkedIn profile URL here.

---

# ⭐ Support

If you find this project useful, consider giving the repository a ⭐ on GitHub.

---

# 📄 License

This project is created for **learning, portfolio, and educational purposes**.
