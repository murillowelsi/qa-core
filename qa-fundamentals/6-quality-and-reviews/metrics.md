# Testing Metrics

## Overview

Metrics measure testing progress, quality, and effectiveness. Data-driven
decisions require meaningful metrics.

---

## Core Metrics

### 1. Test Coverage

**What:** How much of the system have we tested?

**Types:**

### Requirements Coverage

```text
Formula: (Requirements tested / Total requirements) × 100%
Example: 190 tested / 200 total = 95% coverage
Interpretation: All critical requirements tested
```

### Code Coverage

```text
Formula: (Code executed / Total code) × 100%
Example: 8,000 lines executed / 10,000 total = 80%
Limitation: 100% coverage ≠ No defects (ISTQB Principle 7)
```

### Feature Coverage

```text
Formula: (Features tested / Total features) × 100%
Example: 25 tested / 30 total = 83%
```

### Risk Area Coverage

```text
Formula: (Critical areas tested / Total critical areas) × 100%
Most important: Focus on high-risk areas
```

### 2. Test Execution Progress

**What:** Are we on track with testing?

```text
Metrics:
- Tests planned: 200
- Tests executed: 150 (75%)
- Tests passed: 145 (96.7% of executed)
- Tests failed: 5 (3.3% of executed)
- Tests blocked: 0

Status: On track (50% of timeline passed, 75% of tests done)
```

### 3. Defect Metrics

**What:** How many defects are we finding?

#### Defects Found

```text
Total: 45 defects
- Critical: 2
- High: 8
- Medium: 20
- Low: 15
```

#### Defect Density

```text
Formula: (Defects found / KLOC) or (Defects / Requirements)
Example: 45 defects / 10,000 lines = 4.5 defects per KLOC
```

#### Defect Status

```text

- New: 3 (not yet assigned)
- Assigned: 5 (to developer)
- Fixed: 25 (fix completed)
- Verified: 10 (tester confirmed fix)
- Closed: 2 (complete)
```

#### Defect Severity Distribution

```text
Critical: 4% (2 of 45) - System broken
High: 18% (8 of 45) - Major feature broken
Medium: 44% (20 of 45) - Feature incomplete
Low: 33% (15 of 45) - Cosmetic/minor
```

### 4. Defect Detection Effectiveness

**What:** Are we good at finding defects?

```text
Defects found in review: 20
Defects found in testing: 15
Defects escaping to production: 2
Total defects: 37

Detection rate: (20 + 15) / 37 = 95% (excellent)
Escape rate: 2 / 37 = 5% (low, good)
```

### 5. Defect Resolution Time

**What:** How fast do developers fix defects?

```text
Average time to fix: 2 days
- Critical defects: < 4 hours
- High defects: < 1 day
- Medium defects: 2 days
- Low defects: 5 days (lower priority)

Target: Critical fixed within 4 hours
Status: On track
```

---

## Quality Indicators

### Code Quality Metrics

#### Complexity

```text
Cyclomatic Complexity (per module):

- Low (< 5): 40% of modules - Good
- Moderate (5-10): 45% of modules - Acceptable
- High (10-15): 10% of modules - Risky
- Very High (> 15): 5% of modules - Refactor needed
```

#### Maintainability

```text
Duplicated Code: 8% (should be < 5%)
Code Violations: 12 (should be 0)
Technical Debt: High (needs attention)
```

#### Test Quality

```text
Test Coverage: 82%
Test Effectiveness: 92% (finds issues that matter)
Test Reliability: 98% (minimal flaky tests)
```

### Process Quality

#### Requirements Quality

```text
Ambiguous requirements: 5% (ideally < 2%)
Missing acceptance criteria: 8%
Requirement changes: 3 mid-project (track scope creep)
```

#### Design Quality

```text
Design reviews completed: 100%
Design defects found: 12 (fixed before coding)
```

---

## Productivity Metrics

### Testing Throughput

