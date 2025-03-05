# Category Management API

### Author: Shahd Hatem Abd Elgalil
### ID: 4211235

## Overview
The **Category Management API** is a robust and scalable solution for efficiently managing product categories. Built using **Node.js, Express, and MongoDB**, it provides essential CRUD functionality to create, retrieve, update, and delete categories. This API is ideal for **e-commerce platforms, inventory systems, and other category-based applications**.

## Key Features
- **RESTful architecture** ensuring easy integration
- **Full CRUD operations** for category management
- **MongoDB as the database** for seamless data storage
- **Configurable environments** for flexible deployment
- **Error handling & input validation** for improved security

## Setup & Installation

### Prerequisites
Ensure you have the following installed:
- **Node.js** (v14+ recommended)
- **MongoDB**, either locally or hosted in the cloud
- **Postman** (optional) for API testing

### Installation Steps
1. Clone the repository and navigate to the project folder:
    ```sh
    git clone https://github.com/your-repo/category-management-api.git
    cd category-management-api
    ```
2. Install required dependencies:
    ```sh
    npm install
    ```
3. Set up environment variables by creating a `.env` file in the root directory with the following values:
    ```sh
    NODE_ENV=development
    PORT=5000
    MONGO_URI=mongodb://localhost:27017/category_db
    ```
4. Start the development server:
    ```sh
    npm run dev
    ```

## API Documentation

### Base URL
```
http://localhost:5000/api/categories
```

### Endpoints
| Method | Endpoint            | Description               |
|--------|--------------------|---------------------------|
| POST   | /api/categories    | Add a new category        |
| GET    | /api/categories    | Fetch all categories      |
| GET    | /api/categories/:id | Retrieve a category by ID |
| PUT    | /api/categories/:id | Modify an existing category |
| DELETE | /api/categories/:id | Remove a category         |

## Example Requests & Responses

### Creating a Category
**Request:**
```json
POST /api/categories
Content-Type: application/json

{
  "name": "Electronics",
  "description": "Electronic devices and gadgets"
}
```

**Response:**
```json
Status: 201 Created
{
  "_id": "60d21b4667d0d8992e610c85",
  "name": "Electronics",
  "description": "Electronic devices and gadgets",
  "isActive": true,
  "createdAt": "2023-06-22T14:30:00.000Z",
  "updatedAt": "2023-06-22T14:30:00.000Z"
}
```

### Retrieving All Categories
**Request:**
```sh
GET /api/categories
```

**Response:**
```json
Status: 200 OK
[
  {
    "_id": "60d21b4667d0d8992e610c85",
    "name": "Electronics",
    "description": "Electronic devices and gadgets",
    "isActive": true,
    "createdAt": "2023-06-22T14:30:00.000Z",
    "updatedAt": "2023-06-22T14:30:00.000Z"
  }
]
```

## Error Handling
The API returns structured error messages with appropriate HTTP status codes:
- **400 Bad Request** – Invalid input data
- **404 Not Found** – Category does not exist
- **500 Internal Server Error** – Server-side issue encountered

## Testing with Postman
To validate API functionality:
1. Open Postman.
2. Import a pre-configured collection (if available) or manually create requests.
3. Send requests to the available endpoints.
4. Check that responses match expected formats and data integrity is maintained.

---
