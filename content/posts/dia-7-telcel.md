+++
title = 'Crónica de un desastre anunciado'
date = '2026-01-11T22:33:29-06:00'
draft = false
tags = ["Ciberseguridad", "Inseguridad", "Reforma", "México"]
+++

El arranque del nuevo registro obligatorio de telefonía móvil en México ha dejado una lección dolorosa sobre seguridad, confianza y la responsabilidad de manejar datos sensibles a escala nacional. Lo que debía ser una medida de seguridad pública se convirtió, en menos de 24 horas, en una de las mayores exposiciones de datos personales en la historia reciente del país.

### Lo que pasó...

La falla no fue un ataque sofisticado de día cero, sino una vulnerabilidad crítica de lógica en la implementación del portal de registro de **Telcel**. Según documentó el periodista Ignacio Gómez Villaseñor, el sistema presentaba un fallo de seguridad básico:

* **Falta de autorización en el lado del servidor:** Aunque la interfaz visual solicitaba un código SMS para "autenticar" al usuario, el backend devolvía la información completa (Nombre, RFC, CURP, Fecha de nacimiento y Correo) antes de validar dicho código.
* **Exposición de datos vía API:** Bastaba con ingresar un número telefónico para que el sistema entregara un JSON con los datos personales del titular.
* **Riesgo de automatización:** Como bien señalaron los expertos, esta vulnerabilidad permitía que un script simple (bot) pudiera "scrapear" millones de registros de forma sistemática, creando la base de datos de extorsión más potente de México.

### El costo de la desconfianza

Aunque Telcel ha parchado el agujero (ahora devolviendo valores nulos en los campos sensibles si no hay autenticación), la pregunta técnica y ética permanece: **¿Cuántos datos fueron extraídos mientras la puerta estuvo abierta?** No hay logs que reparen la privacidad perdida.

Como desarrolladores, este evento nos recuerda que:
1. La seguridad no es una capa que se añade al final; debe estar en el núcleo de la arquitectura.
2. Crear bases de datos masivas centralizadas crea un "punto único de falla" con consecuencias catastróficas.
3. Una vez que la empresa de telecomunicaciones más grande del país falla en proteger lo más básico, el usuario pierde cualquier incentivo para colaborar con políticas públicas de identidad.

### Conclusión

Este episodio demuestra que sin una infraestructura sólida y procesos de auditoría rigurosos, las políticas de seguridad digital en México seguirán siendo un riesgo para el ciudadano en lugar de una protección.

> "No necesitas ser un hacker para ver datos personales. Esto es extremadamente peligroso." 

---
**Día 7/365**