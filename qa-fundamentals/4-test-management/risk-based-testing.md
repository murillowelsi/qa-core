# Risk-Based Testing

## Overview

Risk-based testing prioritizes testing effort on areas with the highest
risk of failure. It's the most pragmatic approach when you can't test
everything.

---

## Core Concept

**Principle (ISTQB Principle 2):** Exhaustive testing is impossible

**Solution:** Focus testing on what matters most

**Formula:**

```text
Risk = Likelihood × Impact
```

---

## Product Risks vs Project Risks

### Product Risks

**Question:** What could go wrong with the software?

**Examples:**

- Payment processing fails (high likelihood: 20%, impact: critical)
- Login is slow (medium likelihood: 40%, impact: high)
- Report data incorrect (low likelihood: 5%, impact: high)
- Button alignment off (high likelihood: 60%, impact: low)

**Testing Response:** Allocate more testing to higher product risks

### Project Risks

**Question:** What could go wrong with the testing project?

**Examples:**

- Test environment not ready (impact: testing blocked)
- Key tester leaves (impact: expertise loss)
- Requirements unclear (impact: wrong tests)
- Tools don't work (impact: automation delayed)

**Testing Response:** Mitigate project risks (fix environment, document
requirements)

---

## Risk Analysis Process

### Step 1: Identify Risks

**Brainstorm what could go wrong:**

**By Feature:**

- What if users can't log in?
- What if payment fails?
- What if data is lost?
- What if system is too slow?

**By Technical Area:**

- Database failures
- Integration issues
- Security vulnerabilities
- Performance bottlenecks

**By Business Concern:**

- Revenue impact (payment, checkout)
- User satisfaction (performance, usability)
- Compliance (security, data privacy)
- Reputation (crashes, data loss)

**Techniques:**

- Brainstorming with team
- Historical data (past defects)
- Requirements review
- Architecture analysis

### Step 2: Assess Risk Likelihood

**How probable is this risk?**

| Level | Probability | Indicator |
| --- | --- | --- |
| **High** | > 50% | Known issue, complex code, new tech |
| **Medium** | 20-50% | Moderate complexity, similar issues |
| **Low** | < 20% | Simple, tested before, stable |

### Step 3: Assess Risk Impact

**If this risk happens, what's the damage?**

| Level | Impact | Examples |
| --- | --- | --- |
| **Critical** | System down, data loss, security | Payment, lockout |
| **High** | Major feature broken, business impact | Feature broken |
| **Medium** | Feature incomplete, workaround | Missing data, bug |
| **Low** | Minimal impact, easily ignored | Typo, button color |

### Step 4: Calculate Risk Level

```text
RISK MATRIX

                    LIKELIHOOD
          Low        Medium        High

Impact
High    Medium       High         Critical
Medium  Low          Medium        High
Low     Low          Low           Low
```

**Examples:**

```text
Payment fails?
- Likelihood: High (new code, complex, high volume)
- Impact: Critical (revenue loss, customer dissatisfaction)
- Risk Level: CRITICAL → Test extensively

Button misaligned?

- Likelihood: Medium (CSS changes)
- Impact: Low (cosmetic, not functional)
- Risk Level: LOW → Light testing OK
```

---

## Risk-Based Test Prioritization

### Allocation by Risk Level

**Allocate testing effort proportionally to risk:**

```text
Critical Risks:   35% of test effort
High Risks:       40% of test effort
Medium Risks:     20% of test effort
Low Risks:        5% of test effort

Total:           100% of test effort
```

**Example - 200 Hour Testing Budget:**

```text
Critical Areas:   70 hours (intensive testing)
High Areas:       80 hours (thorough testing)
Medium Areas:     40 hours (standard testing)
Low Areas:        10 hours (smoke testing only)
```

### Testing Sequence

**Test in priority order:**

1. **Test critical risks first** (highest value, highest risk)
2. Test high risks
3. Test medium risks
4. Test low risks (if time permits)

**Benefit:** If you run out of time, you've tested what matters most

---

## Risk Mitigation Through Testing

### Control Strategies

**Prevent Risk:** Stop it from happening

- Code review for security issues
- Design review to prevent architecture flaws

**Detect Risk:** Find it before production

- Extensive testing of critical areas
- Automated regression testing

**Contain Risk:** Limit damage if it happens

- Error handling testing
- Fallback mechanisms

**Monitor Risk:** Watch for issues

- Performance monitoring
- Error logging

---

## Example Risk Assessment

### E-Commerce Checkout System

| Area | Likelihood | Impact | Risk | Test Focus |
| --- | --- | --- | --- | --- |
| Payment processing | High | Critical | Critical | Extensive |
| Inventory check | Medium | High | High | Thorough |
| Order confirmation email | Medium | Medium | Medium | Standard |
| UI formatting | High | Low | Low | Smoke |
| International shipping | Low | High | Medium | Standard |
| Gift wrapping | Low | Low | Low | Minimal |

**Test Plan Result:**

- 40% of effort on payment
- 25% on inventory
- 20% on international shipping
- 10% on confirmation
- 5% on other features

---

## Risk Register Template

```text
RISK REGISTER

ID  Risk               Likelihood  Impact  Level   Test Effort    Owner
1   Payment fails      High        Crit    Crit    70 hours       Team Lead
2   Inventory mismatch Med         High    High    40 hours       Inventory QA
3   Checkout slow      High        High    High    40 hours       Perf QA
4   Email not sent     Low         Med     Med     10 hours       Backend QA
5   UI bugs            High        Low     Low     5 hours        UI QA
6   Intl shipping      Low         High    Med     20 hours       IntL QA

Total Testing Effort: 185 hours
```

---

## Risk-Based Testing in Different Contexts

### Safety-Critical System (Medical Device)

- Critical risks: Component failures, incorrect calculations
- Approach: Extensive testing, high coverage (80%+), formal testing

### Startup MVP

- Critical risks: Core feature doesn't work, security breach
- Approach: Focus on core features, less on edge cases, quick feedback

### Maintenance Release

- Critical risks: Breaking existing functionality
- Approach: Heavy regression testing, minimal new feature testing

### Agile Development

- Critical risks: Most impactful stories, integration issues
- Approach: Risk assessment in each sprint, test highest-risk stories first

---

## Remember

- **Not all features are created equal**—focus on high-risk areas
- **Risk assessment is collaborative**—use team knowledge
- **Update risks as you learn**—risks change as development progresses
- **Test critical risks first**—maximize value if time is limited
- **Don't ignore low risks**—do minimal testing to confirm, then move on

Risk-based testing is pragmatic: optimize limited testing resources for
maximum impact.