```text
Tests created per day: 15 tests/day
Tests executed per day: 40 tests/day
Defects reported per day: 3-5 defects/day
```

### Effort Metrics

```text
Test execution time: 0.5 hours per test
Automation setup: 2 hours per test (initial)
Automation maintenance: 0.2 hours per test (per release)
```

### Team Velocity

```text
Weekly throughput:
- Week 1: 150 tests designed
- Week 2: 180 tests executed, 15 defects found
- Week 3: 200 tests executed, 12 defects found
- Week 4: 160 tests executed, 8 defects found

Trend: Velocity steady (good coverage), fewer defects (reaching saturation)
```

---

## Trend Analysis

### Defect Trend

```text
Daily defects found:
Day 1-5: 5 defects/day (ramping up)
Day 6-10: 8 defects/day (peak, testing intensive)
Day 11-15: 5 defects/day (declining, getting found)
Day 16-20: 2 defects/day (reaching saturation, fewer issues remain)

Interpretation: Healthy trend, system stabilizing
```

### Test Execution Progress

```text
Test execution:
End of Week 1: 25% complete (on track)
End of Week 2: 55% complete (ahead, good pace)
End of Week 3: 80% complete (on track)
End of Week 4: 100% complete (ready for release)
```

### Quality Trend

```text
Defect escape rate:
Release 1: 8% (some defects reached production)
Release 2: 4% (improvement)
Release 3: 2% (much better)

Goal: < 1%
Status: Close, improving
```

---

## Metrics Dashboard Template

```text
PROJECT HEALTH DASHBOARD

TEST EXECUTION

- Total Tests: 200
- Executed: 160 (80%)
- Passed: 155 (96.9%)
- Failed: 5 (3.1%)
- Status: ✅ ON TRACK

COVERAGE

- Requirements: 95%
- Code: 82%
- Risk Areas: 100%
- Status: ✅ ACCEPTABLE

DEFECTS

- Total Found: 45
- Fixed: 35
- Verified: 8
- Open: 2
- Critical: 0 (closed)
- High: 2 (in progress)
- Status: ✅ MANAGEABLE

QUALITY

- Escape Rate: 3%
- Detection Rate: 97%
- Severity Trend: ↓ Improving
- Status: ✅ GOOD

SCHEDULE

- Timeline: 4 weeks total
- Elapsed: 3 weeks
- Progress: 85%
- Status: ✅ ON TRACK

OVERALL

- Go/No-Go: GO
- Risks: Low
- Confidence: High
```

---

## Good Metrics vs Bad Metrics

### Good Metrics ✅

- **Actionable** - Data drives decisions
- **Objective** - Measurable, not opinions
- **Relevant** - Matters for the project
- **Comparable** - Can track trends
- **Timely** - Available when needed

### Bad Metrics ❌

- **Vanity metrics** - Look good but mean nothing (e.g., high coverage
with flaky tests)
- **Misleading** - Tell wrong story (high pass rate with lots of skipped tests)
- **Costly** - Effort to collect > value gained
- **Gamed** - Easy to manipulate ("pass tests at any cost")

---

## Common Metric Pitfalls

❌ **100% coverage = Quality**

- Reality: Defect could still exist (ISTQB Principle 7)
- ✅ Target: 75-85% coverage is realistic and useful

❌ **More tests = Better quality**

- Reality: 10 good tests > 100 bad tests
- ✅ Focus: Quality of tests, not quantity

❌ **Zero defects = Success**

- Reality: No testing was done, or tests are inadequate
- ✅ Perspective: Find issues while you can fix them

❌ **Defects per test ratio**

- Reality: Different tests find different issues
- ✅ Use: Defects per feature, per module, per requirement

---

## Remember

- **Metrics inform decisions**—use data, not gut feel
- **Focus on quality metrics**—coverage alone is misleading
- **Track trends**—a single number means little
- **Actionable metrics**—only measure what you'll act on
- **Balance quantitative and qualitative**—numbers don't tell whole story
