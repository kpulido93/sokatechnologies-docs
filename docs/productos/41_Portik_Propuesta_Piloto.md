# Portik - Propuesta Base de Piloto

**Documento:** `docs/productos/41_Portik_Propuesta_Piloto.md`  
**Empresa:** SokaTechnologies  
**Producto:** Portik  
**Versión:** 1.0  
**Estado:** Borrador comercial operativo  
**Última actualización:** 2026-05-13  
**Uso:** Propuesta base para pilotos comerciales con administradores de condominios, conjuntos residenciales y empresas administradoras.  

---

## 1. Resumen de la propuesta

Esta propuesta define un piloto controlado de Portik para validar su uso en la operación diaria de un condominio, conjunto residencial o comunidad cerrada.

Portik es una plataforma web para control de acceso, operación de portería, administración básica y autogestión inicial de residentes. El piloto busca demostrar valor en un alcance limitado, medible y vendible, sin prometer funcionalidades avanzadas que deben evaluarse en fases posteriores.

El piloto se enfoca en:

- Portería.
- Predios y residentes.
- Vehículos.
- Visitantes.
- Registro de ingresos y salidas.
- Parqueaderos de visitantes.
- Reservas básicas.
- Novedades.
- Bitácora y reportes simples.

La intención comercial es validar el valor operativo de Portik y, si el piloto funciona, convertirlo en un servicio mensual recurrente de software, soporte y mejora continua.

---

## 2. Problema identificado

Muchos conjuntos residenciales gestionan su operación diaria con llamadas, mensajes de WhatsApp, hojas de cálculo, cuadernos físicos y criterios informales de portería.

Esto suele generar:

| Problema | Impacto |
|---|---|
| Visitantes autorizados por mensajes dispersos. | Portería pierde tiempo confirmando información. |
| Registros manuales de ingreso y salida. | Baja trazabilidad y dificultad para auditar eventos. |
| Datos de predios, residentes y vehículos desactualizados. | Decisiones lentas o inconsistentes en portería. |
| Reservas manejadas por mensajes o archivos separados. | Cruces, reclamos y falta de visibilidad. |
| Novedades sin seguimiento centralizado. | Administración pierde contexto y control. |
| Dependencia de una persona o portero específico. | La operación se vuelve frágil ante cambios de turno. |

Portik busca ordenar estos procesos en una plataforma web simple, consultable y trazable.

---

## 3. Objetivo del piloto

El objetivo del piloto es validar si Portik mejora la operación diaria del conjunto mediante un alcance inicial controlado.

Objetivos específicos:

- Confirmar que portería puede consultar información clave con rapidez.
- Reducir dependencia de llamadas, cuadernos y archivos dispersos.
- Registrar ingresos, salidas, novedades y reservas con trazabilidad.
- Medir adopción por parte de administración y portería.
- Identificar mejoras necesarias antes de una implementación mensual completa.
- Definir si Portik debe continuar como servicio recurrente para el conjunto.

El piloto no busca resolver todos los procesos administrativos del conjunto desde el primer día. Busca validar el flujo base y el valor operativo.

---

## 4. Alcance incluido

El alcance del piloto debe mantenerse limitado para proteger tiempo, costo y claridad de entrega.

| Área | Incluido en piloto |
|---|---|
| Configuración inicial | Configuración de 1 conjunto o comunidad demo/productiva según acuerdo. |
| Usuarios | Creación de usuarios básicos para administración y portería. |
| Roles | Acceso diferenciado para administración, portería y residente demo si aplica. |
| Predios | Carga inicial básica de apartamentos, casas, torres, bloques o etapas. |
| Residentes/contactos | Registro de residentes o contactos autorizados con datos mínimos necesarios. |
| Vehículos | Registro de vehículos asociados a predios. |
| Búsqueda por placa | Consulta manual de placa para identificar predio asociado. |
| Búsqueda por predio | Consulta de ficha operativa del predio. |
| Visitantes | Registro o consulta de visitantes autorizados. |
| Ingresos y salidas | Registro manual de eventos de entrada y salida. |
| Parqueaderos visitantes | Ocupación y liberación básica de cupos de visitante. |
| Reservas | Solicitud, revisión y estado básico de reservas de áreas comunes. |
| Novedades | Registro de novedades operativas o incidentes simples. |
| Bitácora | Consulta de eventos principales registrados en el sistema. |
| Reportes básicos | Filtros simples por fecha, evento o usuario cuando estén disponibles. |
| Capacitación | Sesión inicial para administración y portería. |
| Seguimiento | Reunión de revisión durante o al cierre del piloto. |

