# Security Policy

## Supported Versions

We release patches for security vulnerabilities. Which versions are eligible for receiving such patches depends on the severity of the vulnerability.

| Version | Supported          |
| ------- | ------------------ |
| 0.1.x   | :white_check_mark: |

## Reporting a Vulnerability

If you discover a security vulnerability within this project, please send an email to [security@gmail.com] instead of using the public issue tracker. All security vulnerabilities will be promptly addressed.

Please do not publicly disclose the vulnerability until it has been addressed by the team.

## Security Measures

This project implements the following security measures:

- **Input Validation**: All user inputs are validated and sanitized
- **Secure Dependencies**: Regular dependency updates and security audits
- **Environment Variables**: Sensitive configuration stored in environment variables
- **HTTPS**: All communications should use HTTPS in production
- **Rate Limiting**: API endpoints implement rate limiting to prevent abuse

## Security Best Practices

When using this project, we recommend:

1. Keep all dependencies up to date
2. Use strong, unique secrets for environment variables
3. Enable HTTPS in production environments
4. Regularly audit your deployment for security issues
5. Monitor logs for suspicious activity

## Data Protection

This project handles the following types of data:

- **Temporary User Identifiers**: Generated for chat sessions
- **Chat Messages**: Stored temporarily in Redis
- **Room Metadata**: Basic room information

All data is automatically deleted when chat rooms expire, ensuring no permanent data retention.

## Privacy Policy

This project does not collect or store personal information. All data is temporary and automatically deleted when rooms expire.

## Contact

For security-related questions or concerns, please contact:

- Email: [securit@gmail.com]
- PGP Key: [Your PGP key if available]

We appreciate your efforts to responsibly disclose your findings and will make every effort to acknowledge your contributions.
