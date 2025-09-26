# Security Policy

## Supported Versions

We release patches for security vulnerabilities. Which versions are eligible for receiving such patches depends on the CVSS v3.0 Rating:

| Version | Supported          |
| ------- | ------------------ |
| 1.x.x   | :white_check_mark: |

## Reporting a Vulnerability

The Employee Management System team and community take security bugs seriously. We appreciate your efforts to responsibly disclose your findings, and will make every effort to acknowledge your contributions.

To report a security issue, please use the GitHub Security Advisory ["Report a Vulnerability"](https://github.com/JacksonMiranda/Funcionario/security/advisories/new) tab.

The Employee Management System team will send a response indicating the next steps in handling your report. After the initial reply to your report, the security team will keep you informed of the progress towards a fix and full announcement, and may ask for additional information or guidance.

### Please include the following information in your report:

- Type of issue (e.g. buffer overflow, SQL injection, cross-site scripting, etc.)
- Full paths of source file(s) related to the manifestation of the issue
- The location of the affected source code (tag/branch/commit or direct URL)
- Any special configuration required to reproduce the issue
- Step-by-step instructions to reproduce the issue
- Proof-of-concept or exploit code (if possible)
- Impact of the issue, including how an attacker might exploit the issue

This information will help us triage your report more quickly.

## Preferred Languages

We prefer all communications to be in English or Portuguese.

## Policy

- We will respond to security reports within 48 hours
- We will provide regular updates on the progress of fixing any reported vulnerabilities
- We will credit reporters in any security advisories (unless they prefer to remain anonymous)

## Security Best Practices

When contributing to this project, please keep in mind:

1. **Input Validation**: Always validate input data before processing
2. **Authentication & Authorization**: Ensure proper access controls are in place
3. **Error Handling**: Don't expose sensitive information in error messages
4. **Dependencies**: Keep dependencies up to date and scan for known vulnerabilities
5. **Secrets Management**: Never commit secrets, API keys, or sensitive data

## Security Features

This application includes:

- Input validation for all user inputs
- CSRF protection via Spring Security
- XSS protection through proper output encoding
- Secure headers configuration
- Regular dependency updates via Dependabot

## Secure Development

- All dependencies are scanned for vulnerabilities
- Code is analyzed using static analysis security testing (SAST)
- Regular security updates are applied promptly

Thank you for helping keep Employee Management System and our users safe!