
# Spring Boot Blog Post Service - Group 03

## Overview
This is a simple Blog Post Service built with Spring Boot that allows users to create, read, update, and delete (CRUD) blog posts. The service uses Spring Data JPA for database interactions and exposes RESTful APIs.

## Features
- Create a new blog post
- Retrieve all blog posts
- Retrieve a single blog post by ID
- Update an existing blog post
- Delete a blog post
- Input validation and basic error handling

## Tech Stack
- Java 17
- Spring Boot 3.x
- Spring Data JPA
- H2 / MySQL Database
- Maven for dependency management
- Lombok for boilerplate code reduction
- Spring Web for REST API development

## Getting Started

### Prerequisites
- Java 17 or above
- Maven 3.x
- MySQL (optional if you want to switch from H2)

### Installation
1. Clone the repository:
```bash
git clone https://github.com/your-username/blogpost-service.git
cd blogpost-service
````

2. Build the project:

```bash
mvn clean install
```

3. Run the application:

```bash
mvn spring-boot:run
```

The application will start on `http://localhost:8080`.

## API Endpoints

* `GET /api/posts` - Get all blog posts
* `GET /api/posts/{id}` - Get a post by ID
* `POST /api/posts` - Create a new post
* `PUT /api/posts/{id}` - Update an existing post
* `DELETE /api/posts/{id}` - Delete a post

### Sample JSON for POST/PUT

```json
{
  "title": "My First Blog",
  "content": "This is the content of my first blog post.",
  "author": "John Doe"
}
```

## Database Configuration

By default, the project uses H2 in-memory database. To switch to MySQL, update `application.properties` or `application.yml`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/blog_db
spring.datasource.username=root
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

## Testing

You can use Postman or cURL to test the API endpoints.

Example:

```bash
 curl -X GET http://localhost:8080/api/posts
```

## Future Improvements

* Add user authentication & authorization (Spring Security + JWT)
* Add pagination and filtering for posts
* Add unit and integration tests
* Add Swagger/OpenAPI documentation

## Authors

**Group 03** – [GitHub](https://github.com/shogunhermit/blog/graphs/contributors)

