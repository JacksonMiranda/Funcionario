# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- Professional repository baseline with comprehensive documentation
- MIT License
- Code of Conduct (Contributor Covenant)
- Contributing guidelines
- Security policy
- Support documentation
- Architecture documentation
- GitHub issue templates
- Pull request template
- CI/CD workflows for Java 17
- CodeQL security analysis
- Dependabot configuration
- Release drafter workflow
- Editor configuration (.editorconfig)
- Git attributes configuration
- Code owners configuration

### Changed
- Updated Java version from 11 to 17
- Improved project structure and organization
- Enhanced README with bilingual support (PT-BR/EN)
- Fixed test package structure alignment

### Fixed
- Test package structure mismatch (com.example.demo vs com.example.myapp)
- Build artifacts exclusion via .gitignore

## [1.0.0] - 2024-09-26

### Added
- Employee management system with Spring Boot
- CRUD operations for employees
- Web interface with Bootstrap styling
- Employee salary calculations
- Employee grouping by role functionality
- Birthday tracking features
- Employee search and filtering
- RESTful API endpoints
- Responsive web design

### Features
- **Employee Management**: Full CRUD operations for employee records
- **Salary Management**: Calculate and apply salary increases
- **Role Grouping**: Group employees by their job functions
- **Birthday Tracking**: Find employees with birthdays in specific months
- **Responsive UI**: Modern web interface with Bootstrap
- **RESTful API**: Complete API for employee operations
- **Data Validation**: Input validation and error handling

### Technical Details
- Java 11 (upgraded to 17 in latest version)
- Spring Boot 2.5.4
- Maven build system
- Thymeleaf templating
- Bootstrap 4.5.2 for styling
- JavaScript for dynamic functionality
- In-memory data storage

### Dependencies
- spring-boot-starter-web
- spring-boot-starter-thymeleaf
- spring-boot-devtools
- spring-boot-starter-test

---

### Legend

- **Added** for new features
- **Changed** for changes in existing functionality
- **Deprecated** for soon-to-be removed features
- **Removed** for now removed features
- **Fixed** for any bug fixes
- **Security** for vulnerability fixes