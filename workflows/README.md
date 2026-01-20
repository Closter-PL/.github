# Workflows Compartidos

Esta carpeta contiene workflows de GitHub Actions compartidos para la organización.

Los workflows definidos aquí pueden ser reutilizados por los repositorios de la organización (`closter-core`, `closter-theme`, etc.) mediante la sintaxis de `workflow_call` o referencias a workflows reutilizables.

## Estado Actual

Actualmente no hay workflows definidos. Se añadirán según se definan los requisitos de CI/CD y automatización para los repositorios de la organización.

## Estructura Propuesta

Cuando se definan workflows, se organizarán por propósito:
- `ci/` - Workflows de integración continua
- `cd/` - Workflows de despliegue continuo
- `automation/` - Workflows de automatización (dependabot, sync, etc.)

## Uso en Repositorios

Los repositorios individuales pueden referenciar workflows compartidos desde este repositorio usando la sintaxis estándar de GitHub Actions.

