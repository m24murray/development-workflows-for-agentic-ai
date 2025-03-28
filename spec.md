# Java Spring REST API with MongoDB - Spec 

## Overview
This document outlines the specification for a **Java Spring REST API** that interacts with **MongoDB**. The API provides CRUD operations for managing `users` and follows a standard **controller-service-repository** structure.

## Tech Stack
- **Java 21**
- **Spring Boot**
- **MongoDB** as the database
- **Gradle** for dependency management (Groovy DSL)
- **JUnit 5 & Mockito** for testing
- **Springdoc OpenAPI** for API documentation
- **Logback** for structured JSON logging

## Data Model: `User`
The API will manage a `User` model with the following fields:

| Field  | Type   | Constraints |
|--------|--------|-------------|
| `id`   | `UUID` | Auto-generated by MongoDB |
| `name` | `String` | Min length: 4, Max length: 30 |
| `email` | `String` | Unique (case-insensitive), must be valid email |

### Data Handling
- `email` is **case-insensitive unique**.
- `name` and `email` are **trimmed** before being stored.
- Hard delete is used (no soft deletes).

## API Endpoints
The API follows RESTful principles with **URL versioning (`/api/v1/users`)**.

### Users CRUD Endpoints
| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/api/v1/users/{id}` | Retrieve a user by ID |
| `POST` | `/api/v1/users` | Create a new user |
| `PUT` | `/api/v1/users/{id}` | Full update of a user |
| `PATCH` | `/api/v1/users/{id}` | Partial update of a user |
| `DELETE` | `/api/v1/users/{id}` | Hard delete a user |

### Health Check Endpoint
| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/api/v1/health` | Check if the service is running |

## API Documentation
- **Springdoc OpenAPI** will generate the OpenAPI spec.
- **Swagger UI** will be available for interactive testing.
- API responses will include descriptions and example values.

## Request/Response Formats
- The API **consumes and produces JSON (`application/json`)**.
- If timestamps are introduced later, they will use **ISO 8601 format**.

## Error Handling
- Standard **HTTP 4xx and 5xx responses** will be used.
- No custom exception handling beyond what Spring provides.

## Logging
- **Logback** will be used for structured **JSON logging**.
- Requests and responses will be logged for debugging.
- Standard logging levels will be maintained (no query logging).

## Testing
- **JUnit 5 & Mockito** for unit tests.
- **Mocked database layer** (no embedded MongoDB for tests).

## Deployment & Configuration
- No **Docker** configuration.
- No **Spring Boot profiles**.
- Configuration will be managed directly in `application.yml`.

## Future Extensibility
- The project will be structured **by feature** to support additional models beyond `users`.
- No batch operations will be included.

---
This specification provides a clear roadmap for implementation. The API is designed for **internal use**, with a focus on maintainability and stability.
