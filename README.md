# 🛒 E-Commerce Backend API

A secure, scalable, and modular **E-Commerce Backend API** built using **Spring Boot**, **Spring Security**, **JWT**, and **MySQL**. This application provides RESTful endpoints for user registration and authentication, product management, cart operations, and order processing—supporting both admin and customer roles.

---

## 🚀 Project Overview

This project serves as the backend for a full-featured e-commerce application. It supports:

- 🔐 Secure authentication with JWT
- 👤 Role-based access control (`ADMIN`, `USER`)
- 📦 Product listing and management
- 🛒 Shopping cart functionality
- 📬 Order placement and tracking
- 📫 Address and user profile management

Designed with **best practices**, **clean architecture**, and **modular design** for production-readiness and easy integration with frontend clients (e.g., React, Angular, etc.).

---

## 📌 Tech Stack

| Layer             | Technology                |
|------------------|---------------------------|
| Language          | Java 17                   |
| Framework         | Spring Boot 3             |
| Security          | Spring Security + JWT     |
| ORM               | Spring Data JPA (Hibernate) |
| Database          | MySQL                     |
| Build Tool        | Maven                     |
| API Style         | RESTful API               |
| Authentication    | Stateless (JWT-based)     |

---

## 📂 Project Structure
src/
├── controller # REST Controllers
├── model # Entity and DTO classes
├── repository # JPA Repositories
├── service # Business logic layer
├── security # JWT filters, config, auth manager
└── util # Utilities, exceptions, constants

## ✅ Features

### 🔐 Authentication & Authorization
- JWT-based login and registration
- BCrypt password hashing
- Role-based access (`ADMIN`, `USER`)
- Stateless session management

### 📦 Product Management
- Admin CRUD for products
- List products by category or keyword

### 🛒 Cart & Checkout
- Add/remove items from cart
- Update quantities
- Place orders from cart

### 📬 Order Management
- View past orders
- Order status tracking (e.g., PENDING, SHIPPED)

### 🧍 User & Address Management
- View/edit user profiles
- Add/manage shipping addresses

---

## ⚙️ Getting Started

### 📦 Prerequisites

- Java 17+
- Maven 3.6+
- MySQL 8+

### 🛠️ Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone https://github.com/your-username/ecommerce-backend.git
   cd ecommerce-backend bash```

2. Database Configuration

    Create a MySQL database named ecommerce

    Open src/main/resources/application.properties and update:

    spring.datasource.username=your_db_user
    spring.datasource.password=your_db_pass

Run the Application

    mvn spring-boot:run

    Access the API

        Base URL: http://localhost:8080/api

        Example:

            POST /auth/register – Register a user

            POST /auth/login – Login to receive JWT

🔑 Sample Credentials (For Testing)

Admin:
Username: admin@example.com
Password: admin123

User:
Username: user@example.com
Password: user123

🔍 API Endpoints Overview
Endpoint	Method	Access	Description
/api/auth/register	POST	Public	Register new user
/api/auth/login	POST	Public	Authenticate user & return JWT
/api/products	GET	Public	List all products
/api/products/{id}	GET	Public	Get product by ID
/api/products	POST	Admin	Add new product
/api/cart	GET	User	View user’s cart
/api/cart/add	POST	User	Add product to cart
/api/orders	GET	User	View orders


🧪 Testing

Use Postman or cURL to test secured endpoints. Pass the Authorization: Bearer <JWT> header for protected routes.
📄 License

This project is licensed under the MIT License. See the LICENSE file for more information.
🤝 Contributing


---

### 🔧 To Customize

You should:
- Replace `your-username` in the clone URL
- Add your Swagger URL if applicable
- Add more endpoints in the API table as needed
- Add screenshots (if you build a frontend later)
