# Reviews (Static Testing)

## Overview

Reviews find defects in documents and code WITHOUT executing the
software. Also called static testing.

---

## Why Reviews Matter

### ISTQB Principle 3: Early Testing

- Defects in requirements are cheaper to fix than defects in code
- Find issues before development begins
- Prevent building on faulty foundations

**Cost Comparison:**

- Defect in requirement: $100 to fix
- Defect in code: $1,000 to fix
- Defect in production: $100,000 to fix

---

## Review Types (in order of formality)

### 1. Informal Review (Desk Check)

**What:** Casual, unstructured review

**How:**

- Colleague reads code/document
- Provides feedback
- No formal process or roles

**When to use:**

- Quick feedback needed
- Low-risk changes
- Peer learning

**Benefit:** Fast, easy
**Limitation:** Inconsistent

---

### 2. Walkthrough

**What:** Author leads team through work

**Process:**

1. Author prepares presentation
2. Discusses section by section
3. Team asks questions
4. No official scribe or roles

**Duration:** 30-60 minutes

**When to use:**

- Knowledge sharing
- Getting buy-in
- Learning from peers

**Benefit:** Good for communication
**Limitation:** Less structured

---

### 3. Technical Review

**What:** Peers review technical work (code, design, architecture)

**Process:**

1. Work is prepared (clean, ready)
2. Reviewer(s) study it beforehand
3. Meeting to discuss findings
4. Minor notes recorded
5. Author addresses comments

**Participants:**

- Author
- Technical experts (2-3)
- Scribe (optional)

**Duration:** 30-90 minutes

**When to use:**

- Code review
- Architecture review
- Design decisions
- Technical documentation

**Checklist Items:**

- Follows coding standards?
- Logic is correct?
- Edge cases handled?
- Performance acceptable?
- Security checked?
- Tests adequate?

**Benefit:** Catches technical issues, knowledge sharing
**Limitation:** Less formal than inspection

---

### 4. Inspection (Most Formal)

**What:** Formal, structured review with defined roles

**Inspection Roles:**

- **Author** - Explains work
- **Inspector/Reviewer** - Finds defects (primary role)
- **Moderator** - Manages process
- **Scribe** - Records findings

**Process:**

1. **Planning** - Assign roles, notify participants
2. **Overview** - Author explains work (optional)
3. **Preparation** - Reviewers independently study
4. **Inspection Meeting** - Find issues, don't fix
5. **Rework** - Author fixes issues
6. **Follow-up** - Verify fixes

**Duration:** 1-2 hours formal meeting + prep time

**Metrics Tracked:**

- Defects found
- Defects by severity
- Inspection time
- Rework time

**When to use:**

- Safety-critical code
- High-risk modules
- Complex algorithms
- Security-sensitive areas

**Benefit:** Most effective at finding defects
**Limitation:** Time-consuming, formal

---

## Review Process

### Planning Phase

**Before Review:**

1. Select reviewers (2-3 technical experts)
2. Notify participants and schedule
3. Provide materials in advance
4. Set clear objectives

**Success Criteria:**

- Everyone prepared
- Materials clear and complete
- Expectations defined

### Preparation Phase

**1-3 days before:**

- Reviewers read/study work
- Note observations
- List questions
- Identify issues

**What reviewers look for:**

- Logic errors
- Missing cases
- Code quality
- Standards compliance
- Performance issues
- Security risks
- Documentation accuracy

### Review Meeting

**During meeting:**

1. Author explains (5-10 min)
2. Team asks questions (10-20 min)
3. Discuss findings (20-30 min)
4. Record issues (5-10 min)

**Ground Rules:**

- Focus on work, not person
- Find defects, don't fix them yet
- Document specifically
- Maintain respect

### Rework Phase

**After meeting:**

- Author fixes issues
- Tracks resolution
- Communicates changes

**Follow-up:**

- Verify all issues addressed
- Check fix quality
- Sign off when complete

---

## What Reviewers Look For

### Code Review Checklist

- ✅ Code follows standards/style
- ✅ Logic is correct
- ✅ Edge cases handled
- ✅ No off-by-one errors
- ✅ Error handling present
- ✅ Null checks included
- ✅ Resource cleanup (close files, connections)
- ✅ Performance acceptable
- ✅ Security considerations addressed
- ✅ Tests adequate
- ✅ Documentation clear
- ✅ No duplication

### Requirements Review Checklist

- ✅ Requirements are clear and unambiguous
- ✅ Requirements are testable
- ✅ Requirements are complete
- ✅ No contradictions
- ✅ Priority is clear
- ✅ Dependencies identified
- ✅ Acceptance criteria defined
- ✅ Feasibility assessed
- ✅ Risks identified

### Design Review Checklist

- ✅ Design meets requirements
- ✅ Scalability addressed
- ✅ Security architecture sound
- ✅ Performance considerations
- ✅ Error handling strategy
- ✅ Data flow clear
- ✅ Component interactions defined
- ✅ Testing strategy feasible
- ✅ Documentation adequate

---

## Review Metrics

### Defect Detection

```text
Defects found in review: 25
Defects found in testing: 5
Defects escaping to production: 1

Review effectiveness: 96% (found 96% of all defects)
```

### Effort

```text
Review meeting: 1.5 hours × 4 people = 6 hours
Preparation: 2 hours × 4 people = 8 hours
Rework: 2 hours
Total: 16 hours to review 500 lines of code
Cost: 16 hours × $75/hour = $1,200

Defect cost if found in production: $50,000
ROI: Highly positive
```

### Trends

```text
Defects per review: 5 (high, good finding rate)
Defect severity in reviews: 60% high/critical (important defects found)
Time for review: 30 minutes (efficient, well-prepared team)
Rework time: 1 day (reasonable fix timeline)
```

---

## Review vs Testing

| Aspect | Review | Testing |
| --- | --- | --- |
| **Method** | Reading code/docs | Executing code |
| **Timing** | Early (design, code) | After build ready |
| **Cost** | Low per hour | Higher per execution |
| **Finds** | Logic errors, design flaws | Functional defects |
| **Effort** | 1-2 hours | Can be hours-days |
| **Effectiveness** | Very high early | Essential later |

**Best Approach:** Use both - reviews catch early, testing catches
runtime issues

---

## Tips for Effective Reviews

✅ **Do's:**

- Review small portions (< 500 lines/doc at a time)
- Prepare thoroughly
- Create checklists for consistency
- Be constructive and respectful
- Document findings specifically
- Track metrics

❌ **Don'ts:**

- Review while tired or distracted
- Review too much at once
- Make it personal ("your code is bad")
- Fix issues in meeting (for formal inspections)
- Skip preparation
- Ignore recommendations

---

## Remember

- Reviews find defects **before execution**
- Early reviews are **cheaper** than late testing
- Reviews **complement** testing, don't replace it
- Formality should match **risk level**
- Reviews are about **the work, not the person**
