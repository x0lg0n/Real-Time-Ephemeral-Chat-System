# Contributing to Real-Time Ephemeral Chat System

First off, thank you for considering contributing to this project! It's people like you that make this such a great tool.

## Code of Conduct

This project and everyone participating in it is governed by our Code of Conduct. By participating, you are expected to uphold this code.

## How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check the existing issues as you might find out that you don't need to create one. When you are creating a bug report, please include as many details as possible:

* **Use a clear and descriptive title** for the issue
* **Describe the exact steps** which reproduce the problem
* **Provide specific examples** to demonstrate the steps
* **Describe the behavior you observed** after following the steps
* **Explain which behavior you expected** to see instead
* **Include screenshots** if possible
* **Include your environment details** (OS, browser, Node.js version, etc.)

### Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues. When creating an enhancement suggestion, please include:

* **Use a clear and descriptive title** for the issue
* **Provide a step-by-step description** of the suggested enhancement
* **Provide specific examples** to demonstrate the steps
* **Describe the current behavior** and **explain which behavior you expected** to see instead
* **Explain why this enhancement** would be useful to most users

### Pull Requests

The process for submitting pull requests:

1. **Fork** the repo and create your branch from `master`
2. **Install dependencies** and make sure all tests pass
3. **Make your changes** following the coding standards
4. **Write or update tests** as needed
5. **Update documentation** if you've changed APIs
6. **Ensure the test suite passes**
7. **Issue the pull request**

### Development Setup

1. Fork and clone the repository
2. Install dependencies: `npm install`
3. Create a branch for your feature: `git checkout -b feature/your-feature-name`
4. Make your changes
5. Run tests: `npm test`
6. Commit your changes following conventional commits
7. Push to your fork and submit a pull request

### Coding Standards

* Use **TypeScript** for all new code
* Follow the existing **code style** (ESLint configuration)
* Write **meaningful commit messages**
* Include **tests** for new functionality
* Update **documentation** when necessary
* Ensure **all tests pass** before submitting

### Commit Message Guidelines

We follow conventional commits format:

```javascript
type(scope): description

[optional body]

[optional footer]
```

Types:

* `feat`: New feature
* `fix`: Bug fix
* `docs`: Documentation changes
* `style`: Code style changes (formatting, etc.)
* `refactor`: Code refactoring
* `test`: Adding or updating tests
* `chore`: Maintenance tasks

Examples:

```text
feat(chat): add message encryption
fix(api): resolve room creation timeout
docs(readme): update installation instructions
```

### Testing

* Write unit tests for new functionality
* Ensure existing tests continue to pass
* Test across different browsers if UI changes are made
* Include edge cases in your tests

### Documentation

* Update README.md if you change functionality
* Add JSDoc comments for new functions
* Update example code if APIs change
* Keep documentation up to date with code changes

## Styleguides

### Git Commit Messages

* Use the present tense ("Add feature" not "Added feature")
* Use the imperative mood ("Move cursor to..." not "Moves cursor to...")
* Limit the first line to 72 characters or less
* Reference issues and pull requests liberally after the first line

### JavaScript/TypeScript Styleguide

* All JavaScript/TypeScript must adhere to ESLint configuration
* Use TypeScript for all new code
* Prefer functional components with hooks over class components
* Use async/await instead of callbacks
* Destructure objects when it improves readability

### CSS/Tailwind Styleguide

* Use Tailwind CSS utility classes
* Follow the existing color palette
* Maintain consistent spacing using the spacing scale
* Use responsive prefixes appropriately

## Additional Notes

### Issue and Pull Request Labels

We use the following labels to help organize and identify issues:

* `bug` - Something isn't working
* `enhancement` - New feature or request
* `documentation` - Improvements or additions to documentation
* `good first issue` - Good for newcomers
* `help wanted` - Extra attention is needed
* `question` - Further information is requested

### Getting Help

If you need help with anything, feel free to:

* Create an issue with your question
* Reach out to the maintainers
* Check existing documentation and issues

Thank you for contributing to making this project better!
