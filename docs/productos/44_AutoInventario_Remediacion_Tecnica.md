# AutoInventario - Plan de Remediación Técnica

**Documento:** `docs/productos/44_AutoInventario_Remediacion_Tecnica.md`  
**Empresa:** SokaTechnologies  
**Producto:** AutoInventario  
**Versión:** 1.0  
**Estado:** Borrador técnico operativo  
**Última actualización:** 2026-05-13  
**Uso:** Planificar la remediación técnica y de seguridad antes de cualquier venta, demo externa o piloto con clientes.  

---

## 1. Resumen del estado actual

AutoInventario es un producto técnico con potencial B2B para inventario automático de activos Windows e integración con herramientas ITSM como ManageEngine ServiceDesk Plus.

El producto no debe venderse ni presentarse como listo hasta completar una remediación técnica y de seguridad. La prioridad actual no es comercializar, sino estabilizar la base técnica, eliminar riesgos críticos y documentar una forma segura de instalar, probar, desplegar y soportar la solución.

Estado recomendado:

| Área | Estado recomendado |
|---|---|
| Comercial | No vender todavía. |
| Demo externa | No ejecutar con clientes hasta completar remediación mínima. |
| Demo interna | Permitida solo con datos ficticios y sin secretos reales. |
| Desarrollo | Enfocado en build, estructura, autenticación, seguridad y pruebas. |
| Despliegue | No desplegar a producción sin pruebas, revisión, backup y rollback. |

Objetivo de remediación:

> Convertir AutoInventario en un producto compilable, instalable, seguro, documentado y demostrable para un piloto técnico controlado.

---

## 2. Bloqueadores críticos

Estos bloqueadores deben resolverse antes de cualquier venta, demo externa o piloto con cliente.

| Bloqueador | Riesgo | Acción requerida |
|---|---|---|
| Build inestable o roto. | No se puede entregar ni probar con confianza. | Normalizar estructura, referencias, dependencias y comandos de build. |
| Estructura de solución desordenada. | Dificulta mantenimiento y revisión. | Definir estructura clara para agente, Webhook, tests, infraestructura y documentación. |
| Secretos expuestos o hardcodeados. | Riesgo crítico de seguridad. | Eliminar, rotar si aplica y mover a gestor seguro o variables protegidas. |
| Autenticación del Webhook incompleta. | Riesgo de recepción no autorizada de datos. | Implementar autenticación, validación y rechazo de solicitudes inválidas. |
| Validación insuficiente del payload. | Riesgo de datos corruptos, falsos o inseguros. | Validar esquema, campos requeridos, tamaños y tipos de datos. |
| Cifrado o integridad no revisados. | Riesgo de manipulación o exposición de inventario. | Revisar diseño de protección, firma o integridad del payload. |
| Dependencias obsoletas o vulnerables. | Riesgo de fallas o exposición. | Revisar, actualizar y documentar dependencias críticas. |
| Tests insuficientes. | Riesgo de regresiones y falsa confianza. | Crear pruebas mínimas para agente, Webhook e integración simulada. |
| Logs con información sensible. | Riesgo de exposición accidental. | Sanitizar logs y definir niveles de detalle por ambiente. |
| Despliegue no reproducible. | Riesgo de errores manuales. | Documentar despliegue, variables, rollback y validaciones. |
| Documentación incompleta. | Producto difícil de instalar, operar y vender. | Crear README, guía de instalación, operación, seguridad y soporte. |

---

## 3. Riesgos de seguridad

AutoInventario maneja información técnica de equipos Windows. Aunque no debe recolectar datos sensibles innecesarios, su operación puede revelar detalles de infraestructura si se maneja mal.

