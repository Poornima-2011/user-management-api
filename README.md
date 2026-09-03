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
