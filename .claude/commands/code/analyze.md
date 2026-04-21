# Code Analysis Command

Analyze the provided code or file(s) for quality, complexity, potential issues, and improvement opportunities.

## Usage

```
/code:analyze [file or code snippet]
```

## What This Command Does

Performs a comprehensive static analysis of the target code, covering:

1. **Complexity Analysis** — Identify overly complex functions, deep nesting, and high cyclomatic complexity
2. **Code Smells** — Detect common anti-patterns, duplicated logic, and poor naming conventions
3. **Dependency Review** — Highlight tight coupling, circular dependencies, or unnecessary imports
4. **Security Concerns** — Flag potential vulnerabilities (e.g., injection risks, insecure defaults, hardcoded secrets)
5. **Performance Hotspots** — Point out inefficient algorithms, unnecessary loops, or memory-heavy operations
6. **Maintainability Score** — Provide an overall assessment of how easy the code is to maintain and extend

## Output Format

Provide the analysis in the following structure:

### Summary
Brief overview of the code's purpose and overall quality rating (1–10).

### Issues Found
List each issue with:
- **Severity**: Critical / High / Medium / Low / Info
- **Location**: File name and line number(s) if applicable
- **Description**: Clear explanation of the problem
- **Suggestion**: Recommended fix or improvement

### Metrics
- Lines of code
- Number of functions/classes
- Average function length
- Estimated complexity level (Low / Medium / High)

### Recommendations
Prioritized list of the top improvements to make, ordered by impact.

## Example

```
/code:analyze src/utils/data_processor.py
```

## Notes

- For large files, focus on the most impactful issues rather than exhaustive line-by-line review
- Consider the language and framework context when evaluating patterns
- Avoid flagging intentional trade-offs without acknowledging the likely rationale
