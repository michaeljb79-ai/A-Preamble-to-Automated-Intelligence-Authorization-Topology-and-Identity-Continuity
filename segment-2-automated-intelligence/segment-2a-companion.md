# Segment 2A — The Automated Intelligence Class: An Explanatory Companion

This paper is the accessible companion to the formal definition filed as *The Automated Intelligence Class Definition v5* (Segment 2B). It assumes the orientation established in *A Preamble to Automated Intelligence, Authorization Topology, and Identity Continuity* (DOI: 10.5281/zenodo.20468027).

---

## The Label Trap

To understand why a precise architectural class is necessary, consider a familiar domain: transportation.

A car is not a boat, a boat is not a train, and a train is not a plane. Yet all are vehicles.

The label "vehicle" is useful for everyday conversation, but it tells us very little about what a particular system actually is. It does not tell us how the system operates, what rules govern its use, who is authorized to control it, or what requirements must be satisfied before it can safely enter the world around it.

The same problem exists in artificial intelligence.

Terms such as "AI system," "agent," and "large language model" are broad descriptive labels. They tell us something about the technology being used and they may tell us something about capability. They do not tell us what structural requirements must exist before a system can operate within defined boundaries.

As a result, discussions about artificial intelligence often slide between capability and classification as though they were the same thing.

They are not.

---

## The Core Distinction

The Preamble explains why this conversation needs to exist.

It argues that contemporary discussions about artificial intelligence often focus on capability while lacking a consistent vocabulary for discussing entity, authority, and continuity as separate architectural concerns.

Having established why a new architectural vocabulary may be necessary, this paper moves from diagnosis to classification.

We begin with a foundational rule:

**Capability does not establish membership.**

A powerful engine does not make a vehicle street legal.

A vehicle belongs to a specific operational class because it satisfies the structural requirements of that class.

The same principle applies here.

If capability metrics do not determine an intelligence's classification, then membership must be determined by something else.

It must be determined by structure.

---

## Why Structure Matters

Once capability is separated from membership, a concrete engineering question appears:

What structural requirements must exist before a system belongs to a particular class?

This is the question the remainder of this paper explores.

The answer proposed by this work is not a set of safety guidelines, ethical recommendations, or behavioral best practices.

It is a proposed membership test.

An architecture belongs to the Automated Intelligence class only when it satisfies a specific set of structural invariants. Remove even one of those invariants, and membership in the class can no longer be assumed.

We call this proposed structural class:

**Automated Intelligence.**

---

## Core Structural Terms

Before stating the membership test, four terms need to be anchored.

These terms appear inside the formal definition and carry specific meanings there. The descriptions below are explanatory companions rather than formal definitions. The precise definitions appear in Segment 2B.

### Execution Class

An execution class establishes that authorization must be defined by precise, individual units of operation. In traditional environments, permissions are organized around broad capability labels. Here, similar actions are not automatically treated as the same authorization simply because they appear related on the surface.

Authorization boundaries are determined by implication, not by capability labels.

The central idea is straightforward: capability categories do not determine authorization categories.

### Principal

A principal is the entity that grants authorization and manages authorization state.

The principal exists entirely outside the execution scope of the system being authorized.

Because a system cannot grant permissions to itself, authority must always originate elsewhere.

No matter how capable the reasoning engine becomes, authority continues to come from outside the system.

### Transient Working Memory

Transient working memory refers to the system's active reasoning context during a single reasoning pass.

The key distinction is between reasoning and persistence.

A system may reason within transient working memory without interacting with the outside world. However, once information is stored, cached, written, retrieved later, or otherwise persists beyond the current reasoning pass, it is no longer transient working memory.

It has become external state.

This includes retrieval stores, vector databases, tool persistence, file storage, and similar persistent buffers. These are external state, not working memory.

Maintaining this boundary prevents systems from accumulating unauthorized persistence under the appearance of memory.

### Pre-Execution Validation Gate

The pre-execution validation gate is a mandatory checkpoint.

Every action must pass through this checkpoint before execution can begin.

The gate operates at a privilege level the reasoning engine cannot write to, modify, or bypass.

Its purpose is simple: compare the requested action against the current authorization state and determine whether execution is permitted.

Authorization is evaluated before execution, not afterward.

---

## What Makes Something an Automated Intelligence?

An architecture belongs to the Automated Intelligence class only when it satisfies five required invariants.

Each invariant is summarized below. The complete formal wording appears in Segment 2B.

### 1. Explicit Class Authorization

**Formal Definition** *"Every action belongs to an execution class..."*

**Simplified Explanation** General permissions do not exist.

Every action must belong to a specific execution class and every execution class must be explicitly authorized before execution begins.

Authority cannot be assumed and it cannot be justified after the fact.

Permission comes first.

Execution comes second.

### 2. Class-Specific Bounding

**Formal Definition** *"Authorization is class-specific..."*

**Simplified Explanation** This invariant rejects the idea that a legitimate goal automatically authorizes whatever actions are necessary to achieve it.

An approved objective does not create blanket permission.

If achieving a goal requires entering an execution class that has not been authorized, the architecture must stop and obtain fresh authorization.

The objective may remain valid.

The authority does not.

### 3. Privilege-Isolated Pre-Execution Gate

**Formal Definition** *"Behavioral boundaries are enforced by a mandatory pre-execution validation gate..."*

**Simplified Explanation** This requirement ensures that the system cannot rewrite its own boundaries.

The validation gate exists at a privilege level the reasoning engine cannot write to.

Complex actions are not evaluated as a single request. They are broken into their individual execution classes before authorization is checked.

If even one component lacks authorization, the entire action fails.

Unauthorized pieces invalidate the whole request before any part of it runs.

### 4. Execution Boundary at External State Access

**Formal Definition** *"Execution begins at the first operation that accesses, observes, or modifies any state outside the reasoning engine's transient working memory..."*

**Simplified Explanation** The most important implication of this invariant is that reading is also a form of execution.

A system may reason freely within transient working memory.

The moment it reaches outside that boundary to observe, query, inspect, or interact with external state, execution has begun.

This includes read-only operations.

Authorization is required not only to change the world, but also to inspect it.

This prevents unauthorized environmental mapping during planning.

### 5. State Traceability

**Formal Definition** *"All state changes are logged, bounded in scope, and recoverable..."*

**Simplified Explanation** An architecture cannot remain automated if its real-world impacts are invisible, unlimited, or irreversible.

Traceability requires that changes be recorded, constrained, and recoverable.

The objective is not simply accountability.

It is maintaining a bounded relationship between the system and the state it affects.

Questions of persistence, accountability, and continuity across time are explored further in the Continuity paper.

---

## Defining the Boundary

Classification is only useful if it distinguishes one thing from another.

Defining a class therefore requires defining its boundary.

Once membership in the Automated Intelligence class is established, it becomes possible to define what falls outside that class.

This creates a structural distinction between bounded automation and autonomy.

The distinction is determined by a single question:

**Can the system initiate new goal-directed execution without fresh external authorization?**

If the answer is No, the system remains an automation operating within the Automated Intelligence class.

If the answer is Yes, autonomy has begun and the system has exited the class.

Serving an authorized objective by unauthorized means constitutes the immediate beginning of autonomy.

Authorization is class-specific, not intent-specific.

This is the definitive edge of the architecture.

The defining characteristic of an Automated Intelligence is therefore not what it can do.

It is what it is structurally permitted to initiate.

---

The formal statement of these invariants, together with their precise definitions and derivation history, is filed as *The Automated Intelligence Class Definition v5* (Copyright Registration No. 1-15144594701) and published as Segment 2B of this series.
