
# To-Do List API

This is a simple RESTful API for managing a to-do list, built with Spring Boot.

## Features

- Create, read, update, and delete tasks.
- Use H2 in-memory database for easy setup and testing.
- Structured in a RESTful style for seamless integration with front-end applications.

## Prerequisites

Before you begin, ensure you have met the following requirements:

- Java Development Kit (JDK) 17 or higher
- Maven 3.8 or higher
- An IDE like IntelliJ IDEA or VSCode

## Getting Started

### 1. Clone the Repository

Clone the repository to your local machine:

```bash
git clone https://github.com/NTNEvil/todo-list.git
cd todo-list
```

### 2. Configure the Database

The project uses an H2 in-memory database for development. You can configure the database settings in the `src/main/resources/application.properties` file.

Default configuration:
```properties
spring.datasource.url=jdbc:h2:mem:todoapp
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=password
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
spring.h2.console.enabled=true
```

### 3. Build and Run the Application

Use Maven to build and run the application:

```bash
mvn spring-boot:run
```

Alternatively, you can build the JAR file and run it:

```bash
mvn clean package
java -jar target/todolist-0.0.1-SNAPSHOT.jar
```

### 4. Access the Application

Once the application is running, you can access it at:

- API Documentation: `http://localhost:8080/api/tasks`
- H2 Database Console: `http://localhost:8080/h2-console`

### API Endpoints

| Method | Endpoint          | Description                      |
|--------|-------------------|----------------------------------|
| `GET`  | `/api/tasks`      | Get all tasks                    |
| `GET`  | `/api/tasks/{id}` | Get a specific task by ID        |
| `POST` | `/api/tasks`      | Create a new task                |
| `PUT`  | `/api/tasks/{id}` | Update an existing task by ID    |
| `DELETE` | `/api/tasks/{id}` | Delete a task by ID            |

### Example Task JSON

When creating or updating a task, use the following JSON format:

```json
{
  "title": "Buy groceries",
  "description": "Buy milk, bread, and eggs",
  "completed": false
}
```

## Contributing

If you want to contribute to this project, please fork the repository and create a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

If you have any questions or suggestions, feel free to reach out:

- GitHub: [@NTNEvil](https://github.com/NTNEvil/)
- Email: natanmarcos11@gmail.com
