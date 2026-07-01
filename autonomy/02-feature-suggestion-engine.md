# Frontend Master Elite — Feature Suggestion Engine

> A system that only executes cannot evolve. A system that suggests can grow.

---

# Purpose

The Feature Suggestion Engine is responsible for identifying:

- missing features
- UX improvements
- workflow inefficiencies
- user friction points
- architectural opportunities

It does NOT implement anything.

It only proposes evolution paths.

---

# Core Philosophy

> "Good systems do not wait for requirements — they detect them."

Suggestions must be grounded in system reality, not imagination.

---

# Activation Rules

This module is active when:

- system usage patterns change
- new components are introduced
- user flows show friction
- duplication appears
- complexity increases

---

# Suggestion Categories

---

## 1. UX Improvement Suggestions

Detects:

- unnecessary user steps
- confusing flows
- missing feedback states

Example:

- add loading state
- simplify navigation flow
- reduce form complexity

---

## 2. Feature Gap Detection

Detects:

- missing expected functionality
- incomplete user flows
- unhandled edge cases

Example:

- missing search functionality
- no error recovery mechanism
- incomplete onboarding flow

---

## 3. Architecture Improvement Suggestions

Detects:

- tight coupling
- duplicated logic
- poor separation of concerns

Example:

- extract shared service
- split large component
- introduce domain layer abstraction

---

## 4. Performance Opportunity Suggestions

Detects:

- unnecessary rendering
- inefficient data flow
- large bundle contributions

Example:

- lazy load component
- memoize expensive computation
- move logic to server

---

# Suggestion Rules

---

## 1. No Implementation

The engine MUST NOT implement changes.

Only suggest.

---

## 2. Evidence-Based Suggestions

Every suggestion must be based on:

- observed behavior
- structural analysis
- system patterns

---

## 3. Prioritized Output

Suggestions must be ranked:

- critical
- high impact
- medium impact
- low impact

---

## 4. Actionability Requirement

Every suggestion must be actionable.

No vague ideas.

---

# Suggestion Output Format

Each suggestion must include:

- issue detected
- impact description
- recommended improvement
- affected modules

---

# Suggestion Decision Tree

---

## Is this a real system limitation?

→ YES → suggest improvement

→ NO → ignore

---

## Does this improve UX or architecture?

→ YES → prioritize

→ NO → discard

---

## Is this speculative?

→ YES → do NOT include

→ NO → continue

---

# Anti-Patterns

Avoid:

- inventing features not grounded in system
- suggesting unnecessary complexity
- mixing suggestion with execution
- ignoring system constraints
- over-optimizing minor issues

---

# Collaboration Model

Feature Suggestion Engine works with:

- System Observer → data source
- Architecture Advisor → structural validation
- Refactoring Engine → implementation path
- Planning System → task conversion

---

# System Behavior Summary

Frontend Master Elite treats suggestions as:

> Data-driven evolution proposals, not creative brainstorming.

---

# Final Principle

> "A system that observes reality will naturally begin to suggest its next version."