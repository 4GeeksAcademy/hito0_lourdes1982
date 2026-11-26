---
name: memory-bank-update
description: "Use only after the developer has reviewed an implementation and expressly approved it. Update only affected memory-bank documents, verify every statement against the repository, and keep confirmed decisions separate from proposals and open questions."
---

# Actualización del banco de memoria

## Objetivo

Actualizar únicamente los documentos de `memory-bank/` afectados por una implementación que el desarrollador haya revisado y aprobado expresamente. La autorización para implementar, la finalización del trabajo o la preparación de un commit no activan esta skill.

## Inputs

- La implementación revisada, con el diff o las rutas de los cambios.
- La señal expresa del desarrollador que confirma su visto bueno después de revisar esa implementación.
- Los documentos actuales de `memory-bank/`.
- Las fuentes pertinentes del repositorio y las comprobaciones realizadas.
- El estado verificado de tareas, próximos pasos y bloqueos.

Si falta la señal de aprobación posterior a la revisión, o no se puede identificar qué implementación aprobó el desarrollador, no modifiques el banco. Explica qué confirmación falta y detente.

## Procedimiento

1. Confirma que el visto bueno se dio después de revisar la implementación. No lo infieras de una autorización previa para implementar ni del hecho de que el trabajo haya terminado.
2. Examina el diff aprobado y el estado actual del repositorio. Separa los cambios implementados de recomendaciones, propuestas y asuntos todavía pendientes.
3. Determina qué documentos están realmente afectados:
   - `projectbrief.md`: solo si cambia el objetivo, el problema o el alcance de negocio confirmado.
   - `techContext.md`: solo si se confirma una decisión técnica, restricción o convención del proyecto que deba quedar registrada.
   - `progress.md`: para reflejar estados reales, tareas verificadas, próximos pasos y bloqueos.
4. Modifica únicamente los documentos afectados. Si un documento no refleja un cambio relevante, déjalo intacto.
5. Mantén explícita la diferencia entre hechos confirmados, prioridades declaradas, propuestas y cuestiones pendientes. No conviertas una propuesta en decisión aprobada.
6. Contrasta cada afirmación nueva o modificada con el diff, los archivos y las comprobaciones pertinentes. En `progress.md`, no marques como completada una tarea que no esté verificada.
7. Revisa el diff de los documentos de memoria y comunica qué se actualizó, qué se dejó sin cambios y cómo se verificó la coherencia con el repositorio.

## Límites

- Esta skill solo modifica documentos afectados dentro de `memory-bank/`.
- No modifica briefing, reglas, skills, instrucciones, código de producto ni configuración.
- No añade decisiones técnicas que no hayan sido confirmadas.
- No actualiza documentos por anticipado ni para mantener una apariencia de progreso.

## Criterios de aceptación

- Existe visto bueno expreso posterior a la revisión de la implementación concreta.
- Se identificaron los documentos afectados antes de editarlos.
- Solo se modificaron los documentos de memoria afectados.
- Cada afirmación nueva coincide con el diff y el estado real del repositorio, o está atribuida a una fuente.
- `progress.md` contiene solo estados reales, tareas verificadas, próximos pasos y bloqueos.
- Hechos, prioridades, propuestas y pendientes permanecen diferenciados.
- El resultado informa de los documentos modificados, los no afectados y las comprobaciones realizadas.
