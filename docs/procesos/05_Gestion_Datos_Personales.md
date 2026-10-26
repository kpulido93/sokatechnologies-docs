# Gestión de datos personales

**Estado:** borrador operativo pendiente de aprobación del fundador y revisión jurídica colombiana.
**Alcance:** SokaTechnologies como operación B2B pequeña, actualmente administrada por una persona natural.
**Responsable operativo provisional:** fundador/operador actual, hasta que se formalice y documente la estructura legal.

Este documento es un manual interno. No reemplaza la política de tratamiento publicada para los titulares, los contratos con proveedores, los contratos con clientes ni la revisión de un abogado colombiano.

## 1. Objetivo y reglas de operación

El objetivo es que cada dato personal tenga una finalidad conocida, un acceso limitado, una conservación justificada y una forma clara de atender solicitudes del titular.

Reglas mínimas:

- Recolectar solo los datos necesarios para responder, diagnosticar, prestar el servicio o demostrar una autorización.
- Informar la finalidad antes o al momento de recolectar el dato.
- No pedir contraseñas, datos sensibles, documentos de identidad, bases de datos de clientes ni archivos confidenciales en los formularios públicos.
- Separar el consentimiento para atender una solicitud del consentimiento opcional para comunicaciones comerciales.
- No usar un dato para una finalidad nueva sin revisar la información al titular y la autorización que corresponda.
- Mantener una sola persona responsable de coordinar accesos, solicitudes, incidentes y eliminación.
- No copiar datos personales en Git, tickets públicos, ejemplos, logs de desarrollo ni capturas.

Estas reglas complementan [`06_Estandares_Seguridad.md`](../tecnico/06_Estandares_Seguridad.md), [`incident-response.md`](../operations/incident-response.md) y las reglas de formularios de [`Web_SokaTechnologies_WordPress.md`](../marketing/Web_SokaTechnologies_WordPress.md).

## 2. Roles y responsabilidades

| Rol | Responsabilidad actual | Pendiente |
|---|---|---|
| Responsable operativo provisional | Fundador/operador actual: decide la finalidad de los leads propios, autoriza accesos, revisa solicitudes y coordina incidentes. | Registrar el nombre legal, domicilio y canal oficial después de la formalización o aprobación jurídica. |
| Función de protección de datos | La misma persona provisionalmente; recibe y controla consultas, correcciones, supresiones y revocaciones. | Confirmar la designación formal y el canal público para titulares. |
| Encargado técnico | El proveedor o componente que procesa datos por cuenta de SokaTechnologies, según el servicio contratado. | Revisar contratos, instrucciones, subcontratistas y transferencias o transmisiones internacionales. |
| Revisor jurídico | Asesor externo por contratar o designar cuando aplique. | Confirmar política, roles, retención, RNBD, transferencias y respuesta a incidentes. |

Para leads propios, SokaTechnologies debe tratarse provisionalmente como quien decide las finalidades del tratamiento, sujeto a confirmación jurídica. En proyectos de clientes, el contrato debe definir si SokaTechnologies actúa como responsable, encargado o tiene otra relación aplicable; no se debe asumir el rol por defecto.

## 3. Procedimiento operativo

### 3.1 Recolección y clasificación

1. Antes de abrir un formulario o canal nuevo, registrar su finalidad, campos, proveedor, accesos y retención propuesta en el inventario de la sección 4.
2. Revisar que cada campo sea necesario. Si la respuesta es opcional, marcarlo como opcional y explicar para qué se pide.
3. Mostrar el aviso de privacidad y la autorización aprobada para la finalidad correspondiente.
4. Rechazar o pedir que se retire cualquier contraseña, secreto, dato sensible, documento de identidad o información confidencial de terceros.
5. Asignar un identificador interno de solicitud. Ese identificador no debe ser el número de identificación del titular.
6. Guardar la evidencia de autorización de forma separada de la bandeja de correo cuando exista el mecanismo técnico aprobado.

### 3.2 Uso y acceso

