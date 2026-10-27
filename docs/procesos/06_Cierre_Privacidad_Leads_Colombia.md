# Cierre de privacidad y leads en Colombia

**Estado:** pendiente de aprobación del fundador y revisión jurídica. Estado operativo actual: **NO-GO** para formularios reales.

**Alcance:** paquete de decisiones para Contacto y Diagnóstico. No modifica la política pública, el catálogo técnico ni los servicios desplegados.

Este documento separa lo que debe decidir el fundador, lo que debe revisar un asesor jurídico y lo que podrá implementar el equipo técnico después. Las propuestas operativas no son obligaciones legales por el solo hecho de estar escritas aquí.

## 1. Referencias y control de versiones

- Procedimiento interno: [`05_Gestion_Datos_Personales.md`](./05_Gestion_Datos_Personales.md).
- Seguridad e incidentes: [`06_Estandares_Seguridad.md`](../tecnico/06_Estandares_Seguridad.md) y [`incident-response.md`](../operations/incident-response.md).
- Política de privacidad en la rama Astro de referencia: [`politica-privacidad.astro`](https://github.com/kpulido93/sokatechnologies-website/blob/feature/web-demo-2026-gsap/src/pages/politica-privacidad.astro). Sigue marcada como borrador.
- Catálogo de consentimiento ya integrado mediante el [PR #17](https://github.com/kpulido93/sokatechnologies-website/pull/17) en la rama Astro `feature/web-demo-2026-gsap`: [`consentCatalog.json`](https://github.com/kpulido93/sokatechnologies-website/blob/feature/web-demo-2026-gsap/src/data/consentCatalog.json). Commit de integración verificado: `92303bf64a25ad24da9c024fd749104ad76d92b6`. Su presencia en Git no equivale a aprobación jurídica, despliegue ni activación del modo `required`.

Antes de publicar, el fundador debe conservar una copia aprobada de la política, los textos de autorización y sus hashes. Una modificación de texto exige una nueva versión, un nuevo hash y actualización coordinada del aviso mostrado por el frontend y validado por el Worker.

## 2. Responsable: campos que faltan

SokaTechnologies es actualmente una operación de una persona natural en Colombia. No se incorpora aquí su identificación, domicilio, dirección ni teléfono. Estos campos deben completarse en un documento controlado y validarse antes de publicar una política definitiva.

| Campo | Situación actual | Aprobación necesaria |
|---|---|---|
| Nombre legal completo del responsable | Pendiente; no publicar el nombre de una persona en este borrador. | Fundador y asesor jurídico |
| Identificación o NIT, si aplica | Pendiente. | Fundador, asesor fiscal/jurídico |
| Domicilio, ciudad y departamento | Pendiente. | Fundador y asesor jurídico |
| Dirección y teléfono de contacto | Pendientes. | Fundador y asesor jurídico |
| Canal para titulares | `info@sokatechnologies.com` como canal operativo previsto; confirmar titularidad, acceso y publicación. | Fundador |
| Persona o función que atiende solicitudes | El fundador opera provisionalmente esta función; falta confirmar la designación y el nombre que se publicará. | Fundador y asesor jurídico |
| Fecha de vigencia y versión de la política | Pendientes hasta aprobar el texto completo. | Fundador y asesor jurídico |
| Situación jurídica de la operación | Persona natural actualmente; formalización empresarial pendiente. | Fundador, asesor jurídico y fiscal |

La política no debe publicarse como definitiva mientras existan campos pendientes, aunque el sitio tenga una página informativa con marcadores.

## 3. Decisiones de conservación

Los siguientes periodos son propuestas operativas para aprobación. No sustituyen la revisión de obligaciones legales, contractuales, contables, tributarias, de defensa de derechos, copias de seguridad o litigios.

| Categoría | Propuesta para decidir | Acción operativa propuesta | Revisión pendiente |
|---|---|---|---|
| Lead sin contrato | 12 meses desde la última interacción útil. | Revisar mensualmente; eliminar datos de contacto y contenido o anonimizar una métrica mínima no personal. | Confirmar finalidad, excepciones y método de eliminación con el asesor jurídico. |
| Propuesta comercial | Hasta 24 meses desde la última actividad, mientras la propuesta esté activa. | Al vencer, eliminar el expediente personal o conservar únicamente una referencia no identificable si existe justificación documentada. | Confirmar relación con contratos, facturación, impuestos y defensa de derechos. |
| Clientes y contratos | Sin periodo numérico en este documento: sujeto a obligaciones legales, contractuales y contables aplicables. | Separar archivo operativo, contractual y contable; restringir acceso y eliminar por partes cuando corresponda. | Asesoría jurídica y contable deben definir periodos y excepciones. |
| Evidencia de consentimiento | Mientras exista la finalidad asociada y durante el periodo que resulte aplicable por obligación, controversia o auditoría. | Mantener solo la evidencia mínima vinculada al `request_id`; eliminar o anonimizar cuando cese la justificación. | Definir periodo, relación con el lead/contrato y tratamiento de una revocación. |
| Solicitudes de titulares e incidentes | Mientras estén abiertos y durante el periodo mínimo aprobado para demostrar su atención. | Acceso restringido; conservar la decisión y la evidencia mínima, no el contenido innecesario. | Asesoría jurídica debe confirmar periodo y excepciones. |

**Decisión del fundador:** aprobar, ajustar o rechazar cada propuesta antes de habilitar formularios. El fundador debe registrar la fecha, versión aprobada y excepción aplicable; no debe convertir esta tabla en una obligación legal sin revisión.

## 4. Proveedores, acceso y transferencias

La matriz sirve para solicitar evidencia y decisiones; no declara que un proveedor cumpla la ley ni que exista una transferencia autorizada.

| Proveedor o servicio | Datos que podría tratar | Finalidad y acceso | Región / transferencia | Evidencia y decisión pendiente |
|---|---|---|---|---|
| Cloudflare Worker | Campos enviados, identificadores técnicos mínimos, estado del procesamiento y referencias de solicitud. | Validar el formulario, aplicar controles y preparar la notificación. Acceso técnico restringido al operador autorizado. | Confirmar regiones, subencargados y tratamiento internacional según cuenta y términos vigentes. | Revisar contrato, DPA, subencargados, logs, retención, incidentes y mecanismo de supresión. |
| Cloudflare Turnstile | Token antiabuso y datos técnicos que el servicio requiera; el token no debe conservarse como evidencia. | Validar que la solicitud no sea automatizada. Acceso al resultado técnico, no a una copia innecesaria del token. | Confirmar ubicación y transferencias en la documentación vigente. | Confirmar términos, configuración, retención y si la política describe correctamente el tratamiento. |
| Resend | Datos incluidos en la notificación de Contacto o Diagnóstico, incluido el correo del remitente y `request_id`; solo cuando se autorice el flujo real. | Enviar la notificación interna a `info@sokatechnologies.com`. Acceso por el proveedor y el fundador como destinatario autorizado. | Confirmar región, subencargados y transferencias/transmisiones internacionales. | Revisar DPA, retención, logs, idempotencia, incidentes, supresión y qué estados pueden confirmarse. |
| Correo corporativo | Mensaje, remitente, destinatario, archivos si algún usuario los envía y metadatos del buzón. | Recibir y responder solicitudes; acceso solo a cuentas autorizadas. | Confirmar proveedor, región, backups, exportaciones y reenvíos. | Documentar contrato, MFA, cuentas individuales, búsqueda, retención, eliminación y revocación de accesos. |
| Google PageSpeed, si se habilita Auditoría | URL pública y métricas técnicas de rendimiento; no enviar automáticamente los datos de Contacto/Diagnóstico. | Generar recomendaciones técnicas para Auditoría server-side. Acceso solo al resultado necesario. | Confirmar regiones, términos, subprocesadores y transferencias antes de publicar Auditoría. | Mantener Auditoría no pública hasta aprobar el inventario, la finalidad, la URL permitida y la eliminación. |

Para cada proveedor, el fundador debe guardar la ficha vigente fuera de Git con: rol contractual, datos exactos, regiones, subencargados, seguridad, retención, incidentes, solicitudes de titulares y mecanismo de eliminación. El asesor jurídico debe confirmar si corresponde hablar de transferencia o transmisión internacional y qué salvaguardas documentar.

## 5. Autorización y consentimiento

### 5.1 Textos actuales que requieren aprobación

El catálogo técnico consultado contiene textos de borrador. Se reproducen para facilitar una decisión explícita; no se cambian aquí sus hashes ni sus versiones.

| Formulario | Aviso | Autorización actual | Finalidad que debe aprobarse |
|---|---|---|---|
| Contacto | `privacy-colombia-draft-v1` | `contact-response-v1`: “Autorizo a SokaTechnologies a tratar los datos personales que envío en este formulario para atender mi solicitud de contacto y comunicarse conmigo sobre ella, de acuerdo con el aviso de privacidad publicado.” | Responder la solicitud de contacto y comunicarse sobre esa solicitud. |
| Diagnóstico | `privacy-colombia-draft-v1` | `diagnostico-response-v1`: “Autorizo a SokaTechnologies a tratar los datos personales que envío en este formulario para revisar mi solicitud de diagnóstico, comunicarse conmigo sobre ella y orientar los próximos pasos, de acuerdo con el aviso de privacidad publicado.” | Revisar el diagnóstico, comunicarse sobre él y orientar los próximos pasos. |

La decisión debe cubrir:

- Si el aviso contiene la identidad, finalidades, derechos, canal, proveedores y conservación que se publicarán.
- Si cada texto es previo, expreso, informado, separado por formulario y técnicamente consultable.
- Si la finalidad de respuesta es necesaria para el flujo y si existe alguna finalidad opcional adicional.
- Que marketing no se activa en esta tarea: cualquier comunicación comercial debe tener una opción separada, no preseleccionada y una versión propia.
- Qué evidencia se conserva: `event_id`, `request_id`, fecha/hora UTC del servidor, formulario, versión del aviso, versión de autorización, hash, finalidad, resultado técnico e idempotencia mínima, sin mensajes completos, IP, user-agent, tokens ni documentos de identidad.
- Cómo se solicita y ejecuta una revocación, especialmente para finalidades opcionales, sin borrar evidencia que deba conservarse por una obligación o controversia pendiente.

### 5.2 Regla de versionado

No actualizar ahora `noticeVersion`, `authorization.version` ni sus hashes. Después de la aprobación:

1. El fundador y el asesor jurídico congelan el texto exacto y la fecha de vigencia.
2. El equipo técnico genera nuevos identificadores y hashes, actualiza frontend y Worker en el mismo cambio y verifica que ambos validen la misma versión.
3. Se conserva la versión anterior para interpretar evidencias históricas, sin reutilizarla para nuevos formularios.
4. La activación sigue bloqueada hasta pasar la matriz GO/NO-GO.

## 6. Operación mínima para un fundador

### 6.1 Recepción y registro

1. Recibir consultas, correcciones, supresiones o revocaciones únicamente en `info@sokatechnologies.com` o en otro canal que el fundador apruebe y publique.
2. Crear un registro privado con: ID interno, fecha/hora, canal, tipo de solicitud, tratamiento afectado, responsable, estado, vencimiento, acciones, respuesta y cierre. No copiar el mensaje completo ni documentos de identidad.
3. Confirmar recepción y verificar razonablemente la identidad. Pedir solo la información necesaria; no solicitar documentos completos por correo salvo que el asesor jurídico apruebe el mecanismo.
4. Calcular el vencimiento usando el procedimiento de [`05_Gestion_Datos_Personales.md`](./05_Gestion_Datos_Personales.md), con calendario de días hábiles y revisión jurídica de cualquier caso dudoso.

### 6.2 Localización y atención

- Si existe `request_id`, buscarlo únicamente en el almacenamiento interno autorizado y relacionarlo con la evidencia mínima; no crear un endpoint público de consulta.
- Si no existe `request_id`, localizar por referencias mínimas del correo corporativo y del formulario, evitando duplicar datos en hojas, tickets o logs.
- Para acceso o corrección, revisar la bandeja, registro autorizado, evidencia de consentimiento y proveedores involucrados.
- Para supresión o restricción, detener usos futuros, aplicar la decisión a los registros internos y solicitar al proveedor la acción correspondiente cuando proceda.
- Para revocación, separar la finalidad revocada de la atención de la solicitud; detener marketing opcional si alguna vez se activa y registrar la fecha, alcance, verificación y excepción.
- Responder por un canal razonablemente seguro, registrar la acción y cerrar solo cuando se haya documentado el resultado.

Las excepciones por obligación legal, contrato, contabilidad, defensa de derechos, incidente o litigio deben ser confirmadas por el asesor jurídico. No se debe prometer eliminación absoluta antes de resolver esas excepciones.

### 6.3 Revisión mensual

El fundador debe realizar una revisión mensual en un sistema privado:

```text
[ ] Leads sin contrato que superen la retención aprobada.
[ ] Propuestas comerciales vencidas.
[ ] Evidencias sin finalidad vigente o sin relación justificable.
[ ] Solicitudes e incidentes cerrados que puedan restringirse o eliminarse.
[ ] Copias o proveedores que todavía conserven información.
[ ] Accesos vigentes y accesos que deban revocarse.
[ ] Fecha, alcance y responsable de cada eliminación o anonimización.
```

### 6.4 Incidentes

Ante un envío equivocado, exposición en un log, acceso no autorizado, credencial comprometida o falla de proveedor: contener el flujo, conservar evidencia técnica mínima, registrar el evento sin pegar datos personales, evaluar alcance y solicitar revisión jurídica. Usar [`incident-response.md`](../operations/incident-response.md); no comunicar cumplimiento ni notificación a una autoridad sin decisión documentada.

## 7. Tabla de decisiones pendientes

| Decisión | Decide o revisa | Estado actual | Salida necesaria |
|---|---|---|---|
| Identidad legal, domicilio, identificación y teléfono del responsable | Fundador + asesor jurídico/fiscal | Pendiente | Datos verificados para la política definitiva; no incluirlos en este borrador. |
| Persona o función que atiende titulares | Fundador + asesor jurídico | Provisionalmente el fundador | Designación, canal y sustitución futura documentados. |
| Política y aviso definitivos | Asesor jurídico; aprobación final del fundador | Borrador | Texto aprobado, versión, fecha de vigencia y publicación autorizada. |
| Textos exactos de Contacto y Diagnóstico | Asesor jurídico; aprobación final del fundador | Borrador técnico | Autorizaciones aprobadas, separadas por finalidad y formulario. |
| Marketing opcional | Fundador + asesor jurídico | No activo | Decidir si existe; no activar por defecto ni mezclarlo con respuesta. |
| Retención de leads y propuestas | Fundador + asesor jurídico | Propuestas 12/24 meses | Periodos aprobados, excepciones y método de eliminación. |
| Retención de clientes, contratos y consentimientos | Asesor jurídico + contable | Pendiente | Matriz por obligación, finalidad, controversia y acceso. |
| Proveedores, contratos y transferencias | Fundador + asesor jurídico | Evidencia incompleta | Fichas vigentes, acuerdos, regiones, subencargados y controles. |
| Registro privado de titulares | Fundador | Procedimiento definido, sistema pendiente | Herramienta privada, acceso restringido y calendario de vencimientos. |
| Evidencia técnica y reconciliación | Equipo técnico; revisión jurídica del diseño | Código integrado mediante PR #17 en la rama Astro; no desplegado ni activado | Aprobación del modelo, retención, revocación y modo operativo. |
| Auditoría con Google PageSpeed | Fundador + asesor jurídico + técnico | No pública | Inventario y proveedores aprobados antes de habilitarla. |
| Activación de formularios | Fundador, jurídico, operativo y técnico | **NO-GO** | Aprobaciones firmes, pruebas, rollback y autorización explícita de despliegue. |

## 8. Checklist GO/NO-GO final

| ID | Requisito | Responsable | Evidencia necesaria | Estado / decisión |
|---|---|---|---|---|
| LEG-01 | Responsable identificado y canal para titulares confirmado. | Fundador + jurídico | Política con datos verificados y canal operativo. | Pendiente; NO-GO |
| LEG-02 | Aviso y política revisados según Ley 1581 de 2012 y Decreto 1074 de 2015. | Asesor jurídico | Texto aprobado, versión, fecha y registro de revisión. | Pendiente; NO-GO |
| LEG-03 | Autorizaciones exactas, separadas por Contacto/Diagnóstico y finalidad. | Asesor jurídico + fundador | Textos aprobados y catálogo final versionado. | Pendiente; NO-GO |
| LEG-04 | Revocación, supresión, corrección y acceso definidos con excepciones. | Asesor jurídico | Procedimiento y respuestas aprobadas. | Pendiente; NO-GO |
| LEG-05 | Retención aprobada para leads, propuestas, clientes y consentimiento. | Fundador + jurídico/contable | Tabla de periodos, excepciones y eliminación. | Pendiente; NO-GO |
| LEG-06 | Proveedores, regiones, contratos y transferencias/transmisiones revisados. | Fundador + jurídico | Fichas de Cloudflare, Turnstile, Resend, correo y PageSpeed. | Pendiente; NO-GO |
| OPS-01 | Registro privado de solicitudes con responsable y vencimiento. | Fundador | Registro de prueba sin datos reales y control de acceso. | Pendiente de operar |
| OPS-02 | Revisión mensual de retención y accesos. | Fundador | Checklist y registro de cada revisión. | Pendiente de operar |
| OPS-03 | Procedimiento de incidentes y escalamiento jurídico probado. | Fundador + técnico | Simulación, contacto de escalamiento y cierre. | Pendiente de operar |
| TEC-01 | Evidencia generada por servidor, minimizada y vinculada por `request_id`. | Equipo técnico | Pruebas del PR #17 y documentación técnica. | Integrado en rama Astro; no desplegado |
| TEC-02 | Frontend y Worker validan la misma versión; modo `off` sigue por defecto. | Equipo técnico | Prueba de coherencia y configuración revisada. | Preparado; no activado |
| TEC-03 | No existen endpoints públicos de lectura, exportación o borrado. | Equipo técnico | Revisión de rutas y controles de acceso. | Pendiente de verificación final |
| DEP-01 | Formularios reales solo se habilitan con autorización explícita. | Fundador | Aprobación escrita y checklist firmado. | **NO-GO** |
| DEP-02 | Rollback al modo demo y respuesta a errores verificados. | Equipo técnico + fundador | Plan de rollback y prueba local. | Pendiente |

### Criterio de decisión

- **GO jurídico:** todos los requisitos `LEG-*` aprobados por el asesor jurídico y el fundador.
- **GO operativo:** `OPS-*` implementados con acceso privado, responsable y registros de prueba sin datos reales.
- **GO técnico:** `TEC-*` verificados en local, sin secretos, sin D1 remoto y con el modo demo conservado hasta la autorización.
- **GO de despliegue:** `DEP-*` aprobados después de los tres bloques anteriores.
- **NO-GO automático:** falta de identidad o canal, política o autorización sin aprobación, finalidad mezclada, proveedor o retención desconocidos, evidencia no consultable, solicitud de datos sensibles, incidente abierto o ausencia de rollback.

## 9. Checklist para el asesor jurídico colombiano

```text
[ ] Confirmar Responsable, Encargado y cualquier rol distinto para leads propios y datos de clientes.
[ ] Confirmar ámbito aplicable, deberes de la Ley 1581 de 2012 y capítulo 25 del Decreto 1074 de 2015.
[ ] Determinar si aplica RNBD u otra obligación registral, sin asumir una excepción por el tamaño de la operación.
[ ] Revisar que el aviso informe responsable, finalidades, derechos, canal, proveedores y conservación.
[ ] Confirmar que las autorizaciones sean previas, expresas, informadas, separadas y consultables.
[ ] Revisar texto de Contacto y Diagnóstico, incluyendo la descripción libre y la prohibición de datos innecesarios.
[ ] Confirmar tratamiento de datos sensibles, de menores y de información de terceros; mantenerlos fuera del formulario mientras no exista decisión.
[ ] Aprobar o cambiar las propuestas de 12 meses para leads y 24 meses para propuestas comerciales.
[ ] Definir conservación de clientes, contratos, consentimientos, solicitudes, copias y registros contables.
[ ] Revisar Cloudflare, Turnstile, Resend, correo y Google PageSpeed: roles, subencargados, regiones, contratos y transferencias/transmisiones.
[ ] Revisar revocación, supresión, corrección, acceso y restricciones, incluidas sus excepciones.
[ ] Confirmar el procedimiento de incidentes, evidencias y posibles comunicaciones a titulares, clientes o autoridad.
[ ] Confirmar la publicación de la política, la fecha de vigencia y la forma de conservar versiones históricas.
[ ] Emitir una aprobación o lista de cambios con fecha, alcance y versión; no aprobar por silencio ni por la existencia del documento.
```

### Fuentes oficiales para la revisión

- [Ley 1581 de 2012 — Gestor Normativo de Función Pública](https://www.funcionpublica.gov.co/eva/gestornormativo/norma.php?i=49981).
- [Decreto 1074 de 2015 — SUIN-Juriscol, texto compilado](https://www.suin-juriscol.gov.co/viewDocument.asp?id=30019935), en especial el capítulo 25 del título 2 de la parte 2 del libro 2.
- [Guía Oficial de Protección de Datos Personales — SIC](https://sedeelectronica.sic.gov.co/sites/default/files/boletin-juridico/boletin/docs/Guia%20de%20datos%202023.pdf).
- [Guía para la Gestión de Incidentes de Seguridad en el Tratamiento de Datos Personales — SIC](https://www.sic.gov.co/sites/default/files/files/Publicaciones/Guia_gestion_incidentes_dic21_2020.pdf).

La revisión jurídica debe contrastar estas fuentes con la versión vigente y con la operación real antes de emitir aprobación.

## 10. Decisión de activación

Hasta completar la tabla y obtener la autorización explícita del fundador, el estado es **NO-GO**:

- Contacto y Diagnóstico permanecen en modo demo.
- No se actualizan hashes ni versiones del catálogo.
- No se habilitan D1 remoto, Resend real, endpoints públicos de evidencia ni Auditoría server-side.
- No se publica la política como definitiva.

La siguiente tarea técnica solo podrá implementar los cambios aprobados y deberá conservar un rollback al modo demo.