| Riesgo | Impacto | Mitigación |
|---|---|---|
| Secretos en repositorio. | Compromiso de Webhook, cloud o ITSM. | Secret scanning, rotación y eliminación de secretos. |
| Credenciales hardcodeadas. | Exposición en build o código fuente. | Usar variables protegidas o gestor de secretos. |
| Webhook público sin autenticación. | Recepción de payloads falsos o abuso. | API key, firma, HMAC u otro mecanismo aprobado. |
| Payload sin integridad. | Manipulación de inventario. | Firma, HMAC o mecanismo equivalente según diseño. |
| Logs excesivos. | Exposición de datos de equipos, usuarios o tokens. | Sanitización y retención limitada. |
| Recolección excesiva. | Riesgo de privacidad y resistencia del cliente. | Principio de mínima información necesaria. |
| Permisos cloud amplios. | Impacto mayor ante error o compromiso. | IAM de menor privilegio. |
| Integración ITSM con permisos excesivos. | Modificación indebida de activos o datos. | Credenciales con permisos mínimos. |
| Dependencias vulnerables. | Riesgo de explotación o fallas. | Revisión periódica y actualización controlada. |
| Datos reales en pruebas o demos. | Riesgo de confidencialidad. | Usar datos ficticios o anonimizados. |
| Despliegue sin rollback. | Riesgo operativo si falla. | Backup, pruebas previas y plan de reversa. |

Regla general:

> Si una remediación afecta autenticación, secretos, infraestructura, datos o despliegue, debe revisarse con diff, pruebas y checklist antes de considerarse aceptada.

---

## 4. Plan de remediación por fases

La remediación debe ejecutarse por fases para reducir riesgo y facilitar revisión.

### Fase 0: congelar venta y ordenar diagnóstico

Objetivo: evitar compromisos comerciales antes de corregir la base técnica.

Acciones:

- Declarar AutoInventario como no vendible temporalmente.
- Revisar estado del repositorio y ramas activas.
- Listar componentes existentes: agente, Webhook, Lambda/backend, tests, infraestructura y documentación.
- Identificar secretos o configuraciones sensibles sin copiarlas a documentación.
- Definir comandos seguros de build y test.
- Crear backlog priorizado.

Criterio de salida:

- Existe lista clara de bloqueadores técnicos y de seguridad.

### Fase 1: secretos, estructura y build

Objetivo: lograr una base compilable y segura para trabajar.

Acciones:

- Eliminar secretos del código y configuración versionada.
- Rotar secretos si se confirma exposición.
- Crear o actualizar `.env.example` con valores ficticios.
- Revisar `.gitignore` para excluir archivos sensibles.
- Normalizar estructura de solución/proyectos.
- Corregir referencias rotas.
- Ejecutar build del agente y backend.
- Documentar comandos de build.

Criterio de salida:

- Build principal pasa en ambiente local.
- No hay secretos conocidos en el diff.
- La estructura del proyecto es comprensible.

### Fase 2: autenticación, validación y payload

Objetivo: proteger la recepción y procesamiento de inventarios.

Acciones:

- Definir mecanismo de autenticación del Webhook.
- Validar payload por esquema o DTO.
- Rechazar payloads incompletos, inválidos o excesivos.
- Revisar cifrado o protección de datos en tránsito.
- Revisar integridad del payload.
- Evitar logging de payload completo.
- Agregar pruebas de solicitudes válidas e inválidas.

Criterio de salida:

- El Webhook rechaza solicitudes no autorizadas o mal formadas.
- Existen pruebas mínimas de autenticación y validación.

### Fase 3: integración ITSM y manejo de errores

Objetivo: estabilizar la sincronización con ManageEngine o herramienta ITSM objetivo.

Acciones:

- Documentar mapeo de campos con valores genéricos.
- Simular respuestas de la herramienta ITSM.
- Manejar errores de API.
- Manejar reintentos controlados.
- Evitar duplicados cuando sea posible.
- Registrar eventos técnicos sin credenciales ni payload sensible completo.
- Definir permisos mínimos de integración.

Criterio de salida:

- La integración puede probarse con datos ficticios o mock sin exponer secretos.

### Fase 4: pruebas, documentación y empaquetado

Objetivo: preparar un producto demostrable y mantenible.

Acciones:

