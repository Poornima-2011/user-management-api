# User Management API

A simple RESTful User Management API built using Java, Spring Boot, Spring Data JPA, and MySQL.

This project demonstrates CRUD operations, layered architecture, database integration, and global exception handling.

---

## 🚀 Features

- Create a new user
- Get all users
- Get user by ID
- Update user
- Delete user
- MySQL database integration
- Spring Data JPA
- RESTful APIs
- Global exception handling
- Custom User Not Found exception
- Postman API testing

---

## 🛠️ Technologies Used

- Java 21
- Spring Boot
- Spring Web
- Spring Data JPA
- Hibernate
- MySQL
- Maven
- Postman
- Git & GitHub

---

## 📁 Project Structure

```text
user-management-api
│
├── src/main/java/com/example/usermanagement
│   │
│   ├── controller
│   │   └── UserController.java
│   │
│   ├── service
│   │   └── UserService.java
│   │
│   ├── repository
│   │   └── UserRepository.java
│   │
│   ├── entity
│   │   └── User.java
│   │
│   ├── exception
│   │   ├── UserNotFoundException.java
│   │   └── GlobalExceptionHandler.java
│   │
│   └── UserManagementApplication.java
│
├── src/main/resources
│   └── application.properties
│
├── pom.xml
├── .gitignore
└── README.md
🏗️ Architecture

The project follows a layered architecture:

Client / Postman
       │
       ▼
 Controller
       │
       ▼
  Service
       │
       ▼
 Repository
       │
       ▼
 MySQL Database
Controller

Handles HTTP requests and exposes REST API endpoints.

Service

Contains the business logic of the application.

Repository

Uses Spring Data JPA to communicate with the database.

Entity

Represents the User table in the MySQL database.

Exception

Handles application-specific exceptions and provides proper error responses.

🗄️ Database Configuration

Create the MySQL database:

CREATE DATABASE user_management;

Update application.properties:

spring.application.name=user-management-api

spring.datasource.url=jdbc:mysql://localhost:3306/user_management
spring.datasource.username=root
spring.datasource.password=YOUR_PASSWORD

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

server.port=8080

Replace YOUR_PASSWORD with your MySQL password.

👤 User Entity

The User entity contains the following fields:

id
name
email
age

The entity is mapped to a MySQL table using JPA annotations.

🔗 API Endpoints
1. Create User

POST

/api/users
Request Body
{
    "name": "Poornima",
    "email": "poornima@gmail.com",
    "age": 23
}
Example Response
{
    "id": 1,
    "name": "Poornima",
    "email": "poornima@gmail.com",
    "age": 23
}
2. Get All Users

GET

/api/users
Example Response
[
    {
        "id": 1,
        "name": "Poornima",
        "email": "poornima@gmail.com",
        "age": 23
    },
    {
        "id": 2,
        "name": "Arun",
        "email": "arun@gmail.com",
        "age": 24
    }
]
3. Get User By ID

GET

/api/users/{id}
Example
/api/users/1
Response
{
    "id": 1,
    "name": "Poornima",
    "email": "poornima@gmail.com",
    "age": 23
}
4. Update User

PUT

/api/users/{id}
Example
/api/users/1
Request Body
{
    "name": "Poornima P",
    "email": "poornimap@gmail.com",
    "age": 24
}
5. Delete User

DELETE

/api/users/{id}
Example
/api/users/1
Response
User deleted successfully
⚠️ Exception Handling

The project uses a custom exception:

UserNotFoundException

If a user does not exist, for example:

GET /api/users/100

the application handles the exception using:

@RestControllerAdvice

The GlobalExceptionHandler provides a proper error response instead of returning an internal server error.

▶️ How to Run the Project
Step 1: Clone the Repository
git clone https://github.com/Poornima-2011/user-management-api.git
Step 2: Open the Project

Open the project using:

IntelliJ IDEA
Eclipse
Spring Tool Suite
Step 3: Configure MySQL

Create the database:

CREATE DATABASE user_management;

Then update the MySQL username and password in:

src/main/resources/application.properties
Step 4: Run the Application

Run:

UserManagementApplication.java

Or use Maven:

mvn spring-boot:run

The application will start at:

http://localhost:8080
🧪 Testing with Postman

The APIs can be tested using Postman.

Create User
POST http://localhost:8080/api/users
Get All Users
GET http://localhost:8080/api/users
Get User By ID
GET http://localhost:8080/api/users/1
Update User
PUT http://localhost:8080/api/users/1
Delete User
DELETE http://localhost:8080/api/users/1
📚 Learning Outcomes

Through this project, I practiced:

Java
Spring Boot
REST API development
CRUD operations
Spring Data JPA
Hibernate
MySQL integration
Layered architecture
Exception handling
HTTP methods
Postman API testing
Maven
Git and GitHub
🔮 Future Improvements

The project can be extended with:

DTO pattern
Input validation
Pagination and sorting
Search users by name or email
Spring Security
JWT authentication
Swagger/OpenAPI documentation
Unit testing with JUnit and Mockito
Docker deployment
👩‍💻 Author

Poornima
