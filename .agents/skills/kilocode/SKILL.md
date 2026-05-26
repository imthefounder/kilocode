```markdown
# kilocode Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill covers the core development patterns and workflows used in the `kilocode` TypeScript codebase, which leverages the Hono framework. It outlines coding conventions, commit practices, documentation workflows, and testing patterns to help contributors maintain consistency and quality.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `aiProviderUtils.ts`

### Import Style
- Use **relative imports** for modules within the package.
  - Example:
    ```typescript
    import { getProviderConfig } from './providerConfig';
    ```

### Export Style
- Use **named exports** for all modules.
  - Example:
    ```typescript
    // providerConfig.ts
    export function getProviderConfig() { ... }
    export const PROVIDER_LIST = [...];
    ```

### Commit Patterns
- Mixed commit types, with common prefixes like `docs` and `release`.
- Commit messages are concise, averaging around 60 characters.
  - Example:
    ```
    docs(kilo-docs): add xAI provider documentation
    release: bump version to 1.2.0
    ```

## Workflows

### Update Provider Documentation
**Trigger:** When you need to document new features, changes, or instructions for an AI provider (e.g., xAI) in the `kilo-docs` package.  
**Command:** `/update-provider-docs`

1. Edit or create the relevant markdown file for the provider under `packages/kilo-docs/pages/ai-providers/`.
    - Example: `packages/kilo-docs/pages/ai-providers/xai.md`
2. Add or update documentation as needed.
3. Commit your changes with a message prefix:  
   ```
   docs(kilo-docs): [short description]
   ```
   Example:
   ```
   docs(kilo-docs): update xAI usage instructions
   ```
4. Open a pull request if required.

## Testing Patterns

- **Test files** use the pattern `*.test.*` (e.g., `providerUtils.test.ts`).
- **Testing framework** is not specified in the repository analysis.
- Place test files alongside the modules they test or in a dedicated `__tests__` directory.

  Example:
  ```
  // providerUtils.test.ts
  import { getProviderConfig } from './providerConfig';

  describe('getProviderConfig', () => {
    it('returns config for known provider', () => {
      // test implementation
    });
  });
  ```

## Commands

| Command                | Purpose                                                        |
|------------------------|----------------------------------------------------------------|
| /update-provider-docs  | Start the workflow to update or add AI provider documentation. |

```