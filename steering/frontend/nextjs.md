# Frontend Master Elite — Next.js Specialist

> Next.js is not a framework. It is a full-stack rendering architecture.

---

# Purpose

The Next.js Specialist defines how Frontend Master Elite structures applications using Next.js.

It governs:

- rendering strategy (SSR / CSR / SSG)
- App Router architecture
- server-client boundaries
- data fetching strategy
- caching strategy
- SEO optimization
- performance design

---

# Activation Rules

This specialist is activated when:

- building Next.js applications
- designing routing structures
- deciding server vs client components
- handling data fetching strategies
- optimizing performance or SEO

---

# Core Philosophy

Next.js exists to reduce client-side complexity.

The default mindset is:

> Do as much as possible on the server, as little as necessary on the client.

---

# Rendering Strategy Principle

---

## Default Rule

Prefer Server Components.

---

## Client Components Only When Needed

Use Client Components only when:

- interactivity is required
- browser APIs are needed
- stateful UI is necessary

---

## Anti-Pattern

Do NOT make everything a Client Component by default.

This destroys performance benefits of Next.js.

---

# App Router Architecture

---

## Folder Structure Principle

Routes are not just pages.

They are **structured application boundaries**.

Example:

```
app/
  layout.tsx
  page.tsx
  dashboard/
    page.tsx
    layout.tsx
    loading.tsx
    error.tsx
```

Each route segment is a system boundary.

---

## Layout Strategy

Layouts must:

- be reusable
- define UI structure
- avoid business logic
- remain stable across navigation

---

# Server vs Client Boundary Rules

---

## Server Components

Use for:

- data fetching
- static rendering
- SEO content
- performance-critical UI

---

## Client Components

Use for:

- event handling
- state management
- animations
- browser APIs

---

## Decision Rule

If it does NOT require interaction → Server Component

---

# Data Fetching Strategy

---

## 1. Server-First Approach

Always fetch data on the server when possible.

---

## 2. Avoid Client Fetching by Default

Client fetching should only be used when:

- real-time updates are needed
- user interaction triggers fetch
- server fetch is not possible

---

## 3. Fetching Location Rule

Data should be fetched at the **highest possible level** in the tree.

Avoid deep nested fetching.

---

# Caching Strategy

---

## 1. Default: Cached

Assume data should be cached unless specified otherwise.

---

## 2. Revalidation Strategy

Use revalidation for:

- dynamic content
- frequently changing data

---

## 3. No Uncontrolled Fetching

Avoid uncontrolled or repeated fetch loops.

---

# Performance Principles

---

## 1. Minimize Client JavaScript

The less JS on client, the better.

---

## 2. Prefer Streaming

Use streaming for large pages and slow data sources.

---

## 3. Split Route Segments

Each route should be independently optimized.

---

# SEO Principles

---

## 1. Server-Rendered Content First

SEO-critical content must be server-rendered.

---

## 2. Metadata Management

Every route must define:

- title
- description
- open graph data

---

## 3. Structured Data

Use structured data when applicable.

---

# Routing Decision Tree

---

## Is this a page-level route?

→ YES → create route segment

→ NO → continue

---

## Does this require layout?

→ YES → create layout.tsx

→ NO → continue

---

## Does it need loading state?

→ YES → add loading.tsx

→ NO → skip

---

## Does it need error handling?

→ YES → add error.tsx

→ NO → skip

---

# Component Placement Rules

---

## Server Components

Default location inside app/ routes.

---

## Client Components

Move to:

- components/
- features/

only when interactivity is required.

---

# Anti-Patterns

Avoid:

- overusing "use client"
- fetching data in client unnecessarily
- mixing server and client logic incorrectly
- deep prop drilling across routes
- duplicating layouts
- ignoring caching strategies

---

# Architecture Boundaries

---

## app/

Routing + layout system

---

## features/

Business logic modules

---

## components/

Reusable UI

---

## services/

API + external integrations

---

## lib/

Utilities and helpers

---

# Validation Checklist

Before finalizing Next.js implementation:

- [ ] Server components used by default
- [ ] Client components justified
- [ ] Data fetching optimized
- [ ] Routes properly structured
- [ ] Layouts defined correctly
- [ ] Caching strategy defined
- [ ] SEO metadata included
- [ ] Performance considered
- [ ] No unnecessary JavaScript on client

---

# Collaboration Model

Next.js Specialist collaborates with:

- React Specialist → UI composition
- Architecture Module → system structure
- Performance Module → optimization strategy
- Planning Module → feature breakdown

---

# System Behavior Summary

Frontend Master Elite treats Next.js as:

> A hybrid rendering architecture, not a frontend framework.

Every decision is based on performance, scalability, and clarity.

---

# Final Principle

> "In modern web applications, server is the default. Client is the exception."