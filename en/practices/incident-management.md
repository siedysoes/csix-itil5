# Incident Management

Incident Management is the practice of restoring normal service operation as quickly as possible and minimizing business impact when a service is disrupted. For help desk and service desk analysts it is the daily core skill: firefighting done well means fast, calm, well-communicated restoration instead of chaos.

## Incident vs problem vs request

| Type | Situation | Goal | Timeframe |
| --- | --- | --- | --- |
| Incident | Service is down or degraded | Restore service now | Immediate |
| Problem | Root cause unknown — can exist with no incidents yet | Find and remove the cause | Investigative, can run long |
| Request | Pre-agreed normal work, nothing is broken | Fulfill via a defined workflow | Planned, within target |

Classify at intake, not at closure. A recurring incident may signal a problem, and a request for access is never an incident.

## The incident lifecycle

```text
detect → log & categorize → prioritize (impact × urgency) → assign / escalate
       → diagnose → resolve → verify → close
```

1. **Detect** — monitoring alert, user contact, or another team's notification.
2. **Log & categorize** — one record with a clear category and subcategory; this powers later reporting.
3. **Prioritize** — priority comes from impact × urgency, not from how loudly someone asks.
4. **Assign / escalate** — functional escalation to a specialist, hierarchical escalation to management when needed.
5. **Diagnose** — apply a known fix or a workaround.
6. **Resolve & verify** — confirm with the user or with monitoring that service is actually restored.
7. **Close** — record the resolution and any workaround for Problem Management.

### Functional vs hierarchical escalation

- **Functional**: the ticket moves to a team with the right skills (network, application, vendor).
- **Hierarchical**: management is brought in when the incident needs authority, visibility, or extra resources — especially during major incidents.

## Key terms

| Term | Meaning |
| --- | --- |
| Incident | An unplanned interruption or reduction in quality of an IT service |
| Impact | How much the business or its users are affected |
| Urgency | How quickly resolution is needed given the circumstances |
| Priority | Combined result of impact and urgency (P1–P4), used for sequencing |
| Escalation | Moving the incident to a more specialized team (functional) or to management (hierarchical) |
| Major incident | A high-impact incident requiring coordinated, urgent handling |
| Workaround | A temporary way to restore service without fixing the cause |
| Swarming | Bringing the right people together on one ticket instead of passing it between queues |

## Priority matrix (typical example)

Every organization defines its own matrix, response targets, and restore targets — verify the values used in your own environment. The numbers below are an illustrative example only.

| Priority | Impact | Urgency | Typical response | Typical restore expectation |
| --- | --- | --- | --- | --- |
| P1 — Critical | High | High | Minutes | Immediate, continuous work until restored |
| P2 — High | High | Low | Same business day | Hours to a few days |
| P3 — Medium | Low | High | Same business day | Hours to a few days |
| P4 — Low | Low | Low | Next business day | Next release or maintenance window |

Urgency can be raised by business timing (for example a month-end close), but impact is a property of the service — always note why a priority was changed.

## What a good incident record contains

- **User and affected service** — who is impacted, not only which system.
- **Symptoms in the user's words** — plus what you observed yourself.
- **Category and subcategory** — chosen at logging time, not at closure.
- **Timeline of actions** — so anyone can pick the ticket up cold.
- **Resolution or workaround** — the line Problem Management will reuse.

## Major incident handling

- Appoint an **incident manager** to coordinate the response and own the timeline.
- Appoint a **communications lead** to keep users, stakeholders, and leadership informed.
- Run a **bridge call** with responders; keep technical discussion there instead of in scattered email threads.
- Send **brief, regular status updates** — what is known, what is being done, when the next update comes. Never go silent.

```text
[14:30] Logins failing for EU users. Suspected database connection exhaustion.
        Team restarting pool nodes. Next update in 15 minutes.
```

After restoration, run a major incident review and hand the findings to Problem Management.

## Good incident practices

| Do | Why it helps |
| --- | --- |
| Give the user a single point of contact | Avoids duplicate work and mixed messages |
| Categorize properly at logging | Makes queue management and reporting accurate |
| Keep the user informed | Trust, and fewer "any update?" follow-up tickets |
| Never close without confirming restoration | Prevents false closures and reopened tickets |
| Record the workaround | Feeds Problem Management and the knowledge base |
| Prioritize from impact × urgency | Fair sequencing instead of loudest-voice-first |

## Common pitfalls

| Pitfall | Consequence |
| --- | --- |
| Categorizing only at closure | Reports are useless; no reliable trend data |
| No major incident process | Everyone talks at once, updates stop, the outage drags on |
| Closing tickets the user never confirmed | Service is still broken for the user; trust erodes |
| "Resolved" status while the service is still degraded | Metrics look good, reality does not |
| Escalating late or not at all | Impact grows while the clock runs |

## Metrics

Track responsiveness and recovery with concepts like **MTTA** (mean time to acknowledge) and **MTTR** (mean time to restore) rather than raw ticket counts, and read them alongside categories. See [Metrics & KPIs](../career/metrics-kpis.md) for how these fit into a wider KPI set.

## In the service value chain

Incident Management sits mainly in **Deliver & Support**, with **Engage** for user communication and **Improve** when incident trends feed improvement work.

## See also

- [Problem Management](problem-management.md)
- [Service Request Management](service-request-management.md)
- [The Service Value System](../fundamentals/service-value-system.md)
- [ITSM Roles & Career](../career/itsm-roles.md)
- [Metrics & KPIs](../career/metrics-kpis.md)
