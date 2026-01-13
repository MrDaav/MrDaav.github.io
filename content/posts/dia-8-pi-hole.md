+++
title = 'Pi Hole'
date = '2026-01-12T22:43:36-06:00'
draft = false
tags = ["DNS", "Redes", "AdBlocker"]
+++

Cualquiera que pase más de 8 horas al día frente a una pantalla sabe que la web moderna es, en gran medida, un campo de batalla por nuestra atención y nuestros datos. Entre anuncios invasivos, telemetría innecesaria de dispositivos "inteligentes" y rastreadores que nos siguen por cada rincón de internet, la experiencia de navegación se ha vuelto pesada y ruidosa.

Aquí es donde entra **Pi-hole**.

### ¿Qué es exactamente un Pi-hole?

A menudo descrito como un "agujero negro" para la publicidad, Pi-hole es un sumidero de DNS (*DNS sinkhole*) que protege todos los dispositivos de tu red sin necesidad de instalar software individual en cada uno.

A diferencia de un bloqueador de anuncios en el navegador (como uBlock Origin o AdBlocker), Pi-hole funciona a nivel de red. Si un dispositivo (ya sea tu laptop, tu smart TV o incluso tu refrigerador inteligente) intenta conectarse a un dominio conocido por servir anuncios o rastreadores, Pi-hole intercepta la solicitud y responde con una dirección vacía. El anuncio nunca se descarga, el rastreo se detiene y tu ancho de banda te lo agradece.

### ¿Por qué deberías tener uno?

Como desarrolladores o entusiastas de la tecnología, las ventajas van más allá de no ver banners:

* **Privacidad total:** Bloquea la telemetría que Windows, Android o incluso las Smart TVs envían constantemente a sus servidores.
* **Mejora de rendimiento:** Al no cargar scripts de rastreo ni imágenes publicitarias, las páginas cargan notablemente más rápido.
* **Control de red:** Te permite ver estadísticas en tiempo real de qué dominios están consultando tus dispositivos (y te sorprenderías de lo que descubres).
* **Bloqueo a nivel de app:** Es la única forma efectiva de bloquear anuncios en aplicaciones donde no puedes instalar extensiones (como apps de noticias o juegos móviles).

### El hardware no es una limitante

Aunque el nombre sugiere el uso de una **Raspberry Pi**, la realidad es que Pi-hole es extremadamente ligero. Se puede ejecutar en un contenedor de Docker, en una máquina virtual vieja, o incluso en un servidor en la nube si configuras un túnel seguro.

### Lo que viene...

Instalarlo es el primer paso para una red más limpia y segura. Sin embargo, hay un par de "trucos" de configuración y manejo de listas que marcan la diferencia entre una red protegida y una red rota.

---

**Mañana publicaré la guía técnica paso a paso:** para esto utilizaré una Raspberry que tengo abandonada desde hace tiempo, así que, ¡nos leemos mañana!

**Día 8/365**