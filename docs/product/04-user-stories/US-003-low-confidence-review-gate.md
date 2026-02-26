# US-003 — Low-Confidence Field Review Gate

As a sales admin,
I want low-confidence extracted fields clearly flagged and gated before verification,
so that incorrect data does not get exported to ERP.

## Acceptance Criteria
- Fields below configured confidence threshold are highlighted
- Verify action is blocked until all flagged fields are reviewed (edited or explicitly confirmed)
- Review actions are logged with user + timestamp
- Export is allowed only for verified documents
