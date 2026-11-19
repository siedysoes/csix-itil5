# Guiding Principles

The seven guiding principles are ITIL's universal advice: recommendations that guide an organization in all circumstances, regardless of changes in goals, strategy, type of work, or management structure. They exist so that a team can make consistent decisions without a rulebook for every situation — which is why they anchor both ITIL 4 and ITIL 5.

## What a Guiding Principle Is

A guiding principle is not a mandatory process step; it is a recommendation you *tailor* to your context. Principles apply at every level: a service desk analyst can use "Keep it simple and practical" when designing an email template, and a CIO can use the same principle when approving a transformation program. When principles conflict (they will), you weigh them against the outcome that creates value — there is no fixed priority order.

> Note: ITIL 5 keeps the same seven guiding principles, unchanged from ITIL 4. **Verify current wording on peoplecert.org / official documentation.**

## The 7 Principles at a Glance

| Principle | Meaning | Practical example in an IT team |
| --- | --- | --- |
| Focus on value | Everything the organization does must map to value for someone | Prioritize the password-reset queue over internal reporting because users are blocked |
| Start where you are | Assess current capabilities before building from scratch | Reuse the existing ticket categories instead of redesigning the whole taxonomy |
| Progress iteratively with feedback | Do work in small steps, review, adjust | Roll the new portal to one department first, then expand |
| Collaborate and promote visibility | Involve the right people; make work and decisions visible | Shared backlog board anyone can see, not a private spreadsheet |
| Think and work holistically | Consider the whole service, not one component | Check downstream monitoring and support docs before go-live |
| Keep it simple and practical | Remove steps that don't contribute to value | Cut the change-approval chain from five approvals to two |
| Optimize and automate | Improve first, then automate the improved process | Fix the broken triage flow before scripting it |

## Deep Dives

### Focus on value

Ask "value for whom?" constantly — customer, user, shareholder, or your own team. An activity with no clear value consumer is a candidate for removal. For example, a weekly status report nobody reads has no value; a monitor that alerts before customers notice an outage does. Value is co-created: it only counts when the customer's outcome improves, not merely when the ticket closes.

### Start where you are

"Start where you are" means honestly assess your current state — including what already works — rather than assuming a greenfield rebuild is needed. Importantly, it does *not* mean "never change": you evaluate what exists with evidence (data, observation), keep what serves you, and change what does not. A team that inherits a legacy ticketing system might keep its working request forms while replacing only the reporting layer.

### Progress iteratively with feedback

Large-bang projects hide problems until it is too late to correct them cheaply. Break work into small, manageable increments, deliver them, gather feedback, and adjust the next increment. A rollout of self-service password reset to 50 users before 5,000 produces fast, cheap lessons. Feedback loops — not just plans — drive the work.

### Collaborate and promote visibility

Decisions made in a vacuum by one team tend to fail in contact with reality. Collaborate with everyone whose work is affected: operations, security, the business, and suppliers. Visibility means dashboards, public backlogs, and open incident channels — when everyone can see the same information, trust rises and surprises drop. A major incident bridge call works precisely because it puts all parties in one visible channel.

### Think and work holistically

A service is more than the server it runs on: it includes documentation, support skills, contracts, data, and user expectations. Optimizing one component at the expense of the whole system creates local wins and global failures — faster builds that operations cannot support. Holistic thinking also covers the four dimensions: check organizations and people, information and technology, partners and suppliers, and value streams for every significant change.

### Keep it simple and practical

Every process step must justify its existence. Complexity accumulates quietly — extra approval fields, redundant reporting, "we've always done it" handoffs — and each item costs time on every future ticket. The test is simple: if removing this step would not harm the outcome, remove it. Simple processes are also the ones people actually follow.

### Optimize and automate

Automate the repeatable, keep humans on the judgment calls. The order matters: automate a broken process and you get broken results, faster — so optimize first, then automate. Good candidates: password resets, user provisioning, disk-space alerts, routine patching. Poor candidates: incident triage for ambiguous outages, ethical or contractual judgments. Automation frees skilled people for work that needs thinking; it is not primarily a headcount tool.

## How They Work Together

- **No priority order.** The principles are a lens you apply together, not a ranked checklist.
- **When they conflict, weigh against value.** "Optimize and automate" might push for a script, while "Think and work holistically" flags that the support team cannot maintain it — value decides.
- **Use them as decision questions.** Before approving work, run it through all seven quickly; the one that trips hardest tells you where the risk is.

## Common Misuse

| Principle | Common misreading | Correction |
| --- | --- | --- |
| Start where you are | "Never change anything; our current state is fine" | Assess honestly; keep what works, change what does not |
| Optimize and automate | Used to justify layoffs | Focus on process and workload; the principle is about work, not people |
| Keep it simple and practical | "Simple" = skipping risk controls | Simplicity removes waste, not necessary controls |
| Focus on value | Interpreted as "only money matters" | Value includes user trust, risk reduction, and staff capability |
| Collaborate and promote visibility | Endless meetings instead of decisions | Collaborate with the *right* people; visibility beats ceremony |
| Progress iteratively | Endless pilots, never scaling | Iterate toward a target; each cycle must move the whole |

## Decision Walkthrough: Should We Build a New Service Desk Tool?

Run a proposed decision through the principles before committing budget:

```text
Proposal: buy a new service desk tool to replace the shared mailbox.

Focus on value            -> Who benefits? Faster responses for users;
                             measurable ticket data for the business.
Start where you are       -> The mailbox works for intake; what exactly
                             fails? Categorization and reporting.
Progress iteratively       -> Pilot with one team (2 weeks), review, expand.
Collaborate & visibility   -> Involve service desk staff, security, finance;
                             publish the evaluation criteria.
Think & work holistically -> Migration, integrations, training, and support
                             docs all needed — not just the license.
Keep it simple             -> Do we need every module, or intake + queue +
                             reporting?
Optimize & automate        -> Clean up duplicate request types BEFORE import;
                             then automate routing rules.

Verdict: phased pilot, not a big-bang purchase.
```

This is how the principles are meant to be used: not as slogans, but as a structured set of questions that surfaces risk early.

## See also

- [What Is ITIL](what-is-itil.md)
- [The Service Value System](service-value-system.md)
- [Four Dimensions of Service Management](four-dimensions.md)
