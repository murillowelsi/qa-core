# Specification-Based Testing

## Overview

Black-box testing techniques based on requirements and specifications,
not code structure.

---

## 1. Equivalence Partitioning (EP)

**Idea:** Divide inputs into groups (partitions) where all values behave the same

**How:**

1. Identify input ranges
2. Divide into partitions
3. Test one value from each partition
4. Test invalid partitions

**Example:**

```text
Age field (valid: 18-65)
- Partition 1: <18 (invalid)
- Partition 2: 18-65 (valid)
- Partition 3: >65 (invalid)

Test cases: 17, 25, 70
```

**Benefit:** Covers many scenarios with few test cases

---

## 2. Boundary Value Analysis (BVA)

**Idea:** Defects cluster at boundaries of input ranges

**How:**

1. Identify boundaries
2. Test at boundaries
3. Test just inside and outside boundaries

**Example:**

```text
Age field (valid: 18-65)
Test: 17, 18, 19, 64, 65, 66
```

**Why it works:** Off-by-one errors, < vs ≤ operators are common

---

## 3. Decision Table Testing

**Idea:** Test all logical combinations of inputs and conditions

**How:**

1. Identify conditions and actions
2. Create table of combinations
3. Test each combination

**Example:**

```text
Conditions: Is logged in? Has credit?
Actions: Allow purchase, Deny purchase

| Logged In | Has Credit | Action |
|-----------|------------|--------|
| Yes       | Yes        | Allow  |
| Yes       | No         | Deny   |
| No        | Yes        | Deny   |
| No        | No         | Deny   |
```

**Best for:** Business rules with multiple conditions

---

## 4. State Transition Testing

**Idea:** Test transitions between system states

**How:**

1. Map all system states
2. Identify valid transitions
3. Test each transition
4. Test invalid transitions

**Example:**

```text
Order states: New → Processing → Shipped → Delivered

Test: New→Processing (valid), Processing→New (invalid)
```

**Use for:** Workflows, state machines, UI navigation

---

## 5. Use Case Testing

**Idea:** Test complete user workflows from start to finish

**How:**

1. Identify use cases
2. Define main flow and alternative flows
3. Test each flow end-to-end
4. Test exceptional scenarios

**Example:**

```text
Use Case: User Login
- Main flow: Enter credentials → System validates → Login successful
- Alternative: Forgotten password → Reset → Login
- Exception: Too many failed attempts → Account locked
```

**Focus:** Real user scenarios, business value

---

## Comparison

| Technique | Best For | Effort | Coverage |
| --- | --- | --- | --- |
| EP | Simple inputs | Low | Good |
| BVA | Numeric ranges | Low | Good |
| Decision Tables | Multiple conditions | Medium | Excellent |
| State Transitions | Workflows | Medium | Excellent |
| Use Cases | End-to-end flows | High | Excellent |

---

## Remember

- **EP:** Divide into groups
- **BVA:** Test boundaries
- **Decision Tables:** Test all combinations
- **State Transitions:** Test state changes
- **Use Cases:** Test real workflows
