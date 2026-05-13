# Portik - Plan de Validación de Mercado

**Documento:** `docs/productos/42_Portik_Validacion_Mercado.md`  
**Empresa:** SokaTechnologies  
**Producto:** Portik  
**Versión:** 1.0  
**Estado:** Borrador estratégico operativo  
**Última actualización:** 2026-05-13  
**Uso:** Validar mercado, dolor, presupuesto, urgencia y disposición a pagar antes de invertir más desarrollo o personalización.  

---

## 1. Hipótesis de mercado

La validación de Portik debe partir de hipótesis claras. Estas hipótesis no deben asumirse como verdad hasta confirmarse con conversaciones, demos y pilotos.

| Hipótesis | Qué se debe validar | Evidencia esperada |
|---|---|---|
| Los conjuntos con portería física tienen problemas de trazabilidad. | Si ingresos, salidas, visitantes y novedades se registran de forma dispersa o manual. | El prospecto describe casos recientes de desorden, reclamos o falta de evidencia. |
| Los administradores pierden tiempo por llamadas y mensajes operativos. | Si administración o portería reciben consultas repetitivas que podrían centralizarse. | El prospecto identifica procesos que consumen tiempo semanalmente. |
| Hay disposición a pagar por orden y control operativo. | Si el prospecto entiende valor mensual, no solo compra única. | Pregunta por precio, piloto, mensualidad o implementación. |
| Portik puede iniciar con un MVP web limitado. | Si el prospecto acepta validar sin app móvil nativa, hardware, pagos en línea, OCR ni WhatsApp automático. | Acepta piloto enfocado en portería, predios, vehículos, visitantes, reservas, novedades y bitácora. |
| Empresas administradoras pueden escalar Portik a varios conjuntos. | Si administradoras tienen procesos repetidos y varios conjuntos con dolores similares. | Mencionan múltiples propiedades y necesidad de estandarizar operación. |
| No todos los conjuntos necesitan Portik. | Si existen segmentos sin dolor, presupuesto o complejidad suficiente. | Prospectos pequeños, sin portería o sin urgencia no avanzan. |

Regla de validación:

> No invertir más desarrollo ni personalización fuerte hasta confirmar dolor real, presupuesto, urgencia y disposición a iniciar un piloto pagado o semi-pagado.

---

## 2. Segmentos a validar

Portik debe validarse por segmentos, no con una idea genérica de "todos los conjuntos".

| Segmento | Prioridad | Qué validar | Riesgo |
|---|---|---|---|
| Administradores independientes de condominios | Alta | Dolor operativo, capacidad de decisión y presupuesto mensual. | Pueden tener presupuesto limitado o depender de junta. |
| Empresas administradoras de propiedades | Muy alta | Potencial multi-conjunto, procesos repetibles y decisión comercial. | Ciclo de venta más largo o más exigencias. |
| Juntas directivas de conjuntos residenciales | Media | Dolor, apoyo interno y proceso de aprobación. | Decisiones lentas o politizadas. |
| Conjuntos medianos con portería física | Alta | Uso diario de visitantes, vehículos, reservas y novedades. | Si el volumen es bajo, el valor puede no justificar mensualidad. |
| Conjuntos pequeños | Baja | Si tienen suficiente dolor y presupuesto. | Pueden no necesitar sistema formal. |
| Conjuntos de alto estándar | Media | Expectativas sobre experiencia, seguridad y soporte. | Pueden exigir app, hardware o integraciones fuera del MVP. |
| Comunidades sin portería | Baja | Si existe otro dolor operativo relevante. | El producto puede no encajar en etapa inicial. |

Segmentos que no deben priorizarse inicialmente:

- Comunidades sin proceso de acceso o portería.
- Conjuntos sin presupuesto.
- Prospectos que exigen app móvil nativa como condición inicial.
- Prospectos que condicionan compra a hardware, OCR, pagos en línea o WhatsApp automático.
- Clientes que no quieren ordenar datos mínimos de predios, residentes y vehículos.

---

## 3. Perfil de cliente ideal

El cliente ideal inicial de Portik debe cumplir la mayoría de estas condiciones:

