# Task Manager API

This is a Task Manager API built with Node.js, Express.js, and MongoDB.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Routes](#routes)
- [Middleware](#middleware)
- [Environment Variables](#environment-variables)

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/task-manager-api.git
    cd task-manager-api
    ```

2. Install the dependencies:
    ```bash
    npm install
    ```

3. Set up environment variables:
    - Create a `.env` file in the root directory.
    - Add the following variables to the `.env` file:
      ```env
      PORT=3000
      MONGO_URI=your_mongodb_connection_string
      ```

4. Start the server:
    ```bash
    npm start
    ```

## Usage

The server will be running on `http://localhost:3000`. You can use tools like Postman or cURL to interact with the API.

## Routes

- **GET /api/v1/tasks** - Get all tasks
- **POST /api/v1/tasks** - Create a new task
- **GET /api/v1/tasks/:id** - Get a single task by ID
- **PATCH /api/v1/tasks/:id** - Update a task by ID
- **DELETE /api/v1/tasks/:id** - Delete a task by ID

## Middleware

- **Static Files Middleware**: Serves static files from the `public` directory.
- **JSON Middleware**: Parses incoming JSON requests.
- **Not Found Middleware**: Handles 404 errors.
- **Error Handler Middleware**: Handles errors and sends appropriate responses.

## Environment Variables

The project uses the following environment variables:

- `PORT`: The port on which the server will listen (default is 3000).
- `MONGO_URI`: The connection string for MongoDB.

## Project Structure

```
.
├── routes
│   └── tasks.js
├── db
│   └── connect.js
├── middleware
│   ├── not-found.js
│   └── error-handler.js
├── .env
├── .gitignore
├── package.json
└── README.md
```

## License

This project is licensed under the MIT License.

