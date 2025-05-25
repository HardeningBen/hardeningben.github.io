---
title: Abrir link compartido de Google Drive teniendo varias cuentas
author: HardeningBen
date: 2025-05-25 10:26:00
categories: [Varios,Google Drive]
tags: [Problemas, Google Drive]
math: true
mermaid: true
hidden: false
---

En este post vamos a resolver un problema que, aunque no está relacionado con la ciberseguridad, me parece interesante al haberme sucedido en varias ocasiones.

El problema en cuestión es que, al abrir un link de contenido compartido de Google Drive teniendo varias cuentas de Google configuradas, el navegador decide abrirla siempre con la cuenta principal, no con la que tenemos seleccionada y estamos usando en ese momento.

Para que sea más claro el ejemplo, vamos a ponerle estos nombres a las cuentas: 
- Cuenta principal de Google
- Segunda cuenta de Google
- Tercera cuenta de Google

Pongamos que alguien nos envía este link de una carpeta compartida de Google Drive:
>https://drive.google.com/drive/folders/\<carpeta_compartida\>

Si queremos abrirlo con nuestra "Segunda cuenta de Google", lo fácil y evidente sería seleccionar esta cuenta en Google Drive y hacer clic en el link del contenido compartido, ¿verdad?... pues no. En vez de abrirse con la cuenta que queremos, el navegador decide que lo va a abrir con la cuenta principal, y da igual las vueltas que le des.

En otras ocasiones me era indiferente utilizar una cuenta u otra, pero en este caso sí que necesitaba abrirlo con otra cuenta distinta a la principal, así que, tras un par de intentos fallidos, y como no quería complicarme demasiado para no demorar lo que realmente tenía que hacer, le he preguntado a ChatGPT... y ninguna de las soluciones que me ha dado la he visto ni práctica ni interesante (las dejo más abajo).

Al final, he encontrado la solución por mi cuenta, observando las diferencias en las URL y llegando a esta conclusión:

Cuando tenemos varias cuentas configuradas, la URL muestra el número de cuenta a utilizar indicando **/u/\<número_de_cuenta\>**. Para obtenerlo, símplemente hay que acceder a la cuenta que vas a utilizar y fijarte qué número tiene:

>- https://drive.google.com/drive**/u/0/**home  _< -- -- Cuenta principal de Google_
>- https://drive.google.com/drive**/u/1/**home  _< -- -- Segunda cuenta de Google_
>- https://drive.google.com/drive**/u/2/**home  _< -- -- Tercera cuenta de Google_

Si te fijas, este dato no está indicado en el link del contenido compartido, con lo que Google Drive asume que debe utilizar la "Cuenta principal de Google", sin importarle la que tenemos seleccionada.
>https://drive.google.com/drive/folders/\<carpeta_compartida\>

Para que este link se abra con nuestra "Segunda cuenta de Google", tenemos que indicar que debe usar esa cuenta, añadiendo el texto **/u/1** a la URL y quedando de esta forma:
>https://drive.google.com/drive**/u/1/**folders/\<carpeta_compartida\>

Como ves, la solución es bastante sencilla, y no es necesario tener que cambiar de navegadores ni hacer cosas demasiado extrañas.

Espero que este artículo te haya servido de ayuda.

Aquí te dejo mi conversación con ChatGPT, por si tienes curiosidad:

![2025-05-25_10-39 ChatGPT1 screenshot](/posts/2025/05/25/2025-05-25_10-39 ChatGPT 1.png)
![2025-05-25_10-40 ChatGPT2 screenshot](/posts/2025/05/25/2025-05-25_10-40 ChatGPT 2.png)