| Criterio | Señal positiva |
|---|---|
| Tipo de operación | Tiene portería física o control de acceso diario. |
| Tamaño | Tiene suficientes predios, visitantes o reservas para justificar orden operativo. |
| Dolor | Reconoce problemas con llamadas, WhatsApp, Excel, cuadernos o falta de trazabilidad. |
| Decisión | Existe administrador, junta o empresa administradora con capacidad de aprobar piloto. |
| Presupuesto | Acepta hablar de setup, piloto y mensualidad. |
| Datos | Puede entregar listados básicos de predios, residentes/contactos y vehículos. |
| Urgencia | Quiere mejorar la operación en semanas, no "algún día". |
| Alcance | Acepta iniciar con MVP web limitado. |
| Continuidad | Entiende que software operativo requiere soporte mensual. |

Perfil recomendado:

> Administrador o empresa administradora que gestiona uno o varios conjuntos con portería física, alto uso de visitantes/vehículos/reservas, problemas de trazabilidad y disposición a probar un piloto web con alcance cerrado.

Perfil no recomendado:

- Conjunto muy pequeño sin volumen operativo.
- Prospecto que solo quiere una app para residentes sin validar portería.
- Cliente que exige desarrollo completo antes de pagar.
- Cliente que pide demo o piloto con datos reales sin controles.
- Administración que no tiene responsable claro ni capacidad de decisión.

---

## 4. Preguntas de diagnóstico

Las preguntas deben descubrir comportamiento actual, dolor, costo del problema, presupuesto, decisión y urgencia.

### 4.1 Operación actual

- ¿Cuántos predios, apartamentos o casas tiene el conjunto?
- ¿Cuántos puntos de acceso o porterías manejan?
- ¿Cuántos turnos de portería existen?
- ¿Cómo autorizan visitantes actualmente?
- ¿Dónde registran ingresos y salidas?
- ¿Cómo consultan vehículos autorizados?
- ¿Cómo controlan parqueaderos de visitantes?
- ¿Cómo manejan reservas de áreas comunes?
- ¿Cómo registran novedades, paquetes o incidentes?
- ¿Qué información necesita ver portería durante una validación?

### 4.2 Dolor y consecuencias

- ¿Qué proceso genera más llamadas o interrupciones?
- ¿Qué errores se repiten con más frecuencia?
- ¿Han tenido reclamos por falta de registro o trazabilidad?
- ¿Cuándo fue la última vez que no pudieron confirmar quién autorizó un ingreso?
- ¿Qué pasa cuando cambia el turno de portería?
- ¿Qué información suele estar desactualizada?
- ¿Cuánto tiempo dedica administración a resolver dudas operativas?
- ¿Qué problema sería urgente resolver en los próximos 30 días?

### 4.3 Presupuesto y decisión

- ¿Ya pagan algún software administrativo o de portería?
- ¿Tienen presupuesto mensual para herramientas operativas?
- ¿Quién aprueba una prueba piloto?
- ¿La decisión la toma administración, junta directiva o empresa administradora?
- ¿Qué tendría que demostrar el piloto para que lo continúen pagando?
- ¿Prefieren pago de configuración + mensualidad, o piloto con setup y mensualidad reducida?
- ¿Qué rango de inversión mensual sería razonable si el sistema reduce trabajo y mejora trazabilidad?

### 4.4 Alcance y adopción

- ¿Aceptarían iniciar con una versión web limitada?
- ¿Qué usuarios participarían en el piloto?
- ¿Portería tiene computador, tablet o equipo con navegador?
- ¿Qué tan cómodo está el equipo de portería usando herramientas digitales?
- ¿Quién entregaría y validaría los datos iniciales?
- ¿Qué funcionalidades son indispensables para un piloto?
- ¿Qué funcionalidades pueden esperar para una fase futura?

---

## 5. Señales de dolor real

No basta con que el prospecto diga "suena interesante". Buscar señales concretas.

