# Test Estimation

## Overview

Estimating testing effort is critical for project planning, resource
allocation, and realistic scheduling.

---

## Estimation Challenges

- Unclear requirements
- Unknown complexity
- Unknowns (new technologies, risks)
- Evolving scope
- Team velocity variability

**Solution:** Use multiple estimation techniques and build in contingency (15-25%)

---

## 1. Expert Judgment

**Method:** Experienced tester estimates based on intuition

**How:**

- Review requirements
- Consider complexity
- Estimate hours for test execution
- Add overhead (design, setup, reporting)
- Add contingency

**Formula (Simple):**

```text
Total Effort = Design + Execution + Reporting + Contingency
            = 20% + 60% + 10% + 10% (of total hours)
```

**Example:**

```text
Web App Testing (200 requirements)
- Design: 20 hours
- Execution: 60 hours
- Reporting: 10 hours
- Contingency: 10 hours (10%)
Total: 100 hours (≈ 2 weeks, 1 tester)
```

**Pros:**

- Quick
- Uses real experience
- Flexible

**Cons:**

- Subjective
- Biased (overestimate or underestimate)
- Inconsistent across team members

---

## 2. Metrics-Based Estimation

**Method:** Use historical data and metrics

### Function Points Approach

1. Calculate function points from requirements
2. Use industry standard: 1 FP ≈ 2-3 hours testing
3. Multiply: Test Hours = FP × 2.5

**Example:**

```text
Application: 500 function points
Test Hours = 500 × 2.5 = 1,250 hours
Team: 5 testers, 2 weeks = 400 hours available
Estimated: 3+ sprints needed
```

### Requirement-Based Estimation

```text
Test Effort = # Requirements × Avg Hours per Requirement
           = 200 requirements × 3 hours
           = 600 hours
```

**Complexity Multiplier:**

```text
Simple requirement = 1 hour
Normal requirement = 3 hours
Complex requirement = 8 hours
Critical requirement = 12 hours
```

### Test Case-Based Estimation

```text
Total Effort = # Test Cases × Avg Hours per Case
            = 500 cases × 0.75 hours
            = 375 hours (test execution only)
            + Design overhead: 100 hours
            + Setup: 50 hours
            Total: 525 hours
```

**Pros:**

- Objective
- Repeatable
- Predictable

**Cons:**

- Requires historical data
- Accuracy depends on data quality
- Doesn't account for unknowns

---

## 3. Three-Point Estimation

**Method:** Estimate optimistic, realistic, and pessimistic scenarios

**Formula:**

```text
Expected Estimate = (Optimistic + 4×Realistic + Pessimistic) / 6
```

**Example:**

```text
Feature: User login
- Optimistic: 8 hours (simple, no surprises)
- Realistic: 12 hours (normal complexity)
- Pessimistic: 20 hours (complex, many edge cases)

Expected = (8 + 4×12 + 20) / 6 = (8 + 48 + 20) / 6 = 12.7 hours
```

**Benefit:** Accounts for uncertainty

---

## 4. Delphi Technique

**Method:** Anonymous expert consensus

**Process:**

1. Multiple experts estimate independently (no collaboration)
2. Estimates collected anonymously
3. Discuss differences
4. Re-estimate
5. Repeat until consensus reached

**Benefit:** Removes personality bias, leverages group knowledge

---

## Effort Estimation Factors

**What affects testing effort?**

### Increases Effort

- ✗ Unclear requirements
- ✗ New technology/tools
- ✗ Distributed team
- ✗ Complex business logic
- ✗ High integration needs
- ✗ Performance requirements
- ✗ Security concerns
- ✗ Tight schedule (increases rework)

### Decreases Effort

- ✓ Clear requirements
- ✓ Familiar technology
- ✓ Co-located team
- ✓ Simple features
- ✓ Reusable test cases
- ✓ Good automation tools
- ✓ Stable requirements
- ✓ Adequate time

---

## Estimation by Test Type

| Test Type | Effort |
| --- | --- |
| Unit testing | 5-10% of dev effort |
| Integration testing | 5-10% of dev effort |
| System testing | 10-15% of dev effort |
| UAT | 5-10% of dev effort |
| Regression | 20-30% of development (ongoing) |
| **Total Testing** | **45-75% of total project effort** |

---

## Estimation Template

```text
Project: [Name]
Date: [Date]

EFFORT BREAKDOWN:

- Test Planning: __ hours
- Test Design: __ hours
- Test Setup: __ hours
- Test Execution: __ hours
- Defect Reporting: __ hours
- Regression Testing: __ hours
- Reporting & Closure: __ hours

Subtotal: __ hours
Contingency (20%): __ hours
TOTAL: __ hours

Resources: __ testers × __ weeks
Cost: __ × $__ per hour = $__
```

---

## Estimation Reality Check

**Ask yourself:**

- Is this consistent with past projects?
- Does the team agree?
- Are all activities included?
- Is contingency realistic?
- Can we deliver in the allocated time?

**Red flags:**

- Estimate too low (schedule risk)
- Estimate too high (credibility issue)
- No contingency (asking for trouble)
- Pressure to reduce estimate (scope creep)

---

## Remember

- Estimation is **not exact science**—build in buffer
- Use **multiple techniques**—compare results
- **Track actuals**—improve future estimates
- **Communicate assumptions**—manage expectations
- **Estimate effort, not calendar time**—account for interruptions
