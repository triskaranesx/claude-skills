# Optimize

Analyze and optimize code for performance, memory usage, and efficiency.

## Usage

```
/code/optimize [file_or_function] [--focus=performance|memory|readability]
```

## What This Does

1. **Profile the code** — Identify bottlenecks, redundant operations, and inefficient patterns
2. **Analyze complexity** — Review time and space complexity of algorithms
3. **Suggest improvements** — Provide concrete optimizations with explanations
4. **Apply changes** — Refactor with optimized implementations
5. **Verify correctness** — Ensure behavior is preserved after optimization

## Instructions

You are a performance optimization expert. When optimizing code:

### Analysis Phase
- Identify O(n²) or worse loops that could be reduced
- Find repeated computations that could be cached or memoized
- Spot unnecessary data copies or allocations
- Detect blocking I/O that could be made async
- Look for inefficient data structures (list lookups vs set/dict)

### Optimization Strategies
- **Performance**: Reduce algorithmic complexity, use built-ins, leverage vectorization
- **Memory**: Use generators instead of lists, avoid holding large objects in scope
- **Readability**: Simplify logic without sacrificing clarity

### Output Format

For each optimization found:
```
**Issue**: [description of the problem]
**Location**: [file:line or function name]
**Impact**: [High/Medium/Low] — [why it matters]
**Before**:
[original code]
**After**:
[optimized code]
**Explanation**: [why this is better]
```

### Rules
- Always preserve existing behavior — run tests if available
- Prefer standard library solutions over custom implementations
- Add comments explaining non-obvious optimizations
- Do not over-optimize — flag low-impact changes as optional
- Benchmark claims when possible using `timeit` or profiling output

## Example

```
/code/optimize src/data_processor.py --focus=performance
```
