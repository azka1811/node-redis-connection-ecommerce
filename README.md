# E-commerce Store with Node.js and Redis

This project is a basic e-commerce store built using Node.js, Express, and Redis. It includes RESTful API endpoints for creating and retrieving products, with Redis used for caching and efficient data management.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This application serves as a simple e-commerce store where you can manage products. It demonstrates the use of Redis for caching, Node.js for server-side logic, and Express for handling API requests. The project follows best coding practices with a modular structure, making it easy to extend and maintain.

## Features

- Create and retrieve product details
- In-memory data caching using Redis
- Modular architecture for easy extension

## Technologies Used

- **Node.js**: JavaScript runtime for server-side development
- **Express**: Web framework for Node.js
- **Redis**: In-memory data structure store for caching
- **dotenv**: Environment variable management

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/azka1811/node-redis-connection-ecommerce.git
   cd ecommerce-store
   ```

2. **Install dependencies:**

   ```bash
   npm install
   ```

3. **Set up environment variables:**

   Create a `.env` file in the root directory and add the following:

   ```
   REDIS_URL=redis://localhost:6379
   ```

4. **Start Redis server:**

   Make sure you have Redis installed and running on your machine. You can download it from the [official website](https://redis.io/download).

5. **Run the application:**

   ```bash
   npm start
   ```

   The server will start on `http://localhost:3000`.

## Usage

Use Postman or any HTTP client to interact with the API. Below are the available endpoints:

## API Endpoints

### Create Product

- **Endpoint**: `POST /api/products`
- **Description**: Creates a new product.
- **Headers**: `Content-Type: application/json`
- **Body** (JSON):

  ```json
  {
    "id": 1,
    "name": "Sample Product",
    "price": 99.99,
    "description": "A great product"
  }
  ```

- **Response**: Returns the created product details.

### Get Product

- **Endpoint**: `GET /api/products/:id`
- **Description**: Retrieves a product by ID.
- **Parameters**: `id` (URL parameter) - The ID of the product.
- **Response**: Returns the product details if found.

## Project Structure

```
ecommerce-store/
├── config/
│   └── db.js           # Database configuration
├── controllers/
│   └── productController.js  # Controllers for handling requests
├── models/
│   └── product.js      # Data models
├── routes/
│   └── productRoutes.js # Route definitions
├── services/
│   └── productService.js # Business logic and services
├── utils/
│   └── cache.js        # Utility functions, e.g., Redis cache
├── .env                # Environment variables
├── app.js              # Express app setup
└── package.json        # Project dependencies and scripts
```

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request for review.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
