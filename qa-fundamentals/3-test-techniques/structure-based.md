# Structure-Based Testing

## Overview

White-box testing techniques based on internal code structure. Also called
structural, glass-box, or code-based testing.

---

## 1. Statement Coverage

**What:** Execute every statement (line of code) at least once

**Formula:** `(Statements executed / Total statements) × 100%`

**Example:**

```java
if (age >= 18) {
    System.out.println("Adult");  // Statement 1
} else {
    System.out.println("Minor");  // Statement 2
}
```

**To achieve 100%:** Test both age ≥ 18 and age < 18

**Limitation:** Doesn't test all decision outcomes

---

## 2. Branch Coverage

**What:** Execute every decision path (both true and false branches)

**Also called:** Decision coverage

**Formula:** `(Decision outcomes covered / Total outcomes) × 100%`

**Example:**

```java
if (age >= 18 && hasLicense) {  // Two conditions
    System.out.println("Can drive");
}
```

**Branches:**

1. True, True → Can drive
2. True, False → Cannot drive
3. False, True → Cannot drive
4. False, False → Cannot drive

**Requirement:** Test all combinations

**Benefit:** Better than statement coverage; finds more defects

---

## 3. Path Coverage

**What:** Execute every possible path through the code

Most comprehensive but hardest to achieve.

**Example:**

```java
if (x > 0) {
    if (y > 0) {
        // Path 1
    } else {
        // Path 2
    }
} else {
    // Path 3
}
```

**Paths:** 3 different execution paths

**Limitation:** Exponential growth with nested conditions (infeasible for
complex code)

---

## Coverage Levels (in order)

| Level | Coverage | What | Finds |
| --- | --- | --- | --- |
| 1 | Statement | Every line | Basic issues |
| 2 | Branch | Every decision | More issues |
| 3 | Path | Every path | Most issues (rarely practical) |

---

## Code Complexity Analysis

**Cyclomatic Complexity:** Measures decision complexity

**Formula:** Complexity = (Decision points) + 1

**Example:**

```java
if (a) {           // +1
    if (b) {       // +1
        if (c) { } // +1
    }
}
// Complexity = 3 + 1 = 4
```

**Interpretation:**

- 1-4: Low complexity
- 5-7: Moderate complexity
- 8+: High complexity (hard to test, risky)

**Use for:** Identifying high-risk code that needs extra testing

---

## Coverage Tools

**Purpose:** Measure how much code is tested

**Popular Tools:**

- JaCoCo (Java)
- Coverage.py (Python)
- Istanbul (JavaScript)
- Cobertura (Java)
- OpenCover (.NET)

**Metrics:**

- Line coverage
- Branch coverage
- Method coverage
- Class coverage

---

## Realistic Coverage Goals

| Project Type | Target |
| --- | --- |
| Safety-critical | 80-100% |
| Enterprise | 70-80% |
| Standard | 60-75% |
| Startup/MVP | 40-60% |

**Reality:** 100% coverage ≠ Zero defects (ISTQB Principle 1)

---

## Remember

- **Statement:** Execute every line
- **Branch:** Execute every decision outcome
- **Path:** Execute every possible path
- Use appropriate coverage level for risk/context
- Coverage is a safety net, not a quality guarantee
