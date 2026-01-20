# Closter

Operational platform for circular fashion, coordinating intake, valuation, consignment and sales workflows across multiple systems.

## Core Repositories

### closter-core
Backend platform and internal admin application that act as the operational hub of Closter.

**Responsibilities:**
- Operational hub: maintains internal state, events and projections
- Business logic, domain rules and workflow orchestration
- APIs and webhooks for external integrations
- Admin / Intake surface for internal operators (Stack Auth)
- Technical documentation in `/doc` (single source of truth)
- Task system in `/tasks` for structured work management

### closter-theme
Public storefront implementation built as a separate repository.

**Responsibilities:**
- End-user facing storefront
- Commerce and customer interactions
- Native platform authentication for end users
- Integration with Closter-Core via APIs and webhooks

## Architecture at a Glance

- **Operational Hub:** Own database (Neon Postgres) used as the internal coordination layer
- **External systems:** Commerce platforms and consignment systems integrated via APIs and webhooks
- **Architecture:** Event-driven, DDD-lite principles, idempotency and observability
- **Surface separation:**
  - Storefront → end users
  - Admin / Intake → internal operators
- **Source of truth:** Technical documentation in `closter-core/doc`

## Documentation

All technical documentation lives in `closter-core/doc` and is the single source of truth for:
- Architecture decisions
- Integration contracts
- Internal workflows
- Technical specifications

## How We Work

1. **Issues** — Created for bugs, features or architectural decisions
2. **Tasks** — For features, a task file is created or updated in `closter-core/tasks/active/` and linked to the issue
3. **Pull Requests** — Must reference the relevant issue (and task when applicable)
4. **Merge** — Changes are merged after review and approval

## Security & Access

- **Storefront:** Native platform authentication for end users
- **Admin / Intake:** Stack Auth for internal operators
- Clear separation of responsibilities and authentication surfaces
