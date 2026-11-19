# Change Enablement

Change Enablement ensures that changes — including emergency changes — are assessed, authorized, scheduled, implemented, and reviewed with minimal risk and disruption. ITIL 4 renamed the older "Change Management" practice to "Change Enablement"; verify current terminology on peoplecert.org / official documentation, since practice names, definitions, and exam content change between releases.

## What counts as a change?

| Change example | Notes |
| --- | --- |
| New hardware | Servers, switches, fleet laptop deployments |
| Software updates | Patches, version upgrades, new applications |
| Configuration changes | Firewall rules, DNS records, permission tweaks |
| Process changes | A new approval step, revised support hours |
| Decommissioning | Retiring hardware, applications, or environments |

If it alters a service, its components, or how it is run, it is a change. The point of the practice is making risk visible before implementation — not adding bureaucracy for its own sake.

## Three change types

| Type | Authorization | Risk & familiarity | Handling |
| --- | --- | --- | --- |
| Standard | Pre-authorized | Low risk, well-understood, repeatable | Follows a documented trigger and procedure (e.g. password reset, routine patch from the approved list) |
| Normal | Assessed and authorized before implementation | Varies | Most changes; risk assessment and approval required |
| Urgent / emergency | Authorized fast because of urgency | Often higher risk | Implemented quickly, still reviewed afterwards |

### Classifying examples

| Change | Type | Why |
| --- | --- | --- |
| Applying a routine OS patch from the approved list | Standard | Pre-approved, low risk, documented procedure |
| Upgrading a database to a new major version | Normal | Needs assessment, testing, and approval |
| Rolling back a broken deployment at 02:00 | Emergency | Delay would cause more harm; review follows |

## The change flow

```text
raise change → classify (standard / normal / emergency) → assess risk & impact
             → authorize (change authority; CAB as advisory) → schedule (change window)
             → implement → verify → review (post-implementation review)
```

## Change roles

| Role | Responsibility |
| --- | --- |
| Requester | Raises the change with a clear business or technical justification |
| Change authority | Approves the change; the level depends on risk and scope |
| Change manager | Runs the process, maintains the schedule, ensures assessments actually happen |
| CAB (Change Advisory Board) | Provides expert input and advice — in ITIL 4+ the CAB's role shifted toward advisory rather than final approval; verify wording |

## The change calendar

A shared view of scheduled changes, releases, and freeze periods. It prevents collisions between teams, shows stakeholders what is happening, and makes it clear when a freeze protects a critical period rather than blocking everything by default.

## Risk and impact checklist

Before a normal change is authorized, confirm:

```text
[ ] What can go wrong? (likelihood of failure)
[ ] How bad would it be? (impact on users and services)
[ ] Backout plan: how do we revert if it fails?
[ ] Testing: tried in a lower environment first?
[ ] Dependencies: other systems, teams, or changes affected
[ ] Timing: change window, blackout periods, business calendar
[ ] Communication: who needs to know before, during, and after
```

## Emergency changes

Emergency changes may be implemented before full authorization when delay would cause greater harm — retrospective approval is allowed. They still need a record, an assessment as far as time allows, a backout plan where feasible, and a post-implementation review; urgency does not cancel accountability.

### Triage under pressure

Not every change during an incident is an emergency:

- Does waiting make the impact worse? If yes, treat it as an emergency change.
- Can it wait for the next scheduled window? If yes, raise a normal change for that slot.
- Is it already covered by a standard procedure? If yes, follow that procedure even under pressure.

## Common pitfalls

| Pitfall | Consequence |
| --- | --- |
| Rubber-stamping every change | The process becomes a formality; risk goes undetected |
| No backout plan | A failed change turns into an outage with no easy exit |
| Skipping the post-implementation review | Repeat failures; lessons never captured |
| Freezing all changes during an incident | Healthy work blocked instead of triaged by risk |
| Overlapping changes in the same window | When something breaks, nobody knows which change caused it |

## Metrics

Change success rate, failed changes, emergency change share, and changes implemented inside their window are common indicators — see [Metrics & KPIs](../career/metrics-kpis.md). Read them with context: a high emergency-change share is a signal to investigate, not an automatic failure.

## In the service value chain

Change Enablement sits mainly in **Design & Transition** (assessing and authorizing what moves into live use) and supports **Obtain/Build** when components are procured or built.

## See also

- [Problem Management](problem-management.md)
- [Information Security Management](information-security-management.md)
- [Four Dimensions of Service Management](../fundamentals/four-dimensions.md)
- [Metrics & KPIs](../career/metrics-kpis.md)
