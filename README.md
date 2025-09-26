# Employee Management System | Sistema de Gerenciamento de Funcionários

> [🇺🇸 English](#english) | [🇧🇷 Português](#português)

[![Java 17](https://img.shields.io/badge/Java-17-orange.svg)](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-2.5.4-green.svg)](https://spring.io/projects/spring-boot)
[![Maven](https://img.shields.io/badge/Maven-3.6+-blue.svg)](https://maven.apache.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

![Employee Management System](https://github.com/JacksonMiranda/Funcionario/assets/10747842/3de16da7-96fb-40fc-b3ee-d86f7e903862)

---

## English

### Overview

A professional HR domain application built with Spring Boot for managing employee records. This system provides comprehensive employee management capabilities with a modern web interface, RESTful APIs, and clean architecture principles.

### C4 Architecture Diagram

```
┌─────────────────────────────────────────────────────────────────┐
│                              User                               │
│                        (HR Manager)                             │
└─────────────────────────────────────────────────────────────────┘
                                   │
                                   ▼
┌─────────────────────────────────────────────────────────────────┐
│                         Frontend Layer                          │
│  ┌─────────────────────────────────────────────────────────────┐ │
│  │        Web Browser (HTML/CSS/JavaScript)                   │ │
│  │  - Bootstrap UI Components                                  │ │
│  │  - Interactive Employee Management                          │ │
│  │  - Real-time Data Updates                                   │ │
│  └─────────────────────────────────────────────────────────────┘ │
└─────────────────────────────────────────────────────────────────┘
                                   │
                                   ▼
┌─────────────────────────────────────────────────────────────────┐
│                   Employee Management API                       │
│  ┌─────────────────────────────────────────────────────────────┐ │
│  │              Spring Boot Application                        │ │
│  │  - RESTful API Endpoints                                    │ │
│  │  - Business Logic Processing                                │ │
│  │  - Data Validation & Error Handling                         │ │
│  └─────────────────────────────────────────────────────────────┘ │
└─────────────────────────────────────────────────────────────────┘
                                   │
                                   ▼
┌─────────────────────────────────────────────────────────────────┐
│                          Data Store                             │
│  ┌─────────────────────────────────────────────────────────────┐ │
│  │                 In-Memory Repository                        │ │
│  │  - Employee Records Storage                                 │ │
│  │  - CRUD Operations                                          │ │
│  │  - Future: Database Integration                             │ │
│  └─────────────────────────────────────────────────────────────┘ │
└─────────────────────────────────────────────────────────────────┘
```

### Features

- ✅ **Employee CRUD Operations** - Create, Read, Update, Delete employee records
- ✅ **Salary Management** - Calculate and apply salary increases
- ✅ **Role-based Grouping** - Organize employees by job functions
- ✅ **Birthday Tracking** - Find employees with birthdays in specific months
- ✅ **Salary Analytics** - Total salary calculations and minimum wage comparisons
- ✅ **Employee Search** - Find oldest employee and alphabetical sorting
- ✅ **Responsive UI** - Modern web interface with Bootstrap
- ✅ **RESTful API** - Complete API for programmatic access

### Technology Stack

- **Backend:** Java 17, Spring Boot 2.5.4, Maven
- **Frontend:** HTML5, CSS3, JavaScript ES6, Bootstrap 4.5.2
- **Testing:** JUnit 5, Spring Boot Test
- **Build:** Maven 3.6+
- **Architecture:** Layered Architecture, MVC Pattern

### Quick Start

#### Prerequisites

- Java 17 or higher
- Maven 3.6.0 or higher

#### Running the Application

```bash
# Clone the repository
git clone https://github.com/JacksonMiranda/Funcionario.git
cd Funcionario

# Build and test
mvn clean install

# Run the application
mvn spring-boot:run

# Access the application
open http://localhost:8080
```

#### Building for Production

```bash
# Build JAR file
mvn clean package

# Run the JAR
java -jar target/my-spring-boot-app-0.0.1-SNAPSHOT.jar
```

### API Documentation

#### Employee Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/funcionarios` | List all employees |
| `POST` | `/funcionarios/inserir` | Insert predefined employees |
| `DELETE` | `/funcionarios/{name}` | Delete employee by name |
| `PUT` | `/funcionarios/aumento` | Apply 10% salary increase |
| `GET` | `/funcionarios/agrupados` | Group employees by role |
| `GET` | `/funcionarios/aniversariantes` | Get birthday employees |
| `GET` | `/funcionarios/mais-velho` | Get oldest employee |
| `GET` | `/funcionarios/total-salarios` | Get total salaries |
| `GET` | `/funcionarios/ordem-alfabetica` | Get employees alphabetically |
| `GET` | `/funcionarios/salarios-minimos` | Get salaries in minimum wages |

### Testing

```bash
# Run all tests
mvn test

# Run with coverage
mvn test jacoco:report

# Run specific test
mvn test -Dtest=MySpringBootApplicationTests
```

### Project Structure

```
src/
├── main/
│   ├── java/com/example/myapp/
│   │   ├── MySpringBootApplication.java
│   │   ├── controller/
│   │   │   └── FuncionarioController.java
│   │   ├── model/
│   │   │   ├── Funcionario.java
│   │   │   └── Pessoa.java
│   │   ├── repository/
│   │   │   └── FuncionarioRepository.java
│   │   └── service/
│   │       └── FuncionarioService.java
│   └── resources/
│       ├── static/
│       │   ├── index.html
│       │   ├── styles.css
│       │   └── scripts.js
│       └── application.properties
└── test/
    └── java/com/example/myapp/
        └── MySpringBootApplicationTests.java
```

### Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests.

### Roadmap

- [ ] Database integration (MySQL/PostgreSQL)
- [ ] User authentication and authorization
- [ ] Advanced search and filtering
- [ ] Employee photo management
- [ ] Audit trail and logging
- [ ] Email notifications
- [ ] Export to PDF/Excel
- [ ] API rate limiting
- [ ] Microservices architecture

### License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Português

### Visão Geral

Uma aplicação profissional do domínio de RH construída com Spring Boot para gerenciar registros de funcionários. Este sistema fornece capacidades abrangentes de gerenciamento de funcionários com uma interface web moderna, APIs RESTful e princípios de arquitetura limpa.

### Diagrama de Arquitetura C4

```
┌─────────────────────────────────────────────────────────────────┐
│                           Usuário                               │
│                      (Gerente de RH)                            │
└─────────────────────────────────────────────────────────────────┘
                                   │
                                   ▼
┌─────────────────────────────────────────────────────────────────┐
│                        Camada Frontend                          │
│  ┌─────────────────────────────────────────────────────────────┐ │
│  │      Navegador Web (HTML/CSS/JavaScript)                   │ │
│  │  - Componentes de UI Bootstrap                              │ │
│  │  - Gerenciamento Interativo de Funcionários                │ │
│  │  - Atualizações de Dados em Tempo Real                     │ │
│  └─────────────────────────────────────────────────────────────┘ │
└─────────────────────────────────────────────────────────────────┘
                                   │
                                   ▼
┌─────────────────────────────────────────────────────────────────┐
│                API de Gerenciamento de Funcionários            │
│  ┌─────────────────────────────────────────────────────────────┐ │
│  │             Aplicação Spring Boot                           │ │
│  │  - Endpoints da API RESTful                                 │ │
│  │  - Processamento de Lógica de Negócios                      │ │
│  │  - Validação de Dados e Tratamento de Erros                 │ │
│  └─────────────────────────────────────────────────────────────┘ │
└─────────────────────────────────────────────────────────────────┘
                                   │
                                   ▼
┌─────────────────────────────────────────────────────────────────┐
│                      Armazenamento de Dados                     │
│  ┌─────────────────────────────────────────────────────────────┐ │
│  │              Repositório em Memória                         │ │
│  │  - Armazenamento de Registros de Funcionários               │ │
│  │  - Operações CRUD                                           │ │
│  │  - Futuro: Integração com Banco de Dados                    │ │
│  └─────────────────────────────────────────────────────────────┘ │
└─────────────────────────────────────────────────────────────────┘
```

### Funcionalidades

- ✅ **Operações CRUD de Funcionários** - Criar, Ler, Atualizar, Deletar registros de funcionários
- ✅ **Gerenciamento de Salários** - Calcular e aplicar aumentos salariais
- ✅ **Agrupamento por Função** - Organizar funcionários por funções de trabalho
- ✅ **Rastreamento de Aniversários** - Encontrar funcionários com aniversários em meses específicos
- ✅ **Análise Salarial** - Cálculos de salário total e comparações com salário mínimo
- ✅ **Busca de Funcionários** - Encontrar funcionário mais velho e ordenação alfabética
- ✅ **Interface Responsiva** - Interface web moderna com Bootstrap
- ✅ **API RESTful** - API completa para acesso programático

### Stack Tecnológico

- **Backend:** Java 17, Spring Boot 2.5.4, Maven
- **Frontend:** HTML5, CSS3, JavaScript ES6, Bootstrap 4.5.2
- **Testes:** JUnit 5, Spring Boot Test
- **Build:** Maven 3.6+
- **Arquitetura:** Arquitetura em Camadas, Padrão MVC

### Início Rápido

#### Pré-requisitos

- Java 17 ou superior
- Maven 3.6.0 ou superior

#### Executando a Aplicação

```bash
# Clonar o repositório
git clone https://github.com/JacksonMiranda/Funcionario.git
cd Funcionario

# Build e teste
mvn clean install

# Executar a aplicação
mvn spring-boot:run

# Acessar a aplicação
open http://localhost:8080
```

#### Build para Produção

```bash
# Build do arquivo JAR
mvn clean package

# Executar o JAR
java -jar target/my-spring-boot-app-0.0.1-SNAPSHOT.jar
```

### Documentação da API

#### Endpoints de Funcionários

| Método | Endpoint | Descrição |
|---------|----------|-----------|
| `GET` | `/funcionarios` | Listar todos os funcionários |
| `POST` | `/funcionarios/inserir` | Inserir funcionários predefinidos |
| `DELETE` | `/funcionarios/{nome}` | Deletar funcionário por nome |
| `PUT` | `/funcionarios/aumento` | Aplicar aumento salarial de 10% |
| `GET` | `/funcionarios/agrupados` | Agrupar funcionários por função |
| `GET` | `/funcionarios/aniversariantes` | Obter funcionários aniversariantes |
| `GET` | `/funcionarios/mais-velho` | Obter funcionário mais velho |
| `GET` | `/funcionarios/total-salarios` | Obter total de salários |
| `GET` | `/funcionarios/ordem-alfabetica` | Obter funcionários em ordem alfabética |
| `GET` | `/funcionarios/salarios-minimos` | Obter salários em salários mínimos |

### Testes

```bash
# Executar todos os testes
mvn test

# Executar com cobertura
mvn test jacoco:report

# Executar teste específico
mvn test -Dtest=MySpringBootApplicationTests
```

### Estrutura do Projeto

```
src/
├── main/
│   ├── java/com/example/myapp/
│   │   ├── MySpringBootApplication.java
│   │   ├── controller/
│   │   │   └── FuncionarioController.java
│   │   ├── model/
│   │   │   ├── Funcionario.java
│   │   │   └── Pessoa.java
│   │   ├── repository/
│   │   │   └── FuncionarioRepository.java
│   │   └── service/
│   │       └── FuncionarioService.java
│   └── resources/
│       ├── static/
│       │   ├── index.html
│       │   ├── styles.css
│       │   └── scripts.js
│       └── application.properties
└── test/
    └── java/com/example/myapp/
        └── MySpringBootApplicationTests.java
```

### Contribuindo

Por favor, leia [CONTRIBUTING.md](CONTRIBUTING.md) para detalhes sobre nosso código de conduta e o processo para enviar pull requests.

### Roadmap

- [ ] Integração com banco de dados (MySQL/PostgreSQL)
- [ ] Autenticação e autorização de usuários
- [ ] Busca e filtragem avançadas
- [ ] Gerenciamento de fotos de funcionários
- [ ] Trilha de auditoria e logging
- [ ] Notificações por email
- [ ] Exportação para PDF/Excel
- [ ] Limitação de taxa da API
- [ ] Arquitetura de microsserviços

### Licença

Este projeto é licenciado sob a Licença MIT - veja o arquivo [LICENSE](LICENSE) para detalhes.
