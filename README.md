# Node.js-Exercise-2

# PICK 'n STEAL API

## Overview

This project is a simple RESTful API built with **Express.js** for a fictional retailer called **PICK 'n STEAL**. The API demonstrates the use of common HTTP methods to manage employee and manager data without using a database. All data is stored in memory using JavaScript arrays.

## Technologies Used

* Node.js
* Express.js
* Nodemon

## Installation

1. Clone the repository:

```bash
git clone <repository-url>
```

2. Navigate to the project directory:

```bash
cd PICK-n-STEAL
```

3. Install the required dependencies:

```bash
npm install
```

## Running the Application

To start the application:

```bash
npm start
```

To run the application in development mode with Nodemon:

```bash
npm run dev
```

The server will start on:

```
http://localhost:3000
```

## API Endpoints

### Home

| Method | Endpoint | Description                   |
| ------ | -------- | ----------------------------- |
| GET    | `/`      | Displays the welcome message. |

### Employees

| Method | Endpoint         | Description                           |
| ------ | ---------------- | ------------------------------------- |
| GET    | `/employees`     | Retrieve all employees.               |
| POST   | `/employees`     | Add a new employee.                   |
| PATCH  | `/employees/:id` | Update specific employee information. |
| DELETE | `/employees/:id` | Delete an employee by ID.             |

### Managers

| Method | Endpoint        | Description                          |
| ------ | --------------- | ------------------------------------ |
| GET    | `/managers`     | Retrieve all managers.               |
| POST   | `/managers`     | Add a new manager.                   |
| PATCH  | `/managers/:id` | Update specific manager information. |
| DELETE | `/managers/:id` | Delete a manager by ID.              |

## Testing the API

The API was tested using **Thunder Client** (or Postman).

### Example Requests

#### GET Employees

```
GET http://localhost:3000/employees
```

#### POST Employee

```
POST http://localhost:3000/employees
```

Request Body:

```json
{
  "id": 3,
  "name": "Peter",
  "position": "Driver"
}
```

#### PATCH Employee

```
PATCH http://localhost:3000/employees/3
```

Request Body:

```json
{
  "position": "Supervisor"
}
```

#### DELETE Employee

```
DELETE http://localhost:3000/employees/3
```

## HTTP Methods Used

### GET

Retrieves data from the server without modifying it.

### POST

Creates and adds a new resource to the collection.

### PATCH

Updates specific fields of an existing resource.

### DELETE

Removes a resource from the collection.

## Project Structure

```
PICK-n-STEAL/
│── routes/
│   ├── employees.js
│   └── managers.js
│── app.js
│── package.json
│── README.md
```

## Notes

* No MySQL or other database is used.
* Data is stored in memory and resets whenever the server restarts.
* The project demonstrates Express routing and REST API fundamentals.