Datos permitidos para demo o preparación:

- Datos ficticios.
- Datos anonimizados.
- Plantillas sin información sensible.

No deben usarse datos reales de clientes, residentes, visitantes, teléfonos, placas o documentos en demos comerciales.

---

## 5. Exclusiones

El piloto no incluye:

- App móvil nativa.
- Pagos en línea.
- Pasarela de pagos.
- Hardware.
- Cámaras.
- OCR.
- Reconocimiento automático de placas.
- WhatsApp automático.
- Correos automáticos avanzados.
- Firma electrónica.
- Integraciones contables.
- Integraciones con ERP, CRM u otros sistemas externos.
- Migraciones complejas desde sistemas anteriores.
- Limpieza masiva de datos desordenados.
- Carga ilimitada de información.
- Personalizaciones ilimitadas.
- Reportes BI avanzados.
- Analítica avanzada.
- Soporte 24/7.
- Operación de mesa de ayuda para residentes.
- Gestión legal, contable o administrativa del conjunto.

Cualquier necesidad fuera de este alcance debe tratarse como mejora, fase adicional o servicio separado.

---

## 6. Entregables

Al finalizar el piloto, SokaTechnologies debe entregar:

| Entregable | Descripción |
|---|---|
| Ambiente de piloto | Acceso a Portik configurado para el conjunto piloto o ambiente acordado. |
| Usuarios iniciales | Usuarios de administración y portería definidos para la prueba. |
| Datos iniciales cargados | Predios, residentes/contactos y vehículos básicos según plantilla validada. |
| Flujos operativos activos | Búsqueda por placa, búsqueda por predio, visitantes, ingresos/salidas, reservas y novedades según alcance. |
| Capacitación inicial | Sesión de uso para administración y portería. |
| Guía básica de uso | Instrucciones simples para los flujos principales. |
| Registro de incidencias y feedback | Lista de hallazgos, errores, dudas y mejoras detectadas durante el piloto. |
| Informe de cierre | Resumen de uso, aprendizajes, criterios de éxito y recomendación de continuidad. |
| Propuesta de continuidad | Opción de mensualidad recurrente para operación, soporte y mejoras. |

Los entregables deben validarse contra el alcance acordado, no contra solicitudes nuevas agregadas durante el piloto.

---

## 7. Cronograma sugerido

Duración recomendada: **30 a 60 días**, según tamaño del conjunto, disponibilidad del cliente y calidad de los datos iniciales.

### Opción sugerida de 4 semanas

| Semana | Actividad | Resultado esperado |
|---|---|---|
| Semana 1 | Diagnóstico corto, confirmación de alcance, plantilla de datos y configuración inicial. | Alcance cerrado, responsables definidos y datos base solicitados. |
| Semana 2 | Carga inicial, usuarios, validación de flujos y capacitación. | Portik listo para uso controlado por administración y portería. |
| Semana 3 | Uso operativo, registro de incidencias y ajustes menores dentro del alcance. | Evidencia de uso real y feedback documentado. |
| Semana 4 | Revisión de métricas, cierre del piloto y propuesta de continuidad. | Decisión de continuidad mensual, ajustes o cierre. |

### Opción de 60 días

Usar 60 días cuando:

- El conjunto tenga mayor cantidad de predios.
- Existan varios turnos de portería.
- La administración requiera más tiempo de adopción.
- Se quiera medir uso de reservas, novedades y bitácora con más datos.
- El cliente necesite aprobación de junta o comité.

---

## 8. Responsabilidades de SokaTechnologies

SokaTechnologies será responsable de:

- Confirmar el alcance funcional del piloto por escrito.
- Configurar el ambiente de piloto acordado.
- Crear usuarios iniciales según roles definidos.
- Cargar datos iniciales recibidos en plantilla acordada.
- Capacitar a usuarios administrativos y de portería.
- Dar soporte durante el período acordado.
- Corregir errores relacionados con el alcance incluido.
- Registrar hallazgos, incidencias y solicitudes de mejora.
- Proteger la confidencialidad de la información recibida.
- Evitar el uso de datos reales en demos públicas.
- Entregar informe de cierre y recomendación de continuidad.

SokaTechnologies no será responsable de:

