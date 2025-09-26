# System Architecture

## Overview

The Employee Management System is built using a layered architecture pattern with Spring Boot, following clean architecture principles and separation of concerns.

## Architecture Diagram

```
┌─────────────────────────────────────────────────────────────────┐
│                           Presentation Layer                    │
│  ┌─────────────────┐  ┌─────────────────┐  ┌─────────────────┐ │
│  │   Web Browser   │  │   Mobile App    │  │   API Client    │ │
│  │   (HTML/CSS/JS) │  │   (Future)      │  │   (REST API)    │ │
│  └─────────────────┘  └─────────────────┘  └─────────────────┘ │
└─────────────────────────────────────────────────────────────────┘
                                   │
                                   ▼
┌─────────────────────────────────────────────────────────────────┐
│                         Controller Layer                        │
│  ┌─────────────────────────────────────────────────────────────┐ │
│  │           FuncionarioController                             │ │
│  │  - REST endpoints for employee operations                   │ │
│  │  - HTTP request/response handling                           │ │
│  │  - Input validation and error handling                      │ │
│  └─────────────────────────────────────────────────────────────┘ │
└─────────────────────────────────────────────────────────────────┘
                                   │
                                   ▼
┌─────────────────────────────────────────────────────────────────┐
│                          Service Layer                          │
│  ┌─────────────────────────────────────────────────────────────┐ │
│  │              FuncionarioService                             │ │
│  │  - Business logic implementation                            │ │
│  │  - Employee operations orchestration                        │ │
│  │  - Salary calculations and business rules                   │ │
│  │  - Data transformation and validation                       │ │
│  └─────────────────────────────────────────────────────────────┘ │
└─────────────────────────────────────────────────────────────────┘
                                   │
                                   ▼
┌─────────────────────────────────────────────────────────────────┐
│                        Repository Layer                         │
│  ┌─────────────────────────────────────────────────────────────┐ │
│  │            FuncionarioRepository                            │ │
│  │  - Data access operations                                   │ │
│  │  - CRUD operations implementation                           │ │
│  │  - Data persistence abstraction                             │ │
│  └─────────────────────────────────────────────────────────────┘ │
└─────────────────────────────────────────────────────────────────┘
                                   │
                                   ▼
┌─────────────────────────────────────────────────────────────────┐
│                           Data Layer                            │
│  ┌─────────────────────────────────────────────────────────────┐ │
│  │                In-Memory Storage                            │ │
│  │  - ArrayList<Funcionario> funcionarios                     │ │
│  │  - Temporary data storage for demo purposes                 │ │
│  │  - Future: Database integration (MySQL/PostgreSQL)         │ │
│  └─────────────────────────────────────────────────────────────┘ │
└─────────────────────────────────────────────────────────────────┘
```

## Component Details

### 1. Model Layer (Domain)

#### Pessoa (Person)
- Base class with common attributes
- Contains name and birth date
- Follows inheritance principles

#### Funcionario (Employee)
- Extends Pessoa
- Adds salary and job function
- Core domain entity

### 2. Repository Layer (Data Access)

#### FuncionarioRepository
- **Responsibilities:**
  - Data persistence operations
  - CRUD operations (Create, Read, Update, Delete)
  - Query operations by different criteria
- **Current Implementation:** In-memory ArrayList
- **Future:** Database integration with JPA/Hibernate

### 3. Service Layer (Business Logic)

#### FuncionarioService
- **Responsibilities:**
  - Business rules implementation
  - Employee management operations
  - Salary calculations and increases
  - Employee grouping and filtering
  - Age calculations and birthday tracking
- **Key Methods:**
  - `inserirTodosFuncionarios()` - Bulk employee insertion
  - `aplicarAumento()` - Apply salary increases
  - `agruparPorFuncao()` - Group by job function
  - `getAniversariantes()` - Find birthday employees

### 4. Controller Layer (API)

#### FuncionarioController
- **Responsibilities:**
  - HTTP request handling
  - Input validation
  - Response formatting
  - Error handling
- **REST Endpoints:**
  - `GET /funcionarios` - List all employees
  - `POST /funcionarios/inserir` - Insert all employees
  - `DELETE /funcionarios/{nome}` - Delete employee
  - `PUT /funcionarios/aumento` - Apply salary increase
  - `GET /funcionarios/agrupados` - Group by function
  - `GET /funcionarios/aniversariantes` - Get birthday employees

### 5. Presentation Layer

#### Static Resources
- **HTML:** User interface structure
- **CSS:** Styling and responsive design
- **JavaScript:** Dynamic functionality and API calls
- **Bootstrap:** UI framework for responsive design

## Technology Stack

### Backend
- **Java 17** - Programming language
- **Spring Boot 2.5.4** - Application framework
- **Spring Web** - Web layer
- **Spring DevTools** - Development tools
- **Maven** - Build and dependency management

### Frontend
- **HTML5** - Markup language
- **CSS3** - Styling
- **JavaScript (ES6)** - Client-side functionality
- **Bootstrap 4.5.2** - CSS framework
- **jQuery** - JavaScript library (minimal usage)

### Development Tools
- **Maven** - Build automation
- **Spring Boot DevTools** - Hot reload
- **JUnit 5** - Testing framework

## Design Patterns

### 1. Layered Architecture
- Clear separation of concerns
- Each layer has specific responsibilities
- Dependencies flow downward

### 2. Repository Pattern
- Abstracts data access logic
- Provides a uniform interface for data operations
- Facilitates testing and future database migration

### 3. Service Layer Pattern
- Encapsulates business logic
- Provides transaction boundaries
- Coordinates between different repositories

### 4. MVC (Model-View-Controller)
- Separates presentation from business logic
- Controller handles HTTP requests
- Model represents data and business logic
- View handles presentation (HTML/CSS/JS)

## Data Flow

1. **User Interaction** → Web browser sends HTTP request
2. **Controller** → Receives request, validates input
3. **Service** → Processes business logic
4. **Repository** → Handles data operations
5. **Data Layer** → Persists/retrieves data
6. **Response** → Data flows back through layers to user

## Security Considerations

- Input validation at controller level
- No direct data access from presentation layer
- Future: Authentication and authorization
- Future: HTTPS enforcement
- Future: SQL injection prevention (when database is added)

## Scalability Considerations

### Current Limitations
- In-memory storage (not persistent)
- Single-node deployment
- No caching layer

### Future Improvements
- Database integration
- Connection pooling
- Caching layer (Redis)
- Horizontal scaling capabilities
- Microservices architecture

## Testing Strategy

- **Unit Tests** - Service and repository layers
- **Integration Tests** - Controller endpoints
- **End-to-End Tests** - Full application flow
- **Test Coverage** - Aim for 80%+ coverage

## Deployment

### Current
- Embedded Tomcat server
- JAR packaging
- Java 17 runtime requirement

### Future
- Docker containerization
- Cloud deployment (AWS/Azure/GCP)
- CI/CD pipeline integration
- Health checks and monitoring