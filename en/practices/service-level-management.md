# Service Level Management

Service Level Management sets clear expectations with customers about service levels, agrees them, monitors performance against them, and drives improvement. It is the practice that makes services measurable and the customer relationship honest instead of anecdotal.

## Key documents

| Term | What it is |
| --- | --- |
| SLA — Service Level Agreement | Agreement with the **customer** (internal or external) covering service levels |
| OLA — Operational Level Agreement | Agreement **between internal IT teams** that supports an SLA |
| Contract / UC — Underpinning Contract | Agreement with an **external supplier** that supports an SLA |
| Service level target | A specific, measurable goal (for example availability or response time) |

```text
SLA  (customer ↔ IT)
 └── OLA  (IT team ↔ IT team)
      └── UC  (IT ↔ external supplier)
```

An SLA promise should be backed all the way down this chain; otherwise IT commits to something no single team can deliver. Verify exact document definitions against current official documentation.

## Customers, internal and external

The customer is whoever consumes the service — another department inside the same company, or an external client. "Internal" does not mean informal: an internal SLA still needs agreed targets, a measurement method, and a review rhythm.

### Starting simple

- Pick a small number of targets you can measure from day one.
- Choose measures the customer cares about, not the ones that are easiest to export.
- Revisit targets after the first review cycle; an untested target is a guess.

## Types of SLA

| Type | Structure | Typical use |
| --- | --- | --- |
| Customer-based | One agreement per customer | Customers with distinct needs |
| Service-based | One agreement per service | The same service used by many customers |
| Multi-level | A combination of the above | Mixed environments |

## The SLM cycle

```text
identify service requirements → define targets → draft & agree → monitor & measure
                             → report → review meeting → improve
```

## What to measure

| Measure | What it tells you | Watch out for |
| --- | --- | --- |
| Availability | How often the service is usable | Define the measurement point and maintenance windows |
| Response time | Speed of first reaction | Scope must be explicit (business hours vs 24/7) |
| Resolution time | Time to restore or fulfill | Can reward fast closure over real fixes |
| Throughput | Volume handled (tickets, transactions) | Volume alone says nothing about quality |
| Satisfaction | Customer perception | Survey design and sample size matter |

Targets must be achievable, measurable, and tied to what the customer actually values — a target nobody can influence is just noise.

## Service level reviews

Regular meetings with customers to walk through report versus target, trends, and upcoming changes. The purpose is joint improvement, not assigning blame — bring data, not excuses.

A useful review agenda:

- Performance since the last review: actual vs target.
- Trends and outliers — what is moving, and in which direction.
- Incidents and breaches, and what was done about them.
- Upcoming changes and their expected effect on levels.
- Agreed actions, owners, and dates.

## Common pitfalls

| Pitfall | Consequence |
| --- | --- |
| Targets nobody measures | Paper compliance; no real insight |
| Vanity metrics | Numbers look good while customers are unhappy |
| SLAs that reward the wrong behavior (e.g. closing tickets fast instead of fixing) | Teams optimize the metric, not the service |
| No OLAs backing the SLA | IT promises internally what it cannot deliver |
| Reviews skipped when performance is good | The relationship only exists when something is wrong |

## Design guidance

Keep it simple: ITIL 4 and later emphasize value over bureaucratic paperwork — a handful of meaningful, measured targets beats a thick agreement nobody reads. Verify current guidance on peoplecert.org / official documentation.

### Keep the agreement readable

- One short section per service: targets, measurement method, and review cadence.
- Plain language — if the customer cannot restate the target, it is not agreed.
- An owner on each side: one in IT, one in the customer's team.

## Metrics

SLA attainment percentage, the number and nature of breaches, and trends over time are the core indicators — see [Metrics & KPIs](../career/metrics-kpis.md).

## In the service value chain

Service Level Management contributes to **Plan** (understanding service requirements), **Engage** (customer communication and review meetings), and **Improve** (acting on performance gaps).

## See also

- [Service Request Management](service-request-management.md)
- [Incident Management](incident-management.md)
- [The Service Value System](../fundamentals/service-value-system.md)
- [Metrics & KPIs](../career/metrics-kpis.md)
