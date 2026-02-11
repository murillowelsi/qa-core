# Testing Principles (ISTQB)

## Overview

These 7 principles form the foundation of all software testing practices
and guide effective test strategies.

---

## 1. Testing Shows Presence of Defects

**What it means:** Testing can find bugs, but cannot prove the absence of bugs.

**Remember:** Testing is about **finding** what's broken, not proving
everything works.

**Why it matters:**

- Testing improves quality by uncovering issues
- No amount of testing guarantees a defect-free system
- Test success = finding defects

---

## 2. Exhaustive Testing is Impossible

**What it means:** You cannot test every possible input, output, and state combination.

**Remember:** You cannot test **everything**—be strategic.

**Why it matters:**

- Test space is infinite in most real systems
- Focus testing on high-risk areas instead
- Use risk-based and priority-based testing

---

## 3. Early Testing

**What it means:** Start testing in the requirements and design phases,
not just after coding.

**Remember:** Test **early**, fix **cheap**.

**Why it matters:**

- Defects found early are 10-100x cheaper to fix
- Prevents building on faulty foundations
- Reviews and inspections find issues before code

---

## 4. Defect Clustering

**What it means:** Most defects are concentrated in a few modules or areas.

**Remember:** Some modules are **buggy**—focus there.

**Why it matters:**

- Follow the 80/20 rule: 80% of defects in 20% of modules
- Allocate more testing resources to high-risk areas
- Use past defect data to guide current testing

---

## 5. Pesticide Paradox

**What it means:** Running the same tests repeatedly stops finding new bugs.

**Remember:** Tests **become stale**—keep them fresh.

**Why it matters:**

- Developers adapt their code to pass existing tests
- You stop finding new defect types
- Continuously add, update, and vary test cases

---

## 6. Testing is Context Dependent

**What it means:** Testing approaches vary based on software type,
industry, and business goals.

**Remember:** **One size does NOT fit all**.

**Why it matters:**

- Banking apps need different testing than games
- Safety-critical systems need rigorous testing
- Risk tolerance shapes testing strategy
- Regulatory requirements drive testing approaches

---

## 7. Absence of Errors Fallacy

**What it means:** No bugs found ≠ good software; finding no defects
doesn't mean users will be satisfied.

**Remember:** **No bugs ≠ Ready to release**.

**Why it matters:**

- Software can pass all tests but not meet user needs
- Quality includes usability, performance, and security
- Test if the software solves the actual problem
- Validation (does it meet requirements) ≠ Verification
  (is it defect-free)

---

## Quick Reference

| Principle | Key Takeaway |
| --- | --- |
| 1. Shows Defects | Tests find bugs but can't prove none exist |
| 2. Impossible | Can't test everything—be strategic |
| 3. Early Testing | Start in requirements, not after coding |
| 4. Clustering | Bugs concentrate in a few areas |
| 5. Paradox | Tests get stale—keep them fresh |
| 6. Context | Testing depends on software type |
| 7. Errors Fallacy | No bugs ≠ good software |

---

## Remember

These principles guide every decision in software testing. Use them to
justify your testing strategy and explain why you test the way you do.
