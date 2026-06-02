# Fake-Data AI Compliance Workflow Example

This is a fictional workflow example. It uses fake company names, fake records, fake findings, and fake evidence. It is meant to show the operating pattern without exposing product code, customer data, or internal systems.

## Scenario

**Company:** Northstar Office Supply  
**Region:** EU  
**Workflow:** AI vendor intake and compliance readiness review  
**Requester:** Operations team  
**Risk:** A new support automation tool may process customer messages that contain personal data.

## Intake Record

```yaml
request_id: demo-2026-06-02-001
vendor_name: "ExampleSupport AI"
workflow_owner: "Operations"
data_categories:
  - customer email
  - support message
  - order reference
regions:
  - EU
  - UK
business_goal: "Reduce repetitive support triage while preserving review and escalation paths."
```

## Agent Roles

| Role | Job | Output |
| --- | --- | --- |
| Intake reviewer | Normalize the request and identify missing fields. | Structured intake summary |
| Data-risk reviewer | Classify likely personal data exposure and risk points. | Data risk notes |
| Policy mapper | Map the workflow to internal policy and compliance checks. | Control checklist |
| Evidence builder | Collect links, artifacts, and assumptions into an evidence bundle. | Review packet |
| Human approver | Accept, reject, or request changes. | Decision and next actions |

## Example Output

```json
{
  "risk_level": "medium",
  "approval_required": true,
  "missing_items": [
    "data retention period",
    "vendor subprocessors",
    "human escalation path"
  ],
  "recommended_controls": [
    "limit message retention to approved period",
    "require escalation for payment, legal, or medical content",
    "log automation decisions with reviewer-visible evidence"
  ]
}
```

## Review Gate

The workflow stops before production approval until a human reviewer confirms:

- the workflow owner is named;
- the vendor data path is understood;
- escalation rules are defined;
- evidence has been captured;
- reporting is available for future audit or customer review.

## Why This Matters

The value is not that an agent can summarize a policy. The value is that the system preserves state, names the owner, captures evidence, identifies missing inputs, and creates a reviewable path before the automation touches real customer workflows.
