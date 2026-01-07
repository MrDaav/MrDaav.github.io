---
title: "Día 2: Los Pilares de la Ciberseguridad (Análisis NSE 1 - Módulo 1)"
date: 2026-01-06T23:00:00-06:00
draft: false
tags: ["Fortinet", "NSE1", "Fundamentos", "Estrategia"]
---

## Módulo 1: Taxonomía de la Defensa

Hoy inicié un análisis profundo del **NSE 1 de Fortinet** a fin de traer contenido al blog y poder compartir un poco del contenido que aprendo, comenzando por el Módulo 1. A diferencia de otras introducciones teóricas, Fortinet clasifica la ciberseguridad en categorías críticas que debemos entender para diseñar una arquitectura de defensa coherente.

### 1. Las 5 Categorías Técnicas de la Ciberseguridad

En este módulo, desglosamos el campo de batalla en cinco frentes principales:

* **Critical Infrastructure Security:** Sistemas que mantienen operativa a la sociedad (energía, agua, salud). Aquí el riesgo no es solo pérdida de datos, sino impacto en la vida real, a este frente en específico se le suele conocer como OT (Operational Technology).
* **Network Security:** El enfoque tradicional de proteger el flujo de datos. Fortinet destaca que ya no basta con un firewall; se requiere visibilidad interna.
* **Cloud Security:** Seguridad en entornos compartidos entendiendo que la responsabilidad compartida es el concepto clave.
* **Application Security (AppSec):** Proteger el software desde su desarrollo. Con el auge de las APIs, este punto se ha vuelto crítico para prevenir fugas de datos masivas.
* **IoT Security:** La explosión de dispositivos "tontos" conectados, estos representan la superficie de ataque más grande y menos gestionada en la actualidad.

### 2. El Pegamento: People and Processes

Lo más valioso de este módulo es que reconoce que la tecnología sola no sirve de nada. La ciberseguridad es un compendio de:

1.  **People (Personas):** La concientización es nuestra primera línea de defensa.
2.  **Processes (Procesos):** Los marcos de trabajo que dictan cómo responder ante un incidente.

### 3. Principios de Seguridad de la Información

Conocido como la tríada CIA, por sus siglas en inglés (Confidentiality, Integrity and Availability), estos conforman la seguridad tripartita de los datos:

1.  **Confidenciality:** Asegurar que los datos solo sean accesibles por personal autorizado, siendo protegido en su mayoría por el control de identidades.
2.  **Integridad:** Garantizar que la información no haya sido alterada, lo que es crucial para la confianza en sistemas financieros, jurídicos o de salud.
3.  **Disponibilidad:** Asegurar que los sistemas y datos estén listos cuando el usuario los necesite, por poner un ejemplo, un ataque de Ransomware ataca directamente este pilar.

A su vez, aprendí acerca de su gemelo malvado, la tríada DAD (Discloure, Alteration and Denial):

1. **Disclosure:** Esto ocurre cuando datos sensibles o privados son expuestos a personas o entidades no autorizadas.
2. **Alteration:** Sucede cuando la información es modificada de manera no autorizada, perdiendo así su veracidad.
3. **Denial:** Pudiéndose conocer como "destruction", se refiere a la pérdida de acceso a los datos o a la elimincación física o lógica de los mismos.

## Reflexión del Día
Ver cómo Fortinet integra estas categorías bajo una visión de negocio me ayuda a entender por qué el **Security Fabric** es tan relevante. No protegemos "computadoras", protegemos infraestructuras críticas y procesos de negocio.

---
**Progreso del reto:** 2/365 