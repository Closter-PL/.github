# Closter

Plataforma operativa para moda circular que coordina workflows de intake, valoración, consignación y venta a través de Shopify e integraciones con sistemas externos.

## Core Repositories

### `closter-core`
Backend FastAPI y aplicación Next.js para administración e intake. Contiene la documentación técnica completa del sistema en `/doc`, que actúa como fuente de verdad única.

**Responsabilidades:**
- Operational Hub: mantiene estado interno, eventos y proyecciones
- API y webhooks para integraciones externas
- Superficie Admin/Intake con autenticación Stack Auth
- Sistema de tareas en `/tasks` para gestión de trabajo

### `closter-theme`
Tema Shopify Liquid para el storefront público. Superficie de usuario final con autenticación nativa de Shopify.

## Architecture at a Glance

- **Operational Hub**: Base de datos propia (Neon Postgres) como centro de coordinación operativa
- **Integraciones externas**: Shopify y ConsignCloud vía APIs y webhooks (no replicación de datos)
- **Arquitectura**: Event-driven con principios DDD-lite, idempotencia y observabilidad
- **Separación de superficies**: Storefront (Shopify auth) vs Admin/Intake (Stack Auth)
- **Fuente de verdad**: Documentación técnica en `closter-core/doc`

## Documentation

La documentación técnica completa del sistema vive en `closter-core/doc` y es la única fuente de verdad. Decisiones arquitectónicas, guías de integración y especificaciones técnicas se mantienen allí.

## How We Work

1. **Issues**: Se crean issues para bugs, features o decisiones arquitectónicas
2. **Tasks**: Para features, se crea/actualiza `Task.md` en `closter-core/tasks/active/` vinculado a la issue
3. **PRs**: Pull requests deben referenciar issues y, cuando aplique, tasks
4. **Merge**: Tras revisión y aprobación, se mergea a la rama principal

## Security & Access

- **Storefront**: Autenticación nativa de Shopify
- **Admin/Intake**: Stack Auth para operadores internos
- Separación clara de responsabilidades y superficies de autenticación

