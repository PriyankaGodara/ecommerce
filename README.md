# E-Commerce API

This project is a backend service built using Spring Boot to support e-commerce operations. It provides API endpoints for category listing, product listing, product details, cart management, order processing, and user authentication.

## Project Structure

ecommerce-api/
├── src/
│   ├── main/
│   │   ├── java/com/example/ecommerce/
│   │   │   ├── controller/          # REST Controllers
│   │   │   ├── entity/              # JPA Entities
│   │   │   ├── repository/          # Spring Data Repositories
│   │   │   ├── service/             # Service Layer
│   │   │   ├── security/            # Security Configuration and JWT Handling
│   │   │   └── EcommerceApiApplication.java  # Main Application Class
│   ├── resources/
│   │   ├── application.properties   # Configuration Properties
│   └── test/                        # Unit and Integration Tests
└── pom.xml                           # Maven Build File


## Features

- **Category Listing:** Retrieve a list of product categories.
- **Product Listing:** Get a list of products based on category.
- **Product Details:** Fetch detailed information of a specific product.
- **Cart Management:** Add products to the cart, view, update, and remove items.
- **Order Placement:** Place orders using products from the cart.
- **Order History:** View the order history for authenticated users.
- **User Authentication:** Register and log in users, with JWT-based authentication.
- **Swagger Documentation:** Comprehensive API documentation with Swagger.

## Technologies Used

- **Java 21**
- **Spring Boot 3**
- **Spring Data JPA**
- **Spring Security with JWT**
- **MySQL**
- **Swagger**
- **Maven**

## Setup and Installation

### Prerequisites

- **Java 21** or higher installed
- **Maven** installed
- **MySQL** installed and running

  ##Swagger API Documentation
For detailed API documentation and testing, visit the Swagger UI:

[Swagger Testing link:](http://localhost:8080/swagger-ui/index.html)

## API ENDPOINTS

# Register a User

-Use the /api/auth/signup endpoint to create a new user account.

  "role": [
    admin,
    user,
    seller    
  ],

# Sign In to Obtain a JWT Token

Use the /api/auth/signin endpoint to log in and receive a JWT token.
Include this token in the Authorization header of subsequent requests to access protected endpoints (e.g., creating categories, products, cart management, etc.).

# Create Categories

Use the /api/categories endpoint to create new product categories. This requires the JWT token for authentication.

# Create Products

Use the /api/products endpoint to add new products to the created categories. This also requires the JWT token for authentication.
