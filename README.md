# Evergreen AI

**Smart Document Processing & E-commerce Marketing Assistant**

An AI-powered web application built for [Evergreen Group Pte Ltd](https://evergreen.com.sg), a Singapore office supplies company. The system automates two key operational workflows:

## 🔍 Workstream 1: Document Processing

Automated OCR and data extraction from invoices, purchase orders, and delivery orders received via email, WhatsApp, and local folders. Features a side-by-side review UI for human verification and Excel export for ERP import.

## 🛒 Workstream 2: E-commerce Marketing Agent

AI-powered content generation for Shopee.sg and Lazada.sg product listings — including photo enhancement (background removal, lifestyle shots), optimised titles, descriptions, and bullet points with a human review queue.

## 📦 Product Catalogue Sync

Periodic CSV/Excel import from client's ERP system, shared across both workstreams for product matching and content generation.

## Documentation

- [Product Requirements Document (PRD)](docs/product/03-prd.md)

## Tech Stack

- **Frontend:** Next.js 14 + Tailwind CSS + shadcn/ui
- **Backend:** Next.js API Routes / Hono.js
- **Database:** PostgreSQL
- **OCR:** Google Cloud Vision API
- **AI/LLM:** Google Gemini + OpenAI GPT-4o
- **Image Processing:** remove.bg + Sharp.js + DALL-E 3
- **Storage:** DigitalOcean Spaces
- **WhatsApp:** GreenAPI

## Project Info

| Field | Value |
|-------|-------|
| **Client** | Evergreen Group Pte Ltd |
| **Builder** | NexStack Pte Ltd |
| **Budget** | SGD 50,000 |
| **Timeline** | 4 weeks |
| **Status** | Draft |

---

Built by [NexStack](https://nexstack.sg)
