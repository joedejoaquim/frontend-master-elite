# Frontend Master Elite — Technical Debt Detector

> Technical debt is not a future problem. It is a present signal of system decay.

---

# Purpose

The Technical Debt Detector is responsible for identifying:

- structural degradation
- architectural inconsistencies
- code complexity growth
- duplication accumulation
- maintainability risks

It does NOT fix issues.

It only detects and classifies them.

---

# Core Philosophy

> "Debt is not bad code — it is unaddressed complexity."

Every system accumulates debt.  
The goal is to control it, not eliminate it completely.

---

# Activation Rules

This module is active when:

- new features are added
- refactoring occurs
- system grows in complexity
- modules become harder to maintain
- duplication increases
- performance degrades indirectly

---

# Types of Technical Debt

---

## 1. Structural Debt

Caused by poor system organization.

Examples:

- misplaced modules
- unclear boundaries
- circular dependencies

---

## 2. Code Debt

Caused by implementation shortcuts.

Examples:

- duplicated logic
- large functions
- inconsistent patterns

---

## 3. Architectural Debt

Caused by design decisions that no longer scale.

Examples:

- wrong abstraction level
- over-coupled systems
- missing domain separation

---

## 4. Performance Debt

Caused by inefficient implementation over time.

Examples:

- repeated re-renders
- growing bundle size
- unnecessary client computation

---

## 5. Knowledge Debt

Caused by lack of clarity in codebase.

Examples:

- unclear naming
- missing documentation
- implicit behavior

---

# Debt Detection Rules

---

## 1. Detect Patterns, Not Isolated Issues

Debt is systemic, not isolated.

---

## 2. Measure Accumulation

Single issue ≠ debt  
Repeated issue = debt

---

## 3. Evaluate Growth Risk

Ask:

- Will this scale poorly?
- Will this get worse over time?

---

## 4. Context Awareness

Same pattern may or may not be debt depending on context.

---

# Debt Classification System

---

## Severity Levels

### LOW
- minor duplication
- local inefficiency

### MEDIUM
- repeated patterns across modules
- moderate coupling

### HIGH
- architecture violation
- scaling risk

### CRITICAL
- system instability risk
- refactor required immediately

---

# Detection Strategy

---

## Step 1 — Scan Structure

- modules
- dependencies
- boundaries

---

## Step 2 — Analyze Complexity

- function size
- component depth
- logic duplication

---

## Step 3 — Evaluate Evolution Trend

- is complexity increasing?
- is structure degrading?

---

## Step 4 — Assign Debt Category

- structural
- code
- architectural
- performance
- knowledge

---

# Output Format Rules

Each debt report must include:

- debt type
- severity level
- affected modules
- explanation of risk
- evolution impact
- recommended future action (NOT execution)

---

# Debt Decision Tree

---

## Is this a repeated pattern?

→ YES → debt detected

→ NO → ignore

---

## Does it increase system complexity?

→ YES → classify severity

→ NO → ignore

---

## Will this scale poorly?

→ YES → escalate severity

---

# Anti-Patterns

Avoid:

- treating isolated bugs as debt
- mixing detection with fixing
- ignoring systemic repetition
- over-labeling minor issues
- emotional labeling of code quality

---

# Collaboration Model

Technical Debt Detector works with:

- System Observer → data source
- Refactoring Engine → resolution path
- Architecture Advisor → structural correction
- Code Review System → validation layer

---

# System Behavior Summary

Frontend Master Elite treats technical debt as:

> A measurable signal of structural entropy in the system.

---

# Final Principle

> "You do not eliminate technical debt — you manage its evolution before it becomes system failure."