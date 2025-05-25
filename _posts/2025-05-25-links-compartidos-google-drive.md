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

Este post no trata un problema de ciberseguridad, pero sí que resuelve fácilmente un problema que podéis tener cuando hay varias cuentas de Google configuradas en el navegador.

Para que sea más claro el ejemplo, vamos a ponerle estos nombres a las cuentas: 
- Cuenta principal de Google
- Segunda cuenta de Google
- Tercera cuenta de Google

El problema en cuestión viene cuando nos han enviado un link de un contenido compartido:

Ejemplo: 
https://drive.google.com/drive/folders/<carpeta_compartida>

Si queremos abrirlo con nuestra "Segunda cuenta de Google", lo fácil y evidente, es seleccionar esta cuenta en Google Drive y hacer clic en el link del contenido compartido... pues no. En vez de abrirse con la cuenta que queremos, se abre con la cuenta principal, y da igual las vueltas que le des.

Llegado a este punto, como no quería complicarme demasiado la existencia y quería darle una solución rápida para poder centrarme en lo que realmente quería hacer, le he preguntado a ChatGPT, pero ninguna de las soluciones que me ha dado la veía práctica ni interesante (las dejo más abajo)

Al final, he tenido que encontrar la solución por mi cuenta, observando las diferencias en las URL y llegando a esta conclusión:

Cuando tenemos varias cuentas configuradas, la URL muestra el número de cuenta a utilizar indicando /u/<número_de_cuenta>. Para obtenerlo, símplemente tenéis que acceder con la cuenta que queráis utilizar y fijaros qué número tiene:

Ejemplo:
- https://drive.google.com/drive/u/0/home  <-- Cuenta principal de Google
- https://drive.google.com/drive/u/1/home  <-- Segunda cuenta de Google
- https://drive.google.com/drive/u/2/home  <-- Tercera cuenta de Google

Este dato no está indicado en el link del contenido compartido, con lo que Google Drive asume que debe utilizar la "Cuenta principal de Google", sin importarle la que tuviésemos seleccionada.

Recordemos el link original: 
https://drive.google.com/drive/folders/<carpeta_compartida>

Para que este link se abra con nuestra "Segunda cuenta de Google", tendremos que indicarle que debe usar esa cuenta añadiendo el texto /u/1 a la URL, quedando de esta forma:
https://drive.google.com/drive/u/1/folders/<carpeta_compartida>

Como véis, la solución es bastante sencilla, y no es necesario tener que cambiar de navegadores ni hay que hacer cosas demasiado extrañas.

Espero que este artículo os haya servido de ayuda.

Aquí os dejo mi conversación con ChatGPT:


![2025-05-25_10-39 ChatGPT1 screenshot](/posts/2025/05/25/2025-05-25_10-39 ChatGPT 1.png)
![2025-05-25_10-39 ChatGPT2 screenshot](/posts/2025/05/25/2025-05-25_10-39 ChatGPT 2.png)



[
En google drive tengo configuradas varias cuentas, selecciono la que me interesa utilizar en este momento, pero al hacer clic en un link que me han pasado con contenido compartido lo abre con otra de las cuentas que tengo, no con la que he seleccionado, ¿por qué? ¿cómo puedo abrirlo con la cuenta que me interesa?
]: #

```
Este es un problema bastante común cuando se tienen varias cuentas de Google abiertas simultáneamente en el mismo navegador. Google utiliza una cuenta como "principal" o "predeterminada", y los enlaces que abres (como los de Google Drive) generalmente se abren con esa cuenta principal, no necesariamente con la que estás usando activamente en otra pestaña.

¿Por qué sucede esto?
Cuando haces clic en un enlace a un archivo compartido en Google Drive:

Google intenta abrirlo con la primera cuenta con la que iniciaste sesión en ese navegador.

Incluso si seleccionas otra cuenta después, esa selección sólo aplica a esa pestaña o sesión, no a cómo se abren nuevos enlaces.

¿Cómo abrir el enlace con la cuenta correcta?
✅ Opción 1: Copiar y pegar el enlace en una ventana del navegador donde ya estés usando la cuenta correcta
Abre una pestaña nueva en tu navegador.

Ve a https://drive.google.com y cambia a la cuenta con la que quieres ver el contenido (si aún no estás en ella).

Una vez que estás en Drive con la cuenta correcta, pega el enlace que te pasaron en la barra de direcciones.

✅ Opción 2: Usar una ventana de incógnito
Abre una ventana en modo incógnito (Ctrl + Shift + N en Chrome).

Pega el enlace allí.

Inicia sesión con la cuenta de Google que debe tener acceso.

✅ Opción 3: Cambiar la cuenta predeterminada (opcional, más técnico)
Cierra sesión en todas tus cuentas de Google.

Vuelve a iniciar sesión primero con la cuenta que quieras que sea la predeterminada.

Luego inicia sesión en las otras cuentas que necesites.

Ahora, los enlaces se abrirán por defecto con esta cuenta.
```