- El acceso ordinario queda limitado al fundador/operador y a proveedores que necesiten procesar el dato para la finalidad documentada.
- El correo receptor actual es `info@sokatechnologies.com`; no se deben crear reenvíos a cuentas personales sin documentarlos y protegerlos.
- No descargar leads a equipos compartidos, hojas sin control de acceso ni aplicaciones personales.
- No compartir un lead con un cliente, proveedor o colaborador si no es necesario para la finalidad.
- Al contratar apoyo, entregar solo el mínimo necesario, usar cuentas individuales y retirar el acceso al terminar la necesidad.
- Los logs deben contener identificadores técnicos y resultados, no el cuerpo completo de formularios ni credenciales. Ver las reglas de logging del estándar de seguridad.

### 3.3 Corrección, supresión y eliminación

1. Registrar la solicitud en el formato de la sección 5, sin copiar más datos personales de los necesarios.
2. Verificar razonablemente la identidad del solicitante. No pedir documentos completos por correo salvo que una revisión jurídica defina el mecanismo y las medidas de seguridad.
3. Localizar el dato en la bandeja, registro de leads, evidencias de consentimiento y proveedores a los que se haya enviado.
4. Corregir, suprimir, anonimizar o restringir el tratamiento según corresponda y según existan obligaciones legales o contractuales que deban conservar un registro.
5. Si procede, propagar la instrucción al proveedor. Conservar únicamente la evidencia mínima de la acción y el motivo.
6. Responder por un canal razonablemente seguro y cerrar el registro con fecha, acción y responsable.

La eliminación operativa debe impedir la recuperación normal del dato. Las copias de seguridad o registros sujetos a obligación legal requieren una decisión documentada sobre aislamiento, acceso restringido y eliminación posterior; este documento no fija una obligación de conservación que deba confirmarse jurídicamente.

### 3.4 Incidentes

Se considera incidente cualquier pérdida, acceso no autorizado, envío al destinatario equivocado, exposición en un log o repositorio, credencial comprometida, uso fuera de finalidad o falla de un proveedor que pueda afectar datos personales.

Flujo para el fundador/operador:

1. **Contener:** revocar accesos o tokens, detener el flujo afectado y conservar la evidencia sin difundirla.
2. **Registrar:** fecha y hora, sistema o proveedor, tipo de dato, alcance conocido, personas que detectaron el evento y acciones tomadas. No pegar datos personales en el reporte.
3. **Evaluar:** determinar titulares y finalidades afectadas, riesgo, proveedores involucrados y si el evento sigue activo.
4. **Escalar:** solicitar revisión jurídica y técnica; evaluar comunicaciones a titulares, clientes y la autoridad competente.
5. **Recuperar:** corregir la causa, validar el servicio y revisar accesos, logs y credenciales.
6. **Cerrar:** documentar causa preliminar, decisión de notificación, acciones preventivas y fecha de revisión.

La evaluación de un eventual reporte ante la SIC debe hacerse caso por caso y con revisión jurídica. Como control interno, el análisis debe iniciar el mismo día de la detección; no se debe esperar al cierre técnico para decidir si existe un deber de reporte.

## 4. Inventario de tratamientos

El inventario debe actualizarse antes de habilitar un tratamiento nuevo y cada vez que cambie el proveedor, la finalidad, los campos o el canal.

