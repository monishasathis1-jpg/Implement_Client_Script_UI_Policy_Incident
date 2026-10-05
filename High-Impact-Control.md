# High Impact Control - UI Policy

## Configuration

- **Name:** High Impact Control
- **Table:** Incident
- **Active:** True
- **Condition:** Impact is 1 - High
- **Reverse if false:** True

## UI Policy Action - Assignment group

- Field: Assignment group
- Mandatory: True

## UI Policy Action - Urgency

- Field: Urgency
- Read-only: True
- Visible: Leave unchanged

## Expected Result

When Impact is High, the configured field behavior is applied.

When the condition becomes false, the policy changes are reversed because **Reverse if false** is enabled.
