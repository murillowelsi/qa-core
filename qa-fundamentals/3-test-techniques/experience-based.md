# Experience-Based Testing

## Overview

Testing techniques based on tester knowledge, intuition, and experience
rather than formal specifications or code analysis.

---

## 1. Error Guessing

**Idea:** Anticipate common errors based on past experience

**How:**

- Think: "What could go wrong?"
- Use knowledge of common defects
- Guess at likely failure points
- Test those areas

**Common Errors to Guess:**

- Off-by-one errors (< vs ≤, 0-indexed arrays)
- Null/empty values
- Negative numbers
- Boundary values
- Special characters
- Maximum/minimum values
- Data type mismatches
- Order dependencies
- Timeout/performance issues

**Example:**

- Date field: Try leap year dates, empty dates, future dates
- Payment: Try $0, negative amounts, max values
- Email: Try special characters, very long addresses

**Benefit:** Quick, finds real-world defects

**Limitation:** Inconsistent, depends on experience

---

## 2. Exploratory Testing

**Idea:** Simultaneously design and execute tests based on learning

**How:**

1. Learn the system
2. Design test cases on-the-fly
3. Execute and observe results
4. Adjust approach based on findings
5. Document what you learned

**Timeboxing:** Often done in fixed time slots (e.g., 1-2 hour sessions)

**Process:**

- Try different inputs
- Notice unexpected behavior
- Investigate further
- Record interesting findings

**Best for:**

- Complex systems
- Unclear requirements
- User experience evaluation
- Finding unexpected issues

**Benefits:**

- Finds issues other methods miss
- Adapts to system behavior
- Quick feedback

**Risk:** Lacks documented coverage, hard to repeat

---

## 3. Checklist-Based Testing

**Idea:** Use a prepared checklist to ensure key areas are tested

**How:**

1. Create checklist of important areas
2. Go through each item
3. Mark complete/pass/fail
4. Track defects

**Example Checklist:**

```text
Login
☐ Valid credentials work
☐ Invalid password rejected
☐ Empty username rejected
☐ Case-sensitive password
☐ "Remember me" works
☐ Forgot password works
☐ Session timeout works

Payment
☐ Valid card accepted
☐ Invalid card rejected
☐ Expired card rejected
☐ CVV validation works
☐ Billing address required
☐ Different shipping address works
```

**Benefits:**

- Ensures consistent testing
- Easy to understand
- Documents what was tested

**Risk:** False confidence (checking box ≠ thorough testing)

---

## 4. Attack-Based Testing

**Idea:** Actively try to break the system with malicious or unusual inputs

**Types:**

### Negative Testing

- Invalid inputs (wrong type, range, format)
- Empty/null values
- Boundary violations
- Incompatible data

### Security Testing

- SQL injection
- Cross-site scripting (XSS)
- Authentication bypass
- Authorization bypass
- Buffer overflows

### Stress Testing

- Extreme load
- Resource exhaustion
- Long input strings
- Rapid requests

**Mindset:** "How can I make this fail?"

**Benefits:** Finds serious defects
**Effort:** High, requires expertise

---

## 3 Test Techniques Compared

| Technique | Approach | Best For | Effort | Consistency |
| --- | --- | --- | --- | --- |
| Specification-Based | Requirements-driven | Functional | Medium | High |
| Structure-Based | Code-driven | Coverage metrics | High | High |
| Experience-Based | Intuition-driven | Real-world issues | Low-High | Low |

---

## Combination Strategy

**Comprehensive testing uses all three:**

1. **Specification-Based:** Ensure requirements are met
2. **Structure-Based:** Ensure code is covered
3. **Experience-Based:** Catch what others miss

---

## Remember

- **Error Guessing:** What usually breaks?
- **Exploratory:** Learn and test simultaneously
- **Checklists:** Ensure nothing is missed
- **Attack-Based:** Try to break it

Experience-based testing is most valuable when combined with formal
techniques, not as a replacement.