| Señal | Interpretación |
|---|---|
| Describe un incidente reciente con visitantes, vehículos o autorizaciones. | Hay dolor operativo concreto. |
| Menciona reclamos de residentes o junta directiva. | El problema tiene presión interna. |
| Dice que administración recibe muchas llamadas repetitivas. | Hay costo de tiempo. |
| Usa varios archivos, cuadernos o grupos de WhatsApp para operar. | Hay dispersión de información. |
| Portería depende de una persona que "se sabe todo". | Hay riesgo operativo. |
| No pueden auditar fácilmente ingresos o novedades. | La trazabilidad tiene valor. |
| Tienen varios conjuntos con procesos distintos. | Puede haber oportunidad multi-conjunto. |
| Preguntan cómo sería un piloto o cuánto cuesta. | Hay intención de avanzar. |
| Preguntan por carga de datos y capacitación. | Están imaginando implementación real. |

Señales débiles:

- "Interesante, mándame información."
- "Podría servir algún día."
- "Queremos algo moderno", sin problema concreto.
- "Nos gustaría una app", sin dolor de portería.
- "Queremos verlo, pero no hay presupuesto."

---

## 6. Señales de presupuesto

El presupuesto debe validarse con señales de comportamiento, no solo opiniones.

| Señal de presupuesto | Nivel |
|---|---|
| Ya pagan software administrativo, seguridad, cámaras, soporte o sistemas internos. | Alta |
| Preguntan por precio, forma de pago, mensualidad o contrato. | Alta |
| Aceptan piloto pagado o semi-pagado con setup inicial. | Alta |
| Tienen administrador profesional o empresa administradora. | Media-alta |
| Piden propuesta formal para junta o comité. | Media |
| Preguntan si el costo puede dividirse entre unidades. | Media |
| Quieren piloto gratis sin compromiso ni fecha de decisión. | Baja |
| Dicen que solo comprarían con pago único bajo y sin soporte. | Baja |
| No identifican quién aprueba ni de dónde saldría el pago. | Baja |

Preguntas útiles:

- ¿Qué presupuesto mensual manejan hoy para herramientas operativas?
- ¿Qué costo tiene para ustedes el desorden actual en tiempo, reclamos o seguridad?
- ¿El conjunto ya paga sistemas, cámaras, administración digital o soporte tecnológico?
- ¿Qué formato de pago sería más fácil de aprobar: setup + mensualidad, piloto reducido o plan mensual?
- ¿Quién tendría que aprobar el gasto?

---

## 7. Objeciones esperadas

| Objeción | Qué significa | Respuesta de validación |
|---|---|---|
| "Ya usamos WhatsApp." | Ven comunicación como solución suficiente. | Preguntar si WhatsApp les da historial, permisos, reportes y trazabilidad por evento. |
| "La portería no es tecnológica." | Temen baja adopción. | Validar si aceptarían un flujo mínimo: buscar placa/predio y registrar ingreso/salida. |
| "Queremos app móvil." | Están pensando en experiencia de residente. | Aclarar que el MVP es web y preguntar si el dolor principal está en portería o residentes. |
| "Necesitamos pagos en línea." | Mezclan administración financiera con operación. | Separar pagos como fase futura; validar si portería y trazabilidad tienen valor sin pagos. |
| "Queremos cámaras o reconocimiento de placas." | Esperan automatización física. | Aclarar que hardware/OCR no son parte del MVP; validar si primero sirve ordenar datos y registros manuales. |
| "Eso lo hace nuestro sistema actual." | Puede haber competencia o baja diferenciación. | Preguntar qué sí resuelve bien y qué sigue siendo manual o problemático. |
| "No tenemos presupuesto." | Dolor débil o prioridad baja. | Preguntar si habría presupuesto ante un piloto corto con alcance claro y beneficio medible. |
| "La junta decide." | Ciclo de decisión indirecto. | Pedir criterios de aprobación, fechas de reunión y material necesario. |
| "Tenemos datos desordenados." | Riesgo de implementación. | Separar carga básica de limpieza profunda; validar si pueden entregar una plantilla mínima. |

No convertir objeciones en promesas. Si piden app móvil nativa, pagos, hardware, OCR o WhatsApp automático, registrarlo como aprendizaje, no como compromiso del MVP.

---

## 8. Experimentos de validación

Los experimentos deben avanzar de menor costo a mayor compromiso.

### 8.1 Experimento 1: entrevistas de problema

