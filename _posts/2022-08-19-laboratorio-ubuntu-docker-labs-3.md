---
title: Laboratorio para pentesting (parte 3)
author: HardeningBen
date: 2022-08-19 19:00:00
categories: [Laboratorio,Docker]
tags: [Maquina virtual,VirtualBox,Ubuntu Server,Docker,Docker Engine,Docker Compose,DVWA,Juice Shop,WebGoat,WebWolf]
math: true
mermaid: true
---

En la segunda parte instalamos *Docker* en nuestra máquina virtual *ubuntu-docker-labs* para crear los contenedores con las aplicaciones de nuestro laboratorio.

En esta tercera parte vamos a instalar por fin las aplicaciones con las que podremos practicar y formarnos en pentesting. Para ello vamos a crear cuatro contenedores de *Docker*, uno para cada una de las aplicaciones web:
- DVWA (Damn Vulnerable Web Application) [(github)](https://github.com/digininja/DVWA)
- Juice Shop [(github)](https://github.com/juice-shop/juice-shop)
- WebGoat 7 [(github)](https://github.com/WebGoat/WebGoat/tree/7.1)
- WebGoat 8 [(github)](https://github.com/WebGoat/WebGoat) + WebWolf 

Vamos a necesitar lo siguiente:
- Archivos docker-compose.yml
- docker-compose

<br>
Instalación de DVWA (Damn Vulnerable Web Application):  
[![Screenshot DVWA](/posts/2022/08/19/04_screenshot.png)](https://youtu.be/Ub6xbiD8NLs "Video: Instalar DVWA"){:target="_blank"}

Instalación de Juice Shop:  
[![Screenshot Juice Shop](/posts/2022/08/19/05_screenshot.png)](https://youtu.be/OrkdpeGOYFc "Video: Instalar Juice Shop"){:target="_blank"}

Instalación de WebGoat 7:  
[![Screenshot WebGoat7](/posts/2022/08/19/06_screenshot.png)](https://youtu.be/Mymscp5d8Jg "Video: Instalar WebGoat 7"){:target="_blank"}

Instalación de WebGoat 8 + WebWolf:  
[![Screenshot WebGoat7](/posts/2022/08/19/07_screenshot.png)](https://youtu.be/SLmZjUeO6e4 "Video: Instalar WebGoat 8 + WebWolf"){:target="_blank"}

Aunque este no es un paso necesario para la instalación del laboratorio, sí que considero recomendable que hagamos una instantánea de nuestra máquina virtual, por si en algún momento queremos volver a este estado, no tener que reinstalar todo desde cero. El proceso de creación de la instantánea es el mismo que el utilizado en la segunda parte con la diferencia que en este caso, por un despiste, no la he creado con la máquina parada:  
[![Screenshot Instantánea](/posts/2022/08/19/08_screenshot.png)](https://youtu.be/NxSzCGcLec8 "Video: Crear instantánea"){:target="_blank"}
