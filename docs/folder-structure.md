# Frontend Master Elite — Folder Structure

## 1. Purpose

This document defines the standard folder structure for all projects generated or managed by Frontend Master Elite.

The goal is to ensure:

- Consistency across projects
- Scalability
- Maintainability
- Clear separation of concerns
- Predictable architecture

---

## 2. Core Principle

> "A project should be understandable without reading the code."

Every folder must have a single responsibility.

---

## 3. Recommended Base Structure (Next.js / React)

```text id="fs2"
src/
│
├── app/                  # Next.js App Router (or pages/ if legacy)
│
├── components/
│   ├── ui/               # Base UI components (buttons, inputs, modals)
│   ├── layout/           # Layout components (navbar, footer)
│   ├── features/        # Feature-specific components
│   └── shared/           # Reusable cross-feature components
│
├── hooks/               # Custom React hooks
├── lib/                 # Utilities and helpers
├── services/           # API calls and external services
├── store/              # State management (Zustand, Redux, etc.)
├── styles/             # Global styles, tokens
├── types/              # TypeScript types and interfaces
├── constants/          # App constants
├── assets/             # Static assets (icons, images)
└── config/             # App configuration


## 4. Folder Responsibilities
app/
Routing layer
Pages and layouts
Server components (Next.js)
components/ui/

Base design system components:

Button
Input
Card
Modal
Dropdown

These must be pure, reusable and stateless.

components/layout/

Structural components:

Navbar
Footer
Sidebar
Page wrappers
components/features/

Feature-specific logic:

Auth system
Dashboard widgets
Checkout flow
User profile
components/shared/

Shared across multiple features:

Loaders
Avatars
Tooltips
Common UI patterns
hooks/

Custom React hooks:

useAuth
useTheme
useDebounce
useFetch
lib/

Pure utilities:

formatters
validators
helpers
math functions

No React logic allowed here.

services/

External communication layer:

API clients
Fetch wrappers
Third-party integrations

Example:

Supabase client
Stripe service
REST API handlers
store/

Global state management:

Auth state
UI state
App settings

Preferred tools:

Zustand (recommended)
Redux Toolkit (advanced apps)
styles/

Design system layer:

Tailwind config
CSS variables
Themes
Typography system
types/

Centralized TypeScript definitions:

User types
API responses
Component props
constants/

Static values:

Routes
API endpoints
Configuration values
config/

App configuration:

environment variables
feature flags
runtime configs
5. Architectural Rules
5.1 No logic inside UI components

UI components must not:

fetch data
contain business logic
manage global state
5.2 Feature isolation

Each feature must be self-contained inside components/features/.

5.3 Shared logic must be abstracted

If reused twice → move to:

shared/
lib/
hooks/
5.4 Services must be framework-agnostic

services/ must NOT depend on React.

6. Scalability Model

This structure supports:

Small landing pages
Medium SaaS apps
Large dashboards
Enterprise applications

Without structural changes.

7. Anti-patterns (FORBIDDEN)

❌ Putting everything in components/

❌ Mixing UI and business logic

❌ Duplicating hooks across features

❌ Direct API calls inside components

❌ Unstructured global state

8. Final Principle

Good architecture is invisible when done correctly, and painful when ignored.