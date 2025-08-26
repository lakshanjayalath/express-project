# Express TypeScript API Project

A scalable and modular Express.js API built with TypeScript, featuring MongoDB integration, JWT authentication, and a layered architecture.

## Table of Contents

- [Project Structure](#project-structure)
- [Technologies Used](#technologies-used)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Available Scripts](#available-scripts)
- [API Routes](#api-routes)
- [Architecture](#architecture)
- [Authentication](#authentication)
- [Development](#development)
- [Build](#build)
- [Contributing](#contributing)
- [License](#license)
- [Author](#author)

## Project Structure

```
src/
├── app.ts                 # Application entry point
├── common/               # Common utilities and handlers
│   ├── responseHandler.ts
│   └── constants/
│       ├── errors.constants.ts
│       └── httpStatus.enum.ts
├── config/              # Configuration files
│   └── app.config.ts
├── controller/         # Route controllers
│   ├── customer.controller.ts
│   └── user.controller.ts
├── dao/               # Data Access Objects
│   └── user.dao.ts
├── interface/         # TypeScript interfaces
│   ├── error.interface.ts
│   └── models/
│       └── user.interface.ts
├── loader/           # Application loaders
│   └── mongo.loader.ts
├── models/           # MongoDB models
│   └── user.model.ts
├── routes/           # API routes
│   ├── customer.route.ts
│   ├── greeting.route.ts
│   ├── routes.ts
│   └── user.route.ts
└── service/         # Business logic layer
    └── user.service.ts
```

## Technologies Used

- **Node.js**: JavaScript runtime for building scalable server-side applications.
- **Express.js (v5.1.0)**: Web framework for building APIs.
- **TypeScript (v5.9.2)**: Strongly typed programming language for scalable development.
- **MongoDB**: NoSQL database for data storage, integrated via **Mongoose (v8.18.0)**.
- **JWT Authentication**: Secure authentication using **jsonwebtoken (v9.0.2)**.
- **Passport.js (v0.7.0)**: Middleware for authentication.

## Prerequisites

- **Node.js**: Install the latest LTS version.
- **MongoDB**: Ensure MongoDB is installed and running locally or accessible via a cloud service.
- **TypeScript Knowledge**: Familiarity with TypeScript is recommended.

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/lakshanjayalath/express-project.git
   cd express-project
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Configure environment variables**:
   - Create a `.env` file in the root directory (if not already present).
   - Add the required environment variables (e.g., `PORT`, `MONGODB_URI`, `JWT_SECRET`).

## Available Scripts

- **Development**:
  ```bash
  npm run dev
  ```
  Starts the development server using `nodemon` and `ts-node`.

- **Watch for TypeScript changes**:
  ```bash
  npm run watch:dev
  ```
  Watches TypeScript files for changes and recompiles.

- **Build for production**:
  ```bash
  npm run build
  ```
  Compiles TypeScript code into JavaScript.

- **Start production server**:
  ```bash
  npm start
  ```
  Runs the compiled JavaScript code.

## API Routes

The API is prefixed with `/api` and includes the following routes:

- **User Routes**: `/api/users`
- **Customer Routes**: `/api/customers`
- **Greeting Routes**: `/api/greetings`

## Architecture

This project follows a layered architecture for better scalability and maintainability:

1. **Routes Layer**: Defines API endpoints.
2. **Controller Layer**: Handles incoming requests and responses.
3. **Service Layer**: Contains business logic.
4. **DAO Layer**: Manages data access and database operations.
5. **Model Layer**: Defines database schemas and models.

## Authentication

- **JWT (JSON Web Tokens)**: Used for secure authentication.
- **Passport.js**: Middleware for handling authentication strategies.
- Protected routes require a valid JWT token in the `Authorization` header.

## Development

1. **Start the development server**:
   ```bash
   npm run dev
   ```
2. The server will start on the configured port (default: check `APP_CONFIG`).

## Build

To build the project for production:

```bash
npm run build
```

The compiled JavaScript files will be output to the `dist/` directory.

## Contributing

We welcome contributions! Follow these steps:

1. Fork the repository.
2. Create your feature branch.
3. Commit your changes.
4. Push to the branch.
5. Create a Pull Request.

## License

This project is licensed under the ISC License.

## Author

lakshanjayalath