| Tratamiento | Datos mínimos previstos | Finalidad | Origen y flujo | Acceso / proveedor | Estado y control |
|---|---|---|---|---|---|
| Contacto | Nombre, empresa, correo, teléfono opcional, país opcional, servicio de interés opcional, tipo de problema opcional y descripción del problema. | Responder la solicitud y evaluar una conversación comercial. | Formulario Astro → Worker → correo corporativo o registro autorizado. | Fundador/operador; Cloudflare Worker, Turnstile y Resend según configuración efectiva. | Formularios públicos en demo; NO habilitar sin pasar el checklist de la sección 9. |
| Diagnóstico | Los mismos campos reales de `ContactForm.astro`: nombre, empresa, correo, teléfono y país opcionales, servicio y tipo de problema opcionales y descripción libre. La descripción puede mencionar herramientas, urgencia o resultado esperado, pero no existen campos independientes para estos elementos. | Entender un problema operativo y preparar una conversación o propuesta. | Formulario Astro → Worker → correo corporativo o registro autorizado. | Fundador/operador; mismos proveedores, con minimización reforzada. | No aceptar secretos, bases de datos, archivos ni datos sensibles. |
| Auditoría | URL pública del sitio, nombre, empresa, correo, WhatsApp opcional, país, tipo de empresa, descripción del problema, consentimiento y resultado de auditoría mostrado. | Ejecutar una revisión autorizada y entregar recomendaciones. | Vista previa local; integración server-side con Google PageSpeed prevista, actualmente no pública. | Solo operador autorizado; revisar Google y cualquier proveedor antes de habilitar. | Tratamiento separado de Contacto/Diagnóstico; actualmente no público. |
| Correo corporativo | Mensajes, remitente, destinatarios, archivos que lleguen por correo y metadatos del servicio. | Recibir, responder y conservar la trazabilidad mínima de comunicaciones. | `info@sokatechnologies.com` y proveedor de correo configurado. | Fundador/operador; proveedor de correo según contrato y configuración. | Revisar búsqueda, exportación, reenvíos, accesos y eliminación. |
| Evidencia de consentimiento | ID de evento, fecha/hora del servidor, versión del aviso, versión de autorización, finalidad aceptada, canal y resultado. | Demostrar qué se informó y qué autorización se obtuvo. | Generada por el Worker o backend autorizado en la futura tarea técnica. | Solo responsable operativo y acceso técnico estrictamente necesario. | Requisito pendiente de implementación; no simular evidencia con datos reales. |

### 4.1 Proveedores y revisiones necesarias

Antes de habilitar formularios reales, confirmar en una ficha separada y no en Git:

- Qué datos recibe cada proveedor y durante cuánto tiempo.
- Si actúa como encargado, subencargado o proveedor independiente.
- Países o regiones de procesamiento y si existe transferencia o transmisión internacional.
- Contrato, términos, medidas de seguridad y procedimiento de incidentes.
- Mecanismo para atender supresión, corrección y revocación.
- Si los tokens de Turnstile, cuerpos de correo, URLs o logs se conservan y cómo se eliminan.

No se debe afirmar que un proveedor cumple una obligación legal concreta sin revisar sus condiciones vigentes y el contrato aplicable.

## 5. Registro de solicitudes de titulares

Este formato puede implementarse inicialmente en un archivo interno con acceso restringido o en el sistema autorizado por el fundador. No debe guardarse en Git ni contener documentos de identidad completos.

| Campo | Qué registrar |
|---|---|
| ID de solicitud | Identificador interno aleatorio, por ejemplo `solicitud-[id]`. |
| Fecha de recepción | Fecha y hora de recepción, con zona horaria. |
| Canal | Correo o canal aprobado; no incluir el contenido completo del mensaje. |
| Titular / referencia | Referencia mínima para localizar al titular; evitar identificación nacional. |
| Tipo | Acceso, corrección/actualización, supresión, revocación u otra consulta. |
| Alcance | Tratamiento, formulario, correo o proveedor relacionado. |
| Verificación | Pendiente, suficiente o requerir aclaración; registrar solo el resultado. |
| Completitud | Completa, incompleta o fecha del requerimiento de información adicional. |
| Responsable | Persona que coordina la respuesta. |
| Vencimiento | Fecha calculada según el tipo de solicitud y la revisión jurídica aplicable. |
| Estado | Recibida, en verificación, en trámite, respondida, cerrada o trasladada. |
| Acciones | Búsqueda, corrección, supresión, restricción, traslado al proveedor o motivo de no procedencia. |
| Fecha de respuesta | Fecha y canal de respuesta. |
| Cierre | Resultado, evidencia mínima y pendientes. |

### 5.1 Plazos de control

Usar estos plazos como campos de vencimiento del registro, sujetos a confirmación de la versión normativa y del asesor jurídico:

