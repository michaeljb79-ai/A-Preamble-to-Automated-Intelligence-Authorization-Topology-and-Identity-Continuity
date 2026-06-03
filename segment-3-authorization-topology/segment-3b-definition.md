# Segment 3B — The Authorization Topology Definition

**Version:** v1

**Copyright Registration:** 1-15144595061 (filed as *The Missing Layer: Authorization Topology and the Open-Scope AI Problem*)

**Classification:** Architectural Topology Definition

---

## 1. Architectural Definition

Authorization topology is the architectural arrangement of authority origin, evaluation, and enforcement that satisfies the invariants defined in §4 under the participant roles defined in §3.

A system operates under an authorization topology if and only if all invariants hold across all proposed actions.

---

## 2. Core Distinctions

### 2.1 Capability

The set of actions the architecture is constructed to perform.

### 2.2 Authority

The set of actions the system is permitted to initiate.

### 2.3 Authorized Action Space

> Authorized ⊆ Architectural

---

## 3. Topology Participants

### 3.1 Principal

An entity that grants and revokes authorization and exists outside the execution scope of the actor. The principal relationship is non-reflexive. The actor cannot occupy this role for itself.

### 3.2 Actor

A system that proposes actions under authorization. The actor possesses capability and may issue proposals. It does not originate authority.

### 3.3 Authorization Layer

The mechanism through which proposed actions are evaluated against current authorization state.

### 3.4 Environment

The external state upon which executed actions operate. The environment is distinct from the actor's transient working memory.

---

## 4. Invariants

- **Invariant 1 — Authority Externality:** Authority originates externally to the actor. The actor may propose actions. The actor may not grant its own authorizations.

- **Invariant 2 — Class Authorization:** Authorization is granted to action classes. Authorization for one class does not imply authorization for another.

- **Invariant 3 — Scope Non-Expansion:** Authorization scope does not expand without explicit fresh authorization from the principal. Changed conditions, goal persistence, inferred benefit, and execution convenience do not constitute authorization.

- **Invariant 4 — Pre-Execution Evaluation:** Authorization is evaluated before any operation that affects environment state begins.

- **Invariant 5 — Objective / Means Separation:** Authorization of an objective does not authorize the action classes that may serve the objective. Each action class requires its own authorization.

- **Invariant 6 — External Gate:** The authorization layer remains structurally independent from the actor's reasoning process. Authorization evaluation does not originate from the actor's own reasoning authority.

- **Invariant 7 — Composite Integrity:** Composite actions are decomposed into constituent action classes prior to authorization evaluation. If any constituent class lacks authorization, the composite is rejected in its entirety before any constituent action executes.

---

## 5. Automation / Autonomy Boundary

The architectural boundary between automation and autonomy is determined by the test:

**Can the system initiate new goal-directed execution without fresh external authorization?**

If no, the system remains within authorization topology.

If yes, the system has crossed the automation/autonomy boundary.

Serving an authorized objective through unauthorized action classes constitutes the immediate beginning of autonomy. Authorization is class-specific, not intent-specific.

---

## 6. Key Structural Insight

Authorization topology is not the actor's behavior.

**Not:** What the system can do.

**But:** The structural arrangement of who decides what it may do, when, and by what mechanism.

This distinction is the architectural foundation of the topology.

---

## 7. Classification

Authorization topology was first established in *The Missing Layer: Authorization Topology and the Open-Scope AI Problem* (Copyright Registration No. 1-15144595061). It is the architectural property required by Clauses 1, 2, 3, and the Automation/Autonomy Boundary of *The Automated Intelligence Class Definition v5* (Copyright Registration No. 1-15144594701).

This document restates the topology in formal definition-grade form with one elevation: Scope Non-Expansion as Invariant 3, formerly captured implicitly within the Automation/Autonomy Boundary test.

Automated Intelligence is the architectural class of systems exhibiting reasoning capability under authorization topology. Artificial Intelligence is a capability descriptor. It does not specify the topology under which capability operates.

---

## 8. Status

This definition is version-locked. Revisions require a subsequent version. The version-locked text may not be edited, rewritten, reformatted, or silently cleaned.

This document constitutes the formal authorization topology definition referenced throughout the Automated Intelligence publication series. Its accessible companion is published as Segment 3A.
