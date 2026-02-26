# US-005 — Cost Centre Budget Validation

As a customer portal user,
I want the system to validate cost-centre budget before order submit,
so that orders comply with budget controls.

## Acceptance Criteria
- User must select a cost centre before submit
- System checks available budget against order amount
- If exceeded, system applies configured rule (block or warn + approval path)
- Budget check result is stored with order snapshot
