---
title: Laboratorio para pentesting
author: HardeningBen
date: 2022-08-20 19:00:00
categories: [Laboratorio,Docker]
tags: [Maquina virtual,VirtualBox,Ubuntu Server,Docker,Docker Engine,Docker Compose,DVWA,Juice Shop,WebGoat,WebWolf]
math: true
mermaid: true
hidden: false
---

En el post de hoy vamos a crear un laboratorio de pentesting con el que podremos aprender diversas técnicas de hacking utilizando un entorno seguro. Para ello vamos a crear la máquina virtual *ubuntu-docker-labs* con VirtualBox e instalaremos en ella una distribución linux Ubuntu Server y varias aplicaciones web (todas ellas vulnerables), mediante la utilización de contenedores Docker.  

Por si se hubiese pasado por alto, quiero recalcar lo de **utilizando un entorno seguro**, ya que las prácticas de pentesting **NO DEBEMOS** realizarlas en páginas reales en producción, sobre todo si no somos propietarios de ellas ni tenemos permiso de los propietarios. Otra cuestión sería que nos hayan contratado para una auditoría, en cuyo caso habría que ceñirse a lo acordado con el cliente.  

Este proyecto tiene como finalidad aprender algunas de las técnicas que utilizan los malos (los ciberdelincuentes), conocer las vulnerabilidades más habituales y así, cuando hagamos una auditoría en un entorno real, poder detectar y corregir los posibles fallos de seguridad que encontremos en las aplicaciones web analizadas.  

Para hacer el proceso más sencillo, he decidido dividir el contenido en tres partes:

- [Parte 1: Creación de la máquina virtual e instalación de Ubuntu Server](../laboratorio-ubuntu-docker-labs-1)
- [Parte 2: Instalación de Docker](../laboratorio-ubuntu-docker-labs-2)
- [Parte 3: Instalación de aplicaciones web vulnerables](../laboratorio-ubuntu-docker-labs-3)

