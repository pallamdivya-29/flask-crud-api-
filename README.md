# Flask CRUD REST API with PostgreSQL and Docker

A simple CRUD (Create, Read, Update, Delete) REST API built using Python Flask, Flask-SQLAlchemy, and PostgreSQL. The application is containerized using Docker and Docker Compose.

## 🚀 Features

- Create a new user
- Get all users
- Get a user by ID
- Update user details
- Delete a user
- REST API endpoints using Flask
- PostgreSQL database integration
- SQLAlchemy ORM
- Dockerized Flask application
- Docker Compose for managing Flask and PostgreSQL containers
- Simple HTML home page

## 🛠️ Technologies Used

- Python 3.6
- Flask
- Flask-SQLAlchemy
- PostgreSQL 12
- SQLAlchemy
- Docker
- Docker Compose
- HTML
- JSON

## 📁 Project Structure

flask-crud-api/
│
├── app.py
├── Dockerfile
├── docker-compose.yml
├── requirements.txt
│
└── templates/
    └── index.html

## 🔗 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/` | Display the home page |
| GET | `/test` | Test the API |
| POST | `/users` | Create a new user |
| GET | `/users` | Get all users |
| GET | `/users/<id>` | Get a user by ID |
| PUT | `/users/<id>` | Update a user |
| DELETE | `/users/<id>` | Delete a user |

## 📌 API Usage

### 1. Test API

**GET**

http://localhost:4000/test

Example response:

{
    "message": "test route"
}

### 2. Create a User

**POST**

http://localhost:4000/users

Request body:

{
    "username": "Supraja",
    "email": "supraja@example.com"
}

Example response:

{
    "message": "user created"
}

### 3. Get All Users

**GET**

http://localhost:4000/users

Example response:

[
    {
        "id": 1,
        "username": "Supraja",
        "email": "supraja@example.com"
    }
]

### 4. Get User by ID

**GET**

http://localhost:4000/users/1

Example response:

{
    "user": {
        "id": 1,
        "username": "Supraja",
        "email": "supraja@example.com"
    }
}

### 5. Update User

**PUT**

http://localhost:4000/users/1

Request body:

{
    "username": "Supraja Updated",
    "email": "updated@example.com"
}

Example response:

{
    "message": "user updated"
}

### 6. Delete User

**DELETE**

http://localhost:4000/users/1

Example response:

{
    "message": "user deleted"
}

## 🐳 Running the Project with Docker

### Prerequisites

Make sure the following are installed:

- Docker Desktop
- Docker Compose
- Git

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/flask-crud-api.git
