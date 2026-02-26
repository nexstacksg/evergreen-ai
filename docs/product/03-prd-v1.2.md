# Product Requirement Document (PRD) — v1.2

| Field | Value |
|---|---|
| Project | Evergreen AI |
| Version | 1.2 |
| Status | Draft |
| Updated | 2026-02-26 |
| Change Type | Scope alignment update |

## What changed from v1.1
- Preserved all v1.1 core workstreams (Document Processing, Marketing Agent, Quotation)
- Added explicit B2B portal scope from latest requirements:
  - customer-specific visibility (contract-only vs all)
  - customer price book + validity logic
  - consignee selection
  - cost centre selection + budget validation
  - sales-order lifecycle status model + transition control

## 1) Product Summary
Evergreen AI helps Evergreen process business documents into ERP-ready structured exports, generate marketplace marketing content faster, generate quotation drafts from customer history, and support B2B customer ordering controls.

## 2) End-to-End Flow (4 Layers)
1. **Master data setup**: products, suppliers, customers, price book, consignee, cost centres.
2. **Operations**: document processing + marketing content + quotation generation.
3. **Customer portal (optional module)**: customer login, visibility policy, pricing policy, order placement.
4. **Order lifecycle tracking**: operational status progression and audit trail.

## 3) Workstream Scope
### WS1 — Document Processing
- Intake: email attachments, WhatsApp images/PDFs, local/network folder drops
- OCR + LLM extraction (doc no/date/company/line items/totals)
- Low-confidence highlighting and review gate
- Product matching with supplier-name ? internal-SKU learning
- Human verification split view
- ERP Excel export

### WS2 — E-commerce Marketing Agent
- Select products from shared catalogue
- AI image enhancement + content variants for Shopee/Lazada
- Human review and approval queue
- Manual marketplace publish in Phase 1

### WS3 — Quotation Generation
- Select customer and load purchase history
- AI line suggestion using history + current price context
- Price resolution with customer price-book precedence
- Sales edits, exports branded PDF, or emails quote

### WS4 — B2B Portal Ordering (Added in v1.2)
- Customer login with visibility mode:
  - Contract-only items
  - Contract + non-contract items
- Pricing resolution:
  - Selling price + valid date window
  - customer-specific contract pricing where applicable
- Consignee (deliver-to) selection
- Cost-centre selection with budget check
- Submit sales order and track lifecycle status

## 4) Sales Order Lifecycle Statuses
- DRAFT
- CONFIRMED
- ALLOCATED
- PARTIAL ALLOCATED
- PICKING
- PARTIAL PICKING
- PICKED
- PACKED
- PARTIAL PACKED
- CANCELLED

## 5) Key Functional Requirements (Consolidated)
- Multi-source document ingestion and OCR extraction
- Confidence-based field verification gate before export
- ERP-format Excel export for verified documents
- Supplier mapping memory for product matching improvement
- AI-assisted marketplace content generation + review workflow
- AI-assisted quotation draft generation with price source transparency
- Customer portal visibility/pricing policy enforcement
- Cost-centre budget validation (warn/block policy configurable)
- Role-based status transition control and transition audit trail

## 6) Price & Policy Rules (v1.2 clarification)
- Price-book validity dates must be enforced.
- Price precedence (default):
  1. Active customer contract/price-book rule
  2. Customer last-sold guidance (for suggestion only)
  3. Catalogue price fallback
- Final quoted/ordered price snapshot must be stored with source tag.

## 7) Non-Functional Emphasis
- Accuracy transparency (confidence visibility)
- Human-in-the-loop controls for risk points
- Full action auditability (verify, map, transition, override)
- Reliable export handoff for ERP import

## 8) Traceability to supporting docs
- Discovery brief: `docs/product/01-discovery-brief.md`
- Scope v0.1: `docs/product/02-scope-v01.md`
- Flow reference: `docs/product/03a-evergreen-flow-reference.md`
- User stories: `docs/product/04-user-stories/*`
- UX flow: `docs/product/05-ux-flows/flow-portal-order.md`
- Change requests: `docs/product/06-change-requests/*`
- Release checklist: `docs/product/07-release-checklist.md`

---

**Note:** v1.1 file is kept unchanged for history. v1.2 is the aligned baseline for current implementation planning.
