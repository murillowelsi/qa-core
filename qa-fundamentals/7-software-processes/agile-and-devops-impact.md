# Agile and DevOps Impact on Testing

## Overview

Agile and DevOps fundamentally change how testing is done: from
end-of-project to continuous throughout.

---

## Testing in Agile

### Agile Principles

- Iterative development (1-2 week sprints)
- Working software every sprint
- Embrace change
- Continuous feedback

### Testing Changes

**Before Agile (Waterfall):**

- Test phase at end (2-3 months)
- Separate QA team
- Testing by test plan
- Defects found late

**In Agile:**

- Test during sprint (continuous)
- QA embedded in team
- Testing by acceptance criteria
- Defects found immediately

### Agile Testing Activities

**In Each Sprint:**

1. **Acceptance Criteria Definition**
   - Team writes criteria with product owner
   - Tests are designed from criteria
   - "Definition of done" includes testing

2. **Test-Driven Development (TDD)**
   - Write test BEFORE code
   - Code written to pass test
   - Reduces defects upfront

3. **Pair Testing**
   - Developer + Tester work together
   - Knowledge sharing
   - Faster feedback

4. **Automated Testing**
   - Unit tests (developer responsibility)
   - Integration tests (QA automation)
   - Regression tests (automated)

5. **Sprint Testing**
   - Test as developed (not at end)
   - Daily standup on testing progress
   - Defects fixed same sprint

### Sprint Testing Timeline

```text
Day 1-2: Design & code
    ↓ Testing runs immediately
Day 2-4: Code & test
    ↓ Continuous integration
Day 4-5: Final regression & demo
    ↓ Ready to release
Sprint End: Potentially shippable product
```

### Challenges in Agile Testing

❌ **Speed:** Pace is fast, testing must keep up

- Solution: Heavy automation, prioritize high-risk tests

❌ **Scope Creep:** Requirements change mid-sprint

- Solution: Limit work-in-progress, clear definition of done

❌ **Technical Debt:** Quick code, less coverage

- Solution: Unit tests required, automation discipline

❌ **Distributed Teams:** Communication harder

- Solution: Daily standups, clear documentation

---

## Shift-Left Testing

### Concept

Move testing **earlier** in development lifecycle.

**Traditional (Testing Late):**

```text
Requirements → Design → Code → Test → Deploy
                               ↑
                           Testing Here
```

**Shift-Left (Testing Early):**

```text
Requirements → Design → Code → Test → Deploy
    ↑         ↑       ↑
Testing Here (Throughout)
```

### Shift-Left Activities

#### Requirements Phase

- Review requirements for testability
- Identify test scenarios early
- Ask "How will we test this?"

#### Design Phase

- Design tests from requirements
- Identify integration points
- Plan test data needs

#### Development Phase

- Developers write unit tests (TDD)
- Continuous testing in pipeline
- Fix defects immediately

**Benefits:**

- Defects found earlier (cheaper to fix)
- Prevents building on bad foundations
- Aligns with ISTQB Principle 3

---

## Continuous Testing

### What is Continuous Testing

Testing is **continuous**, not a phase.

### Continuous Testing Pipeline

```text
Developer Commits Code
    ↓
Automated Build
    ↓
Unit Tests (1-5 min)
    ↓
Integration Tests (5-10 min)
    ↓
Functional Tests (10-20 min)
    ↓
Security Tests (5 min)
    ↓
Performance Tests (5 min)
    ↓
If All Pass: Can Deploy
    ↓
Manual Acceptance Testing (if needed)
    ↓
Deploy to Production
    ↓
Production Monitoring
```

### Continuous Testing Principles

#### Fast Feedback

- Tests run in minutes, not hours
- Developers know status immediately
- Failures fixed before moving on

#### Automation Critical

- Manual testing can't keep up
- Must automate regression tests
- Infrastructure as code for test environments

#### Quality Gates

- Failing tests block deployment
- Code won't merge if tests fail
- Prevents bad code from propagating

#### Metrics-Driven

