# Project brief

## Objective

Show how human behavior - biases, power, trust, pressure and incentives - creates supply chain and third-party risk, and how AI, auditors and accountable people can work together to see it earlier. The output is a map an analyst can use on Monday: which behaviors to watch for, where they leave traces in ordinary business records, what AI can surface, what audit should test, and which decisions must stay with a named person.

## Why this matters

Most supply chain risk programs measure suppliers: lead times, on-time-in-full (OTIF), financial health, concentration. Far fewer look at the buyer side - the decisions that let a risk grow quietly. A documented real case shows why: Kobe Steel's own 2018 investigation report attributed years of falsified quality data to a culture that "prioritized winning purchase orders and meeting delivery deadlines over ensuring quality", an insular organization where personnel were rarely rotated, and internal audits that were not extensive enough [S13]. None of those causes would appear on a supplier scorecard. All of them leave traces in records.

## Scope

| In scope | Out of scope |
|---|---|
| Five supply chain stages plus enabling functions (PLAN, SOURCE, MAKE, DELIVER, RETURN, ENABLE), same stage model as [ai-supply-chain-risk-assessment](https://github.com/Starboy1968/ai-supply-chain-risk-assessment) | Psychological assessment of any individual |
| Behavioral drivers: anchoring, optimism, sunk cost, confirmation bias, authority and power, trust and relationship lock-in, groupthink, fear- and deadline-driven decisions, incentive pressure | Emotion recognition, sentiment scoring of named employees, covert monitoring |
| Evidence in business records: PO/approval logs, override and exception logs, supplier master changes, due-diligence records, risk acceptances, contract changes, S&OP minutes, escalation wording | Building or deploying a production AI system |
| AI as triage: anomaly detection, concentration mapping, aggregate language analysis, LLM-assisted document review | Legal advice; conclusions about real organizations other than the cited, verified case |
| Internal audit use of these signals, and auditing the AI itself | |
| Human-in-the-loop decision points and handoffs | |

The organization is illustrative: a mid-size manufacturer and distributor, as in the earlier assessment.

## Questions this project answers

1. Which behaviors drive supply chain risk at each stage, and what observable trace does each leave?
2. Which of those traces can AI surface reliably, and which need a human to interpret?
3. How should an auditor turn a qualitative behavioral signal into sufficient, reliable, relevant evidence?
4. Where must a named person decide, and what must they record when they do?
5. What must AI never be used for in this work?

## Deliverables

- [Behavior-to-risk map and qualitative indicators](02-behavior-risk-map/)
- [AI integration design, sample prompts, flag-vs-decide table](03-ai-integration/)
- [Five illustrative scenarios](04-scenarios/)
- [Auditing thread](05-auditing/)
- [Human in the loop: where AI isn't enough](06-human-in-the-loop/)
- [Guardrails and ethics](07-guardrails-and-ethics.md)
- [Framework mapping](08-framework-mapping.md)
- [Sources](sources.md)

## Method

1. Reused the stage model and terminology from the earlier AI supply chain risk assessment.
2. For each stage, listed the decisions people make, the behavioral drivers that bend those decisions, and the records each decision leaves.
3. Kept only signals visible in process records or documents, not in people's inner states.
4. For each signal: what AI can do, what an auditor would test, and who must decide.
5. Mapped to frameworks at the level of IDs that were checked against source documents (see [sources](sources.md)); where not checked, function level only.

> Everything in this repo other than the cited Kobe Steel case and the frameworks is illustrative analyst judgment, not measured data.

---
[Back to README](README.md)
