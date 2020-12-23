---
id: 120
title: Como usar DOCKER en un proyecto de DJANGO
date: 2020-02-20
author: robert
layout: post
permalink: /como-usar-docker-y-django/
categories:
- Django
- Python
- Backend
- Docker
- DockerCompose
tags:
- python
- archivos
- produccion
- docker
- devops
- deploy
---
Hola y bienvenidos a este nuevo artículo. Una de las herramientas que más auge ha tenido en los últimos años ha sido **DOCKER y todo su ecosistema**. Nos ha venido a ayudar y hacer más fácil  las tareas despliegue y desarrollo de nuestras aplicaciones.
<!--more-->
## INTRODUCCION
Para los que no sepan que es DOCKER acá les dejo el enlace donde se explica con más detalles pero en resumen es **poder ejecutar dentro de un contenedor(mini máquina virtual) solo nuestro proyecto de DJANGO y sus dependencias**.

 Si, suena raro pero es en realidad bastante simple. Actualmente la mayoría de los ambientes de desarrollo y producción de DJANGO, es una carpeta con todo el código del proyecto, un servidor MYSQL y un virtualenviroment, todo esto en la misma computadora o servidor. Acá puedes ver como hacer una [instalación de DJANGO tradicional](https://www.youtube.com/watch?v=TqSSOhfRzTU).

 Si tenemos un problema en nuestro servidor de bases de datos y tenemos más proyectos en el mismo servidor, todos fallan.

 Los mismo con un proyecto de DJANGO, todos depende de NGINX o APACHE dado que comparten el los mismos recursos del sistemas.

 Docker nos viene a ayudar dando la opción aislar o contener cada proyecto, herramienta (REDIS, RABBITMQ)o servidor de MYSQL en una mini máquina virtual dentro de nuestro servidor, como muestra la imágen.

<img src="/assets/img/posts/dockerex.png" alt="Arquitectura Docker" title="Arquitectura DOCKER" style="width:40%;margin:0 auto; display:block">

En la imagen cada **CONTAINER es independiente de los demás** aunque se ejecutan sobre el mismo KERNEL de sistema.

Si ocurre un error en el **CONTAINER de PHP los demás no se ven afectados**.

## CONFIGURANDO DOCKER
1- En nuestro proyecto de DJANGO creamos en la raíz un archivo llamado DOCKERFILE

<img src="/assets/img/posts/dockerfile.png" alt="Docker con DJANGO" title="Docker con DJANGO" style="width:60%;margin:0 auto; display:block">

2- Agregamos las siguientes líneas para tener las indicaciones de que hará nuestro contenedor.
```
FROM python:3.8  ***Version de python a usar***
ENV PYTHONBUFFERED 1 ***Variable de entorno que necesitarás si haces deploy ***
WORKDIR /app -- Directorio dentro de nuestro contenedor donde estará el código de la aplicación 

COPY requirements.txt /app/requirements.txt  ** Copiar el requirements local y pasarlo al contendor***

RUN pip3 install -r requirements.txt ***Ejecutar el pip para instalar nuestras dependencias***
COPY . /app   ***Copiar todo nuestro código (.) al directorio /app dentro del contenedor ***

CMD python3 manage.py runserver 0.0.0.0:8000 *** Ejecutar el comando para correr el proyecto en el contenedor***
```

3 - **Crear un fichero docker-compose.yml** en la raíz del proyecto:
Docker compose nos va a ayudar a gestionar varios contenedores y a configurar y ejecutar de manera mas sencilla los mismos.

<img src="/assets/img/posts/docker-compose.png" alt="DockerCompose con Django " title="DockerCompose con Django" style="width:60%;margin:0 auto; display:block">

```
version: '3.8'
services: *** Por cada herramienta o aplicación debemos tener un servicio declarado ***
  backend:
    build:
      context: .
      dockerfile: Dockerfile ***Nuestro dockerfile creado anteriormente *** 
    ports:
      - 8000:8000 ***  puerto local del servidor : puerto interno del contenedor docker ***
    volumes:
      - .:/app
    depends_on:
      - db  *** Necesitamos que se ejecute el sevicio de BD antes de ejecutar el django ***
  db:
    image: mysql:5.7.22 *** Versión de mysql ****
    restart: always
    environment:
      MYSQL_DATABASE: admin
      MYSQL_USER: root
      MYSQL_PASSWORD: root
      MYSQL_ROOT_PASSWORD: root
    volumes:
      - .dbdata:/var/lib/mysql  *** montamos todo lo que hay en /var/lib/mysql a nuestro contenedor
    ports:
      - 33066:3306  *** puerto local en le sevidor : puerto interno de docker.

```

Después de tener estos archivos configurados solamente debemos ejecutar :
```
sudo docker-compose up
```

Y debemos tener nuestro proyecto listo en localhost:8000

Para correr un comando dentro de uno de los contenedores :
```
sudo docker-compose exec backend sh
```
Donde BACKEND es el nombre del servicio que creamos en el compose.yml.

**Como dato interesante el contenedor debe estarse ejecutando para poder acceder a él**

Espero les sirva y ayude a entrar en el mundo de DOCKER y todas sus ventajas.

No dudes en contactarme si tienes alguna duda o problema.



