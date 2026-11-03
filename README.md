# University Management System

A backend REST API application developed using **Java, Spring Boot, Spring Data JPA, and MySQL** to manage university records.

The application provides CRUD (Create, Read, Update, Delete) operations for departments, students, courses, and teachers.

## Features

- Manage university departments.
- Manage student records.
- Manage courses offered by departments.
- Manage teacher information.
- Perform CRUD operations through REST APIs.
- Store and retrieve data using MySQL.
- Establish relationships between database entities using JPA.

## Technologies Used

| Technology | Purpose |
|---|---|
| Java | Programming language |
| Spring Boot | Backend framework |
| Spring Data JPA | Database operations |
| Hibernate | ORM |
| MySQL | Relational database |
| Maven | Dependency management |
| Thunder Client | API testing |

## Project Structure

```text
university-management-system/
│
├── src/
│   ├── main/
│   │   ├── java/com/college/student_api/
│   │   │   ├── Controller/
│   │   │   │   ├── CourseController.java
│   │   │   │   ├── DepartmentController.java
│   │   │   │   ├── StudentController.java
│   │   │   │   └── TeacherController.java
│   │   │   │
│   │   │   ├── entity/
│   │   │   │   ├── Course.java
│   │   │   │   ├── Department.java
│   │   │   │   ├── Student.java
│   │   │   │   └── Teacher.java
│   │   │   │
│   │   │   ├── repository/
│   │   │   │   ├── CourseRepository.java
│   │   │   │   ├── DepartmentRepository.java
│   │   │   │   ├── StudentRepository.java
│   │   │   │   └── TeacherRepository.java
│   │   │   │
│   │   │   └── StudentApiApplication.java
│   │   │
│   │   └── resources/
│   │       └── application.properties
│   │
│   └── test/
│
├── .gitignore
├── pom.xml
└── README.md
```

## Database Configuration

The project uses a MySQL database named:

```sql
university_db
```

Configure your database credentials using environment variables in `application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/university_db?createDatabaseIfNotExist=true
spring.datasource.username=${DB_USERNAME:root}
spring.datasource.password=${DB_PASSWORD:}

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

Make sure MySQL is installed and running before starting the application.

## REST API Endpoints

The application runs on:

```text
http://localhost:8080
```

### 1. Department APIs

| Method | Endpoint | Operation |
|---|---|---|
| POST | `/api/departments` | Create department |
| GET | `/api/departments` | Get all departments |
| GET | `/api/departments/{id}` | Get department by ID |
| PUT | `/api/departments/{id}` | Update department |
| DELETE | `/api/departments/{id}` | Delete department |

### 2. Student APIs

| Method | Endpoint | Operation |
|---|---|---|
| POST | `/api/students` | Create student |
| GET | `/api/students` | Get all students |
| GET | `/api/students/{id}` | Get student by ID |
| PUT | `/api/students/{id}` | Update student |
| DELETE | `/api/students/{id}` | Delete student |

### 3. Course APIs

| Method | Endpoint | Operation |
|---|---|---|
| POST | `/api/courses` | Create course |
| GET | `/api/courses` | Get all courses |
| GET | `/api/courses/{id}` | Get course by ID |
| PUT | `/api/courses/{id}` | Update course |
| DELETE | `/api/courses/{id}` | Delete course |

### 4. Teacher APIs

| Method | Endpoint | Operation |
|---|---|---|
| POST | `/api/teachers` | Create teacher |
| GET | `/api/teachers` | Get all teachers |
| GET | `/api/teachers/{id}` | Get teacher by ID |
| PUT | `/api/teachers/{id}` | Update teacher |
| DELETE | `/api/teachers/{id}` | Delete teacher |

## How to Run the Project

**1. Clone the repository**

```bash
git clone https://github.com/Gaurix7/university-management-system.git
```

**2. Navigate to the project directory**

```bash
cd university-management-system
```

**3. Configure MySQL**

Create or allow the application to create the `university_db` database. Set your database username and password as environment variables.

**4. Run the application**

On Windows PowerShell:

```powershell
$env:DB_USERNAME="root"
$env:DB_PASSWORD="your_mysql_password"

.\mvnw.cmd spring-boot:run
```

**5. Test the APIs**

Use Thunder Client or Postman to send HTTP requests to the endpoints listed above.

## Author

**Gauri Rawat**

GitHub: [@Gaurix7](https://github.com/Gaurix7)

## Repository

[University Management System](https://github.com/Gaurix7/university-management-system)