# Test Life Cycle (STLC)

## Overview

The Software Testing Lifecycle (STLC) parallels the Software Development
Lifecycle (SDLC) with planned testing activities at each phase.

---

## 7 STLC Phases

### 1. Planning & Analysis

**When:** Project kickoff, requirements review

**Activities:**

- Identify testing scope and objectives
- Analyze requirements for testability
- Assess risks and prioritize testing
- Estimate resources and timeline
- Define entry/exit criteria

**Output:** Test plan, risk assessment

---

### 2. Test Design

**When:** Requirements/design phase

**Activities:**

- Create test cases from requirements
- Design test data
- Plan test scenarios
- Define expected results
- Prepare test environment specifications

**Output:** Test cases, test data, test scenarios

**Key Principle:** Design tests before coding (ISTQB Principle 3: Early Testing)

---

### 3. Test Environment Setup

**When:** Before test execution

**Activities:**

- Set up test infrastructure
- Install software under test
- Configure databases
- Install test tools
- Verify environment readiness

**Criteria:** Environment matches production (minus scale)

---

### 4. Test Execution

**When:** After build/deployment ready

**Activities:**

- Execute planned test cases
- Log results (pass/fail)
- Report defects found
- Retest after defect fixes
- Track test coverage

**Tracking:**

- Tests executed vs planned
- Pass/fail ratio
- Defects found
- Risks remaining

---

### 5. Defect Reporting & Closure

**When:** Throughout execution

**Activities:**

- Capture defect details (steps, environment, severity)
- Track defect status (new → assigned → fixed → verified → closed)
- Manage severity levels
- Verify fixes with regression testing
- Root cause analysis for critical defects

**Severity Levels:**

- **Critical:** System unusable, data loss
- **High:** Major functionality broken
- **Medium:** Feature doesn't work but workaround exists
- **Low:** Minor issue, cosmetic

---

### 6. Test Closure

**When:** Testing phase complete

**Activities:**

- Analyze test execution summary
- Generate test report
- Document lessons learned
- Archive test artifacts
- Assess readiness for release

**Report Includes:**

- Tests executed/passed/failed
- Defects by severity
- Coverage achieved
- Risks remaining
- Recommendation (go/no-go)

---

### 7. Post-Release

**When:** After production deployment

**Activities:**

- Monitor production issues
- Support user queries
- Log production defects
- Gather feedback for next release
- Document lessons learned

---

## STLC vs SDLC Alignment

| SDLC Phase | STLC Phase | Testing Activity |
| --- | --- | --- |
| Requirements | Planning & Design | Test planning, test case design |
| Design | Test Design | Test scenario design, test data prep |
| Development | Environment Setup | Environment setup, test readiness |
| Testing | Execution | Test execution, defect reporting |
| Deployment | Closure | Release readiness, go/no-go |
| Support | Post-Release | Defect monitoring, feedback |

---

## Entry & Exit Criteria

### Entry Criteria (before testing starts)

- Requirements documented and approved
- Test cases prepared and reviewed
- Test environment ready
- Build available

### Exit Criteria (before release)

- All planned tests executed
- High-severity defects fixed and verified
- Test coverage acceptable
- Risk assessment acceptable

---

## Remember

Testing is not a single event—it's a continuous lifecycle parallel to
development. The earlier you start testing (Principle 3), the cheaper
