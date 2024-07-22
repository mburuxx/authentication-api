# User Authentication API

This is a user authentication API built with Node.js that can be used in any application that uses HTTP. <br> It provides endpoints for user registration, login, and token generation. <br> The API uses JWT for authentication and supports middleware for handling authentication and errors.

## Table of Contents

- [Installation](#installation)
- [Configuration](#configuration)
- [Database](#database)
- [Models](#models)
- [Controllers](#controllers)
- [Middleware](#middleware)
- [Routes](#routes)
- [Utils](#utils)
- [Server](#server)
- [Environment Variables](#environment-variables)
- [API Endpoints](#api-endpoints)
- [License](./LICENSE)

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/user-authentication-api.git
    ```
    <br>

2. Navigate to the project directory:
    ```sh
    cd authentication-api
    ```
    <br>

3. Install dependencies:
    ```sh
    npm install
    ```
    <br>

   Alternatively, you can install dependencies listed in `requirements.txt`:
    ```sh
    npm install $(cat requirements.txt | xargs)
    ```

## Configuration

- `config/db.js`: Contains database connection logic.

# Database

Ensure you have MongoDB installed and running. Configure the database connection in `config/db.js`.

## Models

- `models/userModel.js`: Defines the User schema and model.

## Controllers

- `controllers/userController.js`: Contains logic for user registration and login.

## Middleware

- `middleware/authMiddleware.js`: Middleware to protect routes that require authentication.
- `middleware/errorMiddleware.js`: Middleware for error handling.

## Routes

- `routes/userRoutes.js`: Defines the user-related routes (registration, login).

## Utils

- `utils/generateTokens.js`: Contains functions for generating JWT tokens.

## Server

- `server.js`: Entry point for the API. Configures and starts the server.

## Environment Variables

Create a `.env` file in the root of your project with the following environment variables:

```env
PORT=5000
MONGO_URI=your_mongo_db_uri
JWT_SECRET=your_jwt_secret
