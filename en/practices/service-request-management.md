# Service Request Management

Service Request Management handles all the pre-agreed, user-initiated requests for service — information, advice, access, and changes to standard items — through a defined fulfillment process. Done well, requests feel predictable and fast for users, and plannable for the teams doing the work.

## Request vs incident vs standard change

| | Service request | Incident | Standard change |
| --- | --- | --- | --- |
| Trigger | The user wants or needs something | Something broke | A pre-approved low-risk change |
| Expected? | Yes, normal business | No, unplanned | Yes, routine |
| Outcome | Deliver the service item | Restore service | Implement the change |
| Route | Fulfillment workflow | Incident lifecycle | Standard change procedure |

## Examples of requests

| Request | Fulfillment notes |
| --- | --- |
| New starter setup | Accounts, hardware, and access by role |
| Access to a shared drive | Approval by the data owner |
| Password reset | Often self-service or automated |
| Software installation request | From an approved software list |
| Report request | Data extraction or dashboard build |
| Information or advice question | Answered from the knowledge base |

Requests are recorded, tracked, and reported like incidents — but the mindset is fulfillment, not restoration.

## The request lifecycle

```text
receive / submit → validate (is it in the service catalogue?) → authorize (if needed)
                 → fulfill (assign to fulfillment team) → verify with user → close
```

### Validation checks

```text
[ ] Is the item in the service catalogue?
[ ] Is the requester who they claim to be? (identity check)
[ ] Does the request need approval — if yes, from whom?
[ ] Is anything missing that fulfillment needs (dates, cost centre, manager)?
[ ] Which agreed target applies to this item?
```

### Who fulfills what

- The service desk handles simple, high-volume items: password resets, group membership, standard software.
- Specialist teams handle complex items: hardware builds, privileged access, custom reports.
- Anything with a cost or sensitive access routes through an explicit approval step.

## Service catalogue

The service catalogue is the list of available services and request items users can order. It is what makes requests predictable: a known item with known steps and an expected timeline, instead of ad-hoc email asks that nobody can plan for.

## Pre-authorization and standardization

- **Pre-approved items** need no per-ticket approval — they run straight to fulfillment (for example, a password reset from the approved list).
- **Sensitive items** need explicit authorization — access to confidential data, privileged systems, or anything with a cost.
- **Standard steps** keep fulfillment time consistent and make reporting meaningful: same request, same path, same definition of done.

## Self-service and automation

Portals, knowledge articles, and automated fulfillment deflect tickets — but only if the content is accurate and genuinely solves the problem. Hold a quality bar for self-service: a wrong article is worse than no article, because the user stops trusting the channel and calls anyway.

## When a request becomes an incident

If fulfilling a request reveals that something is broken — an account that should exist but does not, a service that errors when opened — stop and raise an incident instead. The two flows have different priorities, metrics, and escalation paths.

## Good request practices

| Do | Why it helps |
| --- | --- |
| Keep catalogue items short and clearly named | Users self-select the right item first time |
| Define "done" for each request type | No half-finished closures or repeat tickets |
| Review high-volume items for automation | Repetitive work is where automation pays off |
| Record approval for access-related requests | Audit trail when rights are later reviewed |

## Common pitfalls

| Pitfall | Consequence |
| --- | --- |
| Requests handled as incidents | Priority data skewed; incident metrics polluted |
| No documented fulfillment steps | Inconsistent delivery; unclear ownership |
| Unclear definition of "done" | Tickets closed half-finished; users chase again |
| Ignoring request volumes in workload planning | Sudden spikes overwhelm fulfillment teams |
| Same work logged as both incident and request | Double counting and double effort |

## Metrics

Track fulfillment time and the percentage of requests completed within target, kept separate from incident metrics — see [Metrics & KPIs](../career/metrics-kpis.md). Volume trends are also a workload-planning input, and agreed fulfillment targets usually live in the catalogue or SLA.

## In the service value chain

Service Request Management sits mainly in **Engage** (the user-facing interaction) and **Deliver & Support** (the day-to-day fulfillment work).

## See also

- [Incident Management](incident-management.md)
- [Service Level Management](service-level-management.md)
- [Guiding Principles](../fundamentals/guiding-principles.md)
- [ITSM Roles & Career](../career/itsm-roles.md)
- [Metrics & KPIs](../career/metrics-kpis.md)
