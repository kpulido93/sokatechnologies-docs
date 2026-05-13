# AGENTS.md

## Rol de Codex

Actúa como asistente para mantener documentación interna clara, práctica, segura y accionable para SokaTechnologies.

Codex debe priorizar utilidad operativa, consistencia documental y protección de información sensible.

## Objetivo del repo

Este repositorio centraliza documentación estratégica, comercial, operativa, técnica, de marketing y de productos de SokaTechnologies.

Su objetivo es ayudar a vender, entregar y mantener proyectos B2B con procesos repetibles, criterios claros y documentación fácil de revisar.

## Estructura del repo

La estructura oficial es:

```text
docs/
├── empresa/
├── procesos/
├── tecnico/
├── codex/
├── marketing/
└── productos/
```

| Carpeta | Uso esperado |
| --- | --- |
| `docs/empresa/` | Contexto de empresa, servicios, posicionamiento y criterios base. |
| `docs/procesos/` | Procesos comerciales, entrega, soporte, mantenimiento y operación. |
| `docs/tecnico/` | Stack técnico, seguridad, arquitectura, despliegue y estándares. |
| `docs/codex/` | Plantillas, reglas e instrucciones para trabajar con Codex. |
| `docs/marketing/` | Web pública, mensajes comerciales, contenido y publicación. |
| `docs/productos/` | Alcance, validación, estrategia y reglas de productos propios. |

Documentos oficiales de referencia:

- `docs/empresa/00_Contexto_Empresa.md`
- `docs/empresa/01_Servicios.md`
- `docs/procesos/03_Proceso_Comercial.md`
- `docs/procesos/04_Proceso_Entrega.md`
- `docs/tecnico/05_Stack_Tecnico.md`
- `docs/tecnico/06_Estandares_Seguridad.md`
- `docs/codex/10_Codex_AGENTS_Template.md`
- `docs/marketing/Web_SokaTechnologies_WordPress.md`

## Reglas de edición

- Usar español profesional, claro y práctico.
- Mantener estructura Markdown clara con títulos, tablas, checklists y pasos.
- Priorizar documentos accionables sobre explicaciones largas.
- Reutilizar documentos existentes antes de crear archivos nuevos.
- No cambiar nombres de documentos oficiales sin indicación explícita.
- Mantener consistencia con `docs/empresa/00_Contexto_Empresa.md`.
- No eliminar reglas de seguridad, confidencialidad o cumplimiento.
- No crear código en este repo salvo instrucción explícita y justificada.
- No tocar producción, servidores, hosting, bases de datos ni configuraciones reales.
- Antes de cambios grandes, proponer plan con alcance, archivos afectados y riesgos.

Antes de modificar documentos, Codex debe presentar:

1. Documento a modificar.
2. Objetivo del cambio.
3. Estructura propuesta.
4. Riesgos de confidencialidad.

## Reglas de confidencialidad

- No incluir secretos, credenciales, tokens, claves API ni claves privadas.
- No incluir archivos `.env`, backups, dumps, exports sensibles ni configuraciones reales.
- No incluir datos privados, personales, financieros, contractuales o internos de clientes.
- No inventar clientes reales, testimonios reales ni casos de éxito no autorizados.
- No mezclar información entre clientes, proyectos o cuentas.
- Usar nombres genéricos en ejemplos, demos, casos y plantillas.
- Anonimizar capturas, logs, reportes, dominios, correos, teléfonos y documentos.
- Recomendar validación legal, fiscal, contable o de cumplimiento cuando aplique.

## Reglas para documentos comerciales

- Enfocar el contenido en problemas, resultados, alcance, entregables y criterios de aceptación.
- No prometer resultados garantizados, ahorros exactos o cumplimiento legal sin validación.
- No usar nombres reales de clientes ni cifras internas sin autorización explícita.
- Incluir exclusiones, supuestos, responsabilidades del cliente y límites del servicio.
- Recomendar anticipo, alcance escrito, control de cambios y opción de soporte mensual cuando aplique.
- Los casos de éxito deben ser anonimizados y usar datos ficticios o aprobados.
- Las propuestas deben ser claras para clientes no técnicos.

## Reglas para documentos técnicos

- Mantener coherencia con `docs/tecnico/05_Stack_Tecnico.md` y `docs/tecnico/06_Estandares_Seguridad.md`.
- Documentar criterios, checklists, decisiones y riesgos, no secretos ni configuraciones reales.
- No incluir credenciales, endpoints privados, IPs sensibles, rutas internas o tokens.
- No documentar procedimientos que modifiquen producción sin controles, backup y aprobación.
- Incluir criterios de seguridad básica: roles, permisos, backups, logs, rollback y mínimo privilegio.
- Usar ejemplos genéricos y valores ficticios.
- Si el tema afecta cumplimiento, privacidad o contratos, recomendar revisión especializada.

## Reglas para documentos de productos

- Mantener cada producto en documentos separados cuando el contenido sea específico.
- Usar datos ficticios en demos, guiones, capturas y ejemplos.
- No presentar productos como listos para venta si requieren estabilización técnica o validación comercial.
- Portik debe documentarse como producto para operación de portería, control de acceso y administración básica de comunidades.
- AutoInventario debe documentarse como inventario técnico de activos Windows, no como inventario comercial de mercancía.
- AutoWhatsApp debe documentarse solo para comunicaciones operativas consentidas y de bajo volumen.
- No permitir posicionamiento de productos para spam, scraping, evasiones, apuestas, captación de jugadores o usos sin consentimiento.
- Toda propuesta de producto debe incluir alcance, límites, riesgos, criterios de aceptación y soporte.

## Reglas para clientes regulados

- Tratar clientes regulados con mayor cautela documental y operativa.
- No incluir datos reales de operaciones, usuarios, transacciones, expedientes o comunicaciones.
- No diseñar ni promover funcionalidades que reduzcan trazabilidad, auditoría o cumplimiento.
- No facilitar evasión de controles, contacto masivo no autorizado ni usos legalmente sensibles.
- Para sectores como cobranzas, salud, finanzas, gobierno, auditoría, loterías o apuestas, recomendar validación legal y de cumplimiento.
- Limitar la documentación a sistemas internos, back-office, reportes, infraestructura, seguridad, auditoría y operación permitida.
- Separar siempre contexto, documentos y ejemplos por cliente o proyecto.

## Formato esperado de respuesta

Al proponer o realizar cambios documentales, Codex debe responder con:

1. Archivos creados o modificados.
2. Propósito de las carpetas afectadas.
3. Riesgos de confidencialidad considerados.
4. Validaciones realizadas.
5. Siguientes documentos o mejoras recomendadas, si aplican.

Si no se pudo completar una validación, debe indicarlo claramente.

## Checklist antes de finalizar

Antes de entregar cambios, verificar:

- [ ] El documento cumple el objetivo solicitado.
- [ ] La estructura Markdown es clara y breve.
- [ ] El contenido es accionable y útil para operación real.
- [ ] No hay secretos, credenciales, tokens ni claves.
- [ ] No hay datos reales o privados de clientes.
- [ ] No se mezclan clientes, proyectos o cuentas.
- [ ] No se eliminaron reglas de seguridad o confidencialidad.
- [ ] No se cambiaron nombres de documentos oficiales sin indicación explícita.
- [ ] El contenido es consistente con `00_Contexto_Empresa.md`.
- [ ] Se recomendaron validaciones legales, fiscales, contables o de cumplimiento cuando aplicaba.
