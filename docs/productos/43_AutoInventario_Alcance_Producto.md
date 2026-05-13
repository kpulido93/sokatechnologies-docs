# AutoInventario - Alcance de Producto

**Documento:** `docs/productos/43_AutoInventario_Alcance_Producto.md`  
**Empresa:** SokaTechnologies  
**Producto:** AutoInventario  
**Versión:** 1.0  
**Estado:** Borrador estratégico y técnico  
**Última actualización:** 2026-05-13  
**Uso:** Definir alcance correcto, posicionamiento, límites, riesgos y condiciones mínimas antes de comercializar AutoInventario.  

---

## 1. Resumen ejecutivo

AutoInventario es un producto B2B técnico orientado al inventario automático de activos Windows. Su propósito es ayudar a empresas a recopilar información básica y útil de equipos Windows, enviarla de forma controlada a un Webhook, procesarla en infraestructura backend y sincronizarla con herramientas ITSM como ManageEngine ServiceDesk Plus.

AutoInventario no es un sistema de inventario comercial de mercancía. No debe posicionarse como solución para almacenes, punto de venta, facturación, compras, ventas o control de stock.

Estado comercial recomendado:

> AutoInventario no debe venderse todavía. Primero debe completar una fase de remediación técnica y de seguridad que permita demostrarlo, instalarlo, operarlo y soportarlo con confianza.

El objetivo de este documento es delimitar qué es el producto, qué problemas puede resolver, qué componentes técnicos lo sostienen, qué queda fuera de alcance y qué requisitos mínimos deben cumplirse antes de cualquier piloto o venta externa.

---

## 2. Qué es AutoInventario

AutoInventario es una solución para recopilar y centralizar información de activos Windows en entornos empresariales.

Debe entenderse como:

- Agente o componente instalado en equipos Windows.
- Recolector automático de información técnica del equipo.
- Flujo seguro de envío hacia un Webhook.
- Backend de recepción, validación y procesamiento.
- Integración con herramientas ITSM para crear o actualizar activos.
- Base para mejorar trazabilidad de infraestructura, soporte técnico y auditoría de activos.

En una versión comercial madura, AutoInventario debería permitir que una empresa conozca qué equipos Windows tiene, qué características técnicas poseen y cómo se sincronizan esos datos con su herramienta de gestión de servicios o activos.

Ejemplos de información esperada, usando nombres genéricos:

- Nombre lógico del equipo.
- Sistema operativo.
- Modelo del equipo.
- Fabricante.
- Memoria RAM.
- Procesador.
- Disco o almacenamiento básico.
- Usuario asociado, si aplica y está permitido.
- Dirección IP o red, si aplica y está permitido.
- Software relevante instalado, si el alcance lo incluye.
- Fecha de última actualización del inventario.
- Identificador interno del activo.

La recolección debe limitarse a datos necesarios para inventario técnico. No debe recolectar información sensible innecesaria.

---

## 3. Qué no es AutoInventario

AutoInventario no debe presentarse como:

- Inventario comercial de productos.
- Control de almacenes.
- Sistema de ventas.
- Sistema de compras.
- Facturación.
- Punto de venta.
- Sistema POS.
- Control de mercancía.
- Gestión de proveedores.
- Gestión contable.
- ERP.
- CRM.
- Sistema de códigos de barras para productos.
- Sistema para inventario de góndolas, tiendas o bodegas comerciales.
- Herramienta de monitoreo avanzado en tiempo real.
- Herramienta de administración remota completa de equipos.
- Reemplazo de una suite ITSM completa.

Regla comercial:

> Si el prospecto busca inventario de mercancía, ventas, almacén, facturación o POS, AutoInventario no es la oferta correcta.

---

## 4. Cliente ideal

AutoInventario debe enfocarse en empresas con infraestructura Windows y necesidad real de trazabilidad técnica.

| Cliente ideal | Por qué encaja |
|---|---|
| Empresas con parque de equipos Windows. | Necesitan conocer y mantener inventario técnico actualizado. |
| Áreas internas de soporte IT. | Requieren información confiable para atención, auditoría y control. |
| Proveedores de soporte IT gestionado. | Pueden administrar inventario de varios clientes con procesos repetibles. |
| Empresas que usan ManageEngine ServiceDesk Plus. | Pueden beneficiarse de sincronización de activos. |
| Empresas con auditorías de activos tecnológicos. | Necesitan evidencia y actualización periódica. |
| Organizaciones con equipos distribuidos. | El inventario manual se vuelve lento y propenso a errores. |

