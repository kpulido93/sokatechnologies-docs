# SokaTechnologies Docs

Repositorio central de documentacion interna de SokaTechnologies para vender, entregar y mantener proyectos B2B con criterios consistentes.

## Objetivo

Mantener en un solo lugar los procesos, estandares, plantillas y reglas operativas que el equipo necesita para:

- vender con propuestas claras y controladas;
- ejecutar proyectos con menos ambiguedad;
- operar soporte y mantenimiento con expectativas explicitas;
- documentar decisiones repetibles sin depender de memoria informal.

## Como usar este repositorio

1. Busca primero si ya existe un documento o plantilla util.
2. Actualiza el documento mas cercano en lugar de duplicar contenido.
3. Mantén cada archivo breve, accionable y orientado a operacion real.
4. Usa checklists, tablas y plantillas antes que texto narrativo largo.
5. Elimina o anonimiza cualquier dato sensible antes de guardar cambios.

## Reglas no negociables

- No incluir secretos, credenciales, tokens ni archivos de entorno.
- No incluir datos confidenciales de clientes ni mezclar informacion entre cuentas.
- Usar nombres genericos en ejemplos, notas y plantillas.
- Recomendar revision legal, fiscal o contable cuando el tema lo requiera.
- Mantener la documentacion alineada con la forma real de trabajar del equipo.

## Estructura

| Ruta | Proposito |
| --- | --- |
| `docs/company` | Definicion de empresa, posicionamiento y servicios. |
| `docs/sales` | Discovery, propuestas y criterios comerciales. |
| `docs/delivery` | Kickoff, requisitos, control de cambios y cierre. |
| `docs/technical` | Estandares de ingenieria, seguridad y despliegue. |
| `docs/operations` | Soporte, mantenimiento e incidentes. |
| `docs/templates` | Plantillas reutilizables para trabajo recurrente. |
| `scripts` | Scripts auxiliares futuros para automatizacion documental. |
| `tests` | Validaciones o checks automatizados futuros del repositorio. |

## Flujo recomendado para editar

1. Define el resultado operativo que el documento debe habilitar.
2. Revisa [AGENTS.md](./AGENTS.md) antes de tocar contenido.
3. Estructura el cambio con objetivo, pasos, checklist o plantilla.
4. Verifica que no haya informacion sensible.
5. Actualiza enlaces relacionados si el cambio afecta otros documentos.

## Documentos iniciales

- Empresa y servicios: [overview](./docs/company/overview.md), [services](./docs/company/services.md)
- Ventas: [discovery](./docs/sales/discovery.md), [proposal-template](./docs/sales/proposal-template.md), [pricing-principles](./docs/sales/pricing-principles.md)
- Delivery: [project-kickoff](./docs/delivery/project-kickoff.md), [requirements-template](./docs/delivery/requirements-template.md), [change-control](./docs/delivery/change-control.md), [handoff-checklist](./docs/delivery/handoff-checklist.md)
- Tecnico: [engineering-standards](./docs/technical/engineering-standards.md), [security-standards](./docs/technical/security-standards.md), [deployment-standards](./docs/technical/deployment-standards.md), [codex-workflow](./docs/technical/codex-workflow.md)
- Operaciones: [support-process](./docs/operations/support-process.md), [maintenance-plans](./docs/operations/maintenance-plans.md), [incident-response](./docs/operations/incident-response.md)
- Plantillas: [meeting-notes](./docs/templates/meeting-notes.md), [client-brief](./docs/templates/client-brief.md), [case-study-template](./docs/templates/case-study-template.md)
