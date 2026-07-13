```markdown
# luxoranova Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill provides guidance on the development patterns and conventions used in the `luxoranova` Python codebase. It covers file naming, import/export styles, commit patterns, and testing practices. The repository does not use a specific framework, and workflows are primarily manual, with a focus on code organization and testing.

## Coding Conventions

### File Naming
- Use **camelCase** for filenames.
  - Example: `myModule.py`, `dataProcessor.py`

### Import Style
- Use **relative imports** within the project.
  - Example:
    ```python
    from .utils import helperFunction
    ```

### Export Style
- Use **named exports** (i.e., define specific functions/classes to be used elsewhere).
  - Example:
    ```python
    def usefulFunction():
        pass

    class ImportantClass:
        pass
    ```

### Commit Patterns
- Commit messages are **freeform** and do not follow a strict prefix convention.
- Average commit message length: **38 characters**.
  - Example:
    ```
    Fix bug in dataProcessor when input is empty
    ```

## Workflows

### Adding a New Module
**Trigger:** When you need to add new functionality to the project  
**Command:** `/add-module`

1. Create a new Python file using camelCase naming (e.g., `featureModule.py`).
2. Implement functions or classes with clear, descriptive names.
3. Use relative imports to access utilities or other modules.
4. Export functions/classes by defining them at the module level.

### Writing and Running Tests
**Trigger:** When you need to test new or existing code  
**Command:** `/run-tests`

1. Create a test file with `.test.` in the filename (e.g., `featureModule.test.py`).
2. Write test functions for each public function/class.
3. Use the project's preferred or default Python testing tools (framework is unknown; consider using `unittest` or `pytest`).
4. Run tests manually from the command line:
    ```bash
    python featureModule.test.py
    ```
    or, if using pytest:
    ```bash
    pytest
    ```

### Making Commits
**Trigger:** When saving changes to the repository  
**Command:** `/commit-changes`

1. Write a concise, descriptive commit message (no strict prefix required).
2. Keep the message around 38 characters if possible.
3. Example:
    ```
    Add validation to user input in login form
    ```

## Testing Patterns

- **Test files** are named with `.test.` in the filename (e.g., `moduleName.test.py`).
- **Testing framework** is not specified; use standard Python testing practices.
- Example test file:
    ```python
    from .featureModule import usefulFunction

    def test_usefulFunction():
        assert usefulFunction(2) == 4
    ```

## Commands
| Command         | Purpose                                      |
|-----------------|----------------------------------------------|
| /add-module     | Scaffold a new module with correct patterns  |
| /run-tests      | Run all test files in the project            |
| /commit-changes | Make a commit following project conventions  |
```