Cliente no ideal:

- Tiendas que buscan controlar stock de productos.
- Negocios que necesitan ventas, facturación o POS.
- Empresas sin equipos Windows relevantes.
- Clientes sin madurez mínima de soporte o infraestructura.
- Prospectos que requieren monitoreo en tiempo real, EDR, MDM o administración remota completa desde el primer día.

---

## 5. Problema que resuelve

AutoInventario resuelve problemas comunes de control de activos tecnológicos.

| Problema | Impacto |
|---|---|
| Inventario de equipos hecho manualmente. | Alto consumo de tiempo y errores frecuentes. |
| Información técnica desactualizada. | Soporte IT toma decisiones con datos incompletos. |
| Falta de trazabilidad sobre hardware y software. | Dificultad para auditorías, renovación o soporte. |
| Datos dispersos entre hojas de cálculo y sistemas. | No hay fuente confiable de activos. |
| Herramientas ITSM sin activos actualizados. | Tickets y activos no se relacionan correctamente. |
| Equipos distribuidos o difíciles de revisar físicamente. | Inventario manual lento y costoso. |

Resultado esperado:

- Menos inventario manual.
- Mejor trazabilidad de activos Windows.
- Datos técnicos más actualizados.
- Sincronización con una herramienta ITSM.
- Base para soporte, auditoría y mantenimiento.

---

## 6. Alcance funcional esperado

El alcance funcional esperado describe lo que AutoInventario podría incluir en una primera versión comercial futura, después de completar remediación técnica y seguridad.

### 6.1 Agente Windows

El agente debe:

- Ejecutarse en equipos Windows autorizados.
- Recopilar inventario técnico básico.
- Preparar un payload estructurado.
- Cifrar o proteger el envío según diseño aprobado.
- Enviar datos a un Webhook configurado.
- Registrar logs locales mínimos sin secretos.
- Manejar errores de red o envío.
- Ejecutarse manualmente o por programación controlada.
- Permitir actualización o reemplazo controlado del agente.

### 6.2 Recolección de datos

Datos esperados, según alcance aprobado:

- Identificador del equipo.
- Sistema operativo.
- Fabricante y modelo.
- CPU.
- RAM.
- Almacenamiento.
- Dirección de red, si aplica.
- Usuario o responsable, si está permitido.
- Software relevante, si está definido en el alcance.
- Fecha y hora de recolección.
- Versión del agente.

Datos que deben evitarse salvo justificación y aprobación:

- Contraseñas.
- Tokens.
- Archivos de usuario.
- Contenido de documentos.
- Historial de navegación.
- Correos.
- Información personal innecesaria.
- Llaves privadas.
- Capturas de pantalla.
- Datos sensibles fuera del propósito de inventario técnico.

### 6.3 Recepción y procesamiento

La plataforma backend debe:

- Recibir payloads mediante Webhook.
- Validar autenticación del origen.
- Validar estructura del payload.
- Rechazar datos incompletos o inválidos.
- Procesar datos sin exponer secretos.
- Registrar eventos técnicos mínimos.
- Evitar logs con payloads sensibles completos.
- Manejar errores de integración.
- Preparar datos para sincronización con ITSM.

### 6.4 Sincronización con ITSM

La sincronización debe:

- Crear o actualizar activos en la herramienta ITSM.
- Mapear campos del inventario hacia campos del sistema destino.
- Evitar duplicados cuando sea posible.
- Registrar errores de sincronización.
- Permitir reintentos controlados.
- Mantener trazabilidad de última sincronización.

---

## 7. Componentes técnicos principales

AutoInventario debe documentarse como una solución compuesta por varios componentes técnicos.

| Componente | Propósito | Consideraciones |
|---|---|---|
| Agente Windows | Recopilar inventario del equipo. | Debe ser instalable, actualizable y seguro. |
| Configuración local | Definir parámetros no sensibles del agente. | Secretos reales no deben quedar hardcodeados ni versionados. |
| Webhook | Recibir inventarios enviados por los agentes. | Debe autenticar, validar y manejar errores. |
| Lambda o backend serverless | Procesar datos y ejecutar lógica de integración. | Debe tener permisos mínimos y logs controlados. |
| Gestor de secretos | Guardar credenciales de integración. | Usar mecanismo seguro del proveedor cloud cuando aplique. |
| Integración ITSM | Crear o actualizar activos en ManageEngine u otra herramienta. | Requiere mapeo de campos, manejo de errores y límites. |
| Logs técnicos | Permitir diagnóstico. | No deben registrar contraseñas, tokens ni payloads sensibles completos. |
| Pipeline de build | Compilar, probar y empaquetar. | Debe producir artefactos reproducibles y revisados. |
| Documentación | Explicar instalación, configuración, operación y soporte. | Debe usar ejemplos ficticios y valores genéricos. |

