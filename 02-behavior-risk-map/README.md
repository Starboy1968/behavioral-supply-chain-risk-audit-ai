# Behavior-to-risk map

How human behavior turns into supply chain risk, stage by stage. Each row is something an analyst can actually look for in records. Stages match the earlier [AI supply chain risk assessment](https://github.com/Starboy1968/ai-supply-chain-risk-assessment) (PLAN, SOURCE, MAKE, DELIVER, RETURN, ENABLE).

**Rule for every row:** the signal is about a process, decision or document - never a diagnosis of a person. See [guardrails](../07-guardrails-and-ethics.md).

## Behavioral drivers in plain language

| Driver | What it does to a decision | Reference |
|---|---|---|
| Anchoring | First number sticks (last year's forecast, the incumbent's price) even when conditions change | Tversky & Kahneman 1974 [S15] |
| Optimism / planning fallacy | Plans assume the good case; buffers get cut | General concept; see [S15] |
| Sunk cost | Keep investing in a failing supplier or program because of what was already spent | Arkes & Blumer 1985 [S16] |
| Confirmation bias | Look for evidence that the trusted supplier is fine; discount the rest | Nickerson 1998 [S17] |
| Authority and power | Senior person's preference ends the discussion; juniors do not escalate | Concept; see [power-behavior-risk-indicators](https://github.com/Starboy1968/power-behavior-risk-indicators) |
| Trust and relationship lock-in | "We know them" replaces checking; one person owns the relationship | Concept |
| Groupthink | Meetings converge fast; dissent disappears from the record | Janis 1972 [S18] |
| Fear- and deadline-driven decisions | Controls skipped to hit a date; acceptances signed under pressure | Kobe Steel report cites deadline pressure [S13] |
| Incentive pressure | Bonus or KPI rewards speed, savings or volume over risk | COSO fraud-risk "incentives and pressures" [S6] |

## Full map by stage

### PLAN - forecasting, inventory and production planning

| Behavior | Where it shows up | Observable signal | Data source | How AI helps | What a human must judge |
|---|---|---|---|---|---|
| Anchoring | Demand forecast | Forecast barely moves from prior cycle despite changed inputs | Forecast versions, actuals | Flags low forecast change vs. high input change | Was stability justified by real information? |
| Optimism | Safety stock, capacity plans | Buffers cut cycle after cycle; plans never hit downside case | Inventory policy history, plan vs. actual | Trend on bias of plan vs. actual | Is the bias material, and who owns fixing it? |
| Groupthink | S&OP meeting | Minutes show unanimous decisions, no recorded alternatives or dissent | S&OP minutes | Aggregate count of decisions with no alternatives recorded | Is the meeting genuinely aligned or suppressing challenge? |
| Authority | Consensus forecast | Final number equals the senior leader's number, overriding analyst model | Forecast override log | Flags overrides by role level and size | Was the override informed or political? |

### SOURCE - supplier selection, contracts, supplier management

| Behavior | Where it shows up | Observable signal | Data source | How AI helps | What a human must judge |
|---|---|---|---|---|---|
| Trust / lock-in | Supplier relationship | One buyer owns a critical supplier for years, no rotation | Buyer-supplier assignment history | Flags long single-owner tenures on critical suppliers | Is rotation practical; what compensating review exists? |
| Trust | Due diligence | DD waived or abbreviated "because we know them" | DD tracker, waiver records | Finds waivers and missing renewals; reads waiver reasons | Is the waiver reason acceptable? |
| Confirmation bias | Supplier scorecard | Scores flat for years while OTIF or quality data moves | Scorecards vs. OTIF, defect data | Flags divergence between scorecard and hard metrics | Who is scoring, and are criteria still meaningful? |
| Sunk cost | Contract renewal | Renewed after repeated failures; remediation plans rolled over | Contract change history, CAPA logs | Links failures to renewal decisions | Was there a real exit analysis? |
| Incentive pressure | Price savings target | Single-source award to lowest bid, concentration rises | Award history, spend cube | Concentration and single-source mapping, incl. tier-2 where known | Is the savings worth the dependency? |

### MAKE - manufacturing, engineering, quality

| Behavior | Where it shows up | Observable signal | Data source | How AI helps | What a human must judge |
|---|---|---|---|---|---|
| Deadline pressure | Material deviations | Concessions/deviations accepted close to ship dates | Deviation and concession log | Timing analysis of acceptances vs. ship dates | Was the acceptance technically sound? |
| Authority | Quality hold release | Holds released by senior role over quality's objection | Hold/release log, comments | Flags releases where approver outranks objector | Was the override legitimate intervention or override? (COSO distinction [S6]) |
| Normalization | Repeat nonconformance | Same defect closed "use as is" repeatedly | NCR/CAPA records | Clusters repeat NCRs by supplier and disposition | Is this now an accepted but unrecorded risk? |

### DELIVER - logistics, transport, warehousing

| Behavior | Where it shows up | Observable signal | Data source | How AI helps | What a human must judge |
|---|---|---|---|---|---|
| Deadline / incentive | Quarter-end | Expedite requests and premium freight spike before period end | Freight invoices, expedite requests | Seasonality-adjusted anomaly detection | Is the spike demand-driven or target-driven? |
| Optimism | Carrier concentration | One carrier or lane carries most critical volume | TMS data | Concentration mapping | Is a backup carrier qualified? |
| Authority | Shipping before release | Shipments before QA release, approved by sales | WMS/ERP status timestamps | Sequence-violation detection | Was there a legitimate, documented reason? |

### RETURN - returns, warranty, after-sales

| Behavior | Where it shows up | Observable signal | Data source | How AI helps | What a human must judge |
|---|---|---|---|---|---|
| Confirmation bias | Root cause of returns | Returns classified "customer misuse" by default | RMA records | Classification drift vs. lab findings | Is the classification honest? |
| Softened escalation | Warranty trend reports | Language moves from "failure" to "observation" while counts rise | Escalation documents | Aggregate language-shift analysis on documents | Was the risk understated? Who decides to re-escalate? |

### ENABLE - finance/AP, legal, IT, risk

| Behavior | Where it shows up | Observable signal | Data source | How AI helps | What a human must judge |
|---|---|---|---|---|---|
| Authority / urgency | Supplier bank-detail change | Change pushed through on a senior request, call-back skipped | Supplier master change log | Flags changes without verification step | Fraud risk or process gap? (see [R01](https://github.com/Starboy1968/ai-supply-chain-risk-assessment/blob/main/03-findings/risks/R01-supplier-impersonation-payment-fraud.md)) |
| Deadline pressure | Risk acceptance | Acceptances signed in the last days before a deadline, with thin rationale | Risk acceptance register | Timing and completeness checks | Is the acceptance valid and within appetite? |
| Incentive | PO after invoice | Purchase orders raised after the invoice ("after-the-fact POs") | P2P logs | Sequence analysis, full population | Process breakdown or control avoidance? |

## Qualitative indicators

The watch list analysts can use without any AI: [indicators.md](indicators.md).

---
[Back to README](../README.md)
