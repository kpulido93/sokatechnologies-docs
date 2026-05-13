# Portafolio de Productos SokaTechnologies

**Documento:** `docs/productos/46_Portafolio_Productos_SokaTechnologies.md`  
**Empresa:** SokaTechnologies  
**Versión:** 1.0  
**Estado:** Borrador ejecutivo  
**Última actualización:** 2026-05-13  
**Alineado con:** `docs/empresa/00_Contexto_Empresa.md`  
**Productos incluidos:** Portik, AutoInventario, AutoWhatsApp  

---

## 1. Resumen ejecutivo

SokaTechnologies cuenta con tres productos propios con valor estratégico, pero no deben tratarse como si estuvieran en el mismo nivel de madurez comercial, técnica o de riesgo.

La decisión central del portafolio es:

1. **Portik es la prioridad comercial inmediata.** Debe enfocarse en validación de mercado, demo con datos ficticios, conversaciones con administradores y cierre de un piloto pagado o semi-pagado.
2. **AutoInventario tiene potencial B2B técnico, pero no debe venderse todavía.** Primero debe completar remediación técnica y de seguridad para reducir riesgo operativo, reputacional y de entrega.
3. **AutoWhatsApp debe mantenerse como herramienta operativa controlada.** Solo debe usarse para comunicaciones consentidas, de bajo volumen y con controles claros. No debe posicionarse como herramienta de spam, scraping, captación, apuestas, loterías ni cobranzas agresivas.

Este documento sirve como vista ejecutiva para decidir foco comercial, orden de inversión, riesgos, modelo de venta y próximos pasos del portafolio.

---

## 2. Tabla comparativa de productos

| Producto | Problema que resuelve | Cliente objetivo | Estado actual | Prioridad | ¿Vender ahora? | Modelo esperado | Límite clave |
|---|---|---|---|---|---|---|---|
| **Portik** | Desorden en portería, visitantes, vehículos, reservas y trazabilidad en comunidades residenciales. | Administradores de condominios, conjuntos residenciales y empresas administradoras de propiedades. | Producto con mayor cercanía a validación comercial. | 1 - Comercial inmediata | Sí, como piloto controlado. | Setup inicial + mensualidad por conjunto o plan. | No prometer hardware, app móvil nativa, pagos u OCR en el piloto. |
| **AutoInventario** | Falta de inventario automático y trazabilidad de activos Windows. | Empresas con infraestructura Windows, soporte IT, auditoría de activos o herramientas ITSM. | Producto técnico con potencial, pendiente de remediación. | 2 - Remediación técnica | No, hasta completar seguridad y estabilidad. | Setup + soporte mensual + posible tarifa por rango de equipos. | No vender como inventario comercial de mercancía ni como producto listo. |
| **AutoWhatsApp** | Envío controlado de comunicaciones operativas consentidas desde Excel y WhatsApp Web. | Empresas con contactos propios y necesidad de recordatorios o notificaciones operativas de bajo volumen. | Herramienta operativa con riesgos de uso indebido. | 3 - Uso controlado | Solo en casos limitados y revisados. | Implementación controlada, capacitación y soporte limitado. | Prohibido para spam, bases compradas, scraping, loterías, apuestas, captación o cobranzas agresivas. |

---

## 3. Prioridad estratégica

### 3.1 Prioridad 1: Portik

Portik debe recibir el foco comercial principal porque tiene:

- Dolor operativo claro.
- Cliente objetivo identificable.
- Potencial de mensualidad recurrente.
- Demo comercial comprensible para clientes no técnicos.
- Posibilidad de piloto con alcance limitado.
- Oportunidad de crear caso de éxito anonimizado.

La meta estratégica es convertir Portik en el primer producto propio con validación comercial real.

### 3.2 Prioridad 2: AutoInventario

AutoInventario debe recibir foco técnico, no comercial inmediato.

