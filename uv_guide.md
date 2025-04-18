# UV Guide

UV is a modern Python package manager and resolver written in Rust. It offers significant performance improvements over traditional tools like pip and poetry, while providing a unified approach to Python package management.

## Getting Started

### Project Initialization
```bash
uv init my-project
cd my-project
```

This creates a new project with the following structure:
```
my-project/
├── .python-version
├── .gitignore
├── pyproject.toml
└── README.md
```

- `.python-version`: Specifies the Python version
- `pyproject.toml`: Defines project metadata and dependencies
- `.venv`: Created automatically when dependencies are added

## Core Commands

### Package Management
```bash
# Install packages from requirements.txt
uv add -r requirements.txt

# Install a specific package
uv add <package_name>

# Install development dependencies
uv add --dev <package_name>
```

### Project Management
```bash
# Run Python scripts with virtual environment
uv run script.py

# Sync project dependencies
uv sync

# Clean cache
uv clean cache
```

### Development Tools
```bash
# Run tools like ruff, mypy
uvx ruff check .
uvx ruff format *.py --line-length 100
```

## Key Features

1. **Automatic Virtual Environment**
   - No need to manually activate virtual environments
   - `.venv` is automatically created and managed
   - IDE integration is seamless

2. **Dependency Management**
   - Fast dependency resolution
   - Lock file support (`uv.lock`)
   - Reproducible builds

3. **Development Workflow**
   - Integrated development tools
   - Simplified command structure
   - Automatic Python version management

## What UV Replaces

UV can replace multiple traditional Python tools:
- pip (package installation)
- pyenv (Python version management)
- poetry (dependency/build management)
- venv (virtual environment creation)
- pipenv (environment/dependency management)

## Best Practices

1. Use `uv sync` for CI/CD environments
2. Leverage `uv.lock` for reproducible builds
3. Use `uvx` for development tools
4. Keep dependencies in `pyproject.toml`

## Performance

UV is significantly faster than traditional tools:
- Much faster than pip
- Faster than poetry
- Optimized for large projects
- Efficient dependency resolution

## IDE Integration

UV works seamlessly with modern IDEs:
- Automatic virtual environment detection
- No need for manual kernel installation
- Consistent environment across team members
- Simple project sharing
