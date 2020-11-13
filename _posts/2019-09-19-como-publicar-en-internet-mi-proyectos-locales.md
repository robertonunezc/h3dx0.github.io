---
id: 145
title: Como publicar en internet mis proyectos locales
date: 2019-09-19T02:45:30+00:00
author: robert
layout: post
permalink: /como-publicar-en-internet-mi-proyectos-locales/
categories:
- DevOps
- How To
tags:
- ngork
- backend
- devops
- deploy
---
Me pregunté en muchas ocaciones como podría desde mi localhost poder hacerlo visible en internet, para no tener que estar haciendo deploys que en muchos casos son complejos y nos hacen perder mucho tiempo y más cuando el proyecto está en pleno desarrollo.
 <!--more-->
He trabajado en proyectos donde necesito hacer demos para ir presentando los avances,o simplemente tener el proyecto disponible en Internet para que un amigo haga algunas pruebas. 

Después de varios intentos de configuraciones y no encontrar una vía fácil leí en un grupo de Telegram un solución 
muy cómoda a mi manera de ver.

## Solución  
Existe una herramienta llamada <a href="https://ngrok.com/"  target="_blank">NGROK</a>. Esta útil plataforma nos da la opción de 
facilmente poder publicar nuestro proyecto local en Internet y así evitarnos hacer despliegues en VPS, webhosting 
ahorrando muchísimo tiempo y frustración.

## Como funciona
1. Es tan sencillo como entrar a su sitio web <a href="https://ngrok.com/"  target="_blank">NGROK</a>.
2. Registrarnos para que nos de un API_KEY que nos permitirá publicar nuestro localhost. 
3. Descargar ngrok <a href="https://dashboard.ngrok.com/get-started" target="_blank">aquí</a>, está disponible para una amplia variedad de plataformas.
4. Una ves descargado, nos movemos a la carpeta descargada de ngrok y ejecutamos el comando 
```bash
$ ./ngrok authtoken NUESTRO_API_KEY
``` 
5. Suponiendo que tengamos un proyecto de nodejs que queremos probar en internet, el cual ejecutamos con :
```bash
$ npm run dev o node app.js
```
6. El siguiente paso es publicar en internet el puerto por el cual está corriendo nuestra aplicación. Esto lo podemos 
verificar en nuestra consola, ExpressJS por defecto sale en el 3000, Django Python en el 8000.
Ejecutamos
```bash
./ngrok http PUERTO 
```
Ejemplo concreto
```bash
./ngrok http 80
```
Esto nos genera una dirección temporal para probar nuestro servidor en internet.
![NGROK](/assets/img/posts/ngrok-howto.png)

Además de esta dirección en internet, nos permite monitorear los request, tiempos de ejecución todo esto
accediendo a la *http://localhost:4040/*

![NGROK](/assets/img/posts/ngrok-inspect.png)

Esto ha sido una breve introducción a esta gran herramienta, su sitio web tiene muchísima documentación que 
los ayudará con más detalle a descubrir todo su pontencial.

Espero les sea útil y cualquier comentario es bienvenido. 🙂

###### Las imágenes fueron tomadas del sitio oficial de NGROK