# 🚀 Closter Roadmap 2026

> **📋 Important:** Before reading this roadmap, please review our [Planning Methodology](./PLANNING_GUIDE.md) to understand how strategic roadmap phases connect to milestones, issues, and weekly execution.

**From Core Infrastructure to Operational Launch**

## Phase 1: Core & Foundation

### Milestone 0.1 – "The Engine"
**Period:** January 20 – January 27

#### Focus

Establishing the core operational backbone of Closter, including infrastructure, security, and system boundaries.

#### Key Deliverables

**Core Platform Architecture**
- High-efficiency monorepo structure
- FastAPI backend for domain logic, events, and integrations
- Next.js Admin/Intake application for internal operations

**Operational Database**
- Neon PostgreSQL (serverless) as the central operational hub
- Schema migrations managed via Alembic
- Foundation for event storage and read models

**Hybrid Authentication Model**
- Stack Auth for internal operators and administrative access
- Shopify Customer Authentication for storefront users, avoiding duplicate accounts

**Media Infrastructure**
- Supabase Storage (S3-compatible) for images and media assets

#### Goal

Deliver a stable, secure, and scalable foundation on top of which all business workflows can be built, fully aligned with the Shopify ecosystem.

---

## Phase 2: Intelligent Intake & AI

### Milestone 0.5 – "The Brain"
**Period:** January 28 – February 4

#### Focus

Extreme automation of product intake and cataloging through AI-driven workflows.

#### Key Deliverables

**AI Intake Graph**
- LangGraph-based AI pipeline (GPT-4o)
- Automated extraction of brand, size, condition, and category from images

**ConsignCloud Integration**
- Bidirectional synchronization of inventory and categories
- Alignment between external consignment data and Closter's operational state

**Operator Intake UI**
- Warehouse-optimized interface
- Batch uploads and AI-assisted corrections
- Designed for speed and low cognitive load

#### Goal

Reduce product creation time from minutes to seconds while minimizing human error in cataloging.

---

## Phase 3: Shopify Ecosystem & Logistics

### Milestone 0.8 – "The Business"
**Period:** February 5 – February 12

#### Focus

Enable direct sales, intelligent pricing, and automated logistics workflows.

#### Key Deliverables

**Shopify App Proxy Integration**
- Secure exposure of Closter data within the closter.pl domain
- Embedded operational data inside the storefront experience

**AI Pricing Engine (RAG-based)**
- Retrieval-augmented pricing suggestions
- Historical comparable sales analysis to recommend optimal market pricing

#### Goal

Fully automate the flow from sale → fulfillment, allowing the business to scale without proportional increases in administrative workload.

---

## Phase 4: Consignor Portal & Payouts

### Milestone 1.0 – "The Scale"
**Period:** February 13 – February 27

#### Focus

Consignor experience, trust, transparency, and financial settlements.

#### Key Deliverables

**Consignor Portal**
- Visibility into listed items, sales history, and accumulated balance
- Clear, self-service access to operational state

**Payout System**
- Withdrawal logic supporting bank transfers and Stripe / Przelewy24
- Auditable and deterministic financial flows

**Database Security (RLS)**
- Row Level Security for strict data isolation
- Each user can only access their own financial and inventory data

#### Goal

Create a trustworthy, scalable consignor experience that supports long-term retention and growth.

---

## Phase 5: UX Refinement & Operational Hardening

#### Focus

UX polish, operational robustness, and iteration based on real usage.

#### Scope

- Form and workflow refinement
- Edge-case handling
- Performance and usability improvements across all surfaces

---

## Summary

This roadmap represents Closter's progression from a robust operational core to a fully functioning, scalable circular fashion platform, with clear milestones, measurable outcomes, and a strong emphasis on automation, security, and integration.

