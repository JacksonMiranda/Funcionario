# Support

Thank you for using the Employee Management System! This document explains where and how to get help.

## Getting Help

### 📖 Documentation

First, please check our documentation:

- [README.md](README.md) - Project overview and getting started guide
- [Contributing Guide](CONTRIBUTING.md) - How to contribute to the project
- [Architecture Documentation](docs/architecture.md) - System architecture details

### 🐛 Bug Reports

If you think you found a bug, please check the [existing issues](https://github.com/JacksonMiranda/Funcionario/issues) first. If you can't find a similar issue, you can [create a new one](https://github.com/JacksonMiranda/Funcionario/issues/new).

When reporting bugs, please include:

- A clear description of the problem
- Steps to reproduce the issue
- Expected vs actual behavior
- Your environment details (OS, Java version, browser, etc.)
- Screenshots or error messages if applicable

### 💡 Feature Requests

We love feature requests! Please [create an issue](https://github.com/JacksonMiranda/Funcionario/issues/new) with:

- A clear description of the feature
- Why you think it would be useful
- Any implementation ideas you might have

### ❓ Questions

For general questions about using the Employee Management System:

1. Check if your question is already answered in the [Issues](https://github.com/JacksonMiranda/Funcionario/issues)
2. Search through [closed issues](https://github.com/JacksonMiranda/Funcionario/issues?q=is%3Aissue+is%3Aclosed)
3. If you can't find an answer, [create a new issue](https://github.com/JacksonMiranda/Funcionario/issues/new) with the `question` label

### 📧 Direct Contact

For sensitive issues or private inquiries, you can reach out to the maintainers directly:

- **Jackson Miranda** - [@JacksonMiranda](https://github.com/JacksonMiranda)

## Community Guidelines

Please be respectful and constructive in all interactions. We follow our [Code of Conduct](CODE_OF_CONDUCT.md) in all community spaces.

## Response Times

We aim to respond to:

- **Security issues**: Within 48 hours
- **Bug reports**: Within 5 business days
- **Feature requests**: Within 7 business days
- **Questions**: Within 3 business days

Please note that this is an open source project maintained by volunteers, so response times may vary.

## Self-Help Resources

### Common Issues

**Application won't start:**
- Ensure you have Java 17 or higher installed
- Check that port 8080 is not in use
- Verify Maven dependencies are installed correctly

**Build fails:**
- Run `mvn clean install` to refresh dependencies
- Check that you're using the correct Java version
- Ensure all tests are passing

**Frontend issues:**
- Clear your browser cache
- Check browser developer tools for JavaScript errors
- Ensure you're accessing the correct URL (http://localhost:8080)

### Useful Commands

```bash
# Clean and rebuild
mvn clean install

# Run tests
mvn test

# Start the application
mvn spring-boot:run

# Check code style
mvn checkstyle:check
```

## Contributing

If you'd like to help improve the project, please read our [Contributing Guide](CONTRIBUTING.md). We welcome contributions of all kinds!

## Resources

- [Spring Boot Documentation](https://spring.io/projects/spring-boot)
- [Maven Documentation](https://maven.apache.org/guides/)
- [Java 17 Documentation](https://docs.oracle.com/en/java/javase/17/)

Thank you for being part of our community! 🙏