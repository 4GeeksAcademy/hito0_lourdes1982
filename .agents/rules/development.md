# Regla de desarrollo del monorepo

## Alcance

Esta regla se aplica antes de crear, modificar o reorganizar código de producto, componentes, servicios, pipelines, agentes de producto o automatizaciones dentro del monorepo. `AGENTS.md` exige consultarla antes de realizar tareas de desarrollo. Para actualizar el banco de memoria, sigue la skill `memory-bank-update` y su requisito de aprobación; esta regla no autoriza esas actualizaciones.

## Ubicación y estructura

- Antes de crear o modificar código, revisa el árbol y los recursos existentes, el README raíz y el README de la carpeta candidata. Sigue también las guías de subcarpetas que correspondan.
- Coloca cada componente en la responsabilidad definida por la plantilla: interfaces en `uis/`, servicios backend y workers en `services/`, código reutilizable en `packages/`, recursos compartidos no empaquetados en `shared/`, y datos y pipelines en las rutas de `data/` previstas para ellos. Para agentes, skills, servidores MCP y workflows de producto, utiliza respectivamente `/agents`, `/skills`, `/mcps` y `/workflows`.
- No crees un segundo árbol de frontend, backend o API en ubicaciones alternativas a las previstas por la plantilla.
- Si no está clara la ubicación de un componente o servicio, no lo implementes todavía. Presenta la ruta propuesta, justifica su encaje con la estructura y las guías existentes, y espera confirmación del desarrollador.

## Cambios estructurales y dependencias

- Consulta al desarrollador antes de introducir una dependencia nueva.
- Consulta al desarrollador antes de introducir un patrón estructural nuevo, cambiar los límites entre carpetas o añadir una nueva ubicación de producto.
- No conviertas una recomendación de un README en una decisión técnica aprobada. Registra como pendiente cualquier decisión que no esté confirmada.

## Alcance del cambio

- Mantén los cambios dentro de la tarea solicitada y respeta las modificaciones preexistentes del desarrollador.
- No implementes código de producto cuando la petición se limite a análisis, planificación o configuración documental.
- Documenta cada componente nuevo según las convenciones del README correspondiente.

## Referencias

- [Guía del monorepo](../../README.md)
- [Contexto técnico registrado](../../memory-bank/techContext.md)
