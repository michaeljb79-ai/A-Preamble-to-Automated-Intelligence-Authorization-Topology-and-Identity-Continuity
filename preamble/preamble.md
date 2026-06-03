# A Preamble to Automated Intelligence, Authorization Topology, and Identity Continuity

> *We are presenting distinctions that repeatedly appeared during the work and proved useful enough to name. Here is what we noticed.*

---

## Section 1 — Why This Work Exists

The prevailing conversation surrounding artificial intelligence often treats governance as a capability question. As a result, discussions about safety, alignment, and autonomy frequently begin and end with capability itself.

To see the distinction, consider a familiar example: a surgeon. A surgeon may possess world-class medical knowledge, diagnostic reasoning, and technical precision. Yet capability alone does not grant authority to perform surgery, even when working within the hospital. Authority arises through a separate mechanism: the patient's consent. The surgeon may provide recommendations, expertise, and options, but the patient remains the source of authorization.

This distinction is largely uncontroversial in medicine, law, finance, and many other domains. However, it becomes less clear when discussing artificial intelligence. As systems become more capable, discussions about authority often collapse into discussions about capability itself.

### The Industry's Implicit Model

```
┌───────────────────┐
│ More Intelligence │
└───────────────────┘
          ↓
┌───────────────────┐
│  More Capability  │
└───────────────────┘
          ↓
┌───────────────────┐
│  Better Outcomes  │
└───────────────────┘
```

This framing leaves an important question unanswered. Capability can describe what a system is able to do, but capability alone does not explain what the system specifically is, what it is allowed to do, or how it remains bounded over time. While capability and authority are related, they are not the same thing.

### An Observation

```
                    Capability
                        │
              Does not answer by itself
                        │
        ┌───────────────┼───────────────┐
        ▼               ▼               ▼
      Entity        Authority       Continuity
   (What is it?)  (Who decides?)  (What persists?)
```

During the development of the work, a recurring pattern emerged. We repeatedly encountered questions that could not be answered through capability alone. Before discussing behavior, optimization, or alignment, we found ourselves returning to three prior questions:

- What is the automated entity being discussed?
- Who authors the scope of its actions?
- What persists across time?

These questions revealed what we came to regard as a structural gap.

Various industries have built mature operational structures for managing capability, performance, intelligence, reasoning, optimization, and prediction. By comparison, questions of entity, authority, and continuity are rarely treated as primary architectural concerns within artificial intelligence. While structural models exist in adjacent disciplines to verify what is the action, what was the result and who authorized it, these architectural patterns are rarely applied directly to the open-scope action problems emerging in modern AI.

As a result, discussions about intelligence, safety, alignment, autonomy, authority, and continuity frequently become entangled. Concepts that serve different structural roles are often treated as if they describe the same underlying question: *capability*.

The distinction matters.

> An automated system operating without an authorized scope represents an authority problem.

> An automated system operating without durable identity or context represents a continuity problem.

These are separate structural concerns. Neither is resolved merely by increasing the sophistication of the reasoning engine.

The purpose of this work is orientation rather than a final, exhaustive theory. Our objective is more modest: to introduce the set of distinctions that repeatedly proved useful during the work itself and to acknowledge that these questions are not yet served by a shared architectural vocabulary within the contemporary AI community.

The next sections examine three questions in turn—what an automated intelligence is, who authors the scope of its actions, and how identity persists across time. Each question identifies a distinct problem. Each leads to a distinct contribution. Together, they form the foundation of the work that follows.

---

## Scope of This Work

The distinctions introduced in this preamble emerged through three related works, each addressing one of the questions identified above.

### Automated Intelligence

**Question:** What is the automated entity being discussed?

*Automated Intelligence Class Definition v5* establishes a proposed architectural class for automated systems operating under explicit authorization topology. Its focus is not capability, but execution discipline and authorization structure.

U.S. Copyright Registration No. 1-15144594701

### Authorization Topology

**Question:** Who authors the scope of its actions?

*The Missing Layer: Authorization Topology and the Open-Scope AI Problem* examines scope authorship, runtime authorization, and the structural requirements of open-scope systems. It argues that governance challenges in AI arise from authorization architecture rather than capability.

U.S. Copyright Registration No. 1-15144595061

### Identity Continuity

**Question:** What persists across time?

*The Continuity Layer: Artifact-Mediated Identity Reconstruction and Persistent Team Architecture for AI Systems* examines persistence, reconstruction, and continuity across sessions, platforms, and model changes. It proposes identity continuity as a distinct architectural layer rather than a memory feature.

U.S. Copyright Registration No. 1-15161914101

The present work is not a substitute for these documents. It serves as an orientation to the distinctions that connect them and the problems they were developed to address.
