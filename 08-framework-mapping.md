# Framework mapping

IDs below were checked against the source documents listed in [sources](sources.md). Where a specific ID was not checked, the mapping is at function or component level only. No framework text is restated beyond short paraphrase.

## COSO Internal Control - Integrated Framework (2013): Control Environment [S6]

| Principle | Paraphrase | Behavioral link in this project |
|---|---|---|
| 1 | Commitment to integrity and ethical values | Waivers "because we know them"; shipping out-of-spec under pressure (S1, S4) |
| 2 | Board independence and oversight of internal control | Board/committee sees behavioral KRIs, not only supplier metrics |
| 3 | Structures, reporting lines, authorities and responsibilities | Authority overriding Quality; delegation limits on risk acceptance (S4) |
| 4 | Commitment to competent individuals | Training analysts and auditors to read behavioral signals fairly |
| 5 | Holding individuals accountable for internal control responsibilities | Named decision owners; AI tool owners ([human in the loop](06-human-in-the-loop/README.md)) |
| 8 (Risk Assessment) | Considers the potential for fraud | Incentives and pressure at quarter-end; management override (S2) |

COSO also treats **management override** as an inherent limitation of internal control and distinguishes it from documented, legitimate **management intervention** [S6] - used in [audit procedures](05-auditing/evidence-and-procedures.md).

## COSO ERM (2017): Governance & Culture [S7]

| Principle | Name | Link |
|---|---|---|
| 1 | Exercises Board Risk Oversight | Oversight of supplier concentration and risk acceptances |
| 2 | Establishes Operating Structures | Second-line challenge in S&OP and supplier reviews |
| 3 | Defines Desired Culture | Dissent recorded; escalations not softened (S3, S5) |
| 4 | Demonstrates Commitment to Core Values | No executive exemptions from bank-change verification (S2) |
| 5 | Attracts, Develops, and Retains Capable Individuals | Rotation and second reviewers for critical suppliers (S1) |

## NIST CSF 2.0 [S3]

| ID | Paraphrase | Link |
|---|---|---|
| GV.RR-01 | Leadership accountable for cybersecurity risk; fosters risk-aware, ethical, continually improving culture | Culture signals (dissent, softened escalation) |
| GV.RR-02 | Roles, responsibilities and authorities established, communicated, understood, enforced | Decision owners, delegation limits |
| GV.RR-04 | Cybersecurity included in HR practices | Rotation, training; not employee profiling |
| GV.SC-01 | C-SCRM program, strategy, objectives, policies and processes established and agreed | This map as an input to the program |
| GV.SC-02 | C-SCRM roles for suppliers, customers, partners established and coordinated | Relationship owners and second reviewers |
| GV.SC-04 | Suppliers known and prioritized by criticality | Focus on critical suppliers first |
| GV.SC-06 | Planning and due diligence before entering formal relationships | DD waivers (S1) |
| GV.SC-07 | Supplier risks identified, recorded, prioritized, assessed, responded to and monitored over the relationship | Behavioral + hard-metric watch list (AI-5) |

Note: CSF 2.0 GV.SC is framed around cybersecurity supply chain risk; this project applies the same governance outcomes to broader operational supplier risk.

## NIST SP 800-161r1-upd1 (C-SCRM) [S4][S5]

| Control | Name | Link |
|---|---|---|
| SR-3 | Supply Chain Controls and Processes | Controls in each scenario |
| SR-5 | Acquisition Strategies, Tools, and Methods | Dual-sourcing, contract clauses (S1, S5) |
| SR-6 | Supplier Assessments and Reviews | DD currency, scorecards fed by data (S1) |
| PM-30 | Supply Chain Risk Management Strategy | Behavioral indicators feed the enterprise strategy |

## NIST AI RMF 1.0 [S1][S2]

| ID | Link |
|---|---|
| GOVERN (function) | Policies, accountability, culture for AI use |
| GOVERN 1.6 | AI inventory ([auditing the AI](05-auditing/ai-in-audit.md)) |
| GOVERN 2.1 | Roles, responsibilities, lines of communication documented |
| GOVERN 3.2 | Roles for human-AI configurations and oversight |
| GOVERN 6.1 | Policies for third-party AI risks |
| MAP 3.5 | Human oversight processes defined and documented |
| MEASURE, MANAGE (functions) | False-positive tracking, error response, pausing tools |

## IIA Global Internal Audit Standards (2024) and Three Lines Model [S8][S9]

| Reference | Use here |
|---|---|
| Principle 4 / Standard 4.3 Professional Skepticism | Questioning both management statements and AI output |
| Standard 9.4 Internal Audit Plan; 13.2 Engagement Risk Assessment | Behavioral and AI signals inform risk-based planning |
| Standard 9.5 Coordination and Reliance | Relying on second-line AI monitoring |
| Standard 10.3 Technological Resources | Audit use of analytics and AI |
| Standard 11.5 Communicating the Acceptance of Risks | Risk acceptances beyond appetite |
| Standards 14.1, 14.2, 14.3, 14.5, 14.6 | Evidence quality, criteria vs. condition, significance, conclusions, documentation |
| Standard 15.2 | Follow-up on action plans |
| Three Lines Model (2020) | First/second/third-line roles for flags, monitoring and assurance |

## EU AI Act [S10][S11][S12]

| Reference | Use here |
|---|---|
| Art. 5(1)(f) | Prohibition on workplace emotion inference (medical/safety exceptions) |
| Annex III, point 4(b) | Worker performance/behaviour monitoring is high-risk - stay at process level |
| Art. 14 | Human oversight design reference (applies to high-risk systems); high-risk application dates have been amended - check the current timeline [S19] |

---
[Back to README](README.md)