- Decisiones administrativas internas del conjunto.
- Datos incorrectos, incompletos o desactualizados entregados por el cliente.
- Procesos operativos que el cliente no comunique o valide.
- Cambios fuera de alcance solicitados durante el piloto.
- Fallas de conectividad, equipos o infraestructura del cliente.
- Soporte 24/7 si no está contratado por escrito.

---

## 9. Responsabilidades del cliente

El cliente será responsable de:

- Nombrar un responsable principal del piloto.
- Definir quién aprueba decisiones y entregables.
- Entregar datos iniciales en la plantilla acordada.
- Validar que los datos entregados sean correctos y estén autorizados para uso en el piloto.
- Designar usuarios de administración y portería.
- Asegurar disponibilidad de usuarios clave para capacitación.
- Usar el sistema durante el período de piloto.
- Reportar incidencias por el canal acordado.
- Dar feedback oportuno y concreto.
- Comunicar internamente el alcance del piloto.
- No usar el piloto para procesos fuera del alcance acordado.
- Realizar pagos según la forma acordada.

Si el cliente no entrega datos, aprobaciones o usuarios en los tiempos acordados, el cronograma puede ajustarse.

---

## 10. Criterios de éxito

El piloto debe medirse con criterios simples y verificables.

| Criterio | Meta sugerida | Evidencia |
|---|---|---|
| Uso por portería | Portería usa el sistema durante el período acordado. | Registros de búsqueda, ingreso, salida o novedades. |
| Consulta de información | Usuarios consultan predios, placas o visitantes. | Eventos o feedback de uso. |
| Registro de eventos | Se registran ingresos, salidas, novedades o reservas. | Bitácora del sistema. |
| Reducción de desorden | Administración identifica menor dependencia de llamadas o archivos dispersos. | Feedback cualitativo. |
| Adopción básica | Administración y portería completan flujos principales. | Validación en reunión de seguimiento. |
| Datos mínimos útiles | Predios, residentes/contactos y vehículos permiten operar casos reales. | Revisión de carga inicial. |
| Valor percibido | Cliente identifica razones para continuar con mensualidad. | Decisión de continuidad o solicitud de propuesta. |

El piloto se considera exitoso si demuestra valor operativo suficiente para justificar una continuidad mensual, aunque queden mejoras para fases posteriores.

---

## 11. Soporte durante el piloto

El soporte del piloto debe ser limitado y definido.

### Incluido

- Canal de soporte acordado.
- Atención en horario laboral definido.
- Corrección de errores relacionados con el alcance incluido.
- Aclaraciones de uso para administración y portería.
- Registro de incidencias.
- Reunión de seguimiento durante o al cierre del piloto.

### No incluido

- Soporte 24/7.
- Atención ilimitada a residentes.
- Cambios funcionales grandes.
- Nuevos módulos.
- Integraciones externas.
- Carga permanente de datos fuera de lo pactado.
- Soporte de equipos, red, internet, cámaras o hardware del cliente.

### Clasificación simple de solicitudes

| Tipo | Ejemplo | Tratamiento |
|---|---|---|
| Incidencia | Un flujo incluido no funciona como se acordó. | Revisar dentro del soporte del piloto. |
| Duda de uso | Usuario no recuerda cómo registrar una salida. | Resolver por canal acordado o guía básica. |
| Mejora menor | Cambiar texto, filtro simple o ajuste pequeño. | Evaluar si entra dentro del piloto. |
| Cambio de alcance | Nuevo módulo, integración o regla compleja. | Cotizar como fase adicional. |

---

## 12. Precio y forma de pago

El precio final debe definirse según tamaño del conjunto, calidad de datos, duración del piloto, nivel de soporte y alcance confirmado.

### Estructura comercial recomendada

| Concepto | Descripción |
|---|---|
| Setup inicial del piloto | Configuración, carga inicial, usuarios, capacitación y puesta en marcha. |
| Mensualidad del piloto | Soporte durante el piloto, seguimiento y ajustes menores dentro del alcance. |
| Servicios adicionales | Limpieza de datos, carga masiva, personalizaciones, reportes especiales o integraciones futuras. |

### Forma de pago recomendada

Regla comercial:

> No iniciar el piloto sin anticipo o pago inicial confirmado.

Opción A - Piloto pagado:

- 50% al aprobar la propuesta.
- 50% antes de iniciar uso operativo o al completar configuración inicial.
- Mensualidad del piloto pagada por adelantado si aplica.

Opción B - Piloto semi-pagado:

- Pago inicial obligatorio de configuración.
- Mensualidad reducida durante el piloto.
- Compromiso del cliente de participar en seguimiento, validar criterios de éxito y entregar feedback.

No se recomienda piloto completamente gratuito, salvo que exista una razón estratégica clara, documentada y aprobada por SokaTechnologies.

### Campos para completar antes de enviar

```md
Precio de setup: USD [monto]
Mensualidad durante piloto: USD [monto]
Duración del piloto: [30/60] días
Forma de pago: [50/50, setup + mensualidad, otra]
Validez de la propuesta: [15] días calendario
Costos externos incluidos: Sí / No
Costos externos excluidos: hosting, dominio, licencias, servicios de terceros u otros según aplique
```

Validar condiciones fiscales, contractuales y de facturación con asesores correspondientes antes de enviar propuestas formales.

---

## 13. Continuidad después del piloto

Si el piloto cumple los criterios de éxito, la recomendación es convertir Portik en un servicio mensual recurrente.

### Opciones de continuidad

| Opción | Uso recomendado | Incluye |
|---|---|---|
| Plan Básico | Conjunto que necesita portería, predios, vehículos y bitácora. | Operación base, soporte limitado y mantenimiento. |
| Plan Operativo | Conjunto que usa reservas, novedades y seguimiento frecuente. | Módulos base, soporte mensual, ajustes menores y reporte de estado. |
| Plan Multi-conjunto | Administradora con varios conjuntos. | Gestión por conjunto, soporte priorizado y roadmap por fases. |

### Elementos de la mensualidad

La mensualidad puede incluir:

- Uso continuo de Portik según plan acordado.
- Soporte funcional.
- Mantenimiento correctivo.
- Revisión de incidencias.
- Backups y monitoreo básico cuando aplique.
- Ajustes menores dentro de bolsa o alcance mensual.
- Reunión periódica de seguimiento.
- Priorización de mejoras.

### Mejoras futuras posibles

Estas mejoras no forman parte del piloto, pero pueden evaluarse después:

- Reportes avanzados.
- Mejoras de autogestión de residentes.
- Integraciones externas.
- Flujos adicionales por reglas del conjunto.
- App móvil nativa.
- Pagos en línea.
- Hardware.
- OCR o reconocimiento automático de placas.

Cualquier mejora futura debe definirse con alcance, precio, tiempo, criterios de aceptación y responsabilidades.

---

## 14. Condiciones y supuestos

Esta propuesta parte de los siguientes supuestos:

- El piloto se limita a 1 conjunto, salvo acuerdo distinto.
- El cliente entregará datos mínimos en plantilla acordada.
- Los datos entregados por el cliente estarán autorizados para uso operativo.
- La demo comercial usará solo datos ficticios.
- La carga inicial será básica y limitada.
- El alcance no incluye limpieza profunda de datos.
- Los usuarios del cliente estarán disponibles para capacitación y validación.
- La operación se realizará desde navegador web.
- El cliente contará con internet y equipos funcionales para usar el sistema.
- El piloto no incluye app móvil nativa, pagos en línea, hardware, OCR, reconocimiento automático de placas ni WhatsApp automático.
- Los cambios fuera de alcance se cotizarán por separado.
- La continuidad mensual se definirá al cierre del piloto o antes si el cliente decide avanzar.
- Todo acuerdo comercial debe quedar documentado por escrito.

Condiciones recomendadas:

- No iniciar sin anticipo o pago inicial.
- No prometer fechas sin datos y aprobaciones del cliente.
- No usar datos reales en demos públicas.
- No compartir información del conjunto con terceros sin autorización.
- Definir un canal único de soporte.
- Definir responsables de aprobación.
- Validar términos legales, fiscales, privacidad y contratación antes de usar esta propuesta con un cliente real.

---

## Checklist antes de enviar al prospecto

- [ ] Se confirmó dolor operativo.
- [ ] Se identificó responsable de decisión.
- [ ] Se definió alcance incluido.
- [ ] Se explicaron exclusiones.
- [ ] Se acordó duración del piloto.
- [ ] Se completaron precio y forma de pago.
- [ ] Se incluyó anticipo o pago inicial.
- [ ] Se aclaró que no incluye app móvil nativa, pagos, hardware, OCR ni WhatsApp automático.
- [ ] Se definieron criterios de éxito.
- [ ] Se explicó la continuidad mensual.
- [ ] No se incluyeron datos reales de clientes, residentes, placas, teléfonos o documentos.
