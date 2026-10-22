# S2 - Quarter-end expedite rush

> Fictional, illustrative scenario. Numbers are invented.

**Stage:** DELIVER / ENABLE  |  **Drivers:** deadline pressure, incentive pressure, authority

## Setup
In the last two weeks of each quarter, premium freight and expedite requests jump. Several POs are raised after the supplier invoice arrives. One supplier's bank details were changed in the same window on an "urgent, approved by the VP" email.

## Behavioral drivers
- **Deadline / incentive pressure:** volume and revenue targets reward shipping by quarter-end.
- **Authority:** "approved by the VP" short-circuits the call-back step.
- **Fear-driven decisions:** nobody wants to be the one who missed the quarter.

## Hard-data signals
- Expedites in the last 10 business days of the quarter run several times the mid-quarter level.
- After-the-fact POs cluster in the same window.
- Supplier master change without a recorded call-back verification.

## Qualitative signals
- Q3 (expedite spike), Q8 (overrides concentrated in a period), Q11 ("approved by" as rationale).

## What AI surfaces
- **AI-1** anomaly detection on expedite, override and supplier-master logs, seasonality adjusted: cluster flagged in the final two weeks of each quarter.
- Sequence analysis: PO created after invoice date; bank change with no verification step.
- Confidence: high (rule-based sequence checks), medium (seasonal anomaly; only 8 quarters of data).

## Analyst judgment
Some quarter-end expedites are legitimate. The question is whether controls (call-back, PO-before-invoice) are skipped under pressure. The bank-detail change is treated as a potential fraud indicator until verified - compare [R01 in the earlier assessment](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R01-supplier-impersonation-payment-fraud.md).

## Human handoff
Bank change goes **immediately** to the **AP manager** to call the supplier on the number already on file and hold payment. Pattern goes to the **Controller** and **Procurement lead**. Possible override concerns go to **Internal Audit / Ethics** - not to the people involved. See [handoff H2](../06-human-in-the-loop/README.md#h2---bank-detail-change-pushed-through-at-quarter-end).

## Audit angle
- **Procedure:** Management-override testing analog: full-population analytics on supplier master changes, after-the-fact POs and expedites near period end (the procurement equivalent of journal-entry testing). Fraud-risk brainstorming on incentives around quarter-end. Re-perform call-back verification for a selection of changes.
- **Evidence:** System change logs (with completeness and integrity checks), call-back records, approval emails, PO/invoice timestamps.

## Controls and response
- Bank-detail changes: call-back on number on file, dual approval, first-payment hold - no executive exemption.
- After-the-fact PO KRI reported monthly to the Controller.
- Review incentive design with HR/Finance if pressure is structural.

---
[Back to scenarios](README.md)
