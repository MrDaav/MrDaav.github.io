---
title: "La fragilidad del sistema: CVE-2025-66478 y la crisis de seguridad en México"
date: 2026-01-07T22:05:00-06:00
draft: false
tags: ["Opinión", "UNAM", "Ciberseguridad", "DFIR", "Brecha de Talento"]
---

El inicio de 2026 quedará marcado por uno de los incidentes de seguridad digital más significativos en la historia de la ciberseguridad en México. Entre el **31 de diciembre y el 1 de enero**, la UNAM sufrió una intrusión que escaló hasta comprometer el corazón de su infraestructura.

## ¿Qué sucedió?

El ataque, ejecutado por el actor conocido como **"ByteToBreach"**, no fue producto de la casualidad. Se trató de una cadena de fallas que permitieron el control total:

1. **El Vector de Entrada:** Explotación de la vulnerabilidad **CVE-2025-66478** en servidores que utilizaban el framework *Next.js*.
2. **Movimiento Lateral y Escalada:** Los atacantes encontraron **llaves SSH privadas** expuestas en los equipos. Esto les permitió saltar a los balanceadores de carga **F5 BIG-IP**.
> **F5 BIG-IP** es un dispositivo que tiene tres funciones principales: balancear la carga para no colapsar el servicio, optimizar las páginas a fin de que ofrezcan un tiempo de carga menor y protección contra ataques actuando como WAF.
3. **El Botín:** Una vez dentro, obtuvieron acceso de superusuario (*Root*) al directorio **LDAP**, comprometiendo:
    * Datos de **380,000** alumnos y académicos.
    * Correos electrónicos de la **Oficina del Rector**.
    * Facturas, contraseñas cifradas y registros bancarios.
> **LDAP** viene de *Lightweight Directory Access Protocol*, que es en pocas palabras una base de datos que contiene lo necesario para la autenticación de los distintos usuarios, donde la página solicita una comparación entre un value y otro (userXpass == passGiven)

La DGTIC reportó que solo 5 sistemas fueron afectados, pero la evidencia de la filtración del LDAP sugiere un impacto mucho más profundo en la identidad digital de la comunidad.

---

## El factor humano: La vulnerabilidad silenciosa

Un detalle que destaca es la situación laboral detrás de cámaras. Meses antes del ataque, el personal de la **Coordinación de Proyectos Tecnológicos** trabajaba bajo protesta debido a falta de pagos. 

Esto nos recuerda una máxima de la industria: **La ciberseguridad no solo depende de parches de software, sino de la estabilidad del equipo humano que custodia los sistemas.**

Es alarmante que la UNAM tuviera un antecedente de acceso ilícito en **marzo de 2025** y, aun así, dejara llaves SSH privadas expuestas. La seguridad reactiva (arreglar tras el golpe) siempre es más costosa que la proactiva, además que el atacante no solo buscaba vender la base de datos; filtró documentos que evidencian plagios de patentes y abusos de autoridad. ¿Es este el inicio de una era donde el "leaking" se convierte en la única forma de auditoría institucional efectiva?

Tengamos claro que minimizar un ataque diciendo que **"solo afectó 5 sistemas"** cuando el directorio central de usuarios (LDAP) ha sido comprometido, genera una brecha de confianza. La transparencia es vital para que los usuarios (alumnos y maestros) puedan protegerse a tiempo.

---

## Takeaways
Como nota a futuro, en caso de gestionar estructuras similares, me llevo de aprendizaje ajeno tres tareas que sí o sí deben ejecutarse (llueva, truene o relampaguee):
* **Nunca, bajo ninguna circunstancia** dejar llaves SSH o API keys en directorios accesibles o embebidas en código.
* **La segmentación de red** debe ser meticulosa pues un servidor web no debería dar acceso directo al balanceador de carga o al LDAP.
* **Monitoreo de Endpoints:** El ataque duró 18 horas antes de ser contenido, lo que nos deja ver que hace falta más seriedad en el tema de la ciberseguridad.

**¿Crees que este ataque obligará a una reestructuración real en temas de ciberseguridad en México?**

**Día 03/365**