| Campo | Definición |
|---|---|
| Objetivo | Validar dolor antes de mostrar solución. |
| Meta inicial | 10 conversaciones con administradores, juntas o empresas administradoras. |
| Duración | 20 a 30 minutos por conversación. |
| Evidencia buscada | Casos reales de desorden, falta de trazabilidad, llamadas repetitivas o problemas de portería. |
| Criterio de avance | Al menos 5 de 10 prospectos describen dolor concreto y frecuente. |

### 8.2 Experimento 2: demo con datos ficticios

| Campo | Definición |
|---|---|
| Objetivo | Validar si el MVP web genera interés real. |
| Meta inicial | 5 demos con prospectos calificados. |
| Duración | 15 a 25 minutos por demo. |
| Evidencia buscada | Preguntas sobre piloto, precio, usuarios, carga de datos o tiempos. |
| Criterio de avance | Al menos 2 de 5 demos terminan en solicitud de propuesta o siguiente reunión. |

### 8.3 Experimento 3: propuesta de piloto

| Campo | Definición |
|---|---|
| Objetivo | Validar disposición a pagar. |
| Meta inicial | Enviar 3 propuestas a prospectos calificados. |
| Evidencia buscada | Discusión de precio, ajustes de alcance, aprobación interna o anticipo. |
| Criterio de avance | Al menos 1 propuesta avanza a piloto pagado o semi-pagado. |

### 8.4 Experimento 4: piloto pagado o semi-pagado

| Campo | Definición |
|---|---|
| Objetivo | Validar uso operativo y continuidad mensual. |
| Meta inicial | 1 piloto con alcance cerrado. |
| Duración | 30 a 60 días. |
| Evidencia buscada | Uso por portería, feedback de administración, registros de eventos y decisión de continuidad. |
| Criterio de avance | El piloto genera evidencia suficiente para mensualidad o caso de éxito anonimizado. |

### 8.5 Experimento 5: administradora multi-conjunto

| Campo | Definición |
|---|---|
| Objetivo | Validar si Portik puede escalar por empresa administradora. |
| Meta inicial | 3 conversaciones con empresas que administren varios conjuntos. |
| Evidencia buscada | Procesos repetidos, necesidad de estandarización, interés en piloto para un conjunto inicial. |
| Criterio de avance | 1 administradora acepta evaluar piloto en un conjunto específico. |

---

## 9. Métricas de validación

Medir avance con números simples y decisiones claras.

| Métrica | Meta inicial | Qué indica |
|---|---|---|
| Prospectos contactados | 30 | Tamaño del esfuerzo comercial inicial. |
| Conversaciones agendadas | 10 | Interés inicial del mercado. |
| Conversaciones completadas | 8 | Calidad de acceso a decisores o influenciadores. |
| Demos realizadas | 5 | Interés después de escuchar el problema. |
| Prospectos con dolor fuerte | 5 | Confirmación de problema frecuente. |
| Prospectos con presupuesto probable | 3 | Potencial comercial real. |
| Solicitudes de propuesta | 2 a 3 | Disposición a evaluar compra. |
| Pilotos pagados o semi-pagados | 1 | Validación comercial inicial. |
| Tasa de avance conversación -> demo | 50% o más | Mensaje y segmento adecuados. |
| Tasa de avance demo -> propuesta | 40% o más | Demo conecta con dolor y valor. |
| Tasa de avance propuesta -> piloto | 30% o más | Precio, alcance y urgencia razonables. |

Métricas cualitativas:

- Objeciones más repetidas.
- Segmento con más dolor.
- Segmento con más presupuesto.
- Funcionalidad MVP más valorada.
- Funcionalidades solicitadas fuera del MVP.
- Razones de no compra.
- Tiempo estimado de decisión.

---

## 10. Criterios para avanzar, pausar o cambiar enfoque

### 10.1 Avanzar

Avanzar con más desarrollo, propuesta comercial y mejoras del MVP si:

- Al menos 5 de 10 conversaciones muestran dolor real.
- Al menos 3 prospectos preguntan por precio, piloto o implementación.
- Al menos 2 prospectos solicitan propuesta.
- Al menos 1 prospecto acepta piloto pagado o semi-pagado.
- Los prospectos aceptan iniciar sin app móvil nativa, pagos en línea, hardware, OCR ni WhatsApp automático.
- El alcance MVP resuelve un problema suficiente para iniciar.

