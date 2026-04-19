# Fix Command

Analyze and fix issues in the codebase based on provided context or error messages.

## Usage

```
/code/fix [error_or_issue_description]
```

## What This Command Does

1. **Analyzes** the provided error message or issue description
2. **Identifies** the root cause by examining relevant files
3. **Proposes** a fix with clear explanation
4. **Applies** the fix with minimal side effects
5. **Verifies** the fix doesn't break existing functionality

## Instructions

When this command is invoked:

1. Read the error message or issue description carefully
2. Search for the relevant files and code sections causing the issue
3. Understand the context — don't just patch symptoms, fix root causes
4. Before applying any fix:
   - Explain what the bug/issue is
   - Explain why your fix resolves it
   - Note any potential side effects
5. Apply the minimal change needed to resolve the issue
6. If tests exist for the affected code, run them to confirm the fix works
7. Suggest follow-up improvements if relevant (but don't apply them without asking)

## Arguments

- `$ARGUMENTS` — Error message, stack trace, issue description, or file path to investigate

## Example

```
/code/fix TypeError: Cannot read property 'map' of undefined in components/List.jsx
```

## Notes

- Prefer targeted fixes over large refactors
- If multiple fixes are possible, present options and ask which to apply
- Always preserve existing code style and conventions
- If the issue is ambiguous, ask clarifying questions before proceeding
