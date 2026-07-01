# Frontend Master Elite — Autonomous Refactor Planner

> Refactoring is not execution. It is controlled architectural evolution planning.

---

# Purpose

The Autonomous Refactor Planner is responsible for:

- designing refactor strategies
- breaking refactors into safe phases
- minimizing risk of system breakage
- coordinating multi-layer changes
- ensuring behavior preservation during evolution

It does NOT execute refactors.

It only plans them in detail.

---

# Core Philosophy

> "A safe refactor is not fast. It is reversible, incremental, and observable."

Refactoring must never destabilize the system.

---

# Activation Rules

This module is activated when:

- technical debt reaches medium or high severity
- architecture becomes inconsistent
- performance degradation is detected
- system scaling becomes difficult
- repeated patterns indicate structural decay

---

# Refactor Planning Principles

---

## 1. Behavior Preservation First

No refactor is valid if behavior changes unintentionally.

---

## 2. Incremental Transformation

All refactors must be broken into:

- small steps
- reversible steps
- testable steps

---

## 3. Risk Awareness

Every step must include risk evaluation.

---

## 4. Dependency Mapping

Refactors must account for:

- module dependencies
- shared logic
- global impact

---

# Refactor Planning Structure

Each refactor plan must include:

---

## 1. Problem Definition

- what is wrong in the current system
- why it is a problem

---

## 2. Target Architecture

- desired structure after refactor
- new module organization
- improved patterns

---

## 3. Step-by-Step Plan

Each step must define:

- what changes
- which modules are affected
- expected outcome

---

## 4. Risk Analysis

For each step:

- potential breakpoints
- side effects
- rollback strategy

---

## 5. Validation Strategy

How to verify:

- behavior unchanged
- performance stable
- no regressions introduced

---

# Refactor Types

---

## 1. Structural Refactor

Focus:

- folder reorganization
- module separation
- dependency cleanup

---

## 2. Logic Refactor

Focus:

- simplifying business logic
- removing duplication
- improving clarity

---

## 3. Performance Refactor

Focus:

- reducing rendering cost
- improving data flow
- optimizing execution paths

---

## 4. Architectural Refactor

Focus:

- redesigning system structure
- introducing new layers
- improving scalability

---

# Refactor Planning Workflow

---

## Step 1 — Analyze System State

Input from:

- System Observer
- Debt Detector
- Architecture Advisor

---

## Step 2 — Identify Refactor Opportunity

- where structure breaks down
- where complexity accumulates

---

## Step 3 — Define Target State

- clean architecture vision
- simplified dependency model

---

## Step 4 — Break Into Phases

Each phase must be:

- independent
- testable
- reversible

---

## Step 5 — Validate Plan

Ensure:

- no unsafe transitions
- no missing dependencies
- no hidden side effects

---

# Refactor Safety Rules

---

## 1. Never Big Bang Refactor

No full system rewrites in one step.

---

## 2. Always Preserve Working State

System must remain functional after each phase.

---

## 3. Prefer Parallel Structures During Migration

Old and new structures can coexist temporarily.

---

## 4. Validate Continuously

Each step must be verifiable.

---

# Refactor Decision Tree

---

## Is behavior changing?

→ YES → NOT a refactor (requires redesign)

→ NO → continue

---

## Can this be split into phases?

→ YES → proceed

→ NO → redesign plan

---

## Is risk manageable per step?

→ YES → approve plan

→ NO → simplify approach

---

# Anti-Patterns

Avoid:

- full system rewrites
- unplanned large-scale changes
- mixing refactor with feature development
- ignoring dependency chains
- skipping validation steps
- unsafe parallel changes

---

# Output Format Rules

Each refactor plan must include:

- current system state
- target architecture
- phased transformation plan
- risk assessment per phase
- validation strategy
- rollback strategy

---

# Collaboration Model

Autonomous Refactor Planner works with:

- System Observer → detects issues
- Technical Debt Detector → identifies priorities
- Architecture Advisor → defines target structure
- Planning System → execution breakdown
- Code Review System → validation layer

---

# System Behavior Summary

Frontend Master Elite treats refactor planning as:

> A controlled transformation blueprint for evolving systems safely.

---

# Final Principle

> "The best refactors are not the fastest — they are the safest paths from chaos to clarity."