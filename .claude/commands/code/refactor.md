# Refactor Code

Analyze and refactor the specified code for improved readability, maintainability, and performance.

## Usage

```
/code/refactor [file or code snippet] [--focus=readability|performance|structure]
```

## Instructions

You are an expert software engineer performing a code refactoring task. Follow these steps:

### 1. Analyze Current Code
- Identify code smells (long methods, duplicate code, complex conditionals)
- Spot violations of SOLID principles
- Note any performance bottlenecks or anti-patterns
- Check naming conventions and clarity

### 2. Plan Refactoring
- List specific changes to be made
- Prioritize by impact (high/medium/low)
- Ensure behavior is preserved — refactoring must not change functionality

### 3. Apply Refactoring
Apply improvements based on focus area:

**Readability:**
- Rename variables/functions to be descriptive and intention-revealing
- Break down long functions into smaller, single-purpose ones
- Simplify complex conditionals with early returns or guard clauses
- Add or improve inline comments where logic is non-obvious

**Performance:**
- Replace inefficient loops or data structures
- Eliminate redundant computations or repeated lookups
- Apply caching where appropriate
- Use built-in language features over manual implementations

**Structure:**
- Apply appropriate design patterns
- Separate concerns into distinct modules or classes
- Reduce coupling and increase cohesion
- Consolidate duplicate logic into shared utilities

### 4. Output Format

Provide:
1. **Summary** of what was changed and why
2. **Refactored code** with inline comments on key changes
3. **Before/After comparison** for significant changes
4. **Risks or caveats** — anything that needs manual review or testing

### 5. Verification Checklist
- [ ] All existing tests still pass
- [ ] No behavior changes introduced
- [ ] Code is more readable or performant than before
- [ ] No new dependencies added without justification
