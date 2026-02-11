# Monitoring and Control

## Overview

Monitoring tracks testing progress; Control takes corrective action when needed.

---

## Key Metrics to Track

### 1. Test Execution Progress

**What:** How many tests have we run?

**Metrics:**

- Tests planned
- Tests executed
- Tests passed
- Tests failed
- Tests blocked/skipped

**Dashboard:**

```text
Progress: 150 of 200 tests executed (75%)
- Passed: 145 (96.7%)
- Failed: 5 (3.3%)
- Blocked: 0
On track for completion
```

### 2. Defect Metrics

**What:** How many defects are we finding?

**Key Numbers:**

- Total defects found
- Defects by severity (critical, high, medium, low)
- Defects by status (new, assigned, fixed, verified, closed)
- Defects found vs fixed
- Defect escape rate (defects that reach production)

**Example Dashboard:**

```text
Defects: 47 total
- Critical: 2 (still open)
- High: 8 (6 fixed, 2 in progress)
- Medium: 18 (15 fixed, 3 in progress)
- Low: 19 (12 fixed, 7 deferred)

Trend: Finding fewer defects (sign of maturity or coverage saturation?)
```

### 3. Test Coverage

**What:** Have we tested everything?

**Metrics:**

- Requirements coverage (# requirements tested / total)
- Code coverage (% of code executed)
- Feature coverage (# features tested)
- Risk coverage (% of high-risk areas tested)

**Example:**

```text
Coverage:
- Requirements: 95% (190 of 200 requirements tested)
- Code: 82% (statement coverage)
- Features: 100%
- High-risk areas: 100%
```

### 4. Quality Trends

**What:** Is quality improving or declining?

**Metrics:**

- Defect detection rate (defects found per day)
- Defect density (defects per KLOC or per requirement)
- Test effectiveness (defects found in test vs production)
- Mean time to fix (average time to resolve defect)

---

## Monitoring Reports

### Daily Status

**Frequency:** End of each day

**Content:**

- Tests executed today
- Defects found/fixed
- Blockers/issues
- Tomorrow's plan

**Example:**

```text
Daily Report - March 15

Executed: 15 tests

- Passed: 14
- Failed: 1

Defects: 2 found, 1 fixed, 0 closed

Blocker: Database permissions issue (assigned to IT)

Tomorrow: Continue payment module testing
```

### Weekly Summary

**Frequency:** End of each week

**Content:**

- Tests executed (total, passed, failed)
- Defects (found, fixed, closed by severity)
- Coverage achieved
- Risks remaining
- Schedule status (on track, at risk, delayed)
- Issues and blockers

### Milestone Report

**When:** End of test phase

**Content:**

- Total tests executed
- Pass/fail breakdown
- Critical/high defects remaining
- Coverage metrics
- Risks and concerns
- Release recommendation (go/no-go)

---

## Test Control Actions

### When Progress is Behind

**Symptoms:**

- Less than 70% of tests executed by midpoint
- High number of blocked tests
- Test environment unavailable

**Actions:**

- Add more testers or extended hours
- Prioritize critical tests only (reduce scope)
- Fix blockers (environment, data, requirements)
- Report realistic revised schedule

### When Defect Rate is High

**Symptoms:**

- Defect found per test ratio > 5%
- Critical/high defects still being found late
- Trend shows no improvement

**Actions:**

- Allocate more testing time
- Focus on root causes (requirements? design?)
- Increase regression testing
- Recommend code review or refactoring
- Consider schedule extension

### When Coverage is Inadequate

**Symptoms:**

- Code coverage below target
- Risk areas untested
- Requirements gaps

**Actions:**

- Write more tests for uncovered areas
- Focus on high-risk areas
- Test unexplored code paths
- Add edge case and boundary tests
- Extend timeline if needed

### When Schedule is Threatened

**Symptoms:**

- 50% of schedule used, 20% of testing done
- Blockers preventing progress
- Resource constraints

**Actions:**

- Escalate issues to management
- Request more resources
- Reduce scope (defer low-risk items)
- Increase parallelization
- Focus on high-risk areas only

---

## Defect Management

### Defect Life Cycle

```text
New → Assigned → Fixed → Retested → Verified → Closed
      ↓ (Priority assessment)
      → Deferred (for later release)
      → Not a Defect (invalid)
      → Won't Fix (accepted risk)
```

### Severity Levels

| Severity | Impact | Example |
| --- | --- | --- |
| **Critical** | System unusable, data loss | Login doesn't work at all |
| **High** | Major feature broken | Payment fails 50% of time |
| **Medium** | Feature works but incomplete | Report missing one column |
| **Low** | Minor issue, cosmetic | Button text misaligned |

### Priority Levels

| Priority | Timeline | Example |
| --- | --- | --- |
| **Urgent** | Fix immediately | Security vulnerability |
| **High** | Fix before release | Customer-facing defect |
| **Medium** | Fix in reasonable time | Internal tool defect |
| **Low** | Fix when convenient | Nice-to-have improvement |

**Note:** Severity ≠ Priority (critical bug might be low priority if
workaround exists)

---

## Metrics Dashboard Template

```text
TEST EXECUTION STATUS
- Planned: 200 tests
- Executed: 150 (75%)
- Passed: 145 (96.7%)
- Failed: 5 (3.3%)

DEFECT STATUS

- Total Found: 47
- Fixed: 35
- In Progress: 8
- Deferred: 4
- Critical: 2 (both active)

COVERAGE

- Requirements: 95%
- Code: 82%
- Risk Areas: 100%

SCHEDULE

- Original: 4 weeks
- Actual: 2.5 weeks
- Status: ON TRACK

GO/NO-GO ASSESSMENT

- Remaining Risks: Low
- Recommendation: READY TO RELEASE
```

---

## Remember

- **Monitor continuously**—don't wait for surprises
- **Track metrics**—data drives decisions
- **Control proactively**—act before it's too late
- **Communicate openly**—share good news and bad
- **Adjust course**—adapt to reality, not the plan
