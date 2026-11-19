# What Is ITIL

ITIL is the most widely adopted framework of best practices for IT service management (ITSM): guidance on delivering and managing IT services that create real value for customers. This page explains what ITIL actually is, where it came from, how ITIL 4 and ITIL 5 compare, and what it is not — the foundation for everything else in this learning base.

## Definition

ITIL (Information Technology Infrastructure Library) is a framework of best-practice guidance for planning, delivering, and supporting IT services that customers and the business find valuable. Two points matter for beginners:

- **It is guidance, not a rulebook.** ITIL describes *what good looks like*; you tailor it to your organization's size, risk, and culture. A five-person help desk and a global enterprise will implement it differently, and both can "do ITIL" correctly.
- **It is a framework, not a standard.** You do not certify your organization against ITIL itself (see [ITIL vs ISO 20000](#itil-vs-iso-20000) below). Individuals earn PeopleCert-held Foundation-level credentials after passing an exam.

The goal throughout is **value**: an IT activity (patching a server, resetting a password) only matters because someone downstream gets a better outcome.

## Why ITSM Matters

ITIL is the best-known way to practice ITSM. The difference between ad-hoc IT work and basic service management shows up quickly:

| Without ITSM | With ITSM |
| --- | --- |
| Chaotic tickets: requests arrive by email, chat, and hallway conversations | Clear intake: one channel, one queue, prioritized work |
| No ownership: nobody is accountable when something breaks | Clear roles: named owners for incidents, requests, changes |
| Surprise outages discovered by users | Monitored services, defined support hours, escalation paths |
| Unclear costs: nobody can say what IT actually costs | Measurable services: costs, performance, and SLAs visible |
| Every fix is reinvented | Repeatable processes that improve over time |

## Who Uses ITIL

Because ITIL is general-purpose guidance rather than a product, it appears across sectors:

- **In-house IT departments** — from small teams to enterprise IT organizations running help desks, infrastructure, and applications.
- **Managed service providers (MSPs)** — who need consistent processes to serve many clients.
- **Government and public-sector bodies** — ITIL's origin is UK government guidance, and public agencies remain heavy users.
- **Enterprises in any industry** — banking, healthcare, retail, manufacturing — wherever IT services must be reliable and accountable.

No reliable single figure for global adoption should be quoted here; treat any specific statistic you encounter with care and check its source.

## Core Terms in Brief

A few words carry most of the vocabulary in this base:

| Term | Plain meaning |
| --- | --- |
| Service | A means of enabling value co-creation without the customer directly managing specific costs and risks |
| Value | The perceived benefit, usefulness, or importance of something — for the customer, not the provider |
| Customer / User | The customer sponsors and agrees the service; the user consumes it day to day |
| ITSM | IT service management: the discipline of designing, delivering, and improving IT services |
| Practice | A set of resources designed to perform work or achieve an objective (34 in ITIL 4 and ITIL 5) |

## A Brief Version Timeline

ITIL has evolved over nearly four decades. Verify dates against official sources before citing them in study or exam contexts:

```text
Late 1980s   Originates with the UK government (CCTA) as IT service
             management guidance
Early 2000s  ITIL v2 — process-focused (e.g. service support & delivery)
2007         ITIL v3 — the service lifecycle; refreshed edition in 2011
2019         ITIL 4 — Service Value System, 34 practices, 7 guiding principles
Jan 2026     ITIL 5 announced by PeopleCert; official book
             "ITIL Foundation Global Best Practice" (5th edition)
```

Note the ownership history: ITIL was published by AXELOS, and PeopleCert acquired AXELOS in June 2021 and owns the ITIL trademark. **Verify current dates and details on peoplecert.org and official documentation.**

## ITIL 4 vs ITIL 5

ITIL 5 was announced in January 2026. Based on the published overview, the headline comparisons are:

| Aspect | ITIL 4 | ITIL 5 |
| --- | --- | --- |
| Guiding principles | 7 principles | The same 7 principles, unchanged |
| Practices | 34 practices | 34 practices, reorganized: 22 product/service + 12 general |
| Emphasis | Service Value System & value chain | Adds an ITIL Value System view, product/service lifecycle, and stronger value stream mapping emphasis |
| For ITIL 4 holders | — | "ITIL Foundation Bridge (Version 5)" module exists for credential holders |

The practice count is unchanged; the grouping and framing differ. **Verify the current structure, syllabus, and bridge-module details on peoplecert.org / official documentation** — these are exactly the details most likely to change.

## ITIL vs ISO 20000

ITIL and ISO 20000 are often confused. ISO 20000 is an international *standard*: a defined set of requirements that an organization's service management system can be audited and certified against. ITIL is *guidance*: a framework of best practices with no certification for the organization itself. In practice, teams use ITIL ideas to build the processes, then demonstrate conformance through something like ISO 20000 if certification is commercially useful. **Verify current scope and version details of both on official sources.**

## What ITIL Is NOT

- **Not a silver bullet.** Copying ITIL processes onto a dysfunctional organization produces dysfunctional processes, documented.
- **Not tool-specific.** ITSM tools (ServiceNow, Jira Service Management, and others) can support ITIL practices, but buying the tool is not "doing ITIL."
- **Not a substitute for thinking.** ITIL gives principles and structures; judgment about your context remains yours.
- **Not a rigid checklist.** Adopting everything at once is a common failure — start where you are and progress iteratively (see [Guiding Principles](guiding-principles.md)).

## How This Learning Base Is Organized

This CSIX ITIL base has three sections under `csix-itil/en/`:

1. **`fundamentals/`** — this section: what ITIL is, the guiding principles, the Service Value System, and the four dimensions.
2. **`practices/`** — deep dives into key practices such as Incident Management, Problem Management, and Change Enablement.
3. **`career/`** — exam preparation, ITSM roles, and metrics/KPIs.

Start here if you are new; jump to `practices/` for day-to-day operations or `career/` if you are preparing for the Foundation exam.

## Independence and Trademark Note

This is an **independent, unofficial study resource**. It is not affiliated with, endorsed by, or produced by PeopleCert. **ITIL is a trademark of PeopleCert** (which acquired AXELOS in June 2021). Always confirm exam format, syllabus, and credential details on peoplecert.org.

## See also

- [Guiding Principles](guiding-principles.md)
- [The Service Value System](service-value-system.md)
- [Four Dimensions of Service Management](four-dimensions.md)
- [ITIL Foundation Exam](../career/foundation-exam.md)
