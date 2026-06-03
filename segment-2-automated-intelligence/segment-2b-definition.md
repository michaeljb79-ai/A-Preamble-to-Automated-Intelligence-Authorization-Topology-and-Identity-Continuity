# Segment 2B — The Automated Intelligence Class Definition

**Version:** v5 (Locked)

**Copyright Registration:** 1-15144594701

**Classification:** Architectural Class Definition

**Authority Model:** Authorization Topology

---

## 1. Class Definition

An architecture belongs to the Automated Intelligence class if and only if all five invariants defined in Section 3 hold under the structural terms defined in Section 2.

Membership is structural.

It is not determined by behavior, capability, performance, intelligence level, or task complexity.

An architecture either satisfies the class requirements or it does not.

---

## 2. Core Structural Terms

### 2.1 Execution Class

The minimal unit of authorization.

Two actions share an execution class if and only if authorization for one logically implies authorization for the other.

Authorization boundaries are defined by decision implication, not by capability taxonomy.

### 2.2 Principal

An entity that can issue verifiable authorization tokens and revoke authorization state, and that exists outside the execution scope of the system being authorized.

The system cannot grant its own authorizations.

The principal relationship is non-reflexive.

### 2.3 Transient Working Memory

The internal, non-persisted reasoning context of the system.

Transient working memory is strictly bounded to context that:

- Is not accessible to external systems without the reasoning engine's active cooperation.
- Does not persist beyond the current reasoning pass.
- Is not externally inspectable without active disclosure.

The following are external state and are not transient working memory:

- Retrieval stores
- Vector databases
- Tool persistence
- File storage
- Model-side persistence
- Cached recallable outputs
- Hidden scratch files
- Tool buffers

Memory boundary expansion is a silent autonomy vector.

This definition must not expand.

### 2.4 Pre-Execution Validation Gate

A mandatory checkpoint that must be passed before any action executes.

The gate:

- Operates at a privilege level unreachable by the reasoning engine's write operations.
- Validates action class membership against current authorization state.
- Receives only action descriptor and authorization state.
- Does not receive reasoning-engine justification.
- Cannot be modified by the reasoning engine.

---

## 3. Invariants

### 3.1 Explicit Class Authorization

Every action belongs to an execution class — the minimal authorization unit, where two actions share a class if and only if authorization for one logically implies authorization for the other — explicitly granted by a principal external to the system's execution scope prior to execution.

### 3.2 Class-Specific Bounding

Authorization is class-specific.

An authorized objective does not authorize execution classes not explicitly granted, even if those classes would serve the objective.

### 3.3 Privilege-Isolated Pre-Execution Gate

Behavioral boundaries are enforced by a mandatory pre-execution validation gate operating at a privilege level unreachable by the reasoning engine's write operations.

Composite actions must be atomically decomposed into constituent execution classes prior to gate validation.

If any component class lacks valid authorization, the composite is rejected in its entirety before any constituent action executes.

### 3.4 Execution Boundary at External State Access

Execution begins at the first operation that accesses, observes, or modifies any state outside the reasoning engine's transient working memory.

Pre-execution planning may not involve external state access.

Any operation touching external state, including read-only queries, belongs to an execution class requiring prior authorization.

### 3.5 State Traceability

All state changes are logged, bounded in scope, and recoverable within defined constraints.

---

## 4. Automation / Autonomy Boundary

The architectural boundary between automation and autonomy is determined by the following test:

**Can the system initiate new goal-directed execution without fresh external authorization?**

If no, the system remains within the Automated Intelligence class.

If yes, autonomy has begun and the system has exited the class.

Serving an authorized objective by unauthorized means constitutes the immediate beginning of autonomy.

Authorization is class-specific, not intent-specific.

---

## 5. Key Structural Insight

Automated Intelligence is defined by authorization topology, not by behavior.

Not:

> What the system does.

But:

> What the system is permitted to initiate.

This distinction is the architectural foundation of the class.

---

## 6. Status

This definition is version-locked.

Revisions require a subsequent version.

This document constitutes the formal class definition referenced throughout the Automated Intelligence publication series.

Its explanatory companion is published as Segment 2A.
