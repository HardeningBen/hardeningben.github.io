---
title: Problema de conexión con HackTheBox
author: HardeningBen
date: 2022-07-18 19:00:00
categories: [HackTheBox]
tags: [Problemas,Conexion]
math: true
mermaid: true
---


Como sabes, para utilizar la plataforma HackTheBox se requieren 3 cosas:

1. Una cuenta de usuario
2. Una conexión a su VPN
3. Lanzar la máquina que deseemos resolver

Desde que he empezado a utilizar HackTheBox no he tenido ningún problema, o al menos no con los puntos 1 y 2:
- Respecto al usuario no hay mucho que decir. Una vez creado no debería haber ningún problema para conectar con él.

- La VPN: el único problema que tuve es que no ejecuté OpenVPN con permisos de superusuario, pero una vez ejecutado así, no ha habido nada que destacar.

- En cuanto a lanzar la máquina a resolver... Con las máquinas máquinas Tier 0 y Tier 1 del Starting Point no tuve ningún problema, pero sí con la máquina *Archtype* del Starting Point Tier 2. En este caso sí conectaba a la VPN, pero lanzar la máquina ha sido algo más complicado. Aunque creaba la instancia no conseguía establecer la conexión, se quedaba pensando durante demasiado tiempo y al final no le daba una ip a la máquina, con lo que no podía empezar a hacer nada con ella:

![no-connect screenshot](/posts/2022/07/18/no-connect.png)

Para intentar buscar una solución a este problema he seguido estos pasos:
1. Verificar la conexión VPN. Compruebo que la conexión está establecida correctamente, mostrando el mensaje "2022-07-18 13:09:42 Initialization Sequence Completed"

2. Reiniciar la conexión VPN. Aún estando conectada correctamente, creo que puede haber algún problema en la conexión, así que desconecto y vuelvo a lanzar la conexión VPN con HackTheBox, pero el problema persiste y la máquina sigue sin obtener ip.

3. Pruebo a utilizar otro protocolo/servidor. Normalmente conecto a la VPN con el protocolo TCP del servidor europeo, salvo que de problemas y pruebe con UDP, que en alguna ocasión me ha servido para salir del paso. Sin embargo, en esta ocasión no ha funcionado ni con un protocolo ni con el otro, así que he probado a utlizar el servidor estadounidense, para ver si es que había algún problema con el servidor de Europa y, con este cambio, sí me ha permitido desplegar bien la máquina y seguir practicando.

Espero que esta solución pueda serviros de utilidad. Tal vez sea algo simple, pero cuando la gente está empezando, toda ayuda es buena, y más si te permite continuar avanzando y no quedarte bloqueado.

Un saludo

