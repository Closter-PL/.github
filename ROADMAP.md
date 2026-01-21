# 🚀 Closter Roadmap 2026

> **📋 Important:** Before reading this roadmap, please review our [Planning Methodology](./PLANNING_GUIDE.md) to understand how strategic roadmap phases connect to milestones, issues, and weekly execution.

**From Event-Driven Core to Operational Scale**

## Phase 1 — Core Infrastructure & Event Backbone
### Milestone V1 — Foundation / Core Alive

**Period:** Jan 26 – Feb 14

#### Focus

Establish the event-driven foundation of Closter. Introduce the core mechanisms that allow the system to evolve safely without breaking existing contracts.

#### Key Deliverables

**Event-Driven Core**
- Append-only Event Store (PostgreSQL, JSONB)
- In-memory Event Bus (pub/sub)
- Dual-write strategy (DB + events) for backward compatibility
- Correlation & causation groundwork

**Read Model Foundations**
- Items projection
- Deterministic projection handlers
- Feature-flagged read switch (tables → projections)

**Operational Backbone**
- FastAPI backend as the system of record
- Alembic-managed migrations
- Neon PostgreSQL as central operational DB

**Outbox Foundation**
- Outbox tasks table
- First operational task (Shopify sync)
- Worker process with idempotent execution

#### Goal

The system is alive. Core flows work end-to-end, events are first-class citizens, and the platform can grow without architectural rewrites.

---

## Phase 2 — Stability, Lifecycle & Intelligence
### Milestone V1.1 — Stability & Lifecycle

**Period:** Feb 17 – Feb 28

#### Focus

Make the system robust under real operational conditions. Complete lifecycle coverage and add safety mechanisms.

#### Key Deliverables

**Lifecycle Events**
- ProductUpdated, ProductDeleted, ProductPublished
- ValuationRequested / ValuationCompleted

**System Robustness**
- Projection rebuild tooling
- Consistency validation (tables vs projections)
- Retry logic (basic) and failure handling

**AI-Assisted Intake (Integrated)**
- AI-driven intake flows aligned with event model
- Operator-friendly intake UX
- AI corrections without breaking domain invariants

#### Goal

The system tolerates change, failures, and day-to-day operations without data drift or manual fixes.

---

## Phase 3 — Full Read Model & Domain Visibility
### Milestone V1.2 — Full Read Model

**Period:** Mar 3 – Mar 7

#### Focus

Complete the domain read model so the backend no longer depends on operational tables for queries.

#### Key Deliverables

**Domain Projections**
- Listings projection
- Contracts projection
- Offers projection

**Read Isolation**
- All GET endpoints served from projections
- Feature flags for safe rollout and rollback

#### Goal

The domain is fully observable, queryable, and decoupled from write paths.

---

## Phase 4 — Operational Automation & Integrations
### Milestone V2 — Operational Automation

**Period:** Mar 10 – Mar 28

#### Focus

Automate business operations end-to-end using deterministic, event-driven workflows.

#### Key Deliverables

**Outbox Pattern (Complete)**
- All task types implemented
- Idempotent, retryable execution
- Dead-letter handling

**External Integrations**
- Shopify publishing & sync
- PSP and carrier webhooks
- Event → task mapping layer

**Business Logic Automation**
- Contract Readiness Evaluator
- Financial and logistics workflows
- No manual glue code

#### Goal

The system works by itself. Human intervention is the exception, not the rule.

---

## Phase 5 — Scale, Observability & Compliance
### Milestone V3 — Scale, Observability & Compliance-Ready

**Period:** Mar 31 – Apr 11

#### Focus

Prepare Closter for scale, audits, and regulated growth.

#### Key Deliverables

**Observability**
- Prometheus metrics
- Structured logging with correlation IDs
- Event flow inspection endpoints

**Traceability & Debugging**
- Full event chains per request
- Deterministic reasoning for system decisions

**Compliance Readiness**
- VAT / KSeF hooks (no logic yet)
- Auditable financial and operational trails

#### Goal

The system can be debugged, audited, and scaled with confidence.

---

## Summary

This roadmap transitions Closter from a traditional CRUD platform into a deterministic, event-driven operating system for circular fashion.

- Early phases focus on correctness and evolvability
- Middle phases unlock automation and scale
- Final phase ensures observability, trust, and compliance

No hype, no shortcuts — just a system that can survive real growth.

