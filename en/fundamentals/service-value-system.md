# The Service Value System

The Service Value System (SVS) describes how all the components and activities of an organization work together as a system to create value. It is ITIL's big-picture model: rather than a linear lifecycle, it shows the standing ingredients (principles, governance, chain, practices, improvement) and the flow (value chain) that turns opportunity and demand into value.

## What the SVS Is

Value is **co-created**: the provider creates potential value through services, and the customer realizes value by actually using them. The SVS is the set of components that make that co-creation repeatable. Key ideas:

- It is a **system**: the parts are interdependent — practices fail without governance, the value chain stalls without improvement.
- It takes **opportunity and demand** as inputs and produces **value** as an output.
- Its wording stabilized with ITIL 4 and continues into ITIL 5, which adds an ITIL Value System view. **Verify current terminology on peoplecert.org / official documentation.**

## The 5 SVS Components

| Component | What it contributes |
| --- | --- |
| Guiding principles | Common direction and decision-making guidance for everyone |
| Governance | The means of evaluating, directing, and monitoring the organization's work |
| Service value chain | The interconnected activities that convert demand into value |
| Practices | Sets of organizational resources designed to perform work or achieve an objective (34 in total) |
| Continual improvement | The habit of aligning all work with changing needs over time |

## The Service Value Chain: 6 Activities

The value chain is the operating model inside the SVS. The six activities are not a strict sequence — they interlink and iterate depending on the value stream.

| Activity | What it does |
| --- | --- |
| Plan | Understand the shared vision, set direction, policies, and constraints |
| Improve | Ongoing improvement of products, services, and practices across all dimensions |
| Engage | Understand stakeholder needs, maintain relationships and transparency |
| Design & Transition | Ensure services meet expectations for quality, cost, and time-to-market — and move them to live |
| Obtain/Build | Acquire or create service components (hardware, software, licences, scripts) |
| Deliver & Support | Deliver services as agreed and provide support to users |

```text
                 opportunity & demand
                        |
                        v
   +----------------------------------------------+
   |  Plan <----> Engage <----> Improve           |
   |    |            |              ^             |
   |    v            v              |             |
   |  Design & Transition --> Obtain/Build        |
   |    |                         |               |
   |    +-----> Deliver & Support-+               |
   +----------------------------------------------+
                        |
                        v
                     value

  (activities iterate; the loop never "ends")
```

## Value Streams vs the Value Chain

The **value chain** is the set of activities available. A **value stream** is one specific path through those activities, taken to satisfy a particular request. Every request type has its own stream, and mapping them exposes waste.

Worked example — **"new laptop request"**:

```text
Engage            -> user submits request via portal; service desk acknowledges
Plan              -> policy check: standard build, approved vendor, budget ok
Design & Transition-> configure standard laptop profile (pre-agreed design)
Obtain/Build      -> procure device from vendor; image and encrypt
Deliver & Support -> hand over at desk; user signs; support docs updated
Improve           -> measure lead time; fix the slowest step next quarter
```

Worked example — **"software bug fix"**: Engage (bug reported) → Plan (prioritized in backlog) → Design & Transition (fix designed, tested, released) → Obtain/Build (code/component built) → Deliver & Support (deployed, user notified) → Improve (root cause fed back). Trace your own team's most common request this way; the longest wait between activities is usually where the problem lives.

## Continual Improvement: The Engine

Improvement is what keeps the system adapted to change. ITIL describes a **continual improvement model** — a repeating cycle often summarized conceptually as:

1. What is the vision? (align with the organization's direction)
2. Where are we now? (baseline, with data)
3. Where do we want to be? (target state)
4. How do we get there? (the plan)
5. Take action (implement, incrementally)
6. Did we get there? (measure against the baseline — then loop)

**Verify the official wording of the model's steps on peoplecert.org / official documentation.** The point is that improvement is a loop attached to *everything*, not an annual project: each of the six value-chain activities includes improvement in how it operates.

## Common Confusions

Beginners often mix up these terms. One-line disambiguation:

| Term | What it is |
| --- | --- |
| Service Value System | The whole system: all five components working together |
| Service Value Chain | Just the operating model: the six interconnected activities |
| Value stream | One specific route through the chain for one type of request |
| Practice | A defined capability (e.g. Incident Management) that uses the chain |
| Lifecycle (ITIL v3) | The older, stage-based model the value chain replaced |

## Terminology Note

The SVS and value-chain terminology was introduced and stabilized with ITIL 4 (2019) and is carried forward in ITIL 5 (announced January 2026), which layers on an ITIL Value System view and emphasizes value stream mapping. Practice counts and groupings differ between versions — **verify current structure and wording on peoplecert.org / official documentation** before using any of this in exam preparation.

## See also

- [What Is ITIL](what-is-itil.md)
- [Guiding Principles](guiding-principles.md)
- [Four Dimensions of Service Management](four-dimensions.md)
- [Change Enablement](../practices/change-enablement.md)