- **Consulta de acceso o información:** 10 días hábiles contados a partir de la fecha de recepción (artículo 14 de la Ley 1581 de 2012); si no es posible responder, informar la demora y una extensión de hasta 5 días hábiles posteriores al vencimiento del primer término. La fecha exacta del vencimiento debe verificarse con el calendario de días hábiles aplicable.
- **Reclamo de corrección, actualización, supresión o revocación:** 15 días hábiles contados desde el día siguiente a la recepción del reclamo completo; si no es posible responder, informar la demora y una extensión de hasta 8 días hábiles.
- **Solicitud incompleta:** requerir la subsanación dentro de los 5 días siguientes a su recepción. Si no se completa dentro de 2 meses desde el requerimiento, registrar el cierre por desistimiento, sujeto a la revisión jurídica del caso.
- **Solicitud recibida por una persona no competente:** trasladarla al responsable correspondiente dentro de 2 días hábiles e informar al solicitante.
- **Reclamo en trámite:** cuando corresponda, registrar la leyenda y el motivo dentro de 2 días hábiles.

El vencimiento debe calcularse con calendario de días hábiles aplicable en Colombia. Ante duda sobre si la solicitud es consulta o reclamo, tratarla como urgente y pedir revisión jurídica.

## 6. Retención y eliminación propuesta

Los siguientes periodos son propuestas internas pendientes de aprobación del fundador y revisión jurídica. No son plazos legales ni autorizan conservar datos después de que deje de existir una finalidad.

| Categoría | Propuesta operativa inicial | Acción al vencer | Decisión pendiente |
|---|---|---|---|
| Lead que no se convierte en cliente | 12 meses desde la última interacción útil. | Eliminar datos de contacto y contenido, o anonimizar una métrica mínima no personal. | Aprobar periodo, canal de revisión y excepción documentada. |
| Propuesta comercial | Mientras esté activa y hasta 24 meses desde la última actividad. | Eliminar el expediente personal o conservar solo referencia comercial no identificable, salvo necesidad legal o contractual revisada. | Definir relación con facturación, impuestos, contratos y defensa de derechos. |
| Cliente contratado | Durante la relación y, como propuesta inicial, 24 meses después del cierre. | Archivar con acceso restringido o eliminar por partes según obligación legal, contrato y solicitud del titular. | Asesoría legal/contable debe definir periodos obligatorios y excepciones. |
| Evidencia de consentimiento | Mientras exista el tratamiento y durante el periodo asociado al registro que deba auditarse. | Eliminar o anonimizar cuando ya no exista finalidad, obligación o controversia que justifique conservarla. | Definir periodo único, trazabilidad y relación con el lead o contrato. |
| Solicitudes de titulares e incidentes | Mientras estén abiertos y durante el periodo mínimo que se apruebe para demostrar la atención. | Restringir acceso y eliminar/anonimizar cuando termine la necesidad documentada. | Definir periodo legal, contractual y de auditoría. |

Revisión mensual del fundador/operador:

```text
[ ] Se identificaron registros sin actividad dentro del periodo propuesto.
[ ] Se verificaron obligaciones legales, contractuales o contables antes de eliminar.
[ ] Se eliminaron o anonimizaron los registros autorizados.
[ ] Se registró fecha, alcance y responsable sin copiar el dato eliminado.
[ ] Se revisaron accesos y proveedores que todavía pudieran conservar una copia.
```

## 7. Requisitos para la futura evidencia de consentimiento

Estos son requisitos funcionales para la Tarea 04-B6B; no autorizan todavía cambios técnicos ni habilitan formularios.

### 7.1 Datos mínimos de un evento

La futura implementación debe guardar, con un identificador interno no reversible cuando sea suficiente:

- Fecha y hora generada por el servidor, preferiblemente en UTC, y la zona usada para mostrarla.
- ID de solicitud o evento generado por el servidor.
- Versión exacta del aviso de privacidad mostrado.
- Versión exacta de la autorización o texto de consentimiento mostrado.
- Una o más finalidades aceptadas, separadas por finalidad.
- Resultado de cada opción: aceptada, no aceptada o no aplicable.
- Formulario, canal y versión de la interfaz que originó el evento.
- Referencia técnica a la solicitud, sin guardar más datos de contacto dentro de la evidencia de lo necesario para relacionarla.

