# AI integration: where AI fits

AI is useful here for one thing: **triage**. It reads more records than a person can, ranks what looks unusual, and hands a short list to a person with the evidence attached. It does not decide what anything means. Constraints on what AI may do are in [guardrails](../07-guardrails-and-ethics.md); where decisions must sit with people is in [human in the loop](../06-human-in-the-loop/README.md).

## Five uses

| # | Use | Input data | Output | Behavioral driver it helps surface |
|---|---|---|---|---|
| AI-1 | Anomaly detection on override and exception logs | Override, exception, hold-release, expedite logs | Ranked list of unusual clusters (by period, approver role, supplier) | Authority, deadline pressure, incentives |
| AI-2 | Concentration and dependency mapping | Spend, award history, BOM, supplier surveys, tier-2 data where known | Single-source and concentration map; change over time | Optimism, incentive (savings), lock-in |
| AI-3 | Language analysis on documents, **aggregate only** | S&OP minutes, escalation reports, supplier-review minutes | Trend of minimizing / deferral wording and missing alternatives, per process or document set | Groupthink, softened escalation, optimism |
| AI-4 | LLM-assisted review of supplier due-diligence files | DD questionnaires, certificates, audit reports, waivers | Gap list: missing, expired, inconsistent items, each with a page reference | Trust ("we know them"), confirmation bias |
| AI-5 | Pairing behavioral signals with hard metrics | Outputs of AI-1 to AI-4 plus lead time, OTIF, defects, concentration | Combined watch list: where soft signal and hard metric point the same way | All |

**Why pairing matters (AI-5):** a behavioral signal alone is weak and easy to misread. A flat supplier scorecard (soft) next to falling OTIF (hard) is a much stronger reason to look.

## AI-3 boundaries (language analysis)

- Analyze **documents and processes**, not people: "escalation reports in Returns", not "what Person X writes".
- No emotion or sentiment scoring of individuals. The EU AI Act prohibits AI that infers emotions of people in the workplace, except for medical or safety reasons (Art. 5(1)(f)) [S10].
- Use business records that already exist for business purposes. No reading of private messages, no covert collection.
- Report at aggregate level with small-group suppression (do not report a trend for a group so small it identifies a person).
- Language patterns to look for are about **content**, not mood: missing alternatives, deferral ("revisit next quarter") with no owner, severity words downgraded between drafts, risks noted with no action.

## What the AI flags vs what the analyst decides

| AI flags | Analyst / owner decides |
|---|---|
| Overrides in Q4 are 3x the monthly baseline for one plant *(illustrative)* | Whether the spike has a legitimate cause and whether to escalate |
| Supplier X supplies 80% of a critical part *(illustrative)* | Whether to dual-source, accept, or hedge - and who signs |
| Supplier-review minutes for 6 cycles record no alternatives *(illustrative)* | Whether the process needs a challenge role; never a conclusion about attendees |
| DD file missing a current certificate; waiver reason "long-standing supplier" | Whether the waiver is acceptable and must be refreshed |
| Escalation wording for warranty claims softened across drafts | Whether the risk was understated and needs re-escalation |
| Scorecard flat while OTIF fell | Whether scoring criteria or scorer independence must change |
| Model confidence and known limitations for each flag | Whether to trust, override or discard the flag (logged) |

## Sample prompts

Two prompts built on the structure of the reusable [GRC risk-analysis prompt](https://github.com/Starboy1968/ai-assisted-risk-analysis/blob/main/prompt/risk-analysis-prompt.md) in ai-assisted-risk-analysis: role, rules (guardrails), inputs, output format, self-check, and a human review step. See [prompts.md](prompts.md).

## Data the AI needs (and does not)

| Needed | Not needed / not allowed |
|---|---|
| Transaction and log data (PO, approvals, overrides, expedites, master data changes) | Personal communications, chat or email of named individuals for profiling |
| Business documents (minutes, escalation reports, DD files, contracts) | Voice, video, keystroke or biometric data |
| Hard supply chain metrics (lead time, OTIF, defects, concentration) | Personality, emotion or "trustworthiness" scores of employees |
| Role-level identifiers (approver role, function) | Data collected without notice or legal basis |

Approver identity may be needed later for an investigation. That is a human decision made through legal/HR channels, not a default AI output. See [human in the loop](../06-human-in-the-loop/README.md).

---
[Back to README](../README.md)
