# Code Review

Perform a thorough code review of the specified files or recent changes.

## Usage

```
/code/review [files or scope]
```

## What This Does

1. **Analyzes code quality** — checks for readability, maintainability, and consistency
2. **Identifies bugs** — looks for logic errors, edge cases, and potential runtime issues
3. **Security scan** — flags common vulnerabilities (injection, hardcoded secrets, unsafe ops)
4. **Performance hints** — notes obvious inefficiencies or anti-patterns
5. **Style compliance** — verifies adherence to project conventions

## Instructions

Review the following: $ARGUMENTS

If no arguments provided, review the diff of staged/unstaged changes (`git diff HEAD`).

Structure your review as:

### Summary
Brief overall assessment (1-3 sentences).

### Issues
List each issue with:
- **Severity**: `critical` | `major` | `minor` | `nit`
- **Location**: file and line number if applicable
- **Description**: what the problem is
- **Suggestion**: how to fix it

### Positives
Note what is done well — good patterns, clean logic, solid test coverage, etc.

### Action Items
Prioritized list of changes recommended before merging.

## Notes

- Focus on substance over style for `critical` and `major` issues
- Nits are optional suggestions, not blockers
- If reviewing a PR, consider the broader context of the feature
