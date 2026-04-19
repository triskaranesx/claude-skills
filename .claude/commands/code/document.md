# Document Code

Generate comprehensive documentation for the specified code, file, or module.

## Usage

```
/code:document [target]
```

## What This Does

This command analyzes the target code and generates:

1. **Module/File docstrings** — High-level description of purpose and responsibilities
2. **Function/Method docstrings** — Parameters, return values, exceptions, and usage examples
3. **Class docstrings** — Class purpose, attributes, and usage patterns
4. **Inline comments** — Clarify complex logic, non-obvious decisions, and edge cases
5. **Type annotations** — Add missing type hints where appropriate

## Process

1. Read and understand the target file(s) or code block
2. Identify all public and private interfaces
3. Detect existing documentation and preserve intent
4. Generate missing docstrings following the project's docstring style (Google, NumPy, or reStructuredText)
5. Add inline comments for complex logic sections
6. Ensure examples in docstrings are accurate and runnable

## Guidelines

- **Do not change logic** — Only add or update documentation
- **Match existing style** — Use the same docstring format already present in the project
- **Be concise but complete** — Avoid redundant comments that restate obvious code
- **Document why, not just what** — Explain intent and reasoning for non-obvious decisions
- **Include edge cases** — Note boundary conditions, None handling, and error scenarios

## Output

Show a diff of all documentation changes before applying them. Ask for confirmation if changes are extensive.