El producto puede convertirse en una oferta B2B valiosa para empresas con infraestructura Windows, pero venderlo antes de remediar seguridad, build, autenticación, pruebas y despliegue aumentaría el riesgo de incumplimiento, fallas de entrega o exposición de información sensible.

La meta estratégica es llevar AutoInventario a una versión demostrable, instalable y segura antes de cualquier piloto externo.

### 3.3 Prioridad 3: AutoWhatsApp

AutoWhatsApp no debe liderar el portafolio comercial.

Debe tratarse como una herramienta complementaria, interna o de implementación controlada para casos donde exista consentimiento verificable y bajo volumen. Su valor está en apoyar comunicaciones operativas, no en crear campañas masivas.

La meta estratégica es definir si se mantiene como herramienta interna, complemento de automatización o producto limitado con política estricta de uso aceptable.

---

## 4. Estado actual por producto

### 4.1 Portik

**Estado ejecutivo:** producto prioritario para validación comercial.

Portik debe avanzar hacia conversaciones reales con administradores y pilotos controlados. El foco no debe estar en agregar más módulos, sino en demostrar valor operativo con un alcance simple.

Estado recomendado:

- Demo comercial con datos ficticios.
- Pitch claro para administradores.
- Propuesta de piloto documentada.
- Alcance inicial limitado a portería, administración base, predios, vehículos, reservas, novedades y bitácora.
- Criterios de éxito definidos antes de iniciar piloto.
- Soporte mensual incluido desde la propuesta.

No debe incluirse en la primera venta:

- Hardware.
- Reconocimiento automático de placas.
- Pagos en línea.
- App móvil nativa.
- Integraciones complejas.
- Personalizaciones abiertas sin control de cambios.

### 4.2 AutoInventario

**Estado ejecutivo:** producto técnico con potencial, pero no listo para venta.

AutoInventario debe documentarse y desarrollarse como inventario automático de activos Windows. No debe presentarse como inventario comercial de productos, almacén, ventas ni mercancía.

Antes de vender o hacer piloto externo, debe completarse una fase de remediación que cubra:

- Build estable.
- Eliminación y rotación de secretos si existieran exposiciones.
- Autenticación y autorización del endpoint.
- Cifrado y validación de integridad del payload.
- Manejo de logs sin datos sensibles.
- Pruebas mínimas.
- Documentación de instalación.
- Checklist de seguridad.
- Separación de ambientes.
- Plan de soporte y actualización.

Hasta completar esa fase, AutoInventario solo debe manejarse como producto en preparación o demo interna controlada.

### 4.3 AutoWhatsApp

**Estado ejecutivo:** herramienta operativa controlada con riesgo alto de mal uso si se posiciona incorrectamente.

AutoWhatsApp solo debe usarse para comunicaciones operativas donde exista consentimiento verificable del destinatario. Debe mantenerse lejos de usos masivos, invasivos o legalmente sensibles.

Usos permitidos:

- Recordatorios operativos con consentimiento.
- Confirmaciones de citas o servicios.
- Notificaciones a contactos existentes.
- Comunicaciones internas.
- Mensajes de bajo volumen con control humano.

Usos no permitidos:

- Spam.
- Bases compradas.
- Scraping de números.
- Evasión de límites de plataforma.
- Campañas masivas no solicitadas.
- Loterías, apuestas o juegos de azar.
- Captación de jugadores.
- Cobranzas agresivas.
- Contacto a personas sin consentimiento.

Para clientes medianos, regulados o con alto volumen, debe evaluarse WhatsApp Business API o un proveedor autorizado en lugar de automatización sobre WhatsApp Web.

---

## 5. Cliente ideal por producto

