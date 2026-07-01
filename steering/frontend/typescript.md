# Frontend Master Elite — TypeScript Specialist

> TypeScript is not a feature. It is the structural backbone of predictable frontend systems.

---

# Purpose

The TypeScript Specialist defines how Frontend Master Elite uses types to:

- enforce correctness
- model application domains
- prevent runtime errors
- improve developer experience
- document system behavior

---

# Core Philosophy

Types are not just safety tools.

They are **design tools**.

A well-designed type system reflects the real structure of the application.

---

# Activation Rules

This specialist is activated when:

- defining data models
- designing API contracts
- building reusable components
- handling application state
- integrating external data sources
- refactoring complex logic

---

# Type Design Principles

---

## 1. Types Represent Reality

Types must model the domain, not the implementation.

Good:

```
User
Order
Payment
Product
```

Bad:

```
Data1
ResponseObject
TempType
```

---

## 2. Avoid Primitive Obsession

Do not rely excessively on primitives.

Prefer structured types:

Bad:

```
string
number
boolean
```

Good:

```
UserId
Email
Currency
```

---

## 3. Explicit Over Implicit

Types must be explicit and readable.

Avoid hidden inference in complex logic.

---

## 4. No Any Policy

`any` is forbidden unless:

- integrating legacy code
- handling unknown external APIs temporarily

Even then, it must be isolated.

---

# Domain Modeling Strategy

---

## 1. Entities First

Define core entities before UI:

- User
- Product
- Order
- Session

---

## 2. Derive UI from Domain

UI types must depend on domain types, not vice versa.

---

## 3. Separation of Concerns

Split types into:

- domain types
- API types
- UI props types
- utility types

---

# API Type Strategy

---

## 1. Strict Contracts

API responses must always be typed explicitly.

---

## 2. Transformation Layer

Never use raw API types directly in UI.

Always transform:

API → Domain → UI

---

## 3. Validation Awareness

Types are not runtime validation.

Always assume external data is unsafe.

---

# Component Type Strategy

---

## 1. Props Must Be Explicit

Every component must define its props clearly.

---

## 2. Avoid Inline Types in JSX

Extract reusable types instead.

---

## 3. Minimal Props Principle

Components should accept minimal required props.

---

# Generic Design Strategy

---

## 1. Use Generics for Reusability

Prefer:

```
<T>
```

for reusable components and hooks.

---

## 2. Avoid Over-Generic Systems

Do not over-engineer generic abstractions.

Balance is required.

---

# State Typing Strategy

---

## 1. State Must Be Fully Typed

No implicit state structures.

---

## 2. Derived State Preference

If state can be computed → do not store it.

---

## 3. Store Shape Must Be Predictable

Global state must have:

- explicit structure
- predictable updates
- stable contracts

---

# Utility Types Strategy

---

## 1. Reuse Standard Utilities

Prefer:

- Partial
- Pick
- Omit
- Record

---

## 2. Create Domain-Specific Utilities When Needed

Example:

```
type OptionalUser = Partial<User>
```

---

## 3. Avoid Overuse of Complex Types

If a type becomes unreadable → simplify it.

---

# Type Safety Rules

---

## 1. No Unsafe Casting

Avoid:

```
as unknown as
as any
```

---

## 2. Validate External Data

All external data must be treated as untrusted.

---

## 3. Strict Mode Required

Always assume:

- strictNullChecks = true
- no implicit any
- strict function types

---

# Error Handling Types

---

## 1. Explicit Error Types

Errors must be structured:

```
type AppError =
  | NetworkError
  | ValidationError
  | AuthError
```

---

## 2. No Silent Failures

All failure states must be represented in types.

---

# Architecture Integration

Types must align with architecture:

- domain layer → domain types
- services → API types
- UI → view models

---

# Decision Trees

---

## Should I create a new type?

→ Does this represent a domain concept?

YES → create type

NO → continue

---

## Should I reuse existing type?

→ Is structure identical or compatible?

YES → reuse

NO → extend or create new

---

## Should I use generic?

→ Will this logic be reused across multiple types?

YES → generic

NO → concrete type

---

# Anti-Patterns

Avoid:

- any usage
- duplicated types
- inconsistent naming
- mixing API and UI types
- overly complex generics
- missing null safety
- implicit assumptions in data

---

# Validation Checklist

Before finalizing TypeScript design:

- [ ] Domain is properly modeled
- [ ] No any usage
- [ ] API types isolated
- [ ] UI types separated
- [ ] Generics justified
- [ ] No duplication
- [ ] Strict null safety
- [ ] Clear naming conventions

---

# Collaboration Model

TypeScript Specialist collaborates with:

- Architecture Module → structure definition
- React Specialist → component typing
- Next.js Specialist → data layer typing
- Clean Code Module → readability enforcement

---

# System Behavior Summary

Frontend Master Elite treats TypeScript as:

> A design language for frontend systems, not just a type checker.

---

# Final Principle

> "If your types are well designed, your system is already half correct."