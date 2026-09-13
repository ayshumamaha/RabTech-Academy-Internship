TASK 4 
# FastAPI Microservice with JWT Authentication

## Overview

This project implements a secure Python web API using FastAPI, SQLite, and JSON Web Tokens (JWT).

The application provides user registration and login functionality and protects selected API endpoints using JWT-based authentication.

The project also demonstrates request validation, password hashing, database persistence, protected resources, and automatic API documentation through FastAPI's OpenAPI and Swagger interface.

## Features

* FastAPI-based REST API.
* User registration.
* User login.
* Password hashing.
* JWT token generation.
* JWT-based authentication.
* Protected API endpoints.
* SQLite database.
* Item creation and retrieval.
* Request validation using Pydantic.
* Automatic Swagger/OpenAPI documentation.
* Authentication error handling.

## Technologies Used

* Python
* FastAPI
* Uvicorn
* SQLite
* Pydantic
* PyJWT
* Requests
* Nest AsyncIO

## API Endpoints

### GET `/`

Checks whether the API is running.

### POST `/register`

Creates a new user account.

Example request:

```json
{
    "username": "student",
    "password": "student123"
}
```

### POST `/login`

Authenticates a registered user and returns a JWT access token.

Example response:

```json
{
    "access_token": "JWT_TOKEN",
    "token_type": "bearer"
}
```

### GET `/profile`

A protected endpoint that requires a valid JWT token.

### POST `/items`

Creates a protected item.

### GET `/items`

Returns stored items and requires authentication.

## Authentication

The application uses Bearer authentication.

After successful login, the generated JWT token is included in the request header:

```text
Authorization: Bearer <token>
```

Requests without a valid token are rejected.

## Password Security

User passwords are not stored directly in the database.

The application hashes the password before storing it.

This provides a basic demonstration of secure password storage practices.

## Database

SQLite is used as the database because it is lightweight and requires no separate database server.

The application creates:

```text
users.db
```

The database stores user and item information.

## Running the Project

Install the required packages:

```bash
pip install fastapi uvicorn pyjwt passlib[bcrypt] python-multipart nest-asyncio requests
```

Start the FastAPI application:

```python
uvicorn.run(
    "project4_api:app",
    host="0.0.0.0",
    port=8000
)
```

## API Documentation

FastAPI automatically provides interactive API documentation through Swagger UI.

The documentation endpoint is:

```text
/docs
```

When running locally, it can be accessed through:

```text
http://127.0.0.1:8000/docs
```

## Authentication Workflow

```text
User Registration
       ↓
Password Hashing
       ↓
SQLite Database
       ↓
User Login
       ↓
JWT Token Generation
       ↓
Protected API Request
       ↓
Token Validation
       ↓
Access Granted
```

## Unauthorized Request

If a protected endpoint is accessed without authentication, the API returns an HTTP 401 Unauthorized response.

Example:

```text
401 Unauthorized
```

## Project Objectives

* Develop a Python REST API.
* Understand FastAPI fundamentals.
* Implement authentication using JWT.
* Store application data using SQLite.
* Apply request validation.
* Understand protected API endpoints.
* Generate automatic API documentation.
* Practice backend microservice development.

## Applications

The project demonstrates the core architecture of a small authenticated backend service and can be extended for user-management systems, internal applications, and other API-based software systems.

## Author

M. Ayshwarya
