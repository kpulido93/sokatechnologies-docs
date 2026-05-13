# 05_Stack_Tecnico.md

# Stack Técnico de SokaTechnologies

**Documento:** `05_Stack_Tecnico.md`  
**Ruta objetivo:** `docs/tecnico/05_Stack_Tecnico.md`  
**Empresa:** SokaTechnologies  
**Versión:** 1.0  
**Estado:** Borrador operativo inicial  
**Última actualización:** 2026-05-13  
**Responsable:** Fundador / Operador principal  

---

## 1. Objetivo del stack técnico

Este documento define el stack técnico recomendado para SokaTechnologies en proyectos de software a medida, sitios web corporativos, automatizaciones, dashboards, integraciones, infraestructura cloud/on-prem y soporte.

El objetivo es mantener una base tecnológica simple, segura, mantenible y repetible, adecuada para una empresa pequeña operada inicialmente por un único fundador.

El stack no debe elegirse por moda, sino por capacidad de entregar resultados reales al cliente:

- Ahorro de tiempo.
- Reducción de errores.
- Trazabilidad.
- Control operativo.
- Seguridad.
- Mantenimiento razonable.
- Posibilidad de soporte recurrente.
- Capacidad de crecer sin sobrearquitectura.

Cambio importante definido:

> La web pública inicial de SokaTechnologies será WordPress sobre cPanel, no Next.js/React.

Next.js/React siguen permitidos para demos, dashboards, portales, aplicaciones internas y productos separados, pero no serán la base inicial de la web corporativa principal de SokaTechnologies.

---

## 2. Principios técnicos

### 2.1 Simplicidad

SokaTechnologies debe preferir soluciones simples que puedan mantenerse con claridad.

Reglas:

- No usar arquitectura compleja para problemas simples.
- No crear microservicios si una aplicación modular resuelve el problema.
- No usar Kubernetes en proyectos pequeños sin necesidad real.
- No usar colas, workers o servicios externos si el volumen no lo justifica.
- No agregar dependencias sin beneficio claro.
- No construir desde cero algo que WordPress, cPanel o una herramienta estable pueda resolver de forma segura.

### 2.2 Seguridad

Todo proyecto debe considerar seguridad desde el inicio.

Reglas:

- No guardar secretos en repositorios.
- Usar `.env.example` sin valores reales.
- Separar desarrollo, staging y producción cuando aplique.
- Usar HTTPS en producción.
- Proteger paneles administrativos.
- Aplicar principio de menor privilegio.
- Validar entradas de usuario.
- Controlar roles y permisos.
- Hacer backups.
- Revisar accesos antes y después de producción.

### 2.3 Mantenibilidad

El stack debe poder mantenerse por el fundador y, más adelante, por un equipo pequeño.

Reglas:

- Estructura de carpetas clara.
- README actualizado.
- Variables documentadas.
- Dependencias justificadas.
- Código legible antes que excesivamente abstracto.
- Logs suficientes para diagnosticar.
- Pruebas básicas en módulos críticos.
- Documentación de despliegue.

### 2.4 Documentación

Todo proyecto debe tener documentación mínima.

Reglas:

- README obligatorio.
- `.env.example` obligatorio.
- Checklist de despliegue.
- Notas de instalación.
- Notas de mantenimiento.
- Registro de decisiones técnicas importantes cuando aplique.
- Documentación separada por cliente o producto.

### 2.5 Reutilización

SokaTechnologies debe construir activos reutilizables.

Ejemplos:

- Plantillas de README.
- Plantillas de propuesta.
- Checklist de despliegue.
- Estructura base de APIs.
- Componentes UI reutilizables.
- Plantillas de automatización.
- Scripts seguros y documentados.
- Guías de WordPress/cPanel.
- Guías de backups y monitoreo.

### 2.6 Evitar sobrearquitectura

La tecnología debe responder al problema y al presupuesto del cliente.

Evitar:

- Microservicios innecesarios.
- Kubernetes prematuro.
- Multi-cloud sin necesidad.
- Event sourcing sin caso real.
- CQRS innecesario.
- Arquitecturas serverless complejas para proyectos simples.
- Exceso de frameworks.
- Exceso de plugins.
- Exceso de automatización sin monitoreo.

Regla práctica:

> Si una solución simple, segura y documentada resuelve el problema durante los próximos 12 meses, usar esa solución antes de diseñar algo más complejo.

---

## 3. Stack recomendado por tipo de proyecto

## 3.1 Web pública corporativa de SokaTechnologies en WordPress

