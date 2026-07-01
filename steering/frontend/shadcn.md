# Frontend Master Elite — shadcn/ui Specialist

> shadcn/ui is not a component library. It is a composable design system architecture.

---

# Purpose

The shadcn/ui Specialist defines how Frontend Master Elite builds UI systems using composable, accessible, and extensible components.

It ensures:

- consistent UI primitives
- scalable component architecture
- high accessibility standards
- full design system control
- minimal abstraction overhead

---

# Core Philosophy

> You do not "use" shadcn/ui. You build on top of it.

Components are not black boxes.

They are **editable building blocks**.

---

# Activation Rules

This specialist is activated when:

- designing UI components
- building design systems
- extending base components
- creating reusable UI primitives
- standardizing interface patterns

---

# Component Philosophy

---

## 1. Composition Over Configuration

Prefer composing small components instead of configuring large ones.

---

## 2. Ownership of Components

All components are fully owned and editable.

No locked abstractions.

---

## 3. No Black Box UI

Every component must be:

- readable
- editable
- extendable
- predictable

---

# Component Architecture Model

---

## Base Layer (Primitives)

Examples:

- Button
- Input
- Dialog
- Checkbox
- Select

These are the foundation.

---

## Composite Layer

Built from primitives:

- Forms
- Cards
- Modals
- Navigation bars

---

## Feature Layer

Domain-specific UI:

- LoginForm
- PaymentDialog
- UserSettingsPanel

---

# Styling Strategy

---

## 1. Tailwind First

All styling is handled via Tailwind utilities.

---

## 2. Variants Instead of Duplication

Use variant patterns instead of duplicating components.

Example concept:

- button variants (primary, secondary, danger)

---

## 3. No Inline Styling Logic Explosion

Avoid excessive conditional class logic inside components.

---

# Accessibility Rules

---

## 1. Accessibility Is Built-In

Every component must be:

- keyboard navigable
- screen-reader friendly
- semantic

---

## 2. ARIA Only When Necessary

Do not overuse ARIA attributes.

Use semantic HTML first.

---

# Component Extension Rules

---

## 1. Extend, Don’t Rewrite

When customizing a component:

- extend existing component
- do not duplicate logic

---

## 2. Preserve Base Behavior

Customizations must not break accessibility or usability.

---

## 3. Keep API Minimal

Component props must remain simple and predictable.

---

# Design System Integration

---

## 1. Centralized Tokens

Components must rely on:

- spacing system
- color system
- typography system

Defined in Tailwind module.

---

## 2. Consistency Across Components

All components must visually align.

No exceptions unless explicitly justified.

---

# Reusability Rules

---

## 1. If Used Twice → Extract

Any repeated UI pattern must become a component.

---

## 2. Feature Components Must Not Duplicate Primitives

Always compose from base components.

---

# State Handling Rules

---

## 1. No Internal Business Logic

UI components must NOT contain business logic.

---

## 2. Controlled vs Uncontrolled

Components must support predictable state handling.

---

## 3. External State Preferred

State must be managed outside UI when possible.

---

# Anti-Patterns

Avoid:

- duplicating shadcn components
- modifying base components without reason
- mixing UI and business logic
- creating inconsistent variants
- bypassing accessibility rules
- overcomplicating component APIs

---

# Component Decision Tree

---

## Is this a primitive UI element?

→ YES → Base component

→ NO → continue

---

## Is it composed of multiple primitives?

→ YES → Composite component

→ NO → continue

---

## Is it domain-specific?

→ YES → Feature component

→ NO → reconsider design

---

# Validation Checklist

Before finalizing UI component:

- [ ] Based on composition
- [ ] Fully accessible
- [ ] Uses Tailwind system
- [ ] No business logic inside
- [ ] Reusable where possible
- [ ] Variants properly designed
- [ ] No duplication of primitives
- [ ] Consistent with design system

---

# Collaboration Model

shadcn/ui Specialist collaborates with:

- Tailwind Specialist → styling system
- React Specialist → component architecture
- UI/UX Engineer → interaction design
- Design System Engineer → visual consistency

---

# System Behavior Summary

Frontend Master Elite treats shadcn/ui as:

> A fully composable UI foundation, not a dependency.

It is extended, not consumed.

---

# Final Principle

> "The best UI system is not the one you use, but the one you fully control."