Arquitectura conceptual:

```text
Equipo Windows
  -> Agente AutoInventario
  -> Payload protegido
  -> Webhook
  -> Lambda / backend
  -> Validación y normalización
  -> ManageEngine ServiceDesk Plus / ITSM
```

Esta arquitectura es conceptual. No debe incluir endpoints reales, nombres de cuentas, regiones, claves, URLs internas ni configuración sensible.

---

## 8. Integración con ManageEngine

ManageEngine ServiceDesk Plus debe tratarse como una integración ITSM objetivo, especialmente para empresas que ya lo usan o desean mejorar su inventario de activos.

Objetivo de la integración:

- Crear activos tipo workstation o equivalente.
- Actualizar activos existentes.
- Mantener campos técnicos relevantes sincronizados.
- Relacionar equipos con usuarios o responsables cuando aplique.
- Mejorar visibilidad del área de soporte IT.

Campos genéricos que podrían mapearse:

| Campo AutoInventario | Campo ITSM esperado |
|---|---|
| Identificador del equipo | Nombre del activo o asset tag |
| Fabricante | Fabricante |
| Modelo | Modelo |
| Sistema operativo | Sistema operativo |
| CPU | Procesador |
| RAM | Memoria |
| Almacenamiento | Disco |
| Usuario asociado | Usuario asignado |
| Fecha de inventario | Última actualización |
| Versión del agente | Campo personalizado |

Requisitos de integración:

- Credenciales almacenadas de forma segura.
- Permisos mínimos para crear o actualizar activos.
- Manejo de errores de API.
- Rate limits considerados.
- Logs sin credenciales ni respuestas sensibles completas.
- Pruebas con datos ficticios.
- Documentación de mapeo de campos.

La integración con ManageEngine no debe probarse con credenciales reales en documentación, repositorios o prompts. Cualquier prueba con cliente real debe realizarse en ambiente controlado, con autorización y sin exponer secretos.

---

## 9. Alcance fuera de la primera versión comercial

La primera versión comercial de AutoInventario no debe incluir:

- Inventario comercial de mercancía.
- POS.
- Facturación.
- Ventas.
- Compras.
- Control de almacenes.
- Código de barras para productos comerciales.
- Integraciones con ERP contable.
- Dashboard BI avanzado.
- Administración remota completa del equipo.
- Monitoreo en tiempo real de rendimiento.
- EDR, antivirus o respuesta ante amenazas.
- MDM completo.
- Soporte Linux/macOS.
- Recolección de archivos del usuario.
- Capturas de pantalla.
- Auditoría forense avanzada.
- Instalador empresarial complejo sin validación previa.
- Integraciones múltiples con varias herramientas ITSM desde el inicio.
- Alta disponibilidad o arquitectura enterprise sin caso comercial validado.

Cualquier función fuera de la primera versión debe tratarse como fase futura, con alcance, precio, riesgos y criterios de aceptación separados.

---

## 10. Requisitos mínimos antes de venta

AutoInventario no debe venderse ni presentarse como producto listo hasta cumplir requisitos mínimos.

### 10.1 Requisitos técnicos

- Build estable.
- Instalación o ejecución controlada del agente.
- Pruebas mínimas del agente.
- Pruebas mínimas del Webhook.
- Pruebas de integración con datos ficticios.
- Manejo de errores documentado.
- Logs revisados para evitar datos sensibles.
- Documentación de instalación.
- Documentación de operación.
- Checklist de despliegue.
- Plan de rollback o desinstalación.

### 10.2 Requisitos de seguridad

