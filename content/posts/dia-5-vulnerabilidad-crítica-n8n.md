+++
title = "Vulnerabilidad Crítica en n8n: El 'Ni8mare' del RCE (CVSS 10.0)"
date = 2026-01-09T13:41:00-06:00
draft = false
tags = ["n8n", "Vulnerabilidades", "RCE", "Ciberseguridad", "Sistemas"]
+++

Recientemente se ha revelado una vulnerabilidad de severidad máxima (**CVSS 10.0**) apodada como **"Ni8mare"** que afecta a **n8n**, una de las plataformas de automatización de flujos de trabajo más utilizadas en entornos de desarrollo y operaciones.

### ¿En qué consiste el fallo?
La vulnerabilidad permite a un atacante no autenticado lograr la **ejecución remota de código (RCE)** y tomar el control total de la instancia de n8n. Este fallo radica específicamente en una confusión de `Content-Type` al procesar solicitudes en el nodo **Form Webhook**.

En términos técnicos, al enviar una petición HTTP maliciosa y manipular el header `Content-Type`, el atacante puede engañar al *middleware* (la capa de software que gestiona la comunicación entre componentes) para que lea archivos locales del servidor en lugar de procesar una carga útil normal.

#### Impacto y Escalada:
A través de este método, un actor malintencionado podría:
1.  **Exfiltrar datos:** Extraer la base de datos `database.sqlite` y las claves de cifrado en `config`.
2.  **Suplantación de Identidad:** Forjar cookies de sesión de administrador, evadiendo cualquier mecanismo de autenticación previo.
3.  **Control Total:** Una vez dentro del panel con privilegios de administrador, utilizar el nodo `Execute Command` para ejecutar código directamente en el servidor anfitrión.

---

### Versiones Afectadas
El riesgo es crítico para todas las versiones anteriores a la **1.121.0**, especialmente aquellas instancias **auto-alojadas (self-hosted)** que se encuentran expuestas directamente a internet sin capas de seguridad adicionales.

### Medidas de Mitigación Inmediata

Si gestionas instancias de n8n, se recomienda seguir estos pasos de inmediato:

* **Actualización Crítica:** Migrar a la versión **1.121.0** (o preferiblemente la **1.121.3**, que incluye parches de estabilidad adicionales).
* **Aislamiento:** Si no es posible actualizar de inmediato, restringe el acceso a los Webhooks de tipo "Form" mediante reglas de red.
* **Perímetro de Seguridad:** Colocar la instancia detrás de un **firewall estricto** o una VPN para limitar la superficie de exposición.
* **Hardening:** Activar la autenticación obligatoria en todos los formularios públicos y revisar los logs en busca de peticiones HTTP inusuales dirigidas a los endpoints de Webhook.

---
**Día 05/365**