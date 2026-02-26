# 03a — Evergreen Flow Reference (from Luna input)

## 4-layer summary
1. Master data setup (products, suppliers, customers, price book, consignee, cost centres)
2. Operations (document processing, marketing content, quotation)
3. Optional customer portal ordering
4. Sales order lifecycle status tracking

## Flow A — Document Processing
- Intake sources: email, WhatsApp, local/network folders
- OCR + LLM extraction
- Low-confidence highlighting
- Product catalogue matching + learning supplier mapping
- Human verification (split view)
- ERP Excel export

## Flow B — Marketing Agent
- Select products from catalogue
- AI image/text generation for Shopee/Lazada
- Review/approve queue
- Manual publish in Phase 1

## Flow C — Quotation Generation
- Select customer
- Pull purchase history
- AI suggests lines + pricing guidance
- Sales edits and exports PDF/email

## Flow D — Portal Ordering (B2B)
- Customer login with visibility policy (contract-only vs all)
- Customer-specific pricing via valid price book
- Consignee selection
- Cost-centre + budget validation
- Submit and track order statuses

## Sales order statuses
DRAFT, CONFIRMED, ALLOCATED, PARTIAL ALLOCATED, PICKING, PARTIAL PICKING, PICKED, PACKED, PARTIAL PACKED, CANCELLED.
