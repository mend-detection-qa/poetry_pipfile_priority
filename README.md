# Test Case: Poetry Lower Priority Files

## Package Manager
Poetry

## Python Version Detection
- **Source**: Pipfile (PRIORITY #4 for Poetry)
- **Expected Version**: 3.12
- **Conflict**: environment.yml says 3.8 (PRIORITY #5 - lower)

## Files Present
- pyproject.toml - NO python version specified
- poetry.lock
- Pipfile - python_version = "3.12" (SHOULD WIN)
- environment.yml - python=3.8 (SHOULD BE IGNORED)

## Test Purpose
Test lower priority files when high priority files don't specify Python version. Validates Pipfile beats environment.yml.
