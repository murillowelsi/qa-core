# Test Types

## Overview

Test types are categorized by their purpose and approach, not by when they occur.

---

## 1. Functional Testing

**Purpose:** Verify "what" the system does (features and workflows)

**Question:** Does it do what it's supposed to do?

**Typical Tests:**

- Feature functionality
- User workflows
- Data processing
- Calculations
- Business logic

**Example:** Login form accepts valid credentials and rejects invalid ones

---

## 2. Non-Functional Testing

**Purpose:** Verify "how well" the system performs (quality attributes)

### Performance Testing

- Response time and throughput
- Load testing (normal to peak load)
- Stress testing (beyond peak)
- Endurance testing (long-running)

### Security Testing

- Authentication and authorization
- Data encryption
- Injection attacks (SQL, XSS)
- Vulnerability scanning

### Usability Testing

- User interface clarity
- Navigation ease
- Accessibility (WCAG)
- User satisfaction

### Reliability Testing

- System stability
- Error recovery
- Data integrity
- Crash prevention

### Compatibility Testing

- Different browsers
- Operating systems
- Devices
- Screen resolutions

---

## 3. White-Box Testing

**Perspective:** Tester sees internal code structure

**Also called:** Structural testing, glass-box testing

**Approach:**

- Test paths through code
- Check logic branches
- Verify data flow
- Test decision points

**Who:** Developers primarily

**Coverage Types:**

- **Statement coverage** - Execute every line
- **Branch coverage** - Execute every decision path
- **Path coverage** - Execute every possible path

**Tools:** Code analyzers, debuggers, coverage tools

---

## 4. Black-Box Testing

**Perspective:** Tester sees only inputs/outputs (no code)

**Also called:** Behavioral testing

**Approach:**

- Test against requirements
- Try valid and invalid inputs
- Check outputs match expected
- No knowledge of implementation

**Who:** QA/Testing team

**Advantages:**

- Tests real user perspective
- Not biased by code implementation
- Can find requirements mismatches

---

## 5. Change-Related Testing

**Purpose:** Verify changes don't break existing functionality

### Regression Testing

- Existing functionality still works
- New changes don't cause side effects
- Run after bug fixes or new features
- Can be automated for efficiency

### Smoke Testing

- Quick check of critical functionality
- First test after build/deployment
- Decides if deeper testing is worthwhile
- Also called "sanity testing"

---

## Quick Comparison

| Type | Focus | Who | When |
| --- | --- | --- | --- |
| Functional | What it does | QA | Throughout |
| Non-functional | How well | QA/Specialist | Throughout |
| White-box | Code paths | Dev | During dev |
| Black-box | Requirements | QA | All levels |
| Regression | No breaks | QA | After changes |

---

## Remember

- **Functional:** Does it work?
- **Non-functional:** Does it work well?
- **White-box:** Know the code
- **Black-box:** Know the requirements
- **Regression:** Nothing else broke?
