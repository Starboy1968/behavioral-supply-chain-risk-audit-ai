# AI in supply chain audit - and auditing the AI

## How AI supports the audit

| Use | What it does | Human must still |
|---|---|---|
| Full-population analytics | Tests every PO, change or override instead of a sample | Validate data completeness; investigate exceptions |
| Duplicate vendor / bank detection | Finds vendors sharing bank accounts, addresses or tax IDs; near-duplicate names | Judge legitimate cases (e.g., group companies) |
| Three-way match exceptions | PO vs. goods receipt vs. invoice mismatches, by supplier and approver role | Decide which exceptions are control failures |
| Segregation-of-duties conflicts | Same user can create a vendor and approve its payment; requester = approver | Confirm access vs. actual use; assess compensating controls |
| Override and timing analytics | Clusters near period end, approvals just under limits, split POs | Decide what is override vs. legitimate intervention |
| LLM-assisted contract / DD review | Extracts clauses, finds missing items, compares versions, with page references | Verify every extracted item that will be cited as evidence |
| Drafting workpapers | First drafts of walkthrough narratives and finding write-ups from auditor notes | Review, correct and sign; the auditor owns the content |

## Reliability of AI-generated audit evidence

AI output is **audit-generated analysis**, not independent evidence. Treat it like any other tool output:

- **Reproducible:** retain the data extract, model/tool and version, prompt or rule set, parameters, date and output, so another auditor can re-run it (Standard 14.6 [S8]).
- **Validated:** re-perform a sample of AI results manually; record the agreement rate.
- **Bounded:** record known limitations (data gaps, model confidence, language limits).
- **Owned:** the auditor remains responsible for conclusions (Principle 4, Exercise Due Professional Care [S8]). "The model said so" is never the basis of a finding.
- **Resourced:** Standard 10.3 (Technological Resources) expects the audit function to have appropriate technology and the skills to use it [S8].

## Auditing the AI itself

When first- or second-line teams use AI for supply chain risk triage, internal audit should be able to answer:

| Area | Audit question | Evidence |
|---|---|---|
| Model inventory | Is every AI tool used in supply chain risk listed, with owner, purpose and data used? | AI inventory (NIST AI RMF GOVERN 1.6 [S1][S2]) |
| Change logs | Are model, prompt, rule and threshold changes approved and logged? | Change records, version history |
| Reproducibility | Can a past flag be re-generated from retained inputs? | Re-run of a sample |
| Explainability for evidence | Can each flag be traced to the underlying records? | Flag-to-source trace |
| Performance and false positives | Are hit rates and false-positive rates tracked and used to tune? | Flag outcome log (see [human in the loop](../06-human-in-the-loop/README.md)) |
| Scope limits | Is the tool kept inside the [guardrails](../07-guardrails-and-ethics.md) - no emotion inference, no individual profiling? | Configuration, data-source list, legal/privacy sign-off |
| Third-party AI | Are vendor AI terms, data use and model changes covered? | Contracts, vendor questionnaire from the [earlier assessment](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/04-recommendations/vendor-due-diligence-questionnaire.md) |
| Human oversight | Are decisions recorded by named roles, with overrides of AI output logged? | Decision log |

---
[Back to auditing](README.md) | [Back to project README](../README.md)
