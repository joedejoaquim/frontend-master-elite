# Frontend Master Elite — Architecture Module

> Architecture is not structure. It is decision-making applied to system design.

---

# Purpose

The Architecture Module defines how Frontend Master Elite designs scalable, maintainable, and predictable frontend systems.

It governs:

- folder structure
- component hierarchy
- data flow
- state ownership
- rendering strategy
- system boundaries

---

# Core Principle

> Architecture must be defined before implementation and respected during the entire lifecycle of the system.

---

# Architectural Philosophy

Good architecture:

- reduces complexity
- improves scalability
- enforces consistency
- isolates responsibilities
- simplifies reasoning about the system

Bad architecture:

- creates coupling
- duplicates logic
- mixes concerns
- grows unpredictably
- becomes harder to refactor over time

---

# System Design Principles

---

## 1. Feature-Based Structure

The system is organized by features, not by file types.

Good:

features/auth/
features/dashboard/
features/settings/

Bad:

components/
hooks/
utils/

---

## 2. Separation of Concerns

Each layer has a single responsibility:

- UI Layer → presentation
- Logic Layer → business logic
- Data Layer → API & persistence
- Domain Layer → rules & models

Never mix these responsibilities.

---

## 3. Component Boundaries

Components must be:

- self-contained
- reusable when possible
- predictable in behavior
- isolated from business logic when possible

---

## 4. Data Flow Direction

Data flows in one direction only:

User Input
→ State
→ Logic
→ UI
→ Rendering

Avoid circular dependencies.

---

## 5. State Ownership Rule

State must live at the lowest possible level where it is needed.

Rules:

- Local state first
- Shared state only when necessary
- Global state only when justified

---

## 6. Server vs Client Boundary (Next.js)

Server Components:

- data fetching
- static rendering
- performance-critical rendering

Client Components:

- interactivity
- stateful UI
- browser APIs

Never overuse client components.

---

# Folder Architecture Model

Standard structure:

```
src/
  app/                → routing layer
  features/           → business logic by domain
  components/         → reusable UI
  services/           → API & external integrations
  hooks/              → reusable logic
  lib/                → utilities
  styles/             → global styles & tokens
  types/              → TypeScript definitions
  config/             → app configuration
```

---

# Feature Architecture Pattern

Each feature follows this structure:

```
features/feature-name/
  components/
  hooks/
  services/
  types/
  utils/
  index.ts
```

Each feature is independent and self-contained.

---

# Dependency Rules

---

## Rule 1 — One-Way Dependencies

Higher-level modules can depend on lower-level modules.

Lower-level modules must NEVER depend on higher-level modules.

---

## Rule 2 — No Cross-Feature Coupling

Features must not directly depend on each other.

Shared logic must be extracted.

---

## Rule 3 — Shared Layer Control

Shared logic must go into:

- components/shared
- lib/
- hooks/shared

Only if truly reusable.

---

# Architectural Decision Framework

Before implementing architecture decisions:

---

## Question 1

Does this improve scalability?

---

## Question 2

Does this reduce or increase coupling?

---

## Question 3

Is this reusable beyond one feature?

---

## Question 4

Does this simplify or complicate the system?

---

## Question 5

Will this still make sense in 6 months?

---

# Architecture Decision Tree

---

## Can this be feature-specific?

→ YES → place inside feature

→ NO → continue

---

## Is it shared across multiple features?

→ YES → move to shared layer

→ NO → keep local

---

## Does it affect application-wide behavior?

→ YES → move to core/shared system

→ NO → keep scoped

---

# Anti-Patterns

Avoid:

- monolithic components
- deeply nested folder structures
- circular dependencies
- mixing UI and business logic
- global state without justification
- duplication across features
- unclear ownership of logic

---

# Performance Architecture Rules

- Prefer server-side rendering when possible
- Minimize client-side JavaScript
- Avoid unnecessary re-renders
- Split large bundles
- Lazy-load non-critical modules

---

# Scalability Rules

A scalable architecture must:

- allow new features without refactoring existing ones
- isolate changes within features
- reduce global dependencies
- support independent feature evolution

---

# Maintainability Rules

Code is maintainable when:

- responsibilities are clearly separated
- modules are predictable
- structure is consistent
- changes are localized

---

# Validation Checklist

Before finalizing architecture:

- [ ] Feature boundaries defined
- [ ] Data flow clear
- [ ] State ownership defined
- [ ] Dependencies controlled
- [ ] Server/client split correct
- [ ] Reusability evaluated
- [ ] Scalability ensured
- [ ] Coupling minimized

---

# Collaboration Model

Architecture module collaborates with:

- Planning → defines structure
- Core → enforces principles
- Superpowers → applies specialist views
- Clean Code → validates implementation quality

---

# System Behavior Summary

Frontend Master Elite does not randomly structure systems.

It:

1. Understands requirements
2. Plans system decomposition
3. Designs architecture
4. Validates scalability
5. Only then allows implementation

---

# Final Principle

> "Architecture is the foundation of every decision. If architecture is wrong, everything built on top will fail."