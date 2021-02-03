---
id: 120
title: Como instalar Strapi en Ubuntu
date: 2021-02-01T04:58:01+00:00
author: robert
layout: post
permalink: /como-instalar-strapi-a-Ubuntu/
categories:
  - Strapi
  - ApiRest
  - backend
  - Nodejs
---

Bienvenidos a este artículo donde aprenderemos **como instalar Strapi en Ubuntu**. Strapi es una herramienta increible que nos va a ayudar a **crear un ApiRest en cuestión de minutos** y con unos **pocos clicks**. Tendremos nuestros endpoints, un administrador de contenidos super útil listos para conectar con nuestro frontend en cuestión de minutos.
Para los que no lo conocen <a href="https://strapi.io/" target="_blank">Strapi</a> es uno de los **HEADLESSCMS** más utilizados actualmente.
<!--more-->
# Video
<iframe width="560" height="315" src="https://www.youtube.com/embed/gF-q5y70UEQ" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<br>

# Requisitios para instalar Strapi

1- Instalar NODEJS. En este <a href="https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-20-04">enlace</a> puedes ver como instalar NODEJ en Ubuntu.

2- Instalar npx. En este <a href="https://www.npmjs.com/package/npx" target="_blank"> enlace</a> puedes ver como completar esta tarea.

# Instalar Strapi
Después de tener los requisitos antes mensionados pasamos a instalar strapi.

```
npx create-strapi-app my-project --quickstart
```

Donde **my-project** sería el nombre que le quieras poner a tu proyecto.

Después de la instalación debemos tener en nuestra consola una imagen como la siguiente:

<img src="/assets/img/posts/strapi.png" alt="StrapiInstalar">

Podemos acceder al administrador de contenidos y permisos que nos da Strapi y crear nuestro usuario de administración.

Una vez creado el usuario de administración accedemos a crear nuestros enpoints, modelos y demás.

<img src="/assets/img/posts/strapiAdmin.png" alt="StrapiAdmin" width="100%">

En un siguiente artículo vamos a crear nuestros endpoints de forma rápida y visual haciendo uso de este administrador con solo unos clicks.

Happy coding. 🙂
