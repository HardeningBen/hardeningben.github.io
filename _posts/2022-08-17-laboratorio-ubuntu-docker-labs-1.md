---
title: Laboratorio para pentesting (parte 1)
author: HardeningBen
date: 2022-08-17 19:00:00
categories: [Laboratorio,Docker]
tags: [Maquina virtual,VirtualBox,Ubuntu Server,Docker]
math: true
mermaid: true
---

Las prácticas de pentesting **NO DEBEMOS** realizarlas en páginas reales en producción, sobre todo si no somos propietarios de ellas ni tenemos permiso de los propietarios. Otra cuestión sería que nos hayan contratado para una auditoría, en cuyo caso habría que ceñirse a lo acordado con el cliente.

Para poder realizar prácticas de pentesting debemos utilizar un entorno seguro, y para ello vamos a crear nuestro propio laboratorio. Como es una tarea un tanto entretenida, he decidido crear varios posts para que queden más claros todos los pasos.

En esta primera parte vamos a crear la máquina virtual *ubuntu-docker-labs* con VirtualBox para luego instalar en ella la distribución de linux Ubuntu Server en su versión LTS (Long Term Support).

Vamos a necesitar lo siguiente:
- VirtualBox [(download)](https://www.virtualbox.org/wiki/Downloads)
- Linux Ubuntu Server LTS [(download)](https://ubuntu.com/download/server)

<br>
Aquí puedes ver el video con los pasos que debes seguir para instalar Ubuntu Server en una nueva máquina virtual:  
[![Screenshot Máquina Virtual](/posts/2022/08/17/01_screenshot.png)](https://youtu.be/7tA2XWAObEg "Video: Crear máquina virtual con Ubuntu Server"){:target="_blank"}

