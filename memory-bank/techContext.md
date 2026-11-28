# Contexto técnico

Este documento registra el estado técnico comprobable del repositorio. La presencia de una recomendación en la plantilla no significa que se haya aprobado como decisión de arquitectura.

## Hechos confirmados en el repositorio

- El repositorio es una plantilla de monorepo para el proyecto transversal de AI Engineering. Su README asigna responsabilidades a `uis/`, `services/`, `data/`, `agents/`, `skills/`, `mcps/`, `workflows/`, `packages/`, `shared/`, `docs/`, `infra/`, `scripts/` e `internal/`.
- `.devcontainer/devcontainer.json` configura una imagen base Ubuntu 24.04, Python 3.12, Node.js 22, Docker, GitHub CLI y SSH. Configura puertos reenviados 3000, 8000 y 5678.
- Existe `packages/shared/package.json` para `@repo/shared-types`, como paquete privado de tipos compartidos. Tiene versión `0.0.1` y no define scripts.
- `packages/shared/types/index.ts` contiene tipos genéricos de ejemplo (`Id` y `BaseEntity`), no un modelo de dominio completo.
- El README describe el repositorio como una estructura base sin aplicaciones ejecutables ni runner de workspace en la raíz. La existencia de carpetas y guías no implica que sus sistemas estén implementados.

## Convenciones de la plantilla

- El README raíz asigna las interfaces de usuario a `uis/`, los backends y workers a `services/`, los datos a `data/`, el código reutilizable a `packages/` y los recursos compartidos no empaquetados a `shared/`.
- Antes de crear o modificar código de producto, se debe comprobar el árbol y los recursos existentes y consultar el README raíz y el README de la ruta candidata. Si existe una guía local, se sigue esa guía.
- No se debe crear un segundo árbol de frontend, backend o API en una ubicación alternativa a la estructura de la plantilla.
- Si no está clara la ubicación de un componente o servicio, la propuesta debe justificarse y consultarse antes de implementarla.

## Recomendaciones de la plantilla, no decisiones aprobadas

- El README recomienda comenzar con una API FastAPI centralizada y evitar microservicios prematuros. No se encontró una decisión aprobada ni una API implementada en este repositorio.
- Las rutas de ejemplo, tecnologías sugeridas y responsabilidades descritas en los README orientan la organización; no confirman por sí solas la selección de un framework, servicio o arquitectura concreta.

## Decisiones técnicas pendientes

- Frameworks y tecnologías de las aplicaciones de producto, más allá de las herramientas configuradas en el devcontainer.
- Arquitectura y contratos de la API, persistencia, autenticación, despliegue y observabilidad.
- Fuentes de datos, integraciones con los sistemas de punto de venta y mecanismos de ingesta.
- Dependencias de ejecución, gestor de paquetes y configuración de workspace para las aplicaciones futuras.
- Diseño técnico, permisos y flujo de aprobación del agente propuesto para compras.

## Referencias

- [README del monorepo](../README.md)
- [Guía de interfaces](../uis/README.md)
- [Guía de servicios](../services/README.md)
- [Datos fuente](../data/raw/README.md)
- [Pipelines de datos](../data/pipelines/README.md)
- [Datos procesados](../data/process/README.md)
- [Evaluación de datos](../data/eval/README.md)
- [Configuración del devcontainer](../.devcontainer/devcontainer.json)
- [Paquete de tipos compartidos](../packages/shared/package.json)
- [Tipos actuales](../packages/shared/types/index.ts)
- [Project brief](./projectbrief.md)