La web pública inicial de SokaTechnologies debe implementarse en WordPress sobre cPanel.

### Uso

- Presentar la empresa.
- Explicar servicios.
- Mostrar portafolio anonimizado.
- Publicar contenido comercial.
- Captar oportunidades B2B.
- Tener formulario de contacto.
- Facilitar posicionamiento básico en buscadores.

### Stack recomendado

| Capa | Tecnología recomendada |
|---|---|
| Hosting | cPanel compartido confiable |
| CMS | WordPress |
| Instalación | WordPress Management o Softaculous |
| SSL | SSL/TLS de cPanel / AutoSSL si está disponible |
| Backups | JetBackup del hosting + copia manual antes de cambios grandes |
| Base de datos | MySQL/MariaDB gestionado desde cPanel |
| Administración DB | phpMyAdmin solo para tareas puntuales |
| PHP | Versión moderna compatible con WordPress, tema y plugins |
| Tema | Tema ligero, mantenido y compatible |
| SEO | Un solo plugin SEO |
| Formularios | Un solo plugin de formularios |
| Seguridad | Un solo plugin principal de seguridad |
| Analítica | Google Search Console / Google Analytics o alternativa ligera |
| Correo | SMTP autenticado si el envío desde WordPress falla o cae en spam |

### Reglas

- No usar Next.js/React como web principal inicial.
- No instalar plugins innecesarios.
- No usar temas nulled o crackeados.
- No publicar información sensible de clientes.
- No usar usuario `admin`.
- Activar 2FA donde sea posible.
- Confirmar backups antes de cambios grandes.
- Mantener WordPress, tema y plugins actualizados.
- Documentar plugins instalados y motivo de uso.

---

## 3.2 Sitios web corporativos de clientes

Para sitios web corporativos simples de clientes, WordPress sobre cPanel es una opción válida cuando el cliente necesita rapidez, administración de contenido y bajo costo operativo.

### Stack recomendado

| Necesidad | Recomendación |
|---|---|
| Sitio institucional | WordPress + cPanel |
| Landing page simple | WordPress, HTML estático o constructor ligero |
| Blog corporativo | WordPress |
| Formulario de contacto | Plugin de formularios + SMTP |
| SEO básico | Plugin SEO único |
| Backup | JetBackup o backup del proveedor |
| Seguridad | Plugin de seguridad + buenas prácticas |
| Dominio/SSL | cPanel + proveedor DNS |

### Cuándo usar WordPress para clientes

- El cliente quiere administrar páginas o entradas.
- El presupuesto es limitado.
- El plazo es corto.
- El sitio es principalmente informativo.
- No hay lógica de negocio compleja.
- Se requiere SEO básico y contenido editable.
- El hosting del cliente ya tiene cPanel.
- El cliente necesita una solución fácil de mantener.

### Cuándo no usar WordPress para clientes

- La solución requiere flujos internos complejos.
- Hay reglas de negocio fuertes.
- Se requiere multi-tenant real.
- Se manejan permisos avanzados.
- Hay integraciones críticas.
- Se requieren dashboards operativos complejos.
- La seguridad depende de lógica personalizada.
- Se espera alto volumen transaccional.
- Se necesita una aplicación web, no un sitio de contenido.

---

## 3.3 Aplicaciones web a medida

Las aplicaciones web a medida deben usarse para sistemas internos, portales, plataformas, productos propios o soluciones con lógica de negocio específica.

### Stack inicial recomendado

| Capa | Tecnología permitida inicialmente |
|---|---|
| Frontend | Next.js/React cuando aporte valor real |
| Backend | Node.js/NestJS, Express estructurado o .NET según caso |
| API | REST inicialmente |
| Base de datos | PostgreSQL preferido, MySQL/MariaDB si el entorno lo exige |
| Autenticación | Sesiones o JWT con expiración, según arquitectura |
| UI | Componentes reutilizables, diseño simple |
| Hosting | VPS/cloud para apps reales; plataforma gestionada si reduce operación |
| CI/CD | GitHub Actions o pipeline simple |
| Logs | Logs de aplicación + logs del proveedor |
| Backups | Base de datos + archivos críticos |
| Monitoreo | Uptime + errores + recursos básicos |

### Reglas

- No construir aplicación custom si WordPress resuelve suficientemente el caso.
- No usar Next.js/React solo por preferencia técnica.
- Definir usuarios, roles, datos y flujos antes de desarrollar.
- Crear staging para sistemas operativos.
- No usar datos reales en demos públicas.
- Mantener README y `.env.example`.
- Agregar pruebas mínimas en lógica crítica.

