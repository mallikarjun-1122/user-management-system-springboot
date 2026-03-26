# Spring Boot MongoDB CRUD Application

A simple **Spring Boot + MongoDB** project that demonstrates CRUD operations for managing student data.

## Project Structure

```text
src/
 ├── main/
 │   ├── java/com/swarup/
 │   │   ├── controller/
 │   │   │   └── StudentController.java
 │   │   ├── entity/
 │   │   │   └── Student.java
 │   │   ├── repo/
 │   │   │   └── StudentRepository.java
 │   │   ├── service/
 │   │   │   └── StudentService.java
 │   │   └── MongoDbApplication.java
 │   └── resources/
 │       └── application.properties
 │
 └── test/
     └── java/com/swarup/
         └── MongoDbApplicationTests.java
```

## Features

- Create student records
- Read student details
- Update student information
- Delete student records
- MongoDB database integration
- REST API built with Spring Boot

## Tech Stack

- **Java**
- **Spring Boot**
- **Spring Data MongoDB**
- **MongoDB**
- **Maven**

## Prerequisites

Make sure you have installed:

- Java 17 or compatible version
- Maven
- MongoDB
- Git

## Setup and Run

### 1. Clone the repository

```bash
git clone https://github.com/your-username/your-repository-name.git
cd your-repository-name
```

### 2. Configure MongoDB

Update the `application.properties` file with your MongoDB connection details.

Example:

```properties
spring.data.mongodb.uri=mongodb://localhost:27017/studentdb
spring.data.mongodb.database=studentdb
server.port=8080
```

### 3. Build the project

```bash
mvn clean install
```

### 4. Run the application

```bash
mvn spring-boot:run
```

The application will start at:

```text
http://localhost:8080
```

## API Endpoints

Below are example CRUD endpoints for students. Update these if your controller uses different mappings.

### Create Student

```http
POST /students
```

Example request body:

```json
{
  "id": "1",
  "name": "John Doe",
  "department": "CSD",
  "email": "john@example.com"
}
```

### Get All Students

```http
GET /students
```

### Get Student By ID

```http
GET /students/{id}
```

### Update Student

```http
PUT /students/{id}
```

Example request body:

```json
{
  "name": "John Updated",
  "department": "CSD",
  "email": "johnupdated@example.com"
}
```

### Delete Student

```http
DELETE /students/{id}
```

## Repository Layer

- `StudentRepository.java` handles database access using Spring Data MongoDB.

## Service Layer

- `StudentService.java` contains the business logic for student operations.

## Controller Layer

- `StudentController.java` exposes REST API endpoints.

## Main Class

- `MongoDbApplication.java` is the entry point of the Spring Boot application.

## Testing

Run tests with:

```bash
mvn test
```

## Future Improvements

- Add validation for request data
- Add exception handling
- Add Swagger/OpenAPI documentation
- Add unit and integration tests
- Add Docker support

## Author

**Swarup**

## License

This project is for learning and practice purposes.
