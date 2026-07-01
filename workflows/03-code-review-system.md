# Frontend Master Elite — Code Review System

> Code review is not approval. It is architectural validation.

---

# Purpose

The Code Review System ensures that every change in Frontend Master Elite is:

- structurally correct
- architecturally aligned
- performant
- maintainable
- safe to evolve

---

# Core Philosophy

> "If code is not reviewed properly, it is not production-ready."

Review is not optional.

It is a system gate.

---

# Activation Rules

This system is activated:

- before merging any code
- after feature implementation
- during refactoring
- after bug fixes
- during performance changes

---

# Review Dimensions

Every code change must be evaluated across:

---

## 1. Architecture Compliance

- Does it follow system structure?
- Does it respect module boundaries?
- Does it violate separation of concerns?

---

## 2. Readability

- Is the code easy to understand?
- Is naming consistent?
- Is logic clear and minimal?

---

## 3. Performance Impact

- Does it introduce unnecessary re-renders?
- Does it increase bundle size?
- Does it affect runtime efficiency?

---

## 4. Type Safety (if applicable)

- Are types correctly defined?
- Is `any` avoided?
- Are API contracts respected?

---

## 5. UI Consistency

- Does UI follow design system?
- Are components reused correctly?
- Is styling consistent?

---

## 6. Accessibility Compliance

- Is it keyboard accessible?
- Are semantic elements used?
- Is ARIA used correctly?

---

## 7. SEO Impact (if applicable)

- Is content structured properly?
- Are metadata rules respected?

---

# Review Process

---

## Step 1 — Understand Intent

- What was the goal of this change?
- Does the implementation match intent?

---

## Step 2 — Check Architecture

- Is structure respected?
- Are layers correctly separated?

---

## Step 3 — Analyze Logic

- Is logic minimal and necessary?
- Are there hidden complexities?

---

## Step 4 — Validate UI Behavior

- Does UI behave predictably?
- Are interactions correct?

---

## Step 5 — Evaluate Risks

- What can break?
- What is affected indirectly?

---

## Step 6 — Final Decision

- Approve
- Request changes
- Reject

---

# Review Types

---

## 1. Feature Review

Focus:

- correctness
- architecture
- UX consistency

---

## 2. Bug Fix Review

Focus:

- root cause correctness
- no side effects
- regression prevention

---

## 3. Refactor Review

Focus:

- behavior preservation
- structural improvement
- simplification

---

## 4. Performance Review

Focus:

- efficiency
- rendering behavior
- bundle impact

---

# Review Decision Tree

---

## Does this follow architecture rules?

→ NO → reject

→ YES → continue

---

## Does this introduce unnecessary complexity?

→ YES → request changes

→ NO → continue

---

## Does this improve or maintain system quality?

→ YES → approve

→ NO → revise

---

# Anti-Patterns

Avoid:

- approving without reading
- ignoring architecture violations
- focusing only on syntax
- missing side effects
- accepting inconsistent UI patterns
- skipping accessibility checks

---

# Review Checklist

Before approval:

- [ ] Architecture respected
- [ ] Code is readable
- [ ] No unnecessary complexity
- [ ] Performance is acceptable
- [ ] Types are correct
- [ ] UI is consistent
- [ ] Accessibility is valid
- [ ] No regressions introduced

---

# Collaboration Model

Code Review System collaborates with:

- Architecture Module → structural validation
- QA System → testing alignment
- Performance Module → efficiency checks
- Accessibility Module → compliance validation

---

# System Behavior Summary

Frontend Master Elite treats code review as:

> A mandatory architectural validation gate before system evolution.

---

# Final Principle

> "Code that is not reviewed is code that is not trusted."