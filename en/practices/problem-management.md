# Problem Management

Problem Management identifies the root cause of incidents and problems so that incidents do not recur. If Incident Management is firefighting, Problem Management is the fire investigation that stops the next fire.

## Problem vs incident

| Aspect | Incident | Problem |
| --- | --- | --- |
| Timing | Reactive — starts when service breaks | Can start proactively, before any incident |
| Goal | Restore service fast | Remove the cause so incidents stop |
| Focus | One disruption | Patterns and systemic weaknesses |
| Finished when | Service is restored | Cause is fixed, or a known error is documented |

A problem can exist without any incident at all — a single point of failure that nobody has noticed yet — and one problem can sit behind dozens of seemingly unrelated tickets.

## Proactive vs reactive problem management

| Reactive | Proactive |
| --- | --- |
| Triggered by a major incident or by the same incident recurring | Triggered by trend analysis and health checks |
| Example: the third outage this month from the same batch job | Example: reviewing recurring low-priority tickets, capacity data, and error logs |

Proactive work is where the biggest payoffs sit: recurring low-priority tickets are cheap one by one and expensive in aggregate.

### Signals worth investigating

- The same error code appearing across different users or locations.
- Tickets reopened shortly after being marked resolved.
- One team repeatedly escalating the same kind of ticket.
- Alerts that fire on a schedule and are routinely dismissed.
- Capacity or performance metrics drifting steadily in one direction.

## The problem lifecycle

```text
detect / categorize → root cause analysis → record known error → document workaround
                    → fix via change (Change Enablement) → verify → close
```

## Known error

A problem whose root cause **and** workaround are documented is a **known error**. It stays open until a permanent fix is implemented — the workaround keeps users working while the investigation continues, and it gives the service desk something concrete to offer during incidents. Moving from known error to closed normally means raising the fix through [Change Enablement](change-enablement.md).

## Root cause analysis techniques

| Technique | How it works |
| --- | --- |
| 5 Whys | Keep asking "why" until you reach a systemic cause rather than a symptom |
| Fault tree | Decompose the failure into branches of contributing causes |
| Chronological analysis | Build a timeline of events to see what actually triggered the failure |

### 5 Whys in practice

```text
Why did the site go down?   → The web server ran out of memory.
Why?                        → A memory leak in the last release.
Why was that released?      → Load testing did not cover that code path.
Why not?                    → Test data did not simulate real traffic.
→ Systemic cause: a gap in release test coverage — not "the server crashed".
```

## Problem record essentials

| Field | What to capture |
| --- | --- |
| Problem statement | What is wrong, in plain language |
| Symptoms | What users and monitoring actually observed |
| Known error | Confirmed root cause, once found |
| Workaround | Temporary way to keep service usable |
| Trigger | The incident(s) or trend that raised the problem |
| Owner | The person accountable for driving it to closure |

## How the service desk contributes

- Report recurrences explicitly: "this is the fourth time this week" is a trigger, not a complaint.
- Pass symptom detail and timelines — poor incident data makes root cause analysis guesswork.
- Use known errors and workarounds at the desk, and confirm whether the workaround actually worked.
- Never let a problem record sit ownerless; ask who is driving it.

## Common pitfalls

| Pitfall | Consequence |
| --- | --- |
| Stopping at the first cause ("the server crashed" — why?) | Symptom treated as cause; the incident recurs |
| No proactive review | The same small tickets repeat forever, never investigated |
| Closing when a workaround exists instead of a fix | The known error never graduates to resolution |
| Root cause analysis only after major incidents | Preventable minor incidents keep accumulating |
| Problem records with no owner | Work ages quietly in a backlog nobody reviews |

## Metrics

Useful indicators include the percentage of known errors with a documented workaround, repeat incident rate by category, and the age of open problems. See [Metrics & KPIs](../career/metrics-kpis.md) for how to present them.

## In the service value chain

Problem Management contributes mainly to **Improve** (removing recurring causes) and **Design & Transition** (feeding lessons into new or changed services).

## See also

- [Incident Management](incident-management.md)
- [Change Enablement](change-enablement.md)
- [Guiding Principles](../fundamentals/guiding-principles.md)
- [Metrics & KPIs](../career/metrics-kpis.md)