Acción recomendada:

- Cerrar piloto.
- Documentar aprendizajes.
- Mejorar solo los flujos necesarios para el piloto.
- Preparar caso de éxito anonimizado si el piloto funciona.

### 10.2 Pausar

Pausar inversión adicional si:

- Los prospectos dicen que el problema existe, pero no tiene prioridad.
- Hay interés general, pero nadie acepta hablar de precio o piloto.
- La mayoría pide funcionalidades fuera del MVP como condición inicial.
- No se logra acceso a decisores.
- El segmento no tiene presupuesto mensual.

Acción recomendada:

- Ajustar mensaje.
- Cambiar segmento.
- Reducir alcance.
- Validar con empresas administradoras antes de seguir construyendo.

### 10.3 Cambiar enfoque

Cambiar enfoque si:

- El dolor más fuerte no está en portería, sino en otro proceso distinto.
- Los prospectos ya tienen sistemas suficientes y el dolor residual es bajo.
- El mercado espera hardware, app móvil nativa u OCR desde el inicio.
- El presupuesto disponible no soporta setup + mensualidad.
- Los clientes solo quieren soluciones gratuitas o pago único sin soporte.

Posibles cambios:

- Enfocar Portik en empresas administradoras multi-conjunto.
- Reducir MVP a portería + bitácora + predios + vehículos.
- Convertir Portik en módulo de operación residencial más simple.
- Posponer funcionalidades de residente hasta validar portería.
- Crear oferta de diagnóstico operativo para conjuntos antes de vender software.

---

## 11. Plantilla para registrar aprendizajes

Usar esta plantilla después de cada conversación, demo o seguimiento. No incluir datos reales sensibles. Usar nombres genéricos como `Prospecto A`, `Administradora B` o `Conjunto Demo 01`.

```md
## Registro de validación Portik

**Fecha:**  
**Tipo de interacción:** Entrevista / Demo / Propuesta / Seguimiento  
**Prospecto genérico:**  
**Segmento:** Administrador independiente / Empresa administradora / Junta directiva / Otro  
**Tamaño aproximado:** Número de predios o rango, sin datos sensibles  
**Rol de la persona:** Administrador / Miembro de junta / Operación / Otro  

### Contexto operativo
- ¿Tiene portería física?
- ¿Cómo maneja visitantes?
- ¿Cómo registra ingresos y salidas?
- ¿Cómo maneja vehículos?
- ¿Cómo maneja reservas o novedades?

### Dolor identificado
- Dolor principal:
- Frecuencia del problema:
- Impacto operativo:
- Ejemplo anonimizado:

### Presupuesto y decisión
- ¿Existe presupuesto probable? Sí / No / No claro
- ¿Quién decide?
- ¿Hay disposición a setup + mensualidad?
- ¿Hay urgencia? Alta / Media / Baja

### Reacción a Portik
- Funciones que más interesaron:
- Funciones que no generaron interés:
- Objeciones:
- Preguntas sobre precio o piloto:

### Solicitudes fuera del MVP
- App móvil nativa: Sí / No
- Pagos en línea: Sí / No
- Hardware: Sí / No
- OCR o reconocimiento de placas: Sí / No
- WhatsApp automático: Sí / No
- Otras solicitudes:

### Resultado
- Próximo paso:
- Nivel de oportunidad: Alto / Medio / Bajo
- ¿Enviar propuesta? Sí / No
- ¿Candidato a piloto? Sí / No

### Aprendizaje para SokaTechnologies
- Qué se confirmó:
- Qué se rechazó:
- Qué ajustar en pitch/demo:
- Riesgos o dudas:
```

Checklist de confidencialidad para registros:

- [ ] No incluir nombres reales de residentes.
- [ ] No incluir teléfonos, correos, documentos ni placas reales.
- [ ] No incluir nombre real del conjunto salvo autorización explícita.
- [ ] No incluir capturas con datos reales.
- [ ] No mezclar información entre prospectos.
- [ ] No convertir solicitudes fuera del MVP en promesas comerciales.
