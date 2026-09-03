# User Management API

A simple **User Management REST API** built using **Java, Spring Boot, Spring Data JPA, and MySQL**.

This project demonstrates how to build RESTful APIs with a layered architecture and handle exceptions globally.

---

## 🚀 Features

- Create a new user
- Get all users
- Get user by ID
- Update user details
- Delete user
- Global exception handling
- User not found exception handling
- MySQL database integration
- Spring Data JPA
- RESTful API architecture

---

## 🛠️ Technologies Used

- Java 21
- Spring Boot
- Spring Web
- Spring Data JPA
- MySQL
- Maven
- REST API
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
└── README.md

🏗️ Architecture

The project follows a simple layered architecture:

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

🗄️ Database Configuration

Create a MySQL database:

CREATE DATABASE user_management;

Update your application.properties:

spring.application.name=user-management-api

spring.datasource.url=jdbc:mysql://localhost:3306/user_management
spring.datasource.username=root
spring.datasource.password=YOUR_PASSWORD

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

server.port=8080

Replace YOUR_PASSWORD with your MySQL password.

👤 User Entity

Example user fields:

id
name
email
age

The User entity is mapped to a MySQL table using JPA.

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

Example:

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

Example:

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

Example:

/api/users/1
Response
User deleted successfully

▶️ How to Run the Project
Step 1: Clone the repository
git clone https://github.com/Poornima-2011/user-management-api.git
Step 2: Open the project

Open the project in:

IntelliJ IDEA
Eclipse
Spring Tool Suite
Step 3: Configure MySQL

Create the database:

CREATE DATABASE user_management;

Update the MySQL username and password in:

src/main/resources/application.properties
Step 4: Run the application

Run:

UserManagementApplication.java

Or using Maven:

mvn spring-boot:run

The application will start at:

http://localhost:8080

🧪 Testing with Postman

You can test all APIs using Postman.

Create
POST http://localhost:8080/api/users
Get All
GET http://localhost:8080/api/users
Get By ID
GET http://localhost:8080/api/users/1
Update
PUT http://localhost:8080/api/users/1
Delete
DELETE http://localhost:8080/api/users/1

GitHub
🔮 Future Improvements

The project can be extended with:

DTO pattern
Pagination and sorting
Search users by name/email
Spring Security
JWT authentication
Swagger/OpenAPI documentation
Unit testing with JUnit and Mockito
Docker deployment

👩‍💻 Author

Poornima