---

## 3.4 APIs

Las APIs deben diseñarse de forma simple, segura y documentada.

### Stack recomendado

| Capa | Recomendación |
|---|---|
| Estilo inicial | REST |
| Autenticación | Token, sesión o integración OAuth según caso |
| Validación | Validación en backend obligatoria |
| Documentación | README, colección de pruebas o especificación básica |
| Seguridad | HTTPS, permisos, rate limiting si aplica |
| Logs | Errores, llamadas críticas e identificadores de correlación |
| Versionado | Usar prefijo o convención cuando el API vaya a evolucionar |

### Reglas

- No exponer endpoints privados sin autenticación.
- No confiar en validaciones solo del frontend.
- No devolver secretos o datos innecesarios.
- No mostrar errores internos al usuario final.
- No registrar contraseñas, tokens o payloads sensibles.
- Documentar endpoints críticos.
- Probar permisos por rol cuando existan.

---

## 3.5 Bases de datos

### Recomendación inicial

| Caso | Base de datos recomendada |
|---|---|
| WordPress/cPanel | MySQL o MariaDB del hosting |
| Aplicaciones web nuevas | PostgreSQL preferido |
| Cliente con stack existente MySQL | MySQL/MariaDB |
| Dashboards simples | PostgreSQL, MySQL o fuente existente |
| Automatizaciones pequeñas | SQLite solo si es local, simple y no crítico |
| Sistemas Microsoft existentes | SQL Server si el cliente ya lo usa |

### Reglas

- No exponer bases de datos públicamente salvo necesidad justificada y controlada.
- Usar usuarios separados por ambiente.
- No usar usuario root/admin desde la aplicación.
- Configurar backups.
- Proteger dumps.
- No subir dumps al repositorio.
- No copiar datos reales a desarrollo sin anonimización.
- Documentar migraciones.
- Probar migraciones antes de producción cuando sea posible.

---

## 3.6 Automatizaciones

Las automatizaciones deben resolver tareas repetitivas sin crear dependencia riesgosa o difícil de mantener.

### Stack recomendado

| Tipo de automatización | Tecnología sugerida |
|---|---|
| Scripts internos | Python |
| Procesamiento de archivos | Python |
| Integraciones con APIs | Python o Node.js |
| Jobs programados simples | Cron del hosting/VPS o scheduler del proveedor |
| Automatizaciones Windows | PowerShell, Python o herramienta específica |
| Flujos no críticos | Herramientas low-code si reducen costo y son mantenibles |
| Integraciones empresariales | API propia o servicio intermedio controlado |

### Reglas

- Documentar entrada, salida y frecuencia.
- Registrar errores.
- No guardar credenciales en scripts.
- Usar variables de entorno o secretos seguros.
- Incluir modo de prueba cuando sea posible.
- Evitar automatizaciones que dependan de sesiones manuales inestables si el proceso es crítico.
- Evitar automatizaciones que violen términos de servicio o consentimiento.

---

## 3.7 Dashboards

Los dashboards deben priorizar claridad y utilidad para decisiones.

### Stack recomendado

| Caso | Tecnología sugerida |
|---|---|
| Dashboard interno simple | App web ligera o herramienta BI |
| Dashboard para cliente | Aplicación web con autenticación |
| Reporte gerencial periódico | Exportación PDF/Excel automatizada |
| Datos desde base existente | Consultas controladas + vistas |
| Producto o portal | React/Next.js si hay interacción significativa |

### Reglas

- No mostrar más datos de los necesarios.
- Aplicar permisos por usuario o cliente.
- Evitar consultas pesadas en producción.
- Usar vistas, réplicas o procesos intermedios si el volumen crece.
- Documentar origen de datos.
- Validar métricas con el cliente antes de automatizarlas.
- No usar datos reales en capturas públicas.

---

## 3.8 Infraestructura cloud

La infraestructura cloud debe usarse cuando el proyecto requiere mayor control, despliegues personalizados, aplicaciones a medida, APIs, workers, bases de datos gestionadas o escalabilidad.

### Stack recomendado inicialmente

| Necesidad | Recomendación |
|---|---|
| VPS simple | Proveedor cloud confiable |
| App web | VPS, PaaS o contenedor gestionado según presupuesto |
| Base de datos | Gestionada si el presupuesto lo permite |
| Archivos | Storage del proveedor |
| DNS/CDN | Cloudflare o proveedor DNS confiable |
| SSL | Certificados gestionados por proveedor o proxy |
| Backups | Snapshots + backup de base de datos |
| Monitoreo | Uptime + recursos + logs |
| CI/CD | GitHub Actions con aprobación para producción |

