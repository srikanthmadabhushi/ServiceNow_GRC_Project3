# ServiceNow_GRC_Project3
ServiceNow GRC | AI-Driven Risk Mitigation Planner (Yokohama PDI)
# ServiceNow GRC | AI-Driven Risk Mitigation Planner (Yokohama PDI)

## Overview
When a Risk record is **High**, a no-code Flow Designer automation simulates AI to propose an **AI Mitigation Plan** and set **Mitigation Status**. Optionally, it emails the risk manager. This demonstrates predictive, agentic decisioning for GRC.

## Flow Logic
1. **Trigger:** Risk Record created or updated
2. **If Risk Level = High**
   - Update:
     - **AI Mitigation Plan:** “AI detected high risk. Perform root-cause analysis, assign owner, implement corrective controls.”
     - **Mitigation Status:** Proposed
   - *(Optional)* Send email to risk manager
3. **Else**
   - Update:
     - **AI Mitigation Plan:** “Risk within acceptable range; monitor quarterly and reassess controls.”
     - **Mitigation Status:** Proposed

## Highlights
- 100% **no-code** in **Flow Designer**
- **Agentic AI** pattern: read → decide → act → explain
- Works on **Yokohama PDI** without paid plugins
- Portfolio-friendly with execution transparency

## Diagram
![Flow](Diagrams/Flow Daiagram.png)

## Test Examples
| Short Description              | Risk Level | Result                                   |
|-------------------------------|-----------:|-------------------------------------------|
| Repeated audit failure        | High       | Mitigation plan + email (optional)        |
| Minor policy gap              | Medium     | Monitoring plan                           |
| Routine process check         | Low        | Monitoring plan                           |
