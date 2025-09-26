# Contributing to Employee Management System

First off, thank you for considering contributing to the Employee Management System! It's people like you that make this project better.

## Code of Conduct

This project and everyone participating in it is governed by our [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code.

## How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check the existing issues as you might find that the problem has already been reported. When you are creating a bug report, please include as many details as possible:

- **Use a clear and descriptive title** for the issue to identify the problem
- **Describe the exact steps which reproduce the problem** in as many details as possible
- **Provide specific examples to demonstrate the steps**
- **Describe the behavior you observed after following the steps**
- **Explain which behavior you expected to see instead and why**
- **Include screenshots and animated GIFs** if they help explain the problem

### Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues. When creating an enhancement suggestion, please include:

- **Use a clear and descriptive title** for the issue to identify the suggestion
- **Provide a step-by-step description of the suggested enhancement** in as many details as possible
- **Provide specific examples to demonstrate the steps**
- **Explain why this enhancement would be useful**

### Pull Requests

1. Fork the repository
2. Create a feature branch from `main`
3. Make your changes
4. Add or update tests as appropriate
5. Ensure the test suite passes
6. Make sure your code follows the existing style conventions
7. Write clear, descriptive commit messages
8. Push to your fork and submit a pull request

## Development Environment Setup

### Prerequisites

- Java 17 or higher
- Maven 3.6.0 or higher
- Your favorite IDE (IntelliJ IDEA, Eclipse, VS Code, etc.)

### Setting up the project

1. Clone the repository:
   ```bash
   git clone https://github.com/JacksonMiranda/Funcionario.git
   cd Funcionario
   ```

2. Build and test the project:
   ```bash
   mvn clean install
   ```

3. Run the application:
   ```bash
   mvn spring-boot:run
   ```

4. Open your browser and navigate to `http://localhost:8080`

### Running Tests

```bash
# Run all tests
mvn test

# Run tests with coverage
mvn test jacoco:report
```

### Code Style

- Follow Java naming conventions
- Use 4 spaces for indentation (no tabs)
- Line length should not exceed 120 characters
- Include JavaDoc comments for public methods and classes
- Write unit tests for new functionality

### Commit Messages

- Use the present tense ("Add feature" not "Added feature")
- Use the imperative mood ("Move cursor to..." not "Moves cursor to...")
- Limit the first line to 72 characters or less
- Reference issues and pull requests liberally after the first line

Examples:
```
feat: add employee salary calculation feature

fix: resolve null pointer exception in employee search

docs: update API documentation for employee endpoints

test: add unit tests for employee service methods
```

### Commit Message Prefixes

- `feat:` - A new feature
- `fix:` - A bug fix
- `docs:` - Documentation only changes
- `style:` - Changes that do not affect the meaning of the code
- `refactor:` - A code change that neither fixes a bug nor adds a feature
- `perf:` - A code change that improves performance
- `test:` - Adding missing tests or correcting existing tests
- `chore:` - Changes to the build process or auxiliary tools

## Project Structure

```
src/
├── main/
│   ├── java/
│   │   └── com/example/myapp/
│   │       ├── MySpringBootApplication.java
│   │       ├── controller/
│   │       ├── model/
│   │       ├── repository/
│   │       └── service/
│   └── resources/
│       ├── static/
│       └── application.properties
└── test/
    └── java/
        └── com/example/myapp/
```

## Questions?

If you have any questions or need help, feel free to:

1. Open an issue with the question label
2. Start a discussion in the GitHub Discussions tab
3. Contact the maintainers directly

Thank you for contributing! 🚀