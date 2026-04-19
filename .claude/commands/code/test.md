# Generate Tests

Generate comprehensive tests for the specified code or current changes.

## Usage

```
/code/test [target] [options]
```

## Arguments

- `target` — File path, function name, or class to test (defaults to recent changes)
- `--type` — Test type: `unit`, `integration`, `e2e` (default: `unit`)
- `--framework` — Testing framework to use (auto-detected if not specified)
- `--coverage` — Include coverage hints and edge cases (default: true)

## What This Does

1. **Analyzes the target code** to understand its structure, inputs, and outputs
2. **Identifies edge cases** including boundary values, error conditions, and happy paths
3. **Generates test cases** using the project's existing test framework and conventions
4. **Adds fixtures/mocks** where external dependencies are present
5. **Follows project patterns** by examining existing test files for style consistency

## Instructions

Analyze the target code at `$ARGUMENTS` and generate tests following these steps:

1. Read the target file or function to understand what needs testing
2. Check existing test files in the project to match conventions (naming, structure, imports)
3. Identify the testing framework in use (pytest, jest, unittest, mocha, etc.)
4. Generate tests covering:
   - Happy path / expected behavior
   - Edge cases (empty inputs, boundary values, large inputs)
   - Error handling and exceptions
   - Any async behavior if applicable
5. Create or update the appropriate test file following the project's test file naming convention
6. Include clear test names that describe the behavior being tested
7. Add brief comments explaining non-obvious test logic

## Example Output

For a function `calculate_discount(price, percent)`, generate tests like:
- `test_calculate_discount_standard_case`
- `test_calculate_discount_zero_percent`
- `test_calculate_discount_full_discount`
- `test_calculate_discount_raises_on_negative_price`
- `test_calculate_discount_raises_on_percent_over_100`
