# Evidence and audit procedures

## Evidence quality

IIA Standard 14.1 (Gathering Information for Analyses and Evaluation) asks for information that is **relevant, reliable and sufficient**; Standard 14.6 (Engagement Documentation) asks that documentation be sufficient for another competent auditor to repeat the work and reach the same conclusions [S8].

| Quality | Question for a behavioral signal | Example |
|---|---|---|
| Relevant | Does it bear on the control objective being tested? | Waiver records are relevant to "DD is current for critical suppliers"; general office mood is not |
| Reliable | Where did it come from, can it be altered, is it independent? | System-generated override log > manager's summary of overrides |
| Sufficient | Is there enough, from enough sources, to support the conclusion? | One soft indicator is not sufficient; indicator + log analytics + document inspection may be |

## Corroborating qualitative observations

Qualitative signals (from [indicators](../02-behavior-risk-map/indicators.md)) are leads. Before they support a finding:

1. **Record** the observation: date, source, auditor, exact wording or document reference.
2. **Corroborate** with at least one independent, more reliable source (system log, contract record, test data).
3. **Seek the innocent explanation** and document whether it holds - Standard 4.3 (Professional Skepticism) applies both ways: question management's statements and the auditor's own first reading [S8].
4. **Grade the evidence** using the ladder from [power-behavior-risk-indicators](https://github.com/Starboy1968/power-behavior-risk-indicators/blob/main/02-framework/qualitative-methods.md): single observation, repeated pattern, corroborated pattern. Only a corroborated pattern supports a finding.
5. **Frame the finding on the process** (criteria vs. condition, Standard 14.2), not on a person's character or motives.

## Documenting interviews and observations in workpapers

| Item | What to record |
|---|---|
| Inquiry / interview | Date, roles present, questions asked, answers as stated, documents referred to, follow-ups; mark what was corroborated and how |
| Observation (e.g., attending an S&OP meeting) | Announced in advance, scope, what was observed (process steps, not personalities), limitations (observer effect) |
| Walkthrough | Each process step, control, evidence inspected, gaps |
| AI-assisted analytics | Data source and extract date, completeness check, tool/model and version, prompt or rules, parameters, output file, who reviewed it, what was re-performed |

## How auditors use behavioral and AI signals in procedures

| Audit step | How behavioral / AI signals feed in |
|---|---|
| Risk-based planning (Standards 9.4, 13.2) | Indicator clusters and AI concentration maps help pick which suppliers, processes and periods to audit |
| Fraud risk brainstorming | Use COSO Principle 8 (consider potential for fraud, incl. incentives/pressures, opportunity, attitudes/rationalization) [S6]; quarter-end expedite spikes and bank changes are inputs |
| Inquiry | Ask process questions prompted by the signal ("How are waivers approved?"), not accusatory ones |
| Observation | Attend S&OP or supplier reviews, with notice, to see if challenge happens |
| Walkthroughs | Follow one deviation acceptance or bank change end to end |
| Analytics | Full-population tests on logs instead of samples (see [ai-in-audit.md](ai-in-audit.md)) |
| Testing management override | COSO treats override as an inherent limitation of internal control and distinguishes it from documented, legitimate management intervention [S6]. Procurement analogs of journal-entry testing: supplier master changes, after-the-fact POs, approvals above limit, releases over Quality objection, all near period end |
| Follow-up (Standard 15.2) | Confirm corrective actions were implemented; re-run the same analytics to see if the pattern changed |

## What a good finding looks like here

- **Condition:** "In 14 of 40 critical suppliers, DD was waived two or more times with the same reason." *(illustrative)*
- **Criteria:** Policy requires full DD refresh every 24 months; waivers limited to one.
- **Cause (process-level):** No expiry on waivers; single relationship owner; no second-line review.
- **Effect / risk:** Deterioration in critical suppliers may go unseen (link to OTIF trend).
- **Recommendation:** Waiver expiry, second-line approval, rotation or second reviewer.
- **Not included:** speculation about any individual's motives.

---
[Back to auditing](README.md) | [Back to project README](../README.md)
