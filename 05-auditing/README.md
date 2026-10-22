# Auditing: turning behavioral signals into audit evidence

Behavioral signals are only useful to audit if they become **evidence**: sufficient, reliable and relevant information that another competent auditor could follow and reach the same result. This folder covers the records that matter, how auditors use qualitative and AI-detected signals, how AI helps the audit, and how to audit the AI.

Anchored to the IIA Global Internal Audit Standards (2024) [S8], the IIA Three Lines Model [S9] and COSO [S6][S7]. Standard numbers below were checked against the IIA Standards document.

| File | What's inside |
|---|---|
| This page | Audit trails that matter; where audit sits (Three Lines) |
| [evidence-and-procedures.md](evidence-and-procedures.md) | Evidence quality, corroborating qualitative observations, workpapers, audit procedures that use behavioral and AI signals |
| [ai-in-audit.md](ai-in-audit.md) | How AI supports supply chain audit work, and how to audit the AI itself |

## Audit trails that matter in supply chain

| Audit trail | What it can reveal | Behavioral driver it exposes | Integrity checks before use |
|---|---|---|---|
| Supplier master changes (incl. bank details) | Changes without verification; who requested vs. approved | Authority, urgency | Log completeness; cannot be edited by requesters |
| PO and approval logs | After-the-fact POs, split POs under approval limits, approver = requester | Incentive, deadline pressure | Reconcile counts to ERP; check timestamps are system-generated |
| Override and exception logs | Overrides concentrated by role or period | Authority, deadline pressure | Confirm overrides cannot bypass logging |
| Due-diligence records | Waivers, expired items, identical boilerplate reasons | Trust, lock-in | Tracker completeness vs. supplier master |
| Risk acceptance records | Thin rationale, signed near deadlines, beyond delegated authority | Deadline, authority | Signatory authority matrix; version history |
| Contract change history | Side letters, unapproved scope or price changes, rolled-over remediation | Sunk cost, trust | Contract system vs. legal register vs. email |
| S&OP and supplier-review minutes | No alternatives or dissent recorded; deferrals without owners | Groupthink, authority | Minutes approved and versioned; attendance |
| Deviation / hold-release / RMA records | Repeated "use as is", releases over Quality objection, coding drift | Normalization, confirmation bias | Link to lab/test data |

## Where audit sits: Three Lines Model

The IIA Three Lines Model (2020) describes roles, not departments [S9]:

| Line | In this project | Responsibility |
|---|---|---|
| First line | Procurement, planning, plant, logistics, AP | Own and manage supply chain risk; run controls; respond to flags |
| Second line | TPRM, risk management, compliance, quality assurance | Expertise, monitoring and challenge; set indicator thresholds; may operate the AI triage |
| Third line | Internal audit | Independent assurance that the first two lines work - including the AI triage itself |

Internal audit may **use** AI analytics in its own work, but should not own the first- or second-line monitoring it later audits; that would compromise independence. Where audit relies on second-line monitoring, IIA Standard 9.5 (Coordination and Reliance) applies [S8].

## Scenario audit angles

Each [scenario](../04-scenarios/) has an "Audit angle" section with the procedure and evidence.

| Scenario | Main audit procedure | Key evidence |
|---|---|---|
| S1 | Full-population DD currency and waiver test | DD tracker, waivers, scorecard inputs |
| S2 | Override testing analog on supplier master, POs, expedites near period end | Change logs, call-back records, timestamps |
| S3 | Walkthrough and observation of S&OP; override analytics | Override log, minutes, forecast accuracy |
| S4 | Full-population test of deviation acceptances | Deviation log, authority matrix, objections |
| S5 | Re-performance of RMA classification against lab results | RMA records, lab reports, escalation documents |

---
[Back to README](../README.md)
