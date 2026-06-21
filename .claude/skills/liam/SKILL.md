```markdown
# liam Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill provides guidance on contributing to the `liam` TypeScript codebase. It covers the project's coding conventions, file organization, import/export patterns, and testing practices. Whether you're adding new features, fixing bugs, or writing tests, this document will help you align with the established development patterns.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `userProfile.ts`, `dataFetcher.test.ts`

### Imports
- Use **relative imports** for referencing modules within the project.
  - Example:
    ```typescript
    import { fetchData } from './dataFetcher';
    ```

### Exports
- Use **named exports** for all exported functions, types, and constants.
  - Example:
    ```typescript
    // In dataFetcher.ts
    export function fetchData(url: string): Promise<Data> { ... }
    ```

### Commit Messages
- Freeform commit messages, no enforced prefix or format.
- Typical length: ~61 characters.

## Workflows

### Adding a New Feature
**Trigger:** When implementing a new functionality.
**Command:** `/add-feature`

1. Create a new TypeScript file using camelCase naming.
2. Write your feature using named exports.
3. Use relative imports for dependencies.
4. Add or update corresponding test files (`*.test.ts`).
5. Commit your changes with a descriptive message.

### Fixing a Bug
**Trigger:** When resolving an issue in the codebase.
**Command:** `/fix-bug`

1. Locate the relevant file(s) using camelCase naming.
2. Apply your fix, maintaining existing code style.
3. Update or add tests in `*.test.ts` files to cover the fix.
4. Commit with a message describing the bug and resolution.

### Writing Tests
**Trigger:** When adding or updating tests.
**Command:** `/write-test`

1. Create or update a test file matching the pattern `*.test.ts`.
2. Write tests for your functions or modules.
3. Use named exports for any test utilities.
4. Run tests using the project's test runner (framework unknown).

## Testing Patterns

- Test files follow the pattern: `*.test.ts`
- The testing framework is not specified; check project documentation or package.json for details.
- Place tests alongside the modules they test or in a dedicated test directory.
- Example test file:
  ```typescript
  // dataFetcher.test.ts
  import { fetchData } from './dataFetcher';

  test('fetchData returns data', async () => {
    const data = await fetchData('https://example.com');
    expect(data).toBeDefined();
  });
  ```

## Commands
| Command       | Purpose                                  |
|---------------|------------------------------------------|
| /add-feature  | Start the workflow for adding a feature  |
| /fix-bug      | Start the workflow for fixing a bug      |
| /write-test   | Start the workflow for writing tests     |
```
