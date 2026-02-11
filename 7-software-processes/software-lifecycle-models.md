# Software Lifecycle Models

## Overview

Different development models define how software is built. Each impacts
testing differently.

---

## 1. Waterfall Model

**Flow:** Requirements → Design → Development → Testing → Deployment

**Characteristics:**

- Linear, sequential phases
- Each phase completes before next starts
- Detailed upfront planning
- Testing only after coding complete

**Advantages:**

- ✅ Clear structure
- ✅ Easy to plan/estimate
- ✅ Good for simple, well-understood projects
- ✅ Easy to manage

**Disadvantages:**

- ❌ Defects found late (expensive to fix)
- ❌ No feedback until later phases
- ❌ Risk: requirements may change during project
- ❌ Violates ISTQB Principle 3 (Early Testing)

**Testing Approach:**

- Comprehensive test plan upfront
- All testing after coding complete
- Extensive testing needed (defects found late)

**Best For:**

- Regulated industries (requirements fixed)
- Clear requirements
- Low complexity
- Fixed budgets

---

## 2. V-Model

**Flow:** Requirements → Design → Code ↔ Testing at each level

**Characteristics:**

- Left side: Development (requirements, design, code)
- Right side: Testing (mirrored to left side)
- Testing planned with development
- Testing for each level

**Testing Phases:**

```text
Requirements ↔ Acceptance Testing
Design ↔ System Testing
Code ↔ Integration Testing
Code → Unit Testing
```

**Advantages:**

- ✅ Early test planning (ISTQB Principle 3)
- ✅ Testing for each level
- ✅ Defects found earlier
- ✅ Clear test-development alignment

**Disadvantages:**

- ❌ Still sequential (not agile)
- ❌ Requirements must be clear upfront
- ❌ Limited feedback until testing phases

**Testing Approach:**

- Test cases designed during development phases
- Unit tests for code
- Integration tests for design
- System tests for requirements
- Acceptance tests for needs

**Best For:**

- Safety-critical systems
- Regulated projects
- Clear requirements
- Formal documentation needed

---

## 3. Iterative and Incremental Models

**Flow:** Small cycles of design-code-test, delivering working software frequently

**Characteristics:**

- Short iterations (1-4 weeks)
- Each iteration adds features
- Testing throughout each cycle
- Regular releases/demos

**Advantages:**

- ✅ Early and frequent feedback
- ✅ Issues found early in each cycle
- ✅ Requirements can evolve
- ✅ Working software frequently
- ✅ ISTQB Principle 3 (Early Testing) ✅

**Disadvantages:**

- ❌ Harder to estimate total cost
- ❌ Requires continuous testing
- ❌ Less documentation

**Testing Approach:**

- Test each feature as developed
- Regression testing every iteration
- Continuous automation
- Exploratory testing each cycle
- Acceptance testing frequently

**Best For:**

- Evolving requirements
- Innovation projects
- Complex products
- Faster time-to-market needed

---

## 4. Agile Methodologies

**Examples:** Scrum, Kanban, Extreme Programming (XP)

**Characteristics:**

- Iterative development (1-2 week sprints)
- Focus on people and collaboration
- Embraces change
- Working software is measure of progress
- Testing is continuous (Shift-Left)

**Testing in Agile:**

- **Unit testing:** Developers write during sprint
- **Test-Driven Development (TDD):** Write tests before code
- **Automated testing:** Heavy automation focus
- **Continuous testing:** Real-time feedback
- **QA embedded:** In development team
- **Acceptance criteria:** Defined in story

**Advantages:**

- ✅ Quick feedback
- ✅ Defects found immediately
- ✅ Collaborative
- ✅ Flexible to changes
- ✅ Early, continuous testing

**Disadvantages:**

- ❌ Requires discipline and automation
- ❌ Less documentation
- ❌ Harder to enforce standards

**Testing Challenges:**

- Rapid pace (testing must keep up)
- Frequent changes (tests must be maintainable)
- Automation is critical
- Team must understand testing

**Best For:**

- Startups and innovation
- Projects with evolving requirements
- Need for frequent releases
- Small to medium teams

---

## 5. DevOps Approach

**Characteristics:**

- Development and Operations collaboration
- Continuous deployment (multiple releases/day)
- Infrastructure as code
- Automated everything
- Monitoring and feedback from production

**Testing in DevOps:**

- **Shift-Left:** Test before deployment
- **Shift-Right:** Test in production (monitoring)
- **CI/CD Pipeline:** Automated tests on every commit
- **Continuous Testing:** Never "testing phase"
- **Test Infrastructure:** Automated setup/teardown
- **Production Monitoring:** Real-time issue detection

**Testing Pipeline:**

```text
Commit Code → Unit Tests → Integration Tests → System Tests
→ Performance Tests → Security Tests → Deploy → Monitor
(All automated)
```

**Advantages:**

- ✅ Issues caught immediately
- ✅ Fast feedback loops
- ✅ Production data drives improvements
- ✅ Reduced time between releases
- ✅ Continuous improvement culture

**Disadvantages:**

- ❌ Requires heavy automation investment
- ❌ Complex infrastructure
- ❌ Needs cultural change
- ❌ Production issues still possible (Shift-Right testing)

**Best For:**

- Cloud-based applications
- Need for rapid deployments
- Tech-forward organizations
- Mature automation practices

---

## Model Comparison

| Aspect | Waterfall | V-Model | Iterative | Agile | DevOps |
| --- | --- | --- | --- | --- | --- |
| **Test Timing** | Late | Mid | Throughout | Continuous | Continuous |
| **ISTQB Principle 3** | ❌ Violates | ✅ Supports | ✅ Supports | ✅ | ✅ |
| **Automation Need** | Low | Low | Medium | High | Very High |
| **Manual Testing** | High | High | Medium | Medium | Low |
| **Feedback** | Late | Mid | Fast | Very Fast | Real-time |
| **Flexibility** | Low | Low | High | High | High |

---

## Testing Adaptation by Model

### Waterfall

- Comprehensive test plan upfront
- Heavy reliance on test cases
- Long testing phase
- Defect density high late

### V-Model

- Test cases for each level
- Entry/exit criteria per phase
- Formal sign-offs
- Better than waterfall

### Iterative

- Test automation increases
- Regression testing continuous
- Exploratory testing valuable
- Frequent releases

### Agile

- Unit tests by developers (TDD)
- Automated regression tests
- Test automation priority
- QA in development team

### DevOps

- CI/CD pipeline testing
- Infrastructure testing
- Production monitoring
- Feature flags for safe deployments

---

## Remember

- **Each model has trade-offs**—choose based on project needs
- **Early testing matters**—prefer models that support it
- **Testing adapts to model**—not the reverse
- **Automation scales**—essential for frequent releases
- **Feedback is key**—modern models favor rapid feedback

The best model is the one that enables quality software, delivered fast,
with confidence.
