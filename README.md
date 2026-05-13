# SokaTechnologies Docs

Repositorio principal de documentacion estrategica, comercial, operativa y tecnica de SokaTechnologies.

## Proposito

Centralizar informacion practica para vender, entregar y mantener proyectos B2B con criterios consistentes, reutilizables y seguros.

## Que contiene

- Contexto de empresa, servicios y posicionamiento.
- Procesos comerciales, de entrega, soporte y mantenimiento.
- Estandares tecnicos, stack recomendado y criterios de seguridad.
- Plantillas para trabajar con Codex, ChatGPT y documentacion interna.
- Documentacion de marketing, web publica y productos propios.

## Estructura oficial

```text
docs/
├── empresa/
├── procesos/
├── tecnico/
├── codex/
├── marketing/
└── productos/
```

| Carpeta | Descripcion |
| --- | --- |
| `docs/empresa/` | Contexto de SokaTechnologies, servicios, foco de negocio y criterios base. |
| `docs/procesos/` | Procesos comerciales, entrega de proyectos y operacion repetible. |
| `docs/tecnico/` | Stack tecnico, seguridad, arquitectura y estandares de implementacion. |
| `docs/codex/` | Instrucciones, plantillas y reglas para usar Codex en este repo. |
| `docs/marketing/` | Web, mensajes comerciales, contenido publico y materiales de marketing. |
| `docs/productos/` | Documentacion de productos propios, alcance, validacion y propuestas. |

## Documentos principales

- [`00_Contexto_Empresa.md`](./docs/empresa/00_Contexto_Empresa.md)
- [`01_Servicios.md`](./docs/empresa/01_Servicios.md)
- [`03_Proceso_Comercial.md`](./docs/procesos/03_Proceso_Comercial.md)
- [`04_Proceso_Entrega.md`](./docs/procesos/04_Proceso_Entrega.md)
- [`05_Stack_Tecnico.md`](./docs/tecnico/05_Stack_Tecnico.md)
- [`06_Estandares_Seguridad.md`](./docs/tecnico/06_Estandares_Seguridad.md)
- [`10_Codex_AGENTS_Template.md`](./docs/codex/10_Codex_AGENTS_Template.md)
- [`Web_SokaTechnologies_WordPress.md`](./docs/marketing/Web_SokaTechnologies_WordPress.md)

## Reglas de confidencialidad

- No incluir secretos, credenciales, tokens ni claves de API.
- No incluir datos reales o confidenciales de clientes.
- No mezclar informacion entre clientes, proyectos o cuentas.
- Usar nombres genericos en ejemplos, plantillas y casos publicos.
- Validar con asesoria legal, fiscal o contable cuando el documento trate esos temas.

## Uso con ChatGPT

- Compartir solo el fragmento minimo necesario.
- Anonimizar nombres de clientes, contactos, dominios, presupuestos y datos internos sensibles.
- Pedir respuestas accionables: checklists, tablas, pasos o plantillas.
- Revisar cualquier salida antes de incorporarla al repo.

## Uso con Codex

- Revisar y respetar [`AGENTS.md`](./AGENTS.md) antes de modificar documentos.
- Antes de editar, indicar documento, objetivo, estructura propuesta y riesgos de confidencialidad.
- Preferir actualizar documentos existentes antes de crear variantes nuevas.
- Mantener cambios cortos, claros y utiles para operacion real.
- Verificar que no se agreguen secretos ni informacion sensible.

## Que no debe subirse

- Secretos, credenciales, tokens, claves privadas o archivos `.env`.
- Datos reales de clientes, usuarios, contratos o conversaciones privadas.
- Backups, dumps de base de datos o exports internos.
- Capturas, logs o reportes con informacion sensible.
- Archivos generados que no aporten valor documental.

## Flujo para actualizar documentos

1. Confirmar el objetivo operativo del cambio.
2. Buscar si ya existe un documento relacionado.
3. Actualizar el archivo mas cercano y mantener la estructura accionable.
4. Usar listas, tablas, pasos o plantillas cuando aplique.
5. Revisar enlaces y coherencia con otros documentos.
6. Verificar que no haya informacion sensible antes de guardar.
