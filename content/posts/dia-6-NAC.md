+++
title: "Más allá del Firewall: ¿Qué es el NAC y por qué tu red lo necesita?"
date: 2026-01-10T21:26:00-05:00
draft: false
tags: ["NAC", "Seguridad Perimetral", "Zero Trust", "Networking"]
+++

Ayer hablamos sobre los **firewalls** y cómo actúan como el muro de seguridad de nuestra red. Sin embargo, en un mundo donde el teletrabajo, los dispositivos móviles (BYOD, de las siglas Bring Your Own Device) y el IoT (Internet of Things) son la norma, el muro ya no es suficiente. Necesitamos un "portero" inteligente.

Ahí es donde entra el **NAC (Network Access Control)**.

## ¿Qué es exactamente el NAC?

El Control de Acceso a la Red es una solución de seguridad que permite o deniega el acceso a los recursos de una red basándose en políticas de cumplimiento. 

Si el firewall es la puerta de seguridad de un edificio, el **NAC es el sistema de acreditación** que comprueba no solo quién eres, sino si vienes "limpio" y si tienes permiso para estar en la oficina 4 o solo en el lobby.

## Las 3 funciones clave de un sistema NAC

Para entender cómo funciona, podemos dividir sus tareas en tres pilares:

1.  **Identificación:** ¿Quién intenta conectarse? (Usuario, cámara IP, impresora, laptop de la empresa).
2.  **Autenticación y Autorización:** ¿Es quien dice ser? Si es así, ¿a qué partes de la red puede acceder?
3.  **Evaluación de Postura (Compliance):** Esta es la más importante. El NAC revisa si el dispositivo tiene el antivirus actualizado, el sistema operativo al día y si no tiene vulnerabilidades críticas antes de dejarlo entrar.

---

## ¿Por qué no basta con el Firewall?

Imaginemos que una persona lleva su laptop personal a la oficina, la cual está infectada con un malware. Al conectarla directamente al Wi-Fi o a un puerto Ethernet de la oficina, el firewall no podrá hacer mucho, porque la amenaza ya está **dentro** del perímetro.

Un **NAC** detectaría que esa laptop no cumple con las políticas de seguridad y:
* **La pondría en cuarentena** (en una VLAN aislada).
* **Le denegaría el acceso** hasta que se limpie el equipo.
* **Notificaría al equipo de IT.**

## Beneficios principales

* **Visibilidad total:** Sabes exactamente qué dispositivos hay en tu red en tiempo real.
* **Control de Invitados:** Crea accesos temporales y limitados para visitas de forma automática.
* **Seguridad para IoT:** Dispositivos como cámaras o sensores suelen ser inseguros; el NAC los mantiene aislados de los servidores críticos.
* **Filosofía Zero Trust:** No se confía en nadie por defecto, cada conexión debe validarse.

## Conclusión

Implementar un NAC es pasar de una seguridad reactiva a una **seguridad proactiva**. En la era de la movilidad, no podemos controlar qué dispositivos intentarán tocar nuestra red, pero sí podemos controlar bajo qué condiciones les permitimos el paso.

---

En próximas entradas veré la posibilidad de dejar de manera práctica todo lo anterior para poderlo representar de una manera gráfica.

**Día 6/365**