| Producto | Cliente ideal | Cliente no ideal |
|---|---|---|
| **Portik** | Administradores de condominios, conjuntos residenciales con portería física, juntas directivas y empresas administradoras de propiedades. | Comunidades sin portería, edificios muy pequeños sin presupuesto, clientes que exigen hardware o app móvil nativa desde el inicio. |
| **AutoInventario** | Empresas con parque Windows, soporte IT interno o externo, auditoría de activos, inventario tecnológico o herramientas ITSM como ManageEngine. | Tiendas que buscan inventario comercial, negocios que necesitan POS, almacenes, facturación o control de mercancía. |
| **AutoWhatsApp** | Empresas con base propia de contactos, consentimiento documentado y necesidad de recordatorios o notificaciones operativas de bajo volumen. | Empresas que compran bases, hacen campañas no solicitadas, operan apuestas/loterías, buscan scraping o quieren automatizar cobranzas sensibles sin revisión legal. |

---

## 6. Modelo comercial esperado

### 6.1 Portik

Modelo recomendado:

- **Setup inicial:** configuración del conjunto, carga básica de datos, usuarios, reglas iniciales y capacitación.
- **Mensualidad recurrente:** soporte, mantenimiento, hosting, monitoreo básico y mejoras menores.
- **Planes por tamaño o alcance:** piloto, básico, pro y multi-conjunto.
- **Servicios adicionales:** limpieza de datos, personalizaciones, reportes avanzados, integraciones futuras o acompañamiento operativo.

Regla comercial:

> Portik debe venderse primero como piloto con alcance cerrado, no como plataforma ilimitada.

### 6.2 AutoInventario

Modelo recomendado después de remediación:

- **Fase interna de estabilización:** sin venta externa hasta completar seguridad y pruebas.
- **Piloto técnico controlado:** instalación en entorno limitado, con datos mínimos y criterios claros.
- **Setup inicial:** instalación del agente, webhook, configuración de integración y documentación.
- **Mensualidad:** soporte, monitoreo de errores, actualizaciones, revisión de logs y mejoras menores.
- **Escalamiento:** precio por rango de equipos o por nivel de soporte.

Regla comercial:

> AutoInventario solo debe venderse cuando pueda instalarse, ejecutarse, auditarse y soportarse con seguridad básica.

### 6.3 AutoWhatsApp

Modelo recomendado:

- **Uso interno o complemento controlado:** preferible como parte de automatizaciones operativas, no como producto principal.
- **Implementación limitada:** configuración, capacitación, plantilla de Excel, política de uso aceptable y revisión de consentimiento.
- **Soporte limitado:** resolución de errores, ajustes menores y revisión de reportes de ejecución.
- **Sin cobro por volumen masivo:** evitar incentivos que empujen a spam o uso indebido.

Regla comercial:

> AutoWhatsApp no debe venderse como herramienta de marketing masivo ni como alternativa para evadir controles de plataformas.

---

## 7. Riesgos por producto

| Producto | Riesgos principales | Mitigación recomendada |
|---|---|---|
| **Portik** | Exposición de datos personales, segregación incorrecta entre conjuntos, prometer demasiados módulos, baja adopción en portería, soporte mayor al previsto. | Usar datos ficticios en demos, minimizar datos visibles, probar segregación por conjunto, vender piloto limitado, capacitar portería y definir soporte por escrito. |
| **AutoInventario** | Secretos expuestos, autenticación incompleta, recolección de datos innecesarios, fallas de build, payload manipulable, despliegue inconsistente, reputación afectada por vender antes de tiempo. | No vender aún, ejecutar remediación técnica, revisar seguridad, rotar secretos si aplica, documentar instalación, crear pruebas y validar ambientes separados. |
| **AutoWhatsApp** | Uso para spam, bases compradas, scraping, incumplimiento de términos de plataforma, reclamos por falta de consentimiento, uso en loterías/apuestas/captación, cobranzas agresivas. | Política estricta de uso aceptable, consentimiento verificable, opt-out, límites por corrida, revisión legal/compliance cuando aplique y rechazo de casos prohibidos. |

Consideración transversal:

> Ningún producto debe usar datos reales de clientes en demos públicas, documentación comercial o material de entrenamiento sin autorización explícita y anonimización adecuada.

---

## 8. Próximas acciones

### 8.1 Próximos 30 días

| Producto | Acción | Resultado esperado |
|---|---|---|
| Portik | Preparar demo con datos ficticios. | Demo lista para mostrar sin exponer información real. |
| Portik | Definir propuesta de piloto. | Alcance, exclusiones, criterios de éxito, setup y mensualidad claros. |
| Portik | Contactar administradores y agendar conversaciones. | Al menos 3 conversaciones de diagnóstico. |
| AutoInventario | Ejecutar revisión de remediación técnica y seguridad. | Lista priorizada de bloqueadores antes de venta. |
| AutoWhatsApp | Formalizar política de uso aceptable. | Documento y checklist antes de cualquier uso con cliente. |

### 8.2 Próximos 60 días

| Producto | Acción | Resultado esperado |
|---|---|---|
| Portik | Ejecutar demos y ajustar pitch. | Objeciones y aprendizajes documentados. |
| Portik | Cerrar piloto pagado o semi-pagado. | Primer caso real validable sin datos públicos sensibles. |
| AutoInventario | Corregir bloqueadores críticos. | Producto más cercano a demo técnica interna. |
| AutoWhatsApp | Agregar controles mínimos: opt-out, límites, reporte y confirmación de consentimiento. | Reducción de riesgo operativo y reputacional. |

### 8.3 Próximos 90 días

| Producto | Acción | Resultado esperado |
|---|---|---|
| Portik | Convertir piloto en mensualidad. | Validación comercial y base de ingreso recurrente. |
| Portik | Crear caso de éxito anonimizado si el piloto funciona. | Material comercial sin revelar datos reales. |
| AutoInventario | Decidir si pasa a piloto técnico externo. | Go/no-go basado en seguridad, estabilidad y soporte. |
| AutoWhatsApp | Decidir si queda como herramienta interna, complemento o producto limitado. | Posicionamiento claro y controlado. |

---

## 9. Decisiones pendientes

| Decisión | Recomendación inicial | Criterio para decidir |
|---|---|---|
| Precio piloto de Portik | Definir setup + mensualidad antes de nuevas demos. | Tamaño del conjunto, carga de datos, soporte incluido y duración del piloto. |
| Alcance exacto del piloto de Portik | Limitar a portería, administración base, predios, vehículos, reservas, novedades y bitácora. | Debe poder demostrarse y operarse sin personalizaciones complejas. |
| Publicación de Portik en la web de SokaTechnologies | Presentarlo como producto prioritario y piloto disponible. | Demo estable, propuesta clara y formulario de contacto preparado. |
| Venta de AutoInventario | No vender hasta completar remediación técnica y seguridad. | Build estable, secretos controlados, autenticación, pruebas, documentación y checklist de despliegue. |
| Posicionamiento de AutoInventario | Mantenerlo como inventario técnico de activos Windows. | No mezclarlo con inventario comercial, almacén, POS o facturación. |
| Futuro de AutoWhatsApp | Mantenerlo como herramienta controlada o complemento de automatización. | Existencia de consentimiento, bajo volumen, opt-out, límites y revisión de cumplimiento. |
| Uso de WhatsApp para clientes regulados | Preferir API oficial o proveedor autorizado cuando exista volumen, sensibilidad o regulación. | Riesgo legal, reputacional, de plataforma o de datos personales. |
| Nivel de soporte por producto | Incluir soporte mensual desde la primera propuesta. | Criticidad, número de usuarios, horario esperado, monitoreo y responsabilidad operativa. |

Validaciones legales, fiscales, contractuales o de cumplimiento deben solicitarse cuando el producto se use en sectores regulados, comunicaciones sensibles, datos personales, infraestructura crítica o procesos con impacto legal.
