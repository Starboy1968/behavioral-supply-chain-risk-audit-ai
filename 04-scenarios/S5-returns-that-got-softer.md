# S5 - Returns that got softer

> Fictional, illustrative scenario. Numbers are invented.

**Stage:** RETURN  |  **Drivers:** sunk cost, confirmation bias, softened escalation

## Setup
A company invested heavily in a new component supplier two years ago. Warranty returns for the product rise, but monthly escalation reports move from "failure trend" to "observation" to "monitoring". Most returns are coded "customer misuse".

## Behavioral drivers
- **Sunk cost:** admitting the supplier is the problem means admitting the switch was a mistake.
- **Confirmation bias:** returns get coded in the way that protects the decision.
- **Softened escalation:** each layer tones the message down.

## Hard-data signals
- RMA count up quarter over quarter; lab teardown sample shows component failure in most units tested.
- "Customer misuse" share of RMA codes rising.

## Qualitative signals
- Q7 (softened escalation), Q5, Q9.

## What AI surfaces
- **AI-3** aggregate language analysis of 24 escalation reports (using [Prompt 2](../03-ai-integration/prompts.md)): severity wording downgraded while counts rise; deferral wording without owner.
- Classification drift: RMA codes vs. lab findings.
- Confidence: medium; lab sample is small; language analysis cannot know intent.

## Analyst judgment
Is the risk understated? Is the coding wrong or the lab sample unrepresentative? The analyst does not attribute motive; the finding is that the escalation process lets wording drift away from the data.

## Human handoff
To **Head of Quality** and **Product Safety/Legal** if safety may be involved, and to the **risk owner** for supplier decision. See [handoff H5](../06-human-in-the-loop/README.md#h5---softened-escalation-language-vs-rising-returns).

## Audit angle
- **Procedure:** Re-perform RMA classification on a statistical sample against lab results; analytics on code trends; inspect escalation reports vs. underlying counts.
- **Evidence:** RMA records, lab reports, escalation documents, the AI language review (with prompt, model version and output retained).

## Controls and response
- Escalation templates show the metric next to the narrative.
- RMA coding reviewed independently of the team that chose the supplier.
- Supplier exit/dual-source analysis with explicit sunk-cost note: past spend is not a reason to stay.

---
[Back to scenarios](README.md)
