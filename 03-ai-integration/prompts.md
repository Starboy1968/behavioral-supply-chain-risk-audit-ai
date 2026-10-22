# Sample prompts

Both prompts follow the structure of the reusable [GRC risk-analysis prompt (v3)](https://github.com/Starboy1968/ai-assisted-risk-analysis/blob/main/prompt/risk-analysis-prompt.md) in [ai-assisted-risk-analysis](https://github.com/Starboy1968/ai-assisted-risk-analysis): **Role - Rules (guardrails) - Inputs - Output format - Self-check**, then a **human review** step. Same core rules: do not invent facts, use only the inputs, ask rather than guess, the AI drafts and a person decides. Use only approved AI tools with no-training terms (see [R02 in the earlier assessment](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R02-data-leakage-genai-shadow-ai.md)).

## Prompt 1 - Due-diligence file gap review (AI-4)

```text
ROLE
You support a third-party risk analyst. You produce a first-pass gap list
for a human to review. You do not decide whether a supplier is acceptable.

RULES (GUARDRAILS)
1. Do not invent facts. Use only the attached documents. If an item is not
   in them, write "not found".
2. Quote the document name and page/section for every status you give.
3. Do not judge whether a waiver reason is acceptable; list it verbatim.
4. Do not comment on any person's motives, character or attitude.
5. If text is unreadable or ambiguous, say so instead of guessing.

INPUTS
- Supplier criticality: [CRITICAL / HIGH / ...]
- Policy requirements: [e.g., current quality certificate; financial review
  within 12 months; sanctions screening within 12 months; signed code of
  conduct; approved waiver for any missing item]
- Attached: questionnaire, certificates, last audit report, waiver records

OUTPUT FORMAT
A. Table: Requirement | Status (PRESENT / MISSING / EXPIRED / INCONSISTENT)
   | Evidence (document + page) | Notes
B. Waivers: Item waived | Reason (verbatim) | Approver role | Date | Expiry
C. Limitations of this review (what could not be checked)
D. Open questions for the analyst

SELF-CHECK (run before answering)
- Every status has a document reference or says "not found".
- No statement about any person's motives or character.
- Nothing appears that is not in the attached documents.

HUMAN REVIEW
Analyst verifies every MISSING / EXPIRED / INCONSISTENT item against the
source before recording it, decides on waivers, and logs accept/override
of each AI item (feeds tuning - see 06-human-in-the-loop).
```

## Prompt 2 - Aggregate language review of escalation documents (AI-3)

```text
ROLE
You support a risk analyst reviewing a PROCESS (how risk is escalated),
not people. You produce a draft for a human to review.

RULES (GUARDRAILS)
1. Do not infer emotions, intent or attitudes of any author.
2. Do not try to identify authors. Names and initials have been removed.
3. Quote the exact phrases you rely on.
4. Do not invent counts or trends that are not in the documents.
5. State your confidence (high / medium / low) and why.

INPUTS
- Process: [e.g., monthly warranty-escalation reports, product line X]
- Period: [e.g., 24 months]
- Attached: the reports, anonymized
- Incident counts per month: [from the RMA system, if available, else "unknown"]

OUTPUT FORMAT
A. Table per month: Top issue | Severity words used (quoted) | Action, owner
   and date stated? (Y/N) | Deferral wording without an owner (quoted)
B. Trend summary (max 5 lines), placing wording next to incident counts
   where provided
C. What this analysis cannot tell us
D. Confidence and why

SELF-CHECK (run before answering)
- No statement about any author's feelings, intent or character.
- Every trend claim is backed by quoted phrases.
- Missing inputs are listed, not guessed.

HUMAN REVIEW
Analyst compares the trend with RMA counts from the system and decides
whether re-escalation is needed. Decision and reasoning are recorded.
```

## Why these prompts are built this way

- **Evidence references** make the output checkable and auditable ([AI in audit](../05-auditing/ai-in-audit.md)).
- **"Not found" over guessing** reduces hallucinated findings.
- **No motives, no emotions** keeps the use inside the [guardrails](../07-guardrails-and-ethics.md).
- **Limitations and confidence** are required parts of the handoff package in [human in the loop](../06-human-in-the-loop/README.md).
- The language patterns looked for match the "language around risk" lens (minimizing and pre-decided language) in the [power-behavior-risk-indicators catalog](https://github.com/Starboy1968/power-behavior-risk-indicators/blob/main/02-framework/indicator-catalog.md) - but applied to documents in aggregate, not to individual speakers.

---
[Back to AI integration](README.md) | [Back to project README](../README.md)
