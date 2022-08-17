---
title: Laboratorio para pentesting (1)
author: HardeningBen
date: 2022-08-17 19:00:00
categories: [Laboratorio,Docker]
tags: [Maquina virtual,Docker,VirtualBox,Ubuntu Server]
math: true
mermaid: true
---

Las prácticas de pentesting **NO DEBEMOS** realizarlas en páginas reales en producción, sobre todo si no somos propietarios de ellas ni tenemos permiso de los propietarios. Otra cuestión sería que nos hayan contratado para una auditoría, en cuyo caso habría que ceñirse a lo acordado con el cliente.

Para poder realizar prácticas de pentesting debemos utilizar un entorno seguro, y para ello vamos a crear nuestro propio laboratorio. Como es una tarea un tanto entretenida, he decidido crear varios posts para que queden más claros todos los pasos.

En esta primera parte vamos a crear una nueva máquina virtual con VirtualBox para luego instalar en ella la distribución de linux Ubuntu Server en su versión LTS (Long Term Support).

Vamos a necesitar lo siguiente:
- VirtualBox [(download)](https://www.virtualbox.org/wiki/Downloads)
- Linux Ubuntu Server LTS [(download)](https://ubuntu.com/download/server)

<br>
Aquí puedes ver el video con los pasos que debes seguir para instalar Ubuntu Server en una nueva máquina virtual:
<iframe width="560" height="315" src="https://www.youtube.com/embed/nWbQPikt0WE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

