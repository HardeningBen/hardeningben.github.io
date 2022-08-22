---
title: Laboratorio para pentesting (parte 2)
author: HardeningBen
date: 2022-08-18 19:00:00
categories: [Laboratorio,Docker]
tags: [Maquina virtual,VirtualBox,Ubuntu Server,Docker,Docker Engine,Docker Compose]
math: true
mermaid: true
---

En la primera parte empezamos a preparar nuestro laboratorio instalando linux en la máquina virtual *ubuntu-docker-labs*.

En esta segunda parte vamos a instalar *Docker* (Docker Engine + Docker Compose), para poder crear los contenedores que almacenarán las distintas apliaciones de nuestro laboratorio, es decir, las aplicaciones con las que haremos nuestras prácticas de pentesting.

Si no conoces lo que son los contenedores, o si no los has utilizado nunca, se podría decir que son algo similar a las máquinas virtuales, con la diferencia que una máquina virtual alberga un sistema totalmente independiente, y un contenedor depende del sistema operativo base donde se ejecuta el gestor de contenedores (en nuestro caso Docker). ¿Y qué tiene de bueno usar un contenedor? Pues que, para ejecutarse, requiere menos recursos que una máquina virtual, con lo que hace que lanzar y ejecutar una aplicación será más rápido. Si quieres indagar más en las diferencias, échale una ojeada a esta web: [Diferencia entre Contenedores y Máquinas Virtuales](https://www.linkedin.com/pulse/cu%C3%A1l-es-la-diferencia-entre-contenedores-/)

Volviendo a la instalación, vamos a necesitar lo siguiente:
- Docker Engine [(doc)](https://docs.docker.com/engine/install/ubuntu/)
- Docker Compose [(doc)](https://docs.docker.com/compose/install/compose-plugin/#install-using-the-repository)

<br>
Aquí puedes ver el video con los pasos que debes seguir para instalar Docker en la máquina virtual *ubuntu-docker-labs*:  
[![Screenshot Docker](/posts/2022/08/18/02_screenshot.png)](https://youtu.be/EJ0gfUObguo "Video: Instalar Docker"){:target="_blank"}

Aunque este no es un paso necesario para la instalación del laboratorio, sí que considero recomendable que hagamos una instantánea de nuestra máquina virtual, por si en algún momento queremos volver a este estado, no tener que reinstalar todo desde cero:  
[![Screenshot Instantánea](/posts/2022/08/18/03_screenshot.png)](https://youtu.be/Xot_lVLsb9M "Video: Crear instantánea"){:target="_blank"}