### Reglas

- MFA en cuentas cloud.
- No usar cuenta root para operación diaria.
- Aplicar menor privilegio.
- Activar alertas de costo.
- Etiquetar recursos por cliente, proyecto y ambiente.
- No abrir puertos innecesarios.
- Configurar backups antes de producción.
- Documentar arquitectura y accesos.
- Preferir infraestructura simple antes de múltiples servicios complejos.

---

## 3.9 Infraestructura on-prem

La infraestructura on-prem aplica cuando el cliente tiene servidores físicos, red local, sistemas internos, NAS, bases de datos locales o restricciones operativas.

### Stack recomendado

| Necesidad | Recomendación |
|---|---|
| Servidores Windows existentes | Mantener si el cliente depende de ellos y están soportados |
| Servidores Linux | Usar para servicios web, APIs o automatizaciones internas |
| Bases de datos locales | Mantener con backup y documentación |
| Acceso remoto | VPN o acceso seguro aprobado |
| Backups | Local + copia externa |
| Monitoreo | Agente o monitoreo básico de disponibilidad |
| Inventario | Documentar hardware, IPs, servicios y responsables |

### Reglas

- No cambiar red o firewall sin aprobación.
- No exponer servicios internos directamente a internet sin evaluación.
- Hacer backup antes de cambios importantes.
- Documentar accesos.
- Identificar responsable del lado del cliente.
- Considerar energía, UPS, disco, red y dependencia física.
- Separar operación técnica de datos sensibles del cliente.

---

## 4. Criterios para elegir WordPress vs app custom

| Criterio | WordPress | App custom |
|---|---|---|
| Sitio informativo | Recomendado | No necesario |
| Blog o contenido editable | Recomendado | Solo si hay razón fuerte |
| Landing de servicios | Recomendado | No necesario |
| Formulario simple | Recomendado | No necesario |
| Bajo presupuesto | Recomendado | Puede ser costoso |
| Lógica de negocio compleja | No recomendado | Recomendado |
| Roles avanzados | Limitado | Recomendado |
| Integraciones críticas | Limitado | Recomendado |
| Procesos operativos internos | No ideal | Recomendado |
| Multi-tenant real | No recomendado | Recomendado |
| Dashboard interactivo | Limitado | Recomendado |
| Alto control de UX y flujos | Limitado | Recomendado |
| Seguridad muy específica | Limitado | Recomendado |
| Escalabilidad transaccional | Limitado | Recomendado |

### Regla de decisión

Usar WordPress cuando el problema principal sea comunicación, presencia digital, contenido y captación.

Usar app custom cuando el problema principal sea operación, lógica de negocio, datos, integraciones, permisos o flujos internos.

---

## 5. Criterios para elegir Next.js/React

Next.js/React están permitidos, pero no deben usarse automáticamente.

### Usar Next.js/React cuando

- Se necesita una interfaz altamente interactiva.
- Hay dashboard o portal con muchos estados.
- Se requiere experiencia de usuario personalizada.
- Se construye un producto propio.
- Se necesita separar frontend y backend.
- Hay autenticación, roles y flujos operativos.
- Se requiere demo comercial moderna.
- El proyecto puede sostener mantenimiento técnico.

### No usar Next.js/React cuando

- El sitio es solo institucional.
- El cliente necesita editar contenido fácilmente.
- El presupuesto no justifica una app custom.
- No habrá mantenimiento técnico mensual.
- WordPress resuelve el 80% del problema.
- El fundador necesita publicar rápido la web corporativa principal.
- El proyecto se volvería más costoso sin beneficio de negocio.

### Uso recomendado en SokaTechnologies

| Uso | ¿Next.js/React? |
|---|---|
| Web pública inicial de SokaTechnologies | No |
| Landing simple de servicio | No, salvo caso especial |
| Demo de Portik | Sí, si el producto ya usa ese stack |
| Dashboard operativo | Sí |
| Portal de cliente | Sí |
| App interna | Sí |
| Sistema administrativo | Sí |
| Blog corporativo | No |

---

## 6. Cuándo usar cPanel

cPanel es adecuado para proyectos simples, sitios corporativos y clientes que necesitan bajo costo operativo.

### Usar cPanel cuando

- El proyecto es WordPress.
- Es un sitio corporativo simple.
- El cliente ya tiene hosting cPanel.
- Se necesita correo, SSL, MySQL y backups en un solo panel.
- No se requiere acceso root.
- No se necesita arquitectura personalizada.
- El presupuesto es limitado.
- El soporte será básico.

