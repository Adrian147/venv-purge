# Contributing to venv-purge

First of all, thank you for considering contributing to venv-purge! This document outlines the guidelines for contributing to this project.

## Code of Conduct

This project follows a [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code. Please report unacceptable behavior to [adrian47mcdonald@gmail.com](mailto:adrian47mcdonald@gmail.com).

## How Can I Contribute?

### Reporting Bugs

Before creating a bug report, please check the existing issues to see if the problem has already been reported. If it hasn't, create a new issue with a clear title and description that includes:

- Steps to reproduce the behavior
- Expected behavior
- Actual behavior
- System information (OS, Python version, etc.)
- Any relevant logs or error messages

### Suggesting Enhancements

Enhancement suggestions are always welcome! When submitting an enhancement suggestion, please include:

- A clear and descriptive title
- A detailed description of the proposed functionality
- Any potential implementation details you can think of
- Why this enhancement would be useful to most users

### Pull Requests

Pull requests are the best way to propose changes to the codebase. Here's how to submit a PR:

1. Fork the repository and create your branch from `main`
2. Install the development dependencies (see [Development Guide](docs/development.md))
3. Make your changes
4. Add or update tests as necessary
5. Run the test suite to ensure all tests pass
6. Run the linters and type checkers to ensure code quality
7. Update documentation if necessary
8. Submit the PR with a clear description of the changes and why they're needed

### Development Process

Please refer to the [Development Guide](docs/development.md) for detailed instructions on setting up your development environment and the development workflow.

## Style Guidelines

### Code Style

This project uses:

- [Ruff](https://github.com/charliermarsh/ruff) for linting
- [MyPy](https://mypy.readthedocs.io/) for static type checking
- [Pre-commit](https://pre-commit.com/) hooks to enforce these checks

Code should follow these guidelines:

- Follow PEP 8 style guidelines
- Write clear, descriptive variable and function names
- Include type annotations for all function parameters and return values
- Document all public functions, classes, and modules with proper docstrings (Google style)
- Keep functions focused and modular (do one thing well)

### Commit Messages

Follow the [Conventional Commits](https://www.conventionalcommits.org/) specification:

```text
<type>: <description>

[optional body]

[optional footer(s)]
```

Types include:

- `feature`: A new feature
- `fix`: A bug fix
- `docs`: Documentation only changes
- `style`: Changes that do not affect the meaning of the code
- `refactor`: A code change that neither fixes a bug nor adds a feature
- `perf`: A code change that improves performance
- `test`: Adding missing tests or correcting existing tests
- `chore`: Changes to the build process or auxiliary tools

### Documentation

- Keep documentation up to date as you change code
- Use clear, simple language and avoid jargon
- Include examples where appropriate
- Ensure all docstrings follow Google style format

## Questions?

If you have any questions about contributing, feel free to open an issue or contact the maintainers directly.