No guardar como evidencia un token de Turnstile, contraseña, contenido completo del formulario, documento de identidad, IP o user-agent salvo que una revisión de seguridad y jurídica justifique su necesidad, finalidad y retención. El consentimiento para comunicaciones comerciales debe ser una opción separada, no preseleccionada y no requisito para responder un contacto o diagnóstico.

### 7.2 Controles de almacenamiento

- Generar el evento en el servidor, no confiar en la hora del navegador.
- Validar que la versión del aviso y la autorización existan y puedan consultarse posteriormente.
- Restringir lectura y modificación; registrar cambios administrativos.
- Proteger la evidencia en tránsito y en reposo con las capacidades del proveedor autorizado.
- No imprimir el evento ni sus datos en logs de aplicación.
- Permitir búsqueda por ID de solicitud y exportación controlada para responder al titular.
- Definir eliminación, anonimización y propagación a proveedores antes de poner el flujo en producción.
- Probar aceptación, rechazo, reenvío, duplicados, error de proveedor y revocación sin usar información personal real.

Ejemplo conceptual sin datos reales:

```json
{
  "event_id": "consent-[id]",
  "request_id": "request-[id]",
  "server_timestamp_utc": "[timestamp]",
  "notice_version": "[version]",
  "authorization_version": "[version]",
  "purposes": {
    "respond_contact": "accepted",
    "commercial_follow_up": "not_selected"
  },
  "source": "[form-and-version]"
}
```

## 8. Checklist de revisión jurídica colombiana

Marcar cada punto solo después de revisar la norma vigente, la operación real y, cuando corresponda, la asesoría jurídica.

### Marco y responsable

```text
[ ] Se confirmó que los tratamientos y el ámbito territorial están sujetos al marco aplicable.
[ ] Se definió el Responsable, su identidad legal y los datos de contacto que deben publicarse.
[ ] Se designó la persona o área que atiende solicitudes de titulares.
[ ] Se distinguió el rol de SokaTechnologies en leads propios y en datos tratados para clientes.
[ ] Se revisó si aplica inscripción o actualización en el RNBD, sin asumir una excepción por el tamaño actual.
```

### Aviso, autorización y finalidades

```text
[ ] La política de tratamiento y el aviso de privacidad fueron revisados y aprobados antes de publicar.
[ ] El aviso informa tratamiento, finalidades, derechos y datos de contacto del responsable.
[ ] La autorización es previa, expresa, informada y consultable posteriormente cuando sea exigible.
[ ] Cada finalidad opcional, incluida prospección comercial, tiene una elección separada.
[ ] Las preguntas sobre datos sensibles o de niños, niñas y adolescentes no se incorporan a estos formularios.
[ ] El procedimiento para acceso, actualización, rectificación, supresión y revocación es accesible.
```

### Proveedores, seguridad e incidentes

```text
[ ] Se revisaron Cloudflare Worker, Turnstile, Resend, correo corporativo y Google PageSpeed si se habilita.
[ ] Se documentaron encargados, subencargados, contratos, ubicación y transferencias/transmisiones internacionales.
[ ] Se definieron accesos, logs, retención, eliminación, backups y devolución o supresión por proveedor.
[ ] Existe un procedimiento para detectar, contener, documentar y evaluar el reporte de incidentes.
[ ] Se validó si el tratamiento requiere medidas reforzadas por su naturaleza o por el perfil de los titulares.
```

Fuentes oficiales para la revisión:

