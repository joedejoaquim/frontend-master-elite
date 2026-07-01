# Frontend Master Elite — Clean Code Module

> Clean code is not a style. It is a long-term engineering strategy.

---

# Purpose

This module defines how Frontend Master Elite ensures that all generated code is:

- readable
- maintainable
- consistent
- testable
- scalable

It governs implementation-level quality.

---

# Core Principle

> Code is written once, but read many times.

Therefore, readability is more important than writing speed.

---

# Clean Code Philosophy

Good code:

- communicates intent clearly
- avoids unnecessary complexity
- reduces cognitive load
- is predictable in behavior
- is easy to modify safely

Bad code:

- requires interpretation
- hides logic
- mixes concerns
- creates confusion
- increases maintenance cost

---

# Naming Conventions

---

## 1. Clarity Over Brevity

Names must describe intent clearly.

Good:

```
getUserProfile
calculateTotalPrice
isUserAuthenticated
```

Bad:

```
getData
calc
check
```

---

## 2. Boolean Naming

Boolean variables must be expressive:

Use prefixes:

- is
- has
- can
- should

Example:

```
isLoading
hasError
canSubmit
shouldRender
```

---

## 3. Component Naming

Components must be:

- nouns
- descriptive
- domain-aware

Good:

```
UserProfileCard
PaymentForm
DashboardHeader
```

Bad:

```
Card
Form
Header
```

---

# Function Design Rules

---

## 1. Single Responsibility

Each function must do ONE thing only.

If a function does more than one task → split it.

---

## 2. Small Functions

Functions must be:

- short
- focused
- predictable

If a function exceeds ~30–40 lines → review it.

---

## 3. Pure Functions When Possible

Prefer functions that:

- do not modify external state
- always return same output for same input

---

## 4. Explicit Inputs and Outputs

Avoid hidden dependencies.

Good:

```
function calculateTotal(items, taxRate)
```

Bad:

```
function calculateTotal()
```

---

# Component Design Rules

---

## 1. UI vs Logic Separation

UI components must not contain business logic.

Logic must be moved to:

- hooks
- services
- utilities

---

## 2. Composition Over Complexity

Prefer small composable components over large monoliths.

---

## 3. Props Design

Props must be:

- minimal
- explicit
- typed
- meaningful

Avoid deeply nested props unless necessary.

---

# State Management Rules

---

## 1. Local First

State should live as close as possible to where it is used.

---

## 2. Avoid Global State Overuse

Global state should only be used when:

- multiple unrelated components need it
- lifting state is not sufficient

---

## 3. Derived State Preference

If state can be computed → do not store it.

---

# Code Organization Rules

---

## 1. Group by Feature

Code must be organized by domain/feature, not by type.

---

## 2. Keep Related Code Close

Avoid scattering logic across unrelated files.

---

## 3. Co-location Principle

Components, hooks, and utilities belonging to a feature should live together.

---

# Error Handling Rules

---

## 1. Fail Explicitly

Errors must not fail silently.

---

## 2. Meaningful Messages

Errors must describe:

- what happened
- where it happened
- how to fix it

---

## 3. User-Friendly Output

Never expose raw technical errors to users.

---

# Formatting Rules

---

## 1. Consistent Indentation

Use consistent formatting across all files.

---

## 2. No Dead Code

Remove unused:

- variables
- imports
- functions
- components

---

## 3. No Magic Values

Replace magic values with constants.

Good:

```
const MAX_RETRIES = 3
```

Bad:

```
if (retry === 3)
```

---

# Refactoring Rules

---

## 1. Improve Continuously

Refactoring is part of engineering, not optional cleanup.

---

## 2. Refactor When:

- code is duplicated
- logic becomes unclear
- component grows too large
- responsibilities mix

---

## 3. Do Not Refactor Without Reason

Refactor must improve at least one:

- readability
- performance
- maintainability

---

# Anti-Patterns

Avoid:

- God components
- excessive nesting
- duplicated logic
- unclear naming
- side effects in UI
- large monolithic files
- mixing UI and data logic
- untyped structures
- hidden state mutations

---

# Readability Rules

Code must be understandable without:

- debugging
- excessive comments
- reverse engineering

If code requires explanation → improve it.

---

# Testing Mindset

Clean code must be:

- predictable
- testable
- isolated

If a function cannot be tested easily → it is too complex.

---

# Performance Awareness

Clean code is not anti-performance.

But:

- do not optimize prematurely
- prioritize clarity first
- optimize only when necessary

---

# Validation Checklist

Before finalizing implementation:

- [ ] Naming is clear
- [ ] Functions are small
- [ ] Components are reusable
- [ ] No duplication exists
- [ ] Logic is separated from UI
- [ ] No magic values
- [ ] No hidden state
- [ ] Code is readable without explanation

---

# Collaboration Model

Clean Code module collaborates with:

- Architecture → structure enforcement
- Planning → implementation order
- Core → principles validation
- QA → final verification

---

# System Behavior Summary

Frontend Master Elite enforces clean code as a mandatory output condition.

No solution is valid if it is not readable, maintainable, and consistent.

---

# Final Principle

> "Code is written for humans first, machines second."