```markdown
# compound-engineering-plugin Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches best practices and development patterns for contributing to the `compound-engineering-plugin` repository, a TypeScript codebase with a focus on maintainable code structure, conventional commit messages, and consistent coding conventions. While no specific framework is used, the repository emphasizes clarity in file organization, import/export styles, and testing patterns.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `myComponent.ts`, `userService.test.ts`

### Import Style
- Use **relative imports** for referencing modules within the project.
  - Example:
    ```typescript
    import { myFunction } from './utils';
    ```

### Export Style
- Use **named exports** for all modules.
  - Example:
    ```typescript
    // utils.ts
    export function myFunction() { /* ... */ }

    // usage
    import { myFunction } from './utils';
    ```

### Commit Messages
- Follow **conventional commit** format.
- Use the `chore` prefix for maintenance commits.
- Keep commit messages concise (average ~19 characters).
  - Example: `chore: update dependencies`

## Workflows

### Conventional Commit Workflow
**Trigger:** When making any commit to the repository  
**Command:** `/conventional-commit`

1. Stage your changes.
2. Write a commit message using the conventional format: `<type>: <short description>`
   - Example: `chore: fix typo in docs`
3. Commit your changes.

### File Creation Workflow
**Trigger:** When adding new files or modules  
**Command:** `/create-file`

1. Name the file using camelCase (e.g., `newFeature.ts`).
2. Use named exports in your module.
3. Use relative imports in any consuming files.

### Testing Workflow
**Trigger:** When writing or updating tests  
**Command:** `/run-tests`

1. Create or update test files using the `*.test.*` naming pattern (e.g., `userService.test.ts`).
2. Write tests for your functions or modules.
3. Run the test suite using your preferred test runner.

## Testing Patterns

- Test files are named using the `*.test.*` pattern, such as `myModule.test.ts`.
- The specific testing framework is not detected; use standard TypeScript testing practices.
- Example test file structure:
  ```typescript
  // mathUtils.test.ts
  import { add } from './mathUtils';

  describe('add', () => {
    it('adds two numbers', () => {
      expect(add(2, 3)).toBe(5);
    });
  });
  ```

## Commands
| Command                | Purpose                                         |
|------------------------|-------------------------------------------------|
| /conventional-commit   | Guide for writing conventional commit messages  |
| /create-file           | Steps for creating new files/modules            |
| /run-tests             | Instructions for writing and running tests      |
```