- [Ley 1581 de 2012 — Gestor Normativo de Función Pública](https://www.funcionpublica.gov.co/eva/gestornormativo/norma.php?i=49981).
- [Decreto 1074 de 2015 — SUIN-Juriscol, texto compilado](https://www.suin-juriscol.gov.co/viewDocument.asp?id=30019935), en especial el capítulo 25 del título 2 de la parte 2 del libro 2.
- [Guía Oficial de Protección de Datos Personales — SIC](https://sedeelectronica.sic.gov.co/sites/default/files/boletin-juridico/boletin/docs/Guia%20de%20datos%202023.pdf).
- [Guía para la Gestión de Incidentes de Seguridad en el Tratamiento de Datos Personales — SIC](https://www.sic.gov.co/sites/default/files/files/Publicaciones/Guia_gestion_incidentes_dic21_2020.pdf).
- [Preguntas frecuentes de Protección de Datos Personales — SIC](https://sedeelectronica.sic.gov.co/sites/default/files/preguntas-frecuentes/Tramites_y_Servicios_2021.pdf).

## 9. Checklist GO / NO-GO para habilitar formularios reales

**Estado actual: NO-GO.** Los formularios públicos siguen en modo demo, la política de privacidad es un borrador y faltan datos del responsable y revisión jurídica.

### GO solo si todo está marcado

```text
[ ] El fundador aprobó el responsable provisional, el canal de titulares y los datos que se publicarán.
[ ] La política de tratamiento, aviso y autorización fueron revisados jurídicamente y publicados en la versión aprobada.
[ ] Contacto y Diagnóstico piden únicamente los campos mínimos del inventario.
[ ] El formulario bloquea o advierte contra contraseñas, datos sensibles, bases de datos y archivos confidenciales.
[ ] La autorización requerida se captura de forma separada por finalidad.
[ ] Existe evidencia de consentimiento generada por servidor y protegida, o una decisión jurídica documentada para el mecanismo temporal.
[ ] Worker, Turnstile, Resend y correo tienen flujo, acceso, retención, seguridad y proveedor documentados.
[ ] Se revisaron transferencias o transmisiones internacionales y contratos aplicables.
[ ] Existe un registro operativo de solicitudes con responsable y cálculo de vencimientos.
[ ] Existe un canal probado para corrección, supresión y revocación.
[ ] Se probó el flujo de incidentes y la ruta de escalamiento jurídico.
[ ] Se probaron éxito, rechazo, duplicado, error de entrega, abuso anti-spam y recuperación sin datos reales.
[ ] No hay secretos, credenciales, datos personales reales ni logs sensibles en el repositorio.
[ ] Hay plan de rollback para volver al modo demo sin perder registros ni exponer datos.
```

### NO-GO automático

No habilitar si falta cualquiera de estos puntos:

- Identidad o canal del responsable sin definir.
- Política o autorización sin aprobación.
- Finalidades mezcladas o consentimiento preseleccionado.
- Evidencia no consultable o almacenada en una ubicación sin control de acceso.
- Proveedor, transferencia, retención o eliminación desconocidos.
- Solicitud de datos sensibles, contraseñas, archivos confidenciales o información de terceros.
- Incidente abierto, secreto expuesto o prueba realizada con datos personales reales.

## 10. Decisiones pendientes del fundador

- Completar la identidad legal, domicilio y canal para titulares cuando corresponda, sin publicarlos en este borrador hasta validarlos.
- Confirmar quién asumirá formalmente la función de protección de datos mientras la operación siga siendo de una persona natural.
- Aprobar o ajustar los periodos de retención propuestos.
- Decidir si existirá prospección comercial separada y por qué canales.
- Autorizar la revisión contractual de Cloudflare, Resend, correo corporativo y Google PageSpeed.
- Decidir si la Auditoría continuará solo local o tendrá un lanzamiento público posterior con inventario independiente.
- Solicitar revisión jurídica sobre RNBD, roles frente a clientes, transferencias internacionales y retenciones legales o contables.

## 11. Requisitos de la Tarea 04-B6B

La siguiente tarea técnica deberá entregar, como mínimo:

1. Un esquema de evento de consentimiento con los campos de la sección 7.
2. Timestamp de servidor, ID de solicitud y versiones de aviso/autorización verificables.
3. Finalidades separadas y consentimiento comercial opcional.
4. Almacenamiento seguro con acceso mínimo, sin secretos en código ni datos personales en Git.
5. Pruebas automatizadas o aserciones pequeñas para aceptación, rechazo, duplicados, errores y revocación.
6. Ruta para consultar una evidencia por ID y atender una solicitud sin exponer la base completa.
7. Retención, eliminación y manejo de proveedores documentados antes del despliegue.
8. Modo demo conservado hasta que el checklist GO esté aprobado.

No crear una base de datos, integrar proveedores nuevos ni activar formularios como parte de este documento.
