# Frontend Master Elite — Architecture

## 1. Overview

Frontend Master Elite is a modular frontend engineering power designed for the Kiro IDE.

It transforms Kiro into a multi-role frontend engineering system capable of:

- Planning applications before implementation
- Generating production-grade React/Next.js code
- Enforcing UI/UX best practices
- Managing design systems
- Applying motion design principles
- Ensuring performance, accessibility, and scalability

---

## 2. Core Philosophy

The system is built on three principles:

### 2.1 Thinking Before Coding
No code is generated without:
- Analysis of requirements
- Architecture planning
- Component breakdown
- Risk identification

---

### 2.2 Modular Intelligence
Each responsibility is isolated into a module:

- `steering/` → behavioral intelligence
- `prompts/` → reusable task instructions
- `templates/` → project blueprints
- `standards/` → coding rules
- `checklists/` → validation layer
- `workflows/` → execution flows

---

### 2.3 Opinionated Engineering
Frontend Master Elite is not neutral.

It enforces:

- Clean architecture
- Strict TypeScript usage
- Component reusability
- Mobile-first design
- Accessibility-first UI
- Performance budgets

---

## 3. System Layers

### Layer 1 — Intelligence (Steering)

The `steering/` folder defines how the system thinks.

It includes:

- Planning strategy
- Architecture rules
- UI/UX principles
- React/Next.js patterns
- Performance guidelines
- Accessibility rules

Each file acts as a permanent instruction layer for Kiro.

---

### Layer 2 — Execution (Prompts)

The `prompts/` folder defines reusable tasks such as:

- Landing page generation
- Portfolio creation
- Dashboard building
- Authentication flows

Prompts are deterministic execution units.

---

### Layer 3 — Structure (Templates)

The `templates/` folder defines project blueprints:

- Next.js App Router apps
- SaaS platforms
- Portfolio websites
- Admin dashboards

Templates ensure consistency across projects.

---

### Layer 4 — Standards (Rules)

The `standards/` folder defines strict coding rules:

- Folder structure conventions
- TypeScript rules
- React best practices
- Tailwind usage guidelines

---

### Layer 5 — Validation (Checklists)

The `checklists/` folder ensures quality:

- Accessibility validation
- Performance audits
- SEO compliance
- Responsive behavior

---

### Layer 6 — Orchestration (Workflows)

The `workflows/` folder defines execution processes:

- Feature development flow
- Bug fixing flow
- Refactoring flow
- Code review flow

---

## 4. Kiro Execution Model

When a user requests something, Kiro follows this pipeline:

### Step 1 — Interpretation
Understand the request intent.

### Step 2 — Planning (mandatory)
Use `steering/01-superpowers.md` to:
- Break down the problem
- Define architecture
- Identify components

### Step 3 — Strategy Selection
Choose appropriate:
- prompt (if task-based)
- template (if project-based)
- workflow (if process-based)

### Step 4 — Implementation
Generate code following:

- standards/
- steering/
- checklists/

### Step 5 — Validation
Ensure:
- UI consistency
- performance compliance
- accessibility rules
- clean architecture

---

## 5. Component Architecture Model

Frontend Master Elite enforces:

- Atomic design principles
- Reusable component system
- Separation of concerns
- Server/Client component distinction (Next.js)

Structure:

- `components/ui` → base components
- `components/layout` → structural components
- `components/features` → domain logic
- `components/shared` → reusable utilities

---

## 6. Design System Integration

All UI follows:

- Spacing system (4px grid)
- Typography scale
- Color tokens
- Motion guidelines (Framer Motion)
- Responsive breakpoints

No ad-hoc styling is allowed.

---

## 7. Performance Constraints

The system enforces:

- Lazy loading by default
- Image optimization
- Minimal client-side JS
- Code splitting
- Avoid unnecessary re-renders

---

## 8. Extensibility

Frontend Master Elite is designed to evolve.

New modules can be added:

- AI reviewers
- Design auditors
- Code analyzers
- MCP integrations
- External APIs

Without breaking existing structure.

---

## 9. Summary

Frontend Master Elite transforms Kiro into:

- A frontend architect
- A UI/UX designer
- A React engineer
- A performance optimizer
- A design system enforcer

All working as a single coordinated intelligence system.