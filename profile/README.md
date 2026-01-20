# Closter

Operational platform for circular fashion that coordinates intake, valuation, consignment, and sales workflows through Shopify and integrations with external systems.

## Core Repositories

### `closter-core`
FastAPI backend and Next.js application for administration and intake. Contains the complete technical documentation of the system in `/doc`, which serves as the single source of truth.

**Responsibilities:**
- Operational Hub: maintains internal state, events, and projections
- API and webhooks for external integrations
- Admin/Intake surface with Stack Auth authentication
- Task system in `/tasks` for work management

### `closter-theme`
Shopify Liquid theme for the public storefront. End-user surface with native Shopify authentication.

## Architecture at a Glance

- **Operational Hub**: Own database (Neon Postgres) as operational coordination center
- **External integrations**: Shopify and ConsignCloud via APIs and webhooks (no data replication)
- **Architecture**: Event-driven with DDD-lite principles, idempotency, and observability
- **Surface separation**: Storefront (Shopify auth) vs Admin/Intake (Stack Auth)
- **Source of truth**: Technical documentation in `closter-core/doc`

## Documentation

The complete technical documentation of the system lives in `closter-core/doc` and is the single source of truth. Architectural decisions, integration guides, and technical specifications are maintained there.

## How We Work

1. **Issues**: Issues are created for bugs, features, or architectural decisions
2. **Tasks**: For features, `Task.md` is created/updated in `closter-core/tasks/active/` linked to the issue
3. **PRs**: Pull requests must reference issues and, when applicable, tasks
4. **Merge**: After review and approval, merge to main branch

## Security & Access

- **Storefront**: Native Shopify authentication
- **Admin/Intake**: Stack Auth for internal operators
- Clear separation of responsibilities and authentication surfaces

