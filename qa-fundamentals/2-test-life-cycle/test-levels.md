# Test Levels

## Overview

Testing occurs at different levels throughout the software development
lifecycle. Each level has specific objectives and scope.

---

## 1. Unit Testing

**Focus:** Individual components (functions, methods, classes)

**Who:** Developers

**Objective:** Verify that code works as designed

**Scope:** Single unit in isolation

**Techniques:**

- White-box testing
- Test-driven development (TDD)
- Code coverage (line, branch, path)

**Benefits:**

- Catch defects early (cheapest phase)
- Document code behavior
- Enable refactoring safely

---

## 2. Integration Testing

**Focus:** Interactions between components/modules

**Who:** Developers or QA

**Objective:** Verify components work together correctly

**Scope:** Multiple components, not the full system

**Approaches:**

- Bottom-up (components → modules)
- Top-down (high-level → components)
- Big bang (all together)
- Incremental (group by group)

**Typical Issues Found:**

- Interface mismatches
- Data flow problems
- Incorrect assumptions between components

---

## 3. System Testing

**Focus:** Complete, integrated system

**Who:** QA/Testing team

**Objective:** Verify end-to-end functionality against requirements

**Scope:** Entire system as a whole

**Tests:**

- Functional requirements
- Non-functional requirements (performance, security, usability)
- System workflows
- Error handling

**Environment:** Test environment matching production

---

## 4. Acceptance Testing

**Focus:** Does the system meet user/business requirements?

**Who:** Business users, customers, product owners

**Objective:** Verify system is fit for business purpose

**Types:**

- **User Acceptance Testing (UAT)** - Business users test real workflows
- **Operational Acceptance Testing (OAT)** - Operations team tests
  deployability
- **Compliance Acceptance Testing** - Verify regulatory/legal requirements

**Outcome:** Go/no-go decision for production release

---

## Test Level Pyramid

```text
        Acceptance
       System
      Integration
     Unit
```

**Principle:** More tests at lower levels (cheaper to fix), fewer at
higher levels (more expensive).

---

## Key Differences

| Level | Scale | Who | Cost | Speed |
| --- | --- | --- | --- | --- |
| Unit | Single unit | Dev | Cheapest | Fastest |
| Integration | Components | Dev/QA | Medium | Medium |
| System | Whole system | QA | Higher | Slower |
| Acceptance | Business needs | Users | Highest | Slowest |

---

## Remember

- **Unit tests** catch bugs early
- **Integration tests** find interaction issues
- **System tests** verify complete functionality
- **Acceptance tests** confirm business value
