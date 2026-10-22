# S1 - The supplier we always use

> Fictional, illustrative scenario. Numbers are invented.

**Stage:** SOURCE  |  **Drivers:** trust and relationship lock-in, confirmation bias, single point of knowledge

## Setup
"Alder Castings" has supplied a critical housing for 11 years. One senior buyer has owned the relationship the whole time. Due diligence was last fully refreshed six years ago; two renewals were waived with the reason "long-standing supplier, no issues". The supplier scorecard has shown "Green" every quarter.

## Behavioral drivers
- **Trust** replaces checking ("we know them").
- **Confirmation bias**: good history makes small warnings easy to dismiss.
- **Lock-in**: no one else knows the supplier well enough to challenge.

## Hard-data signals
- Single source for a critical part; ~100% of spend for that part.
- OTIF slid from 97% to 88% over four quarters while the scorecard stayed Green.
- Lead time variance doubled.

## Qualitative signals
- Q1 (no rotation), Q2 (DD waived), Q5 (scorecard never changes) from the [indicator list](../02-behavior-risk-map/indicators.md).

## What AI surfaces
- **AI-2** concentration map: single source, no qualified alternate; supplier survey shows Alder relies on one foundry (tier-2) - compare [two-suppliers-one-factory](https://github.com/Starboy1968/two-suppliers-one-factory).
- **AI-4** DD review: financial review and certificate expired; two waivers with identical reason text.
- **AI-5** pairing: scorecard flat vs. OTIF down. Confidence: high on data gaps, medium on trend (only four quarters).

## Analyst judgment
Is this a deteriorating supplier hidden by a stale process, or a temporary dip? The analyst checks for documented causes (e.g., a known capacity move) before rating. The issue is the **process** (no rotation, waivers allowed to stack), not the buyer's integrity.

## Human handoff
Package to the **Category Manager (risk owner)** and **TPRM lead**: AI flags, confidence, limitations (tier-2 data self-reported by supplier). Questions: refresh DD now? Qualify a second source? Decision recorded in risk register with rationale and date. See [handoff H1](../06-human-in-the-loop/README.md#h1---single-source-supplier-with-stale-due-diligence).

## Audit angle
- **Procedure:** Test the full population of critical suppliers for DD currency and waivers; inspect waiver approvals; walk through how scorecards are produced and who scores.
- **Evidence:** DD tracker extract (with completeness check), waiver records, scorecard inputs vs. OTIF data, assignment history. Inquiry notes with the buyer and category manager documented in workpapers and corroborated against records.

## Controls and response
- Waivers expire and cannot be renewed twice without second-line approval.
- Relationship rotation or a second reviewer for critical suppliers.
- Scorecards fed from system data, not self-entered.
- Dual-source or buffer-stock decision by risk owner within 90 days.

---
[Back to scenarios](README.md)
