# S4 - Friday-evening risk acceptance

> Fictional, illustrative scenario. Numbers are invented. Real analog cited: Kobe Steel [S13].

**Stage:** MAKE  |  **Drivers:** deadline pressure, authority, normalization of deviance

## Setup
A supplier's alloy test results are slightly out of spec. A customer shipment is due Monday. A plant director signs a deviation acceptance late Friday; Quality's objection is in an email but not in the acceptance record. The same deviation has been accepted four times this year.

## Behavioral drivers
- **Deadline pressure** and **fear** of missing the customer date.
- **Authority:** the director outranks the quality engineer.
- **Normalization:** "we accepted it before and nothing happened."

## Real analog (verified)
Kobe Steel's 2018 report on its quality-data misconduct cited a culture prioritizing purchase orders and delivery deadlines over quality, a false assumption that products below customer specifications could be shipped if there was no safety issue, and internal audits that were not sufficiently extensive [S13][S14]. The scenario above is fictional; the analog shows the pattern is real.

## Hard-data signals
- Repeat deviation for same supplier and characteristic.
- Acceptance timestamps clustered near ship dates.

## Qualitative signals
- Q4 (acceptance under deadline pressure), Q8, Q9 (repeated extensions), objection outside the record.

## What AI surfaces
- **AI-1** timing analysis of deviations vs. ship dates; repeat-deviation clustering.
- **AI-4** review of acceptance records: missing technical rationale field; objection referenced elsewhere but not attached.
- Confidence: high on repeats and timing; cannot judge technical acceptability.

## Analyst judgment
Was each acceptance technically justified? Only qualified engineering/quality staff can say. The analyst flags the process gap: acceptances do not capture objections or require independent quality sign-off.

## Human handoff
To **Head of Quality** (independent of plant management) for technical review; to **Risk/Compliance** for the process gap. See [handoff H4](../06-human-in-the-loop/README.md#h4---repeated-deviation-acceptances-near-ship-dates).

## Audit angle
- **Procedure:** Full-population test of deviation acceptances: approver authority, quality sign-off, rationale, timing. Inquiry with Quality, documented and corroborated. Reconcile objections in email to acceptance records (with legal/privacy-approved scope).
- **Evidence:** Deviation log, acceptance forms, test certificates, delegation-of-authority matrix.

## Controls and response
- Deviation acceptance requires Quality sign-off that cannot be overridden by line management alone.
- Third repeat triggers supplier corrective action and second-line review.
- Objections must be attached to the acceptance record.

---
[Back to scenarios](README.md)
