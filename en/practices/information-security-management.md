# Information Security Management

Information Security Management protects the confidentiality, integrity, and availability of information and services. It is one of the practices in the ITIL framework and the bridge that connects day-to-day IT service management with security — every incident, change, and access request carries a security angle.

## The CIA triad

| Principle | Meaning | Simple example |
| --- | --- | --- |
| Confidentiality | Only authorized people can see it | Payroll data visible only to HR |
| Integrity | Data is accurate and unchanged | An order total nobody can silently edit |
| Availability | Services are there when needed | The intranet up during working hours |

### Everyday habits

- Verify identity before disclosing, changing, or resetting anything.
- Grant the smallest access that completes the task.
- Log what you did — an unlogged action cannot be reviewed later.

## Why security belongs in ITSM

- An **incident** can be a security incident — data exposure, malware, account takeover.
- A **change** can break security — a firewall rule opened "temporarily".
- A **request** can leak access — rights granted too broadly or to the wrong person.

Security is a habit applied inside every practice, not a separate silo that appears at the end.

### Security angles in everyday work

| Practice | The question to ask |
| --- | --- |
| Incident Management | Could this be a security incident? If suspected, escalate early |
| Change Enablement | Does this change weaken or bypass a control? |
| Service Request Management | Is this access justified, approved, and time-bound? |
| Problem Management | Do recurring failures point to a control weakness? |

## Security controls

| Type | Purpose | Examples |
| --- | --- | --- |
| Preventive | Stop the unwanted event | Firewall, access control, MFA |
| Detective | Notice that it happened, or is happening | Logging, monitoring, alerting |
| Corrective | Limit damage and recover | Patching, restore from backup |

Controls overlap: a detective control does not stop an attack, but it shortens how long the attack runs unseen. The aim is not perfect security — it is reducing risk to a level the business accepts and can explain.

## Risk basics

```text
asset → threat → vulnerability → impact → risk
```

Example: a customer database (asset) faces unauthorized access (threat); the server is unpatched (vulnerability); records could be exposed (impact) — the resulting risk tells you whether to patch now, monitor, or restrict access. Risk language is how you prioritize, because you cannot protect everything equally.

## Security incident handling

A security-flavored incident still flows through Incident Management, with containment steps and early escalation to the security team:

```text
detect → contain → eradicate → recover → learn
```

- **Contain**: stop the spread — isolate the host, disable the account.
- **Eradicate**: remove the cause — malware, malicious account, vulnerable configuration.
- **Recover**: restore service and verify it is clean.
- **Learn**: feed findings to Problem Management and to the controls themselves.

Suspected data exposure may carry legal and notification duties — escalate, and do not investigate alone.

## Access requests: a practical flow

```text
verify identity → confirm the business need → check approval (data / system owner)
                → grant least privilege → set a review or expiry date → log the grant
```

Least privilege means granting only what the task requires. A review or expiry date is what stops "temporary" access from becoming permanent.

## Linking to other frameworks

ISO/IEC 27001 is the certifiable information security management standard, and ITIL provides the service management practice around it — the day-to-day work of embedding security in how services are run. Verify details against official documentation; this resource does not restate standard requirements.

## Common pitfalls

| Pitfall | Consequence |
| --- | --- |
| Security as an after-the-fact checkbox | Problems found late, at much higher cost |
| Access granted "just this once" and never revoked | Privileges accumulate; insider risk grows |
| No periodic review of user rights | Former staff or dormant accounts still have access |
| Ignoring third-party and supplier risk | The weakest link is often an unmanaged vendor |
| Treating security tickets as lower priority | Small exposures quietly become big incidents |

## Defensive framing

This practice is about protecting services and the people who rely on them — understanding it helps you spot risk early and keep services trustworthy. This is an independent, unofficial study resource; ITIL is a PeopleCert trademark.

## In the service value chain

Information Security Management contributes to **Deliver & Support** (operating securely day to day), **Design & Transition** (building security into new services), and **Improve** (raising the security baseline over time).

## See also

- [Change Enablement](change-enablement.md)
- [Incident Management](incident-management.md)
- [Four Dimensions of Service Management](../fundamentals/four-dimensions.md)
- [What Is ITIL](../fundamentals/what-is-itil.md)
