# Guardrails and ethics

**Guardrails are constraints on what AI may do.** Where decisions must sit with people is covered in [Human in the loop](06-human-in-the-loop/README.md); this page does not repeat it, but cross-references it.

The core rule: **analyze processes, decisions and documents - not individuals' psychology.** Behavioral drivers are used as a lens to design better controls, never as a diagnosis of a person.

## 1. Prohibited uses in this project

| Do not | Why |
|---|---|
| Infer emotions of employees (voice, face, text "sentiment" about a person) | The EU AI Act prohibits placing on the market, putting into service for this purpose, or using AI systems "to infer emotions of a natural person in the areas of workplace and education institutions", except where intended for medical or safety reasons - Article 5(1)(f), applicable since 2 February 2025 [S10] |
| Score or rank individual employees for "risk", trustworthiness or personality | Unfair, unreliable, and outside the purpose of supply chain risk. AI used to monitor and evaluate the performance and behaviour of workers is listed as high-risk under the EU AI Act (Annex III, point 4(b)) [S12] |
| Covert monitoring of employees or reading private communications | Disproportionate; likely unlawful in many jurisdictions; destroys trust and speak-up culture |
| Treat an AI flag as a verdict | AI is triage only; see [human in the loop](06-human-in-the-loop/README.md) |
| Use unapproved or training-enabled AI tools on company data | Data leakage; see [R02 in the earlier assessment](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R02-data-leakage-genai-shadow-ai.md) |

## 2. Required constraints

| Guardrail | In practice |
|---|---|
| Purpose limitation | Written purpose: improve supply chain and third-party risk controls. Any new use needs fresh approval |
| Data minimization | Use existing business records; role-level identifiers by default; names only when a human decides an investigation is warranted |
| Aggregate language analysis only | Documents and processes, with small-group suppression; no per-author profiles ([AI integration](03-ai-integration/README.md#ai-3-boundaries-language-analysis)) |
| Proportionality | Depth of analysis matches the criticality of the supplier or process |
| Transparency | Employees are told, in plain language, which records are analyzed and why |
| Legal, privacy and works-council review | Before go-live: data protection review (e.g., DPIA where required) and employee-representative consultation where local law gives works councils rights over monitoring technology |
| False-positive management | Track false-positive rates; never act on a flag without corroboration; tune or pause tools that misfire |
| Documentation | AI inventory, data sources, prompts/rules, versions, owners, change log |

## 3. Guardrails for AI-generated audit evidence

| Guardrail | In practice |
|---|---|
| Reliability | AI output is re-performed on a sample before it supports a finding; agreement rate recorded |
| Reproducibility | Inputs, model/version, prompt or rules, parameters and outputs retained so another auditor can re-run (IIA Standard 14.6 [S8]) |
| Traceability | Every flag cited in a workpaper links to source records |
| Auditor responsibility | The auditor owns every conclusion (IIA Principle 4 [S8]); AI drafts are reviewed and signed by a person |
| No surveillance through audit | Audit analytics follow the same no-profiling, no-emotion-inference rules |

## 4. Tie to frameworks

| Framework | Where it lands |
|---|---|
| NIST AI RMF 1.0 | **Govern:** policies, roles, inventory (GOVERN 1.6, 2.1, 3.2); **Map:** context and intended use, human oversight processes (MAP 3.5); **Measure:** false-positive and error tracking (function level); **Manage:** responding to errors, pausing tools (function level) [S1][S2] |
| COSO ICIF 2013 - Control Environment | Principle 1 (integrity and ethical values): no covert surveillance; Principle 3 (structures, authorities): named AI owners; Principle 5 (accountability): decision records [S6] |
| COSO ERM 2017 - Governance & Culture | Principle 3 (defines desired culture) and 4 (commitment to core values): analytics must support speak-up culture, not chill it [S7] |
| EU AI Act | Art. 5(1)(f) prohibition; Annex III 4(b) high-risk category; Art. 14 human oversight as a design reference [S10][S11][S12] |

See full mapping in [08-framework-mapping.md](08-framework-mapping.md).

---
[Back to README](README.md)