- Track test execution time
- Monitor failure trends
- Dashboard shows pipeline health

---

## Test Automation in CI/CD

### CI/CD Pipeline

**CI (Continuous Integration):**

- Code committed multiple times/day
- Automated build on each commit
- Automated tests run immediately
- Fast feedback (pass/fail in minutes)

**CD (Continuous Deployment):**

- Passing tests automatically deploy
- Multiple releases per day
- Feature flags for safe rollout
- Production monitoring critical

### Testing in CI/CD

#### Level 1: Unit Tests (Fastest)

```text
- Run in seconds
- Test individual functions
- Usually written by developers
- 100s or 1000s of tests
- Must be reliable
```

#### Level 2: Integration Tests (Medium)

```text
- Run in minutes
- Test component interactions
- Usually automated
- 10s or 100s of tests
- Need test data
```

#### Level 3: Functional Tests (Slower)

```text
- Run in 10-20 minutes
- Test features end-to-end
- Automated or manual
- 10s of tests
- Most brittle
```

#### Level 4: Performance Tests (Optional)

```text

- Run every release or less frequent
- Load/stress testing
- Can be expensive
- Identify bottlenecks
```

### Pipeline Strategy

**Fast Feedback (< 10 min):**

- Unit tests (must pass)
- Quick integration tests
- Critical path tests only

**Thorough Testing (10-30 min):**

- All automated tests
- Security scanning
- Performance benchmarks

**Final Verification (30 min - 2 hours):**

- Exploratory testing (if time)
- Manual acceptance testing
- Production readiness sign-off

---

## Quality in DevOps

### Shift-Right Testing

Testing doesn't stop at deployment.

**Production Monitoring:**

- Real user monitoring
- Error logging
- Performance metrics
- User behavior analytics

**Feedback Loop:**

```text
Deploy → Monitor → Detect Issues → Fix → Deploy
                  ↑                       ↓
              Learning / Improvement
```

### DevOps Quality Practices

#### Feature Flags

- Deploy code behind toggle
- Enable for subset of users
- Disable if problems occur
- Safe deployments

#### Canary Releases

- Deploy to 1% of users
- Monitor for issues
- If good, gradually increase
- Fast rollback if needed

#### Blue-Green Deployment

- Two identical environments
- Deploy to inactive environment
- Switch traffic when ready
- Quick rollback possible

#### Testing in Production

- Synthetic monitoring (automated tests)
- Real user monitoring
- Alert on anomalies
- Metrics-based decisions

---

## Impact Summary

| Aspect | Waterfall | Agile | DevOps |
| --- | --- | --- | --- |
| **Test Timing** | End-of-project | Per-sprint | Continuous |
| **Feedback** | Weeks | Days | Minutes |
| **Automation** | 20% | 50% | 90%+ |
| **Defects Found** | Late | Early | Real-time |
| **QA Role** | Separate | Embedded | Engineering |
| **Release Frequency** | Quarterly | Monthly | Daily/Weekly |

---

## Transition Challenges

### Moving to Agile Testing

- ❌ Team not used to fast pace
  - ✅ Training and practice
- ❌ No automation infrastructure
  - ✅ Build gradually, invest in frameworks
- ❌ Legacy code hard to test
  - ✅ Refactor incrementally
- ❌ Manual testers uncomfortable
  - ✅ Upskilling and support

### Moving to DevOps Testing

- ❌ Requires automation mastery
  - ✅ Hire skilled engineers
- ❌ Infrastructure complex
  - ✅ Use Infrastructure as Code
- ❌ Cultural resistance
  - ✅ Leadership support and incentives
- ❌ Production failures risky
  - ✅ Start with lower-risk applications

---

## Remember

- **Agile requires testing discipline**—automation is key
- **Shift-Left saves money**—find bugs early
- **Continuous testing is expectation**—not optional
- **DevOps needs production monitoring**—Shift-Right too
- **Quality is everyone's job**—not just QA
- **Automation investment pays off**—required for velocity
