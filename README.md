# REST API with Node.js and Express

## UserProfileAPI

UserProfileAPI is a RESTful API developed with Node.js and Express, designed to manage user profiles in a MongoDB database. It supports creating, reading, updating, and deleting (CRUD) user profiles with fields for name, email, age, country, and password.

## Approach

The API is built on the MVC architecture to ensure a separation of concerns. Models define the schema for user data, controllers handle the business logic, and routes manage the API endpoints. Passwords are hashed before storage and excluded from API responses to enhance security.

## Features

- CRUD operations for user profiles
- Password hashing with bcryptjs
- Validation of email formats
- Exclusion of passwords from API responses

## Getting Started

Pre-requisites:

- Node.js
- MongoDB
- NPM or Yarn (Node Package Manager or Yarn Package Manager)

## Installation

1. Clone the repository

```bash
git clone
```

2. Install dependencies

```bash
npm install
```

3. Start the server

```bash
npm start
```

## Usage

The API can be accessed at http://localhost:3000/api/users
Also find deployed URL at https://mongo-curd.vercel.app/users

Endpoints:

| Method | Endpoint   | Description                     | Body                                                                                                        |
| ------ | ---------- | ------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| GET    | /users     | Fetch all user profiles         | N/A                                                                                                         |
| POST   | /users     | Create a new user profile       | { "name": "John Doe", "email": "john@example.com", "age": 30, "country": "USA", "password": "password123" } |
| PUT    | /users/:id | Update an existing user profile | { "name": "Jane Doe", "email": "jane@example.com", "age": 25, "country": "Canada" }                         |
| DELETE | /users/:id | Delete an existing user profile | N/A                                                                                                         |

## Sample Data for Testing

Create a new user profile:

- POST /users

```bash
{
  "name": "John Doe",
  "email": "john.doe@example.com",
  "age": 28,
  "country": "USA",
  "password": "securePassword123"
}  "password": "password123"
```

Update an existing user profile:

- PUT /users/<user-id>

```bash
{
  "name": "Jane Doe",
  "age": 29,
  "country": "Canada"
}
```

Get all user profiles:

- GET /users

```bash
N/A
```

Delete an existing user profile:

- DELETE /users/<user-id>

```bash
N/A
```

## Live Deployed Endpoint

You can access the API via the following live deployed endpoint:

[https://mongo-curd.vercel.app/users](https://mongo-curd.vercel.app/users)
