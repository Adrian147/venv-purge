# venv-purge User Guide

`venv-purge` is a command-line tool that helps you find and manage Python virtual environments across your system. It can detect environments created with various tools and methods, and helps you clean up unused or forgotten environments.

## Installation

### Using pip/pipx (recommended)

```bash
# Install with pipx (recommended)
pipx install venv-purge

# Or with pip
pip install venv-purge
```

### From source

```bash
# Clone the repository
git clone https://github.com/Adrian147/venv-purge.git
cd venv-purge

# Install
pip install .
```

## Basic Usage

### Interactive TUI Mode

The simplest way to use venv-purge is in interactive TUI mode:

```bash
venv-purge scan ~/projects
```

This will:

1. Scan the specified directory for virtual environments
2. Display them in an interactive terminal UI
3. Allow you to browse, filter, and select environments to delete

In the TUI:

- Use arrow keys to navigate
- Press Space to select environments
- Press Enter to view details or confirm actions
- Type in the search box to filter environments

### Command-line Mode

If you prefer to use traditional command-line mode, you can use these commands:

#### List environments

```bash
# List all environments in a directory
venv-purge list ~/projects

# List environments in multiple directories
venv-purge list ~/projects ~/experiments /tmp
```

#### Delete specific environments

```bash
# Delete specific environments
venv-purge delete ~/projects/.venv ~/projects/project2/venv
```

#### Scan and delete

```bash
# Scan directories and interactively choose which to delete
venv-purge scan ~/projects ~/experiments

# Scan and batch delete all found environments (use with caution!)
venv-purge scan ~/projects --batch --no-interactive
```

## Options

### Global options

These options can be used with any command:

- `--dry-run`: Show what would be deleted without actually deleting
- `--debug` / `-d`: Show debug information
- `--allow-system-envs`: Allow scanning and deleting environments in system directories (off by default for safety)
- `--version` / `-v`: Show version information and exit

### Command-specific options

#### `scan` command

- `--batch` / `-b`: Delete all found environments without individual confirmation
- `--interactive` / `--no-interactive`: Enable or disable interactive TUI mode

#### `delete` command

- `--batch` / `-b`: Delete all specified environments without confirmation

## Examples

### Find and clean up virtual environments in your projects directory

```bash
venv-purge scan ~/projects
```

### Find all environments, including in your home directory

```bash
venv-purge scan ~ --allow-system-envs
```

### Do a dry run to see what would be deleted

```bash
venv-purge scan ~/projects --dry-run
```

### Delete all old environments in a specific directory

```bash
venv-purge scan ~/old-projects --batch --no-interactive
```

## Safety Features

`venv-purge` includes several safety features to prevent accidental deletion:

1. System directories are never scanned by default
2. Confirmation is required before deletion (unless `--batch` is specified)
3. Dry run mode allows previewing what would be deleted
