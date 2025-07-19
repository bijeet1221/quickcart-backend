# 🛒 E-Commerce Backend API

A secure, scalable, and modular **E-Commerce Backend API** built with **Spring Boot**, **Spring Security**, **JWT**, and **MySQL**.  
Provides RESTful endpoints for user registration, authentication, product management, cart operations, and order processing—supporting both admin and customer roles.

---

## 🚀 Project Overview

This backend supports:

- 🔐 Secure authentication with JWT  
- 👤 Role-based access control (`ADMIN`, `USER`)  
- 📦 Product listing and management  
- 🛒 Shopping cart functionality  
- 📬 Order placement and tracking  
- 📫 Address and user profile management  

Designed with **clean architecture**, **modular design**, and **best practices** for production-readiness and easy frontend integration.

---

## 📌 Tech Stack

| Layer         | Technology                     |
|---------------|--------------------------------|
| Language      | Java 17                        |
| Framework     | Spring Boot 3                  |
| Security      | Spring Security + JWT          |
| ORM           | Spring Data JPA (Hibernate)    |
| Database      | MySQL                          |
| Build Tool    | Maven                          |
| API Style     | RESTful                        |
| Auth Strategy | Stateless (JWT-based)          |

---

## 📂 Project Structure

```text
src/
├── controller    # REST Controllers
├── model         # Entity and DTO classes
├── repository    # JPA Repositories
├── service       # Business logic layer
├── security      # JWT filters, config, auth manager
└── util          # Utilities, exceptions, constants
```

✅ Features
🔐 Authentication & Authorization

   - JWT-based login & registration
   - BCrypt password hashing
   - Role-based access (ADMIN, USER)
   - Stateless session management

📦 Product Management

   - Admin CRUD for products
   - List products by category or keyword

🛒 Cart & Checkout

   - Add/remove items from cart
   - Update quantities
   - Place orders from cart

📬 Order Management

   - View past orders
   - Order status tracking (e.g., PENDING, SHIPPED)

🧍 User & Address Management

   - View/edit user profiles
   - Add/manage shipping addresses


## 🛠️ Setup Instructions

### 1. Clone the repository
```bash
git clone https://github.com/your-username/ecommerce-backend.git
cd ecommerce-backend
```
### 2. Configure the database

   - Create a MySQL database named ecommerce.
   - Open src/main/resources/application.properties and update:

   ```bash
   spring.datasource.url=jdbc:mysql://localhost:3306/ecommerce
   spring.datasource.username=your_db_user
   spring.datasource.password=your_db_pass
   jwt.secret=your_jwt_secret
   ```

### 3. Run the application
```
mvn clean install
mvn spring-boot:run
```
### 4. Access the API

- Base URL: http://localhost:8080/api
```bash
    POST /auth/register – Register a user
    POST /auth/login – Login to receive a JWT
```

## 🔑 Sample Credentials (For Testing)

| Role  | Username           | Password   |
|-------|--------------------|------------|
| Admin | admin@example.com  | admin123   |
| User  | user@example.com   | user123    |

## 🔍 API Endpoints Overview

| Endpoint               | Method | Access | Description                    |
|------------------------|--------|--------|--------------------------------|
| `/api/auth/register`   | POST   | Public | Register a new user            |
| `/api/auth/login`      | POST   | Public | Authenticate user & return JWT |
| `/api/products`        | GET    | Public | List all products              |
| `/api/products/{id}`   | GET    | Public | Get product by ID              |
| `/api/products`        | POST   | Admin  | Add new product                |
| `/api/cart`            | GET    | User   | View user’s cart               |
| `/api/cart/add`        | POST   | User   | Add product to cart            |
| `/api/orders`          | GET    | User   | View user’s orders             |

## 🧪 Testing

Use **Postman** or **cURL** to test endpoints.  
Include the header:
```
Authorization: Bearer <YOUR_JWT_TOKEN>
```

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

