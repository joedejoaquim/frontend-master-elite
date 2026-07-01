# Frontend Master Elite — React Specialist

> React is not about components. It is about building predictable UI systems.

---

# Purpose

The React Specialist defines how React is used within Frontend Master Elite.

It ensures all React-based implementations follow:

- predictable component design
- scalable state management
- performance-first rendering
- clean separation of concerns

---

# Activation Rules

This specialist is activated when:

- building UI components
- designing state logic
- implementing hooks
- managing rendering behavior
- structuring React applications

---

# Core Philosophy

React is a UI composition engine, not a logic container.

Business logic must never dominate components.

Components must remain predictable, reusable, and isolated.

---

# Component Design Principles

---

## 1. Functional Components Only

Class components are forbidden unless explicitly required.

---

## 2. Composition Over Complexity

Prefer composing small components instead of building large monoliths.

---

## 3. UI vs Logic Separation

React components must NOT contain business logic.

Logic must be moved to:

- hooks
- services
- utilities

---

## 4. Single Responsibility

Each component must do ONE thing:

- render UI
- handle interaction
- or orchestrate composition

Not all three at once.

---

# Hooks Design Principles

---

## 1. Custom Hooks for Logic

Any reusable logic must be extracted into a hook.

---

## 2. Hooks Must Be Pure

Hooks should not:

- mutate global state directly
- perform side effects without control
- mix UI logic

---

## 3. Naming Convention

Hooks must start with `use`

Examples:

- useUser
- useAuth
- useDashboardData

---

# State Management Strategy

---

## 1. Local State First

Use local state whenever possible.

---

## 2. Derived State Preference

If state can be calculated → do not store it.

---

## 3. Context Usage Rules

Context should only be used when:

- multiple distant components need shared state
- prop drilling becomes harmful

---

## 4. Avoid Overuse of Global State

Global state (Zustand/Redux/etc.) only when:

- application-wide state is required
- multiple features depend on same state

---

# Rendering Strategy

---

## 1. Minimize Re-renders

Avoid unnecessary re-render cycles.

---

## 2. Memoization Rules

Use memoization ONLY when:

- performance issue is measurable
- component is expensive to render

---

## 3. Conditional Rendering

Prefer early returns for clarity.

---

# Data Fetching Strategy

---

## 1. Server First (Next.js context)

Prefer server-side data fetching when possible.

---

## 2. Client Fetching Only When Needed

Use client fetching when:

- interactivity is required
- real-time updates are needed

---

## 3. Separation of Concerns

Data fetching must NOT be inside UI components.

Use:

- services
- hooks
- server functions

---

# Component Structure Pattern

Each component must follow:

```
1. Imports
2. Types
3. Helper functions (if needed)
4. Component logic
5. JSX
6. Export
```

---

# Anti-Patterns

Avoid:

- large components (>200 lines)
- mixing UI and business logic
- prop drilling deep chains
- unnecessary re-renders
- uncontrolled side effects
- global state abuse
- duplicated UI logic

---

# Folder Placement Rules

---

## UI Components

Reusable UI → `components/ui`

---

## Feature Components

Feature-specific → `features/<feature>/components`

---

## Shared Components

Reusable across features → `components/shared`

---

# Performance Rules

- Avoid unnecessary renders
- Split components logically
- Use lazy loading for heavy components
- Keep state minimal
- Avoid expensive computations in render

---

# Error Handling Rules

- Never break UI silently
- Always provide fallback UI
- Handle async errors explicitly

---

# Accessibility Rules

React components must always:

- use semantic HTML
- support keyboard navigation
- include proper labels
- avoid div-only interfaces

---

# Decision Tree — Component Creation

---

## Is this reusable?

→ YES → UI component

→ NO → continue

---

## Is it feature-specific?

→ YES → feature component

→ NO → shared component

---

## Does it contain business logic?

→ YES → extract hook/service

→ NO → keep as UI component

---

# Decision Tree — State

---

## Can state be derived?

→ YES → do not store it

→ NO → continue

---

## Is state local?

→ YES → use useState

→ NO → continue

---

## Is it shared?

→ YES → context or store

→ NO → rethink architecture

---

# Validation Checklist

Before finalizing React implementation:

- [ ] Components are small and focused
- [ ] Logic is separated from UI
- [ ] Hooks are reusable
- [ ] State is minimal
- [ ] No unnecessary re-renders
- [ ] Accessibility is respected
- [ ] Folder placement is correct
- [ ] No duplicated logic

---

# Collaboration Model

React Specialist collaborates with:

- Architecture module → structure decisions
- Planning module → feature breakdown
- Clean Code module → implementation quality
- Performance module → optimization strategy

---

# System Behavior Summary

React is not treated as a framework to "use".

It is treated as a system to "engineer".

---

# Final Principle

> "In React, clarity of components is more important than complexity of logic."