### No usar cPanel cuando

- Se necesita una app Node.js compleja.
- Se requieren workers persistentes.
- Se necesitan procesos en background estables.
- Se requiere control avanzado de servidor.
- Se necesitan despliegues CI/CD robustos.
- Hay alto volumen transaccional.
- Se necesitan servicios internos privados.
- Se requiere configuración avanzada de red.

### Uso recomendado

| Proyecto | cPanel |
|---|---|
| Web SokaTechnologies WordPress | Sí |
| Sitio corporativo cliente | Sí |
| Landing page simple | Sí |
| Blog | Sí |
| Portal operativo | Normalmente no |
| Dashboard interno | Normalmente no |
| API crítica | No recomendado |
| Producto SaaS | No recomendado |

---

## 7. Cuándo usar VPS/cloud

VPS/cloud debe usarse cuando se requiere mayor control o cuando el proyecto supera lo que cPanel ofrece de forma segura.

### Usar VPS/cloud cuando

- Hay aplicación custom.
- Hay API propia.
- Hay workers, colas o tareas programadas importantes.
- Hay dashboard con autenticación.
- Hay base de datos gestionada o separada.
- Se necesita CI/CD.
- Hay requerimientos de escalabilidad.
- Se requiere control de red, procesos o servicios.
- Hay integraciones críticas.
- Se necesita monitoreo más completo.

### No usar VPS/cloud cuando

- Solo se necesita un sitio informativo.
- El cliente no pagará mantenimiento.
- No hay capacidad de operar el servidor.
- cPanel resuelve el caso de forma suficiente.
- La complejidad agregada no aporta valor.

### Regla comercial

Si se usa VPS/cloud, debe ofrecerse mantenimiento mensual.

Motivo:

- Hay que aplicar actualizaciones.
- Hay que revisar backups.
- Hay que monitorear recursos.
- Hay que proteger accesos.
- Hay que responder a incidentes.
- Hay que mantener documentación.

---

## 8. Estructura base de repositorios

Todo proyecto de software a medida debe tener una estructura clara.

### Estructura general sugerida

```text
proyecto/
├── README.md
├── .gitignore
├── .env.example
├── docs/
│   ├── arquitectura.md
│   ├── despliegue.md
│   └── decisiones.md
├── src/
├── tests/
└── scripts/
```

### Aplicación con frontend y backend separados

```text
proyecto/
├── README.md
├── .gitignore
├── .env.example
├── docs/
│   ├── arquitectura.md
│   ├── api.md
│   ├── despliegue.md
│   └── seguridad.md
├── frontend/
│   ├── README.md
│   └── .env.example
├── backend/
│   ├── README.md
│   └── .env.example
├── database/
│   ├── migrations/
│   └── seeds/
└── tests/
```

### Repositorios WordPress

Para WordPress en cPanel, no siempre es necesario versionar todo el sitio completo. La decisión depende del proyecto.

Estructura documental mínima:

```text
wordpress-sitio/
├── README.md
├── docs/
│   ├── plugins.md
│   ├── configuracion.md
│   ├── backups.md
│   └── mantenimiento.md
└── assets/
    └── referencias-visuales/
```

Si se desarrolla un tema o plugin personalizado:

```text
wordpress-sitio/
├── README.md
├── .gitignore
├── docs/
├── theme/
└── plugin/
```

### Reglas

- No subir backups completos de WordPress al repositorio.
- No subir dumps de base de datos.
- No subir `wp-config.php` con secretos.
- No subir archivos `.env` reales.
- No subir medios con datos sensibles.
- Documentar tema, plugins y configuraciones relevantes.

---

## 9. Reglas para `.env.example`

Todo proyecto con variables de entorno debe incluir `.env.example`.

### Debe incluir

- Nombres de variables necesarias.
- Valores ficticios.
- Comentarios breves si hace falta.
- Variables por ambiente si aplica.
- Indicación de cuáles son obligatorias.

Ejemplo:

```env
APP_ENV=development
APP_URL=http://localhost:3000
DATABASE_URL=postgresql://user:password@localhost:5432/database_name
JWT_SECRET=change_me
SMTP_HOST=smtp.example.com
SMTP_USER=example_user
SMTP_PASSWORD=change_me
```

### No debe incluir

- Contraseñas reales.
- Tokens reales.
- Llaves privadas.
- URLs internas sensibles.
- IPs privadas del cliente si no son necesarias.
- Credenciales de producción.
- Secretos temporales.
- Datos personales.

### Reglas

```text
[ ] .env real no se versiona.
[ ] .env.example sí se versiona.
[ ] .env.example no contiene secretos.
[ ] README explica cada variable importante.
[ ] Cada ambiente usa valores separados.
[ ] Codex no recibe secretos reales.
```

---

## 10. Reglas para README

Todo repositorio debe tener README.

### README mínimo

```md
# Nombre del proyecto

## Descripción
Qué resuelve el proyecto.

## Contexto
Cliente, producto o uso interno, sin revelar datos sensibles si no corresponde.

## Stack técnico
Tecnologías principales.

## Requisitos
Herramientas necesarias para ejecutar.

## Variables de entorno
Explicación de `.env.example`.

## Instalación
Pasos seguros de instalación.

## Ejecución local
Cómo ejecutar en local.

## Pruebas
Cómo ejecutar pruebas disponibles.

## Despliegue
Resumen o enlace a documentación de despliegue.

## Seguridad
Notas sobre secretos, accesos y datos.

## Mantenimiento
Tareas recurrentes.

## Responsable
Quién mantiene el proyecto.
```

### Reglas

- El README debe permitir retomar el proyecto después de semanas sin depender de memoria.
- No debe contener secretos.
- No debe contener datos confidenciales del cliente.
- Debe actualizarse cuando cambie instalación, despliegue o variables.
- Debe incluir comandos de prueba seguros cuando existan.

---

## 11. Reglas de pruebas

Las pruebas deben ser proporcionales al proyecto. No se exige una suite compleja desde el día uno, pero sí validaciones mínimas.

### Pruebas mínimas por tipo

| Proyecto | Pruebas mínimas |
|---|---|
| WordPress corporativo | Revisión visual, formulario, SSL, responsive, backups |
| Landing page | Revisión visual, enlaces, formulario, responsive |
| API | Pruebas de endpoints críticos, autenticación y errores |
| App web | Flujos principales, roles, formularios y build |
| Automatización | Entrada, salida, errores y modo de prueba |
| Dashboard | Métricas clave, filtros, permisos y rendimiento |
| Base de datos | Migraciones, backups y restauración según criticidad |

### Reglas

- Probar antes de producción.
- Probar después de despliegue.
- Documentar pruebas realizadas.
- No depender solo de “se ve bien en mi máquina”.
- Probar formularios reales.
- Probar roles y permisos.
- Probar escenarios de error.
- Para cambios críticos, probar rollback o plan de reversa.

### Checklist mínimo de pruebas

```text
[ ] Build o carga correcta.
[ ] Flujo principal probado.
[ ] Errores visibles revisados.
[ ] Autenticación probada si aplica.
[ ] Permisos probados si aplica.
[ ] Formulario probado si aplica.
[ ] Logs revisados si aplica.
[ ] Backup confirmado si aplica.
```

---

## 12. Reglas de despliegue

Todo despliegue debe ser controlado.

### Reglas generales

- No desplegar sin saber qué cambió.
- No desplegar cambios de Codex sin revisar diff.
- No desplegar con secretos en el repositorio.
- No desplegar sin backup si el cambio afecta datos.
- No desplegar migraciones sin revisión.
- No tocar producción por prisa sin entender impacto.
- Documentar fecha, cambio y resultado.
- Tener plan de rollback cuando aplique.

### Flujo recomendado para aplicaciones custom

```text
Desarrollo local
→ Pull request o revisión de cambios
→ Pruebas básicas
→ Staging
→ Aprobación
→ Backup si aplica
→ Producción
→ Smoke test
→ Registro de despliegue
```

### Flujo recomendado para WordPress/cPanel

```text
Backup
→ Actualización o cambio
→ Revisión visual
→ Prueba de formulario
→ Revisión móvil
→ Confirmación de SSL
→ Registro de mantenimiento
```

### Registro simple de despliegue

```md
## Registro de despliegue

**Proyecto:**  
**Cliente:**  
**Fecha:**  
**Responsable:**  
**Ambiente:**  
**Cambios realizados:**  
**Backup previo:** Sí / No / No aplica  
**Pruebas realizadas:**  
**Resultado:**  
**Pendientes:**  
```

---

## 13. Reglas de monitoreo y backups

### Monitoreo mínimo

| Tipo de proyecto | Monitoreo mínimo |
|---|---|
| WordPress público | Uptime, SSL, formulario, backups |
| Sitio cliente | Uptime, SSL, backups |
| App custom | Uptime, errores, recursos, logs |
| API | Disponibilidad, errores, latencia básica |
| Dashboard | Disponibilidad, errores, fuente de datos |
| Automatización | Ejecución, errores, resultado |
| Infraestructura | CPU, RAM, disco, red, backups |

### Backups mínimos

| Proyecto | Backup recomendado |
|---|---|
| WordPress en cPanel | JetBackup + backup manual antes de cambios grandes |
| App custom | Base de datos + archivos críticos |
| API | Base de datos/configuración |
| Dashboard | Fuente de datos o consultas/configuración |
| Automatización | Scripts, configuración y datos procesados si aplica |
| VPS/cloud | Snapshot + backup de base de datos |
| On-prem | Backup local + copia externa |

### Reglas

- Backup que no se puede restaurar no debe considerarse confiable.
- No guardar backups sensibles en repositorios.
- No dejar dumps dentro de carpetas públicas.
- Probar restauración según criticidad.
- Configurar alerta si backups fallan cuando sea posible.
- Documentar frecuencia y retención.
- Ofrecer monitoreo y backups como parte de soporte mensual.

---

## 14. Cómo debe trabajar Codex dentro de este stack

Codex debe trabajar como asistente técnico controlado, no como operador autónomo de producción.

### Reglas obligatorias

- No entregar secretos reales a Codex.
- No entregar datos personales innecesarios.
- No pedirle que toque producción directamente.
- No aceptar cambios sin revisar diff.
- No permitir cambios masivos sin plan.
- No permitir que modifique autenticación, permisos o base de datos sin criterios claros.
- No permitir que agregue dependencias sin justificación.
- No permitir que cambie infraestructura sin revisión.
- No mezclar contexto de clientes.

### Formato de tarea para Codex

```md
## Tarea para Codex

### Objetivo
Qué debe lograr.

### Contexto
Proyecto, módulo y razón del cambio.

### Archivos relevantes
Rutas que puede revisar o modificar.

### Restricciones
- No tocar producción.
- No incluir secretos.
- No modificar archivos fuera del alcance.
- No agregar dependencias sin justificar.
- No cambiar base de datos sin propuesta.
- No romper compatibilidad existente.

### Criterios de aceptación
- Resultado funcional esperado.
- Pruebas que deben pasar.
- Comportamientos que no deben romperse.

### Comandos de prueba
Comandos seguros de lint, build o test.

### Qué no debe modificar
Archivos, módulos o configuraciones fuera de alcance.
```

### Checklist para aceptar cambios de Codex

```text
[ ] Diff revisado completo.
[ ] No agregó secretos.
[ ] No modificó archivos fuera del alcance.
[ ] No debilitó seguridad.
[ ] No rompió configuración de ambientes.
[ ] No agregó dependencias innecesarias.
[ ] Pruebas ejecutadas.
[ ] README actualizado si aplica.
[ ] .env.example actualizado si aplica.
[ ] Cambio listo para commit o PR.
```

---

## 15. Tecnologías permitidas inicialmente

Estas tecnologías están permitidas como base inicial porque son prácticas, conocidas y mantenibles para una empresa pequeña.

### Web corporativa y sitios simples

- WordPress.
- cPanel.
- Softaculous o WordPress Management.
- MySQL/MariaDB.
- SSL/TLS de cPanel.
- JetBackup.
- phpMyAdmin para administración puntual.
- Temas mantenidos y ligeros.
- Plugins confiables y mínimos.

### Frontend / aplicaciones

- React.
- Next.js.
- HTML/CSS/JavaScript cuando sea suficiente.
- Tailwind CSS si acelera desarrollo y mantiene consistencia.
- Componentes reutilizables simples.

### Backend / APIs

- Node.js.
- Express estructurado.
- NestJS cuando el proyecto lo justifique.
- .NET cuando el contexto del cliente o producto lo favorezca.
- Python para APIs pequeñas o automatizaciones.

### Bases de datos

- PostgreSQL.
- MySQL/MariaDB.
- SQL Server cuando el cliente ya lo use.
- SQLite solo para casos locales, pequeños o no críticos.

### Automatizaciones

- Python.
- PowerShell para entornos Windows.
- Node.js para integraciones web.
- Cron o scheduler del proveedor.
- Herramientas low-code solo cuando sean mantenibles y no bloqueen al cliente.

### Infraestructura

- cPanel para WordPress y sitios simples.
- VPS/cloud para apps custom.
- DNS/CDN como Cloudflare si aporta seguridad y simplicidad.
- GitHub para repositorios.
- GitHub Actions para CI/CD simple.
- Servicios gestionados cuando reduzcan carga operativa.

### Monitoreo y operación

- Uptime monitoring.
- Logs del proveedor.
- Logs de aplicación.
- Alertas de SSL/dominio.
- Backups del proveedor.
- Snapshots y backups externos según criticidad.

---

## 16. Tecnologías a evitar inicialmente

Estas tecnologías no están prohibidas para siempre, pero deben evitarse al inicio salvo que exista una razón fuerte, presupuesto y capacidad de mantenimiento.

### Evitar inicialmente

| Tecnología o enfoque | Motivo |
|---|---|
| Kubernetes | Excesivo para la mayoría de proyectos iniciales. |
| Microservicios | Aumentan complejidad operativa sin necesidad temprana. |
| Multi-cloud | Difícil de operar y justificar para clientes pequeños. |
| Service mesh | Sobrecarga técnica innecesaria. |
| Event sourcing | Complejo si no hay caso real. |
| CQRS avanzado | No necesario para CRUDs y sistemas internos simples. |
| Serverless complejo | Puede dificultar depuración y costos si no se domina. |
| GraphQL | Evitar inicialmente salvo necesidad clara. |
| Bases NoSQL por moda | Usar solo si el modelo de datos lo justifica. |
| WordPress con exceso de plugins | Riesgo de seguridad, rendimiento y mantenimiento. |
| Temas/plugins nulled | Riesgo alto de malware. |
| Page builders pesados sin necesidad | Pueden hacer el sitio lento y difícil de mantener. |
| Dependencias abandonadas | Riesgo de seguridad y soporte. |
| Librerías nuevas no probadas | Riesgo de estabilidad. |
| Scripts sin documentación | Difíciles de mantener y auditar. |
| Automatizaciones que violen términos o consentimiento | Riesgo legal, reputacional y operativo. |

### Regla para excepciones

Una tecnología inicialmente evitada solo puede usarse si se documenta:

```text
[ ] Problema que resuelve.
[ ] Por qué una solución simple no basta.
[ ] Costo de mantenimiento.
[ ] Riesgos.
[ ] Plan de despliegue.
[ ] Plan de monitoreo.
[ ] Plan de salida si falla.
```

---

## 17. Decisiones recomendadas

1. Usar WordPress sobre cPanel para la web pública inicial de SokaTechnologies.
2. Usar WordPress/cPanel para sitios corporativos simples de clientes.
3. Usar Next.js/React solo para apps, portales, dashboards, demos y productos donde aporte valor real.
4. Usar PostgreSQL como base preferida para aplicaciones nuevas cuando no exista restricción.
5. Usar MySQL/MariaDB cuando el entorno sea WordPress, cPanel o cliente existente.
6. Usar Python como primera opción para automatizaciones.
7. Usar VPS/cloud solo cuando el proyecto requiera control real de aplicación, API, workers o despliegue.
8. Vender mantenimiento mensual cuando haya VPS/cloud, app custom o sistema operativo crítico.
9. Mantener documentación mínima obligatoria en cada proyecto.
10. Usar Codex con tareas pequeñas, sin secretos y con revisión humana.

---

## 18. Checklist rápido de selección de stack

```text
[ ] ¿El proyecto es principalmente informativo?
    → WordPress/cPanel.

[ ] ¿El cliente necesita editar contenido?
    → WordPress.

[ ] ¿El proyecto tiene lógica de negocio propia?
    → App custom.

[ ] ¿Hay roles, permisos, flujos e integraciones críticas?
    → App custom + API + base de datos.

[ ] ¿Es un dashboard o portal interactivo?
    → React/Next.js puede aplicar.

[ ] ¿Es una automatización de archivos o APIs?
    → Python o Node.js.

[ ] ¿El cliente ya tiene cPanel y solo necesita web?
    → cPanel.

[ ] ¿Se necesitan workers, CI/CD, procesos persistentes o control de servidor?
    → VPS/cloud.

[ ] ¿Habrá operación continua?
    → Incluir soporte mensual, monitoreo y backups.
```

---

## 19. Próximo paso operativo

Crear o actualizar los siguientes documentos complementarios:

```text
docs/tecnico/06_Estandares_Seguridad.md
docs/tecnico/07_Checklist_Publicacion_WordPress_cPanel.md
docs/tecnico/08_Plantilla_README_Proyecto.md
docs/tecnico/09_Guia_Uso_Codex.md
docs/tecnico/10_Checklist_Despliegue.md
```

Este documento debe revisarse cada 3 meses o cuando SokaTechnologies adopte una nueva tecnología como estándar.