- No hay secretos en repositorios.
- No hay credenciales hardcodeadas.
- Los secretos expuestos, si existieron, fueron rotados.
- Autenticación del Webhook implementada.
- Validación de payload implementada.
- Cifrado o protección del envío revisada.
- Integridad del payload considerada.
- Permisos cloud mínimos.
- Credenciales de ManageEngine protegidas.
- Separación de ambientes.
- Datos reales excluidos de demos y pruebas públicas.
- Logs sin contraseñas, tokens ni payloads sensibles completos.

### 10.3 Requisitos comerciales

- Alcance comercial definido.
- Cliente ideal definido.
- Exclusiones claras.
- Precio piloto definido.
- Modelo de soporte mensual definido.
- Criterios de aceptación para piloto.
- Guía de diagnóstico comercial.
- Riesgos y responsabilidades documentados.

Regla de decisión:

> Hasta completar estos requisitos, AutoInventario debe mantenerse como producto en preparación, no como producto listo para venta.

---

## 11. Modelo comercial futuro

El modelo comercial de AutoInventario debe evaluarse después de la remediación técnica y de seguridad.

### 11.1 Piloto técnico controlado

Primer paso recomendado:

- Piloto con cantidad limitada de equipos.
- Datos mínimos necesarios.
- Ambiente controlado.
- Integración ITSM validada con datos ficticios o autorizados.
- Criterios de éxito claros.
- Soporte durante el piloto.

No iniciar piloto sin alcance escrito, responsables definidos y pago inicial o acuerdo comercial aprobado.

### 11.2 Estructura posible de cobro

| Concepto | Descripción |
|---|---|
| Setup inicial | Instalación, configuración, integración y documentación. |
| Mensualidad de soporte | Monitoreo de errores, soporte, ajustes menores y revisión de sincronización. |
| Rango por equipos | Precio según cantidad de activos Windows inventariados. |
| Integraciones adicionales | Cobro separado por nuevas herramientas ITSM o flujos personalizados. |
| Seguridad y hardening | Servicio adicional si el cliente requiere controles más estrictos. |

### 11.3 Planes posibles

| Plan futuro | Cliente objetivo | Alcance |
|---|---|---|
| AutoInventario Starter | Empresa pequeña con parque Windows limitado. | Agente, Webhook, integración básica y soporte limitado. |
| AutoInventario Pro | Empresa con más equipos y soporte IT activo. | Sincronización, revisión mensual, reportes básicos y soporte priorizado. |
| AutoInventario Managed | Proveedor IT o empresa con varios entornos. | Operación más controlada, monitoreo, documentación y mejoras por fases. |

Estos planes son hipótesis comerciales. Deben validarse con prospectos técnicos antes de convertirse en ofertas públicas.

---

## 12. Riesgos

| Riesgo | Impacto | Mitigación recomendada |
|---|---|---|
| Vender antes de remediar seguridad. | Riesgo reputacional, técnico y legal. | No vender hasta cumplir requisitos mínimos. |
| Secretos expuestos o versionados. | Acceso no autorizado o compromiso de integraciones. | Eliminar, rotar y auditar secretos antes de demo o piloto. |
| Recolección excesiva de datos. | Riesgo de privacidad y resistencia del cliente. | Limitar datos al inventario técnico necesario. |
| Webhook sin autenticación fuerte. | Recepción de datos falsos o acceso indebido. | Implementar autenticación, validación y rate limiting si aplica. |
| Payload sin integridad verificable. | Riesgo de manipulación de inventario. | Revisar cifrado, firma o HMAC según diseño. |
| Logs con datos sensibles. | Exposición interna o accidental. | Sanitizar logs y limitar acceso. |
| Integración ManageEngine mal mapeada. | Activos duplicados o datos incorrectos. | Probar mapeo con datos ficticios y validación manual. |
| Dependencia de configuración manual. | Errores de instalación y soporte difícil. | Documentar instalación y preparar checklist. |
| Expectativas de monitoreo o administración remota. | Desalineación comercial. | Explicar que el alcance inicial es inventario técnico, no MDM/EDR. |
| Cliente busca inventario comercial. | Venta equivocada y baja satisfacción. | Redirigir a otra solución o descartar oportunidad. |
| Uso de datos reales en demos. | Riesgo de confidencialidad. | Usar datos ficticios o anonimizados. |
| Falta de soporte mensual. | Producto queda sin mantenimiento. | Incluir soporte recurrente en toda propuesta futura. |

Decisión recomendada:

> AutoInventario debe avanzar primero por remediación técnica y validación interna. Solo después debe pasar a demo técnica controlada y piloto externo con alcance limitado.
