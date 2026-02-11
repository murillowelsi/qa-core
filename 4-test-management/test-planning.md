# Test Planning

## Overview

Test planning defines the testing strategy, scope, approach, and
resources needed for a project.

---

## Test Plan Contents

### 1. Test Objectives

- What are we testing?
- Why are we testing it?
- What do we want to achieve?

**Example:**

- Verify system meets functional requirements
- Verify performance meets SLA (< 2 second response)
- Verify security standards are met

### 2. Test Scope

- **In-Scope:** What will be tested
- **Out-of-Scope:** What won't be tested (and why)

**Example - In Scope:**

- Login functionality
- User profile management
- Payment processing

**Example - Out-of-Scope:**

- Third-party library internals
- Hardware drivers
- Legacy integration modules

### 3. Test Strategy

**What approach will you use?**

**Common Strategies:**

**Risk-Based:** Focus on high-risk areas first

- Analyze risks
- Allocate more tests to high-risk
- Test lower risks if time permits

**Requirements-Based:** Test all requirements equally

- Map tests to requirements
- Ensure each requirement tested
- Good for safety-critical systems

**Regression-Based:** Prevent breaking existing features

- Automate regression tests
- Run after every change
- Good for maintenance phases

**Exploratory:** Dynamically test while learning

- Tester discovers behavior
- Tests designed during execution
- Good for unclear requirements

### 4. Test Approach

**How will tests be conducted?**

**Manual Testing:**

- Pros: Flexible, human intuition
- Cons: Slow, inconsistent, human error
- Use for: UI/UX, exploratory

**Automated Testing:**

- Pros: Fast, repeatable, consistent
- Cons: Setup time, maintenance, brittleness
- Use for: Regression, smoke tests, data validation

**Combination:** Manual + automation (most realistic)

### 5. Entry & Exit Criteria

**Entry Criteria** (before testing starts):

- Requirements finalized and approved
- Build available and testable
- Test environment ready
- Test cases written and reviewed

**Exit Criteria** (before release):

- All planned tests executed
- Defects logged and triaged
- Critical/high defects fixed and verified
- Test report generated
- Stakeholders approve

---

## Test Schedule

**When will testing occur?**

| Phase | Duration | Team | Deliverable |
| --- | --- | --- | --- |
| Planning | Week 1 | Lead | Test plan |
| Design | Week 2-3 | Testers | Test cases |
| Execution | Week 4-6 | Testers | Defect reports |
| Closure | Week 7 | Lead | Test report |

**Critical Path:** Identify dependencies and risks to schedule

---

## Resource Allocation

**What resources are needed?**

### People

- QA Lead/Manager
- Test Engineers (automation, manual)
- Test Data Specialist
- Performance Tester
- Security Tester

### Environment & Tools

- Test environment (≈ production)
- Test data
- Test management tool (TestRail, Zephyr)
- Automation framework
- CI/CD pipeline
- Monitoring tools

### Budget & Timeline

- Total effort (hours/days)
- Tools licensing
- Training needs
- Contingency buffer

---

## Test Effort Estimation

**How to estimate?**

### Methods

**Historical Data:**

- Use past project data
- Adjust for project size and complexity
- Most accurate if similar projects exist

**Expert Judgment:**

- Experienced tester estimates
- Factor in unknowns (30% buffer)
- Useful for new types of projects

**Parametric:**

- Function points → estimate hours
- Size of system × complexity factor
- More scientific but requires data

**Bottom-Up:**

- Estimate each test case
- Sum to total effort
- More accurate but time-consuming

**Formula (Rough):**

```text
Test Effort = (# Requirements × Complexity Factor × 2 hours)
              + (Automation Setup: 40 hours)
              + (Contingency: 20%)
```

---

## Risk-Based Testing Approach

**Prioritize high-risk areas:**

1. **Identify Risks**

   - What could go wrong?
   - What's the impact?
   - What's the likelihood?

2. **Calculate Risk Level**

   ```text
   Risk = Likelihood × Impact
   ```

3. **Allocate Testing**

   ```text
   Critical Risk → 30% of testing effort
   High Risk → 40% of testing effort
   Medium Risk → 20% of testing effort
   Low Risk → 10% of testing effort
   ```

4. **Test Critical Areas First**

---

## Test Plan Approval

**Who approves?**

- Project Manager
- Development Lead
- Product Owner
- QA Manager

**Questions they'll ask:**

- Is testing scope adequate?
- Are resources sufficient?
- Is schedule realistic?
- Are risks addressed?

---

## Remember

Invest time in planning. A good test plan:

- Prevents surprises later
- Allocates resources efficiently
- Sets clear expectations
- Reduces rework
