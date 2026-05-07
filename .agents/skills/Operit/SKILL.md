```markdown
# Operit Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the Operit Kotlin codebase. It covers file organization, code style, commit practices, and testing patterns. By following these guidelines, contributors can write consistent, maintainable code and collaborate effectively.

## Coding Conventions

### File Naming
- Use **snake_case** for all file names.
  - Example: `user_service.kt`, `order_processor.kt`

### Import Style
- Use **relative imports** to reference other modules or files within the project.
  - Example:
    ```kotlin
    import ../utils/date_utils
    ```

### Export Style
- Use **named exports** for functions, classes, or objects.
  - Example:
    ```kotlin
    // In payment_processor.kt
    fun processPayment() { ... }
    ```

### Commit Messages
- Follow the **conventional commit** format.
- Use the `feat` prefix for new features.
  - Example:
    ```
    feat: add user authentication to login endpoint
    ```

## Workflows

### Feature Development
**Trigger:** When starting work on a new feature  
**Command:** `/feature-dev`

1. Create a new branch for the feature.
2. Implement the feature following coding conventions.
3. Write or update tests in corresponding `*.test.*` files.
4. Commit changes using the `feat` prefix.
5. Open a pull request for review.

### Code Review
**Trigger:** When reviewing a pull request  
**Command:** `/code-review`

1. Check that file naming, import, and export conventions are followed.
2. Ensure commit messages use the correct format.
3. Verify that tests are present and passing.
4. Provide feedback or approve the changes.

### Testing
**Trigger:** Before merging or deploying code  
**Command:** `/run-tests`

1. Identify all files matching the `*.test.*` pattern.
2. Run tests using the project's preferred method or tool.
3. Confirm all tests pass before proceeding.

## Testing Patterns

- Test files follow the `*.test.*` naming pattern.
  - Example: `user_service.test.kt`
- The testing framework is not specified; use the project's standard approach.
- Place tests alongside the code they validate or in a dedicated `tests/` directory.

## Commands
| Command         | Purpose                                   |
|-----------------|-------------------------------------------|
| /feature-dev    | Start a new feature development workflow   |
| /code-review    | Perform a code review workflow            |
| /run-tests      | Run all tests in the codebase             |
```