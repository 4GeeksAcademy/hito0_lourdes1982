# Instrucciones para agentes de código

## Inicio de sesión

Al inicio de cada sesión, consulta estos documentos en este orden:

1. `memory-bank/projectbrief.md`
2. `memory-bank/techContext.md`
3. `memory-bank/progress.md`

Si falta alguno, indícalo y no inventes su contenido. `progress.md` es un registro de estado, no una fuente de decisiones: contrasta sus afirmaciones con el repositorio antes de actuar. Distingue hechos confirmados, prioridades declaradas, propuestas y cuestiones pendientes. Las propuestas y recomendaciones no son decisiones aprobadas.

## Desarrollo en el monorepo

Antes de realizar cualquier tarea de desarrollo, consulta obligatoriamente [la regla de desarrollo](.agents/rules/development.md) y sigue su alcance.

Antes de crear o modificar código de producto:

- Revisa el árbol y los recursos existentes.
- Consulta el README raíz y el README de la ubicación candidata, además de las guías locales que correspondan.
- Usa las ubicaciones previstas por la plantilla. No crees un segundo árbol de frontend, backend o API en una ubicación alternativa.
- Si la ubicación no está clara, explica y justifica una propuesta y espera confirmación antes de implementar.
- Consulta antes de introducir dependencias o patrones estructurales nuevos.

`/agents` y `/skills` son carpetas del producto. No las confundas con `.agents/`, que contiene configuración del agente de código.

## Mantenimiento de memoria

La autorización para implementar no autoriza a actualizar el banco de memoria. Actualízalo solo después de que el desarrollador haya revisado la implementación y haya dado su visto bueno expreso. En ese momento, sigue la skill [memory-bank-update](.agents/skills/memory-bank-update/SKILL.md), identifica los documentos afectados y modifica solo esos documentos.

En `progress.md` registra únicamente estados reales, tareas verificadas, próximos pasos y bloqueos. No conviertas propuestas en decisiones aprobadas. Comprueba que toda actualización coincide con el estado del repositorio.

## Rutas protegidas

No crees, modifiques, renombres ni elimines estas rutas sin confirmación expresa del desarrollador:

- `AGENTS.md`
- `.agents/**`
- `memory-bank/projectbrief.md`
- `memory-bank/techContext.md`
- `BRIEFING*`
- `CONTEXT*`
- `data/raw/**`
- `.devcontainer/**`
- `infra/**`

Las actualizaciones de `memory-bank/projectbrief.md` y `memory-bank/techContext.md` quedan permitidas únicamente mediante el procedimiento de mantenimiento anterior, tras el visto bueno expreso. `progress.md` solo puede actualizarse mediante ese mismo procedimiento y con el alcance descriptivo indicado.

## Comprobaciones antes de cada commit

Completa estos pasos en orden antes de cualquier commit:

1. Revisa la rama y el estado de Git; identifica cambios preexistentes y no los reviertas ni los incluyas por accidente.
2. Inspecciona el diff completo y confirma que los cambios corresponden al alcance solicitado.
3. Ejecuta las comprobaciones pertinentes y registra los resultados; no presentes como satisfactorias las que hayan fallado o no se hayan ejecutado.
4. Comprueba que no se incluyen secretos, datos personales ni datos fuente de forma indebida.
5. Prepara solo los archivos previstos e inspecciona el diff preparado.
6. Crea el commit únicamente si el desarrollador lo ha solicitado expresamente.