- Crear pruebas mínimas del agente.
- Crear pruebas del Webhook.
- Crear pruebas de integración simulada.
- Documentar instalación local.
- Documentar configuración por ambiente.
- Documentar operación y soporte.
- Crear checklist de demo interna.
- Crear checklist de piloto técnico.
- Preparar empaquetado o artefacto instalable si aplica.

Criterio de salida:

- Existe documentación suficiente para instalar, probar y operar el producto sin conocimiento tribal.

### Fase 5: despliegue controlado y piloto técnico

Objetivo: validar operación en ambiente controlado antes de venta.

Acciones:

- Preparar ambiente de staging o demo técnica.
- Configurar secretos en mecanismo seguro.
- Configurar logs y monitoreo básico.
- Ejecutar pruebas antes de despliegue.
- Confirmar backup cuando el cambio afecte datos o configuración persistente.
- Definir rollback.
- Ejecutar demo interna con datos ficticios.
- Documentar resultados.

Criterio de salida:

- Producto apto para evaluar piloto técnico limitado, todavía con alcance y riesgos documentados.

---

## 5. Checklist de secretos y credenciales

Antes de avanzar a demo externa o piloto, completar:

```text
[ ] No hay secretos hardcodeados en código fuente.
[ ] No hay tokens, API keys, contraseñas ni llaves privadas en repositorio.
[ ] No hay archivos `.env` reales versionados.
[ ] Existe `.env.example` con valores ficticios.
[ ] `.gitignore` excluye archivos sensibles.
[ ] Se ejecutó revisión de patrones de secretos en el repositorio.
[ ] Se identificaron secretos expuestos sin copiarlos a documentación.
[ ] Se rotaron secretos si existió exposición real.
[ ] Credenciales de ITSM se guardan en mecanismo seguro.
[ ] Credenciales cloud se guardan en mecanismo seguro.
[ ] Variables sensibles no aparecen en logs.
[ ] Variables sensibles no aparecen en errores de aplicación.
[ ] No se incluyeron secretos en prompts de Codex o ChatGPT.
[ ] Se documentó cómo configurar secretos sin registrar valores reales.
```

Archivos y datos prohibidos en repositorio:

- `.env` reales.
- Dumps.
- Backups.
- Tokens.
- Llaves privadas.
- Certificados privados.
- Credenciales de ManageEngine.
- Credenciales cloud.
- Endpoints privados de clientes.
- IPs sensibles.
- Datos reales de equipos, usuarios, seriales o clientes.

---

## 6. Checklist de build y pruebas

Antes de declarar estable la base técnica:

```text
[ ] Existe comando documentado para restaurar dependencias.
[ ] Existe comando documentado para compilar agente.
[ ] Existe comando documentado para compilar Webhook/backend.
[ ] Build local pasa en configuración de desarrollo.
[ ] Build de release pasa si aplica.
[ ] No hay referencias rotas a rutas antiguas.
[ ] No hay archivos duplicados o proyectos abandonados que confundan el build.
[ ] Dependencias críticas están revisadas.
[ ] Dependencias vulnerables fueron actualizadas o justificadas.
[ ] Tests unitarios mínimos del agente pasan.
[ ] Tests del Webhook pasan.
[ ] Tests de validación de payload pasan.
[ ] Tests de autenticación pasan.
[ ] Tests de integración simulada pasan.
[ ] No se usan datos reales en tests.
[ ] No se usan secretos reales en tests.
[ ] Se documentan pruebas que no pudieron ejecutarse y por qué.
```

Pruebas mínimas recomendadas:

- Payload válido.
- Payload sin autenticación.
- Payload con autenticación inválida.
- Payload incompleto.
- Payload con campos de tamaño excesivo.
- Error de red hacia ITSM.
- Respuesta inválida de ITSM.
- Reintento controlado.
- Log sin secretos.

---

## 7. Checklist de autenticación

Antes de exponer un Webhook fuera del entorno local:

```text
[ ] Webhook requiere autenticación.
[ ] El secreto de autenticación no está hardcodeado.
[ ] Solicitudes sin autenticación son rechazadas.
[ ] Solicitudes con autenticación inválida son rechazadas.
[ ] Payload se valida antes de procesarse.
[ ] Se considera firma, HMAC o mecanismo equivalente para integridad.
[ ] Se limita tamaño máximo del payload.
[ ] Se limita método HTTP permitido.
[ ] Se registra evento de rechazo sin exponer datos sensibles.
[ ] Se evita devolver errores internos al cliente.
[ ] Se considera rate limiting si el endpoint queda expuesto.
[ ] Se considera allowlist o controles adicionales si el contexto lo requiere.
[ ] Se documenta cómo rotar credenciales.
[ ] Se documenta cómo revocar acceso de un agente o cliente.
```

Requisitos de autorización:

- Cada cliente o entorno debe poder separarse lógicamente.
- Un agente no debe poder enviar datos como otro cliente sin control.
- Las credenciales de integración ITSM deben tener permisos mínimos.
- Los logs de autenticación deben ayudar a investigar sin revelar secretos.

---

## 8. Checklist de despliegue

No desplegar a producción sin pruebas, revisión y rollback.

Antes de cualquier despliegue controlado:

```text
[ ] Ambiente objetivo identificado: desarrollo / staging / producción.
[ ] Cambios revisados por diff.
[ ] Build ejecutado correctamente.
[ ] Tests mínimos ejecutados.
[ ] Secretos configurados fuera del repositorio.
[ ] Variables de entorno documentadas con valores ficticios.
[ ] Permisos cloud revisados bajo menor privilegio.
[ ] Logs configurados sin secretos.
[ ] Monitoreo básico definido.
[ ] Backup realizado si el cambio afecta datos, configuración persistente o integración crítica.
[ ] Plan de rollback documentado.
[ ] Responsable del despliegue definido.
[ ] Ventana de despliegue definida si afecta usuarios.
[ ] Validación posterior al despliegue definida.
[ ] Resultado del despliegue documentado.
```

Checklist posterior:

```text
[ ] Webhook responde en healthcheck o prueba equivalente.
[ ] Solicitudes no autorizadas son rechazadas.
[ ] Payload ficticio válido se procesa correctamente.
[ ] Integración ITSM simulada o controlada responde como se espera.
[ ] Logs no exponen secretos ni payload sensible completo.
[ ] Alertas o errores críticos se revisaron.
[ ] Rollback no fue necesario o quedó documentado.
```

Producción solo debe considerarse cuando:

- Exista aprobación explícita.
- El ambiente de staging haya sido validado.
- Los datos reales estén protegidos.
- Exista backup y rollback.
- Exista responsable de soporte.

---

## 9. Tareas sugeridas para Codex

Codex puede apoyar solo con tareas pequeñas, revisables y sin tocar producción. Cada tarea debe ejecutarse en una rama o cambio acotado, con diff revisable y pruebas documentadas.

### Tarea 1: revisar estructura y build

```md
Objetivo:
Identificar y corregir referencias rotas para que el build local compile.

Restricciones:
- No tocar producción.
- No eliminar archivos sin revisar su uso.
- No agregar secretos.
- No cambiar lógica funcional salvo lo necesario para compilar.

Criterios de aceptación:
- Build del agente pasa.
- Build del backend/Webhook pasa.
- Comandos ejecutados quedan documentados.
- No aparecen secretos en el diff.
```

### Tarea 2: crear `.env.example` seguro

```md
Objetivo:
Crear o actualizar `.env.example` con variables necesarias y valores ficticios.

Restricciones:
- No copiar valores reales.
- No incluir URLs privadas.
- No incluir tokens, API keys ni credenciales reales.

Criterios de aceptación:
- `.env.example` documenta variables requeridas.
- `.env` reales siguen ignorados por Git.
- El diff no contiene secretos.
```

### Tarea 3: implementar validación de payload

```md
Objetivo:
Validar estructura del payload recibido por el Webhook antes de procesarlo.

Restricciones:
- No registrar payload completo en logs.
- No cambiar contrato sin documentarlo.
- No usar datos reales en tests.

Criterios de aceptación:
- Payload válido pasa.
- Payload incompleto se rechaza.
- Payload excesivo se rechaza.
- Tests mínimos pasan.
```

### Tarea 4: reforzar autenticación del Webhook

```md
Objetivo:
Asegurar que el Webhook rechace solicitudes no autorizadas.

Restricciones:
- No hardcodear secretos.
- No exponer valores de autenticación en logs.
- No desplegar a producción.

Criterios de aceptación:
- Solicitud sin autenticación se rechaza.
- Solicitud con autenticación inválida se rechaza.
- Solicitud válida se procesa.
- Tests de autenticación pasan.
```

### Tarea 5: sanitizar logs

```md
Objetivo:
Revisar logs del agente, Webhook e integración para evitar datos sensibles.

Restricciones:
- No eliminar logs útiles para soporte.
- No registrar tokens, credenciales ni payloads completos.
- No incluir datos reales.

Criterios de aceptación:
- Logs mantienen diagnóstico básico.
- Logs no exponen secretos.
- Casos de error quedan documentados.
```

### Tarea 6: documentar instalación y operación

```md
Objetivo:
Crear documentación mínima de instalación, configuración, pruebas y soporte.

Restricciones:
- Usar ejemplos ficticios.
- No incluir rutas internas sensibles.
- No incluir endpoints reales.

Criterios de aceptación:
- README o guía técnica permite instalar y probar localmente.
- Variables están documentadas sin secretos.
- Checklist de pruebas queda incluido.
```

### Tarea 7: preparar pruebas de integración simulada

```md
Objetivo:
Validar flujo hacia ITSM usando mocks o datos ficticios.

Restricciones:
- No usar credenciales reales.
- No llamar APIs reales de clientes.
- No usar datos reales de equipos.

Criterios de aceptación:
- Se prueban respuestas exitosas.
- Se prueban errores de API.
- Se prueban reintentos o manejo de fallo.
```

---

## 10. Criterios para declarar el producto vendible

AutoInventario solo puede considerarse vendible cuando cumpla criterios técnicos, de seguridad, documentación, operación y comercialización.

### 10.1 Criterios técnicos

- Build estable y reproducible.
- Agente ejecutable o instalable de forma controlada.
- Webhook funcional.
- Integración ITSM validada con datos ficticios o ambiente controlado.
- Manejo de errores documentado.
- Logs útiles y sanitizados.
- Dependencias revisadas.
- Pruebas mínimas pasando.

### 10.2 Criterios de seguridad

- Sin secretos en repositorio.
- Secretos expuestos rotados si aplica.
- Webhook autenticado.
- Payload validado.
- Integridad del payload revisada.
- Credenciales fuera del código.
- Permisos mínimos en cloud e ITSM.
- Datos reales fuera de demos públicas.
- Checklist de despliegue completado.

### 10.3 Criterios operativos

- Guía de instalación.
- Guía de configuración.
- Guía de operación.
- Guía de soporte.
- Checklist de troubleshooting.
- Plan de rollback o desinstalación.
- Responsable de soporte definido.

### 10.4 Criterios comerciales

- Alcance comercial claro.
- Exclusiones documentadas.
- Precio piloto definido.
- Modelo de soporte mensual definido.
- Criterios de aceptación del piloto definidos.
- Riesgos explicados al cliente.
- Contrato, términos o acuerdo revisado según país y contexto.

### 10.5 Decisión final

AutoInventario puede avanzar a piloto externo solo si:

```text
[ ] Build pasa.
[ ] Tests mínimos pasan.
[ ] No hay secretos conocidos en repositorio.
[ ] Webhook tiene autenticación.
[ ] Payload se valida.
[ ] Logs no exponen secretos.
[ ] Integración ITSM se probó con datos ficticios o ambiente controlado.
[ ] Documentación mínima existe.
[ ] Despliegue tiene checklist, backup si aplica y rollback.
[ ] Alcance comercial y soporte mensual están definidos.
```

Si alguno de estos puntos críticos falla, el producto debe seguir en remediación y no debe venderse.
