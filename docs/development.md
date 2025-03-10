# Development Guide

This guide will help you set up your development environment and contribute to venv-purge.

## Setting Up the Development Environment

### Prerequisites

- Python 3.12+
- Git
- [uv](https://docs.astral.sh/uv/)

### Initial Setup

1. Clone the repository:

```bash
git clone https://github.com/Adrian147/venv-purge.git
cd venv-purge
```

2. Create and activate a virtual environment:

```bash
# initialise the environment.
uv venv

# activate the environment.
source .venv/bin/activate
```

3. Install the package in development mode with all dependencies:

```bash
# sync your environment with the uv.lock file.
uv sync --all-extras --dev
```

4. Install pre-commit hooks:

```bash
pre-commit install
```

## Development Workflow

### Code Structure

The project follows a standard Python package structure:

```text
venv-purge/
├── src/
│   └── venv_purge/           # Main package
│       ├── __init__.py       # Package initialization
│       ├── cli.py            # Command-line interface
│       ├── config.py          # Configuration handling
│       ├── logger.py         # Logging configuration
│       ├── search_engine.py  # Core detection logic
│       └── ui.py             # TUI implementation
├── tests/                    # Test suite
├── docs/                     # Documentation
└── examples/                 # Usage examples
```

### Running Tests

Tests are run using pytest:

```bash
# Run all tests
pytest

# Run tests with coverage report
pytest --cov=src

# Run specific tests
pytest tests/test_search_engine.py
```

### Code Quality Tools

The project uses several tools to ensure code quality:

#### Ruff (Linting)

```bash
# Check code
ruff check

# Auto-fix issues
ruff check --fix
```

#### MyPy (Type Checking)

```bash
# Check types
mypy .
```

#### Pre-commit

```bash
# Run all checks
pre-commit run --all-files
```

### Building the Package

```bash
# Build the package
uv build
```

## Making Contributions

### Pull Request Process

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/my-feature`)
3. Commit your changes with descriptive commit messages
4. Run tests and code quality checks
5. Push to your branch
6. Create a Pull Request to the main repository

### Coding Standards

- Follow PEP 8 style guidelines
- Write docstrings in Google style format
- Include type annotations for all functions
- Write tests for new features or bug fixes
- Keep functions focused and modular

### Commit Messages

Follow the conventional commits format:

```text
feature: add new feature X
fix: resolve issue with Y
docs: update instructions
refactor: simplify search algorithm
test: add tests for feature Z
```

## Documentation

The project uses Markdown for documentation:

- `README.md`: Project overview
- `docs/user-guide.md`: User guide and usage instructions
- `docs/development.md`: Development instructions (this file)
- `docs/contributing.md`: Contribution guidelines

## Release Process

1. Update version in `src/venv_purge/__init__.py`
2. Update CHANGELOG.md
3. Create a new release on GitHub with release notes
4. CI will automatically publish the package to PyPI

## Getting Help

If you need help or have questions, please:

1. Check the existing issues on GitHub
2. Create a new issue with a clear description of your problem
3. Reach out to the maintainers via the contact information in README.md
