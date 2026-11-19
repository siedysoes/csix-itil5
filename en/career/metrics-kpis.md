# Metrics & KPIs

Measurement is how service management learns: you can't improve what you don't measure, and the wrong metric can be worse than no metric at all. This page defines the basic terms, shows where metrics apply in common practices, and lists the mistakes that make dashboards useless. Metric terminology evolves — verify current definitions in official ITIL and organizational documentation.

## Definitions

| Term | Definition | Tiny example |
| --- | --- | --- |
| Metric | A single measurement | 42 incidents opened today |
| KPI | A metric tied to an objective that tells you if you're on track | 95% of incidents resolved within target this month |
| CSF | Critical Success Factor — the condition that must be achieved for an objective to succeed | "Users experience minimal disruption during upgrades" |
| Baseline | Where you are now, so change is measurable | Current MTTR: 4 hours |

## Metric levels

| Level | Cadence | Examples |
| --- | --- | --- |
| Operational | Daily / weekly | Tickets resolved, current backlog, incidents open |
| Tactical | Monthly / quarterly | SLA attainment, problem fix rate |
| Strategic | Yearly | Customer satisfaction, cost per ticket |

## What makes a good metric

| Rule | Notes |
| --- | --- |
| Tied to a customer-visible outcome | If customers can't feel it, question it |
| You can actually collect it | A metric nobody can gather won't survive contact with reality |
| Has a target AND a baseline | Target without baseline is a wish; baseline without target is trivia |
| Doesn't reward gaming | Goodhart's law: when a measure becomes a target it stops being a good measure |

## ITSM metrics by practice

Define targets carefully for your own context — **verify your own targets** against business needs; never copy thresholds blindly.

| Practice | Example metrics |
| --- | --- |
| Incident | MTTA, MTTR, reopen rate, % major incidents |
| Problem | Repeat incident rate, % known errors with workaround, fixes implemented |
| Change | Success/failure/rollback rate, % changes with post-implementation review |
| Request | Average fulfillment time, % fulfilled within target |
| Service Level | SLA attainment %, number of breaches, trend over time |

## Common mistakes

| Mistake | Why it hurts |
| --- | --- |
| Vanity metrics | Numbers that look good but drive no decision |
| Measuring volume instead of outcome | 100 closed tickets may mean nothing was actually fixed |
| Targets that punish quality | "Close tickets fast" encourages premature closures |
| No baseline | Without a starting point you can't claim improvement |
| Reporting nobody reads | Unread reports are cost without benefit |

### A quick sanity check before publishing a metric

- Would a customer recognize this as something they care about?
- Can two people compute the same number from the same data?
- Do we have a baseline to compare against?
- What decision changes if this number moves?

## A reporting rhythm

```text
Daily:   ops dashboard for the team — volume, open majors, blockers.
Weekly:  backlog & trends for leads — where work is piling up.
Monthly: service review with customers/stakeholders — SLA attainment, breaches, trend.
Quarterly: improvement candidates — pick 1-2 things to change next quarter.
```

## Choosing your first KPIs

Start from customer value and the guiding principle "Focus on value" (see [Guiding Principles](../fundamentals/guiding-principles.md)). Pick 1-2 metrics per practice at most — a short list you actually review beats a wall of numbers nobody trusts.

A practical selection sequence:

1. Write the objective in business language ("users get help quickly when something breaks").
2. Identify the condition that must hold (CSF: major incidents are restored within the agreed window).
3. Pick the smallest set of metrics that shows whether that condition holds.
4. Record the baseline before you change anything.
5. Set a target with a date, then review it at the agreed rhythm.

## How to collect without a data team

- Start from what your ticketing system already records — timestamps, categories, status changes.
- Agree definitions with the team before counting (what counts as an "incident"? what is "resolved"?).
- Keep a simple spreadsheet first; automate only after the definitions survive a month of use.
- Re-check definitions whenever the tooling or process changes.

## How this connects

Metrics feed continual improvement in the Service Value System: measure, compare to baseline, act, re-measure (see [The Service Value System](../fundamentals/service-value-system.md)). Service level reporting uses exactly these numbers to hold conversations with customers (see [Service Level Management](../practices/service-level-management.md)).

## Disclaimer

This is an unofficial, independent study resource. ITIL is a PeopleCert trademark. Metric terminology and recommended measures evolve — verify current metric terminology in official ITIL documentation and your organization's own reporting standards.

## See also

- [ITIL Foundation Exam](foundation-exam.md)
- [ITSM Roles & Career](itsm-roles.md)
- [The Service Value System](../fundamentals/service-value-system.md)
- [Service Level Management](../practices/service-level-management.md)
- [Incident Management](../practices/incident-management.md)
