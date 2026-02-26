# US-006 — Sales Order Status Transition Rules

As an operations user,
I want controlled status transitions,
so that order tracking remains accurate and auditable.

## Acceptance Criteria
- Allowed transitions are enforced by workflow rules
- Role-based permissions define who can transition each status
- Invalid transitions are blocked with clear error message
- Transition history includes from/to status, user, and timestamp
