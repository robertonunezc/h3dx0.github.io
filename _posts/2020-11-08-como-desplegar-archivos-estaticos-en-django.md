---
id: 120
title: Como visualizar archivos estáticos en django cuando subimos a producción usando NGINX
date: 2020-02-20
author: robert
layout: post
permalink: /como-desplegar-archivos-estaticos-django/
categories:
- Django
- Python
- Backend
tags:
- python
- archivos
- produccion
---
Hola y bienvenidos a este rinconcito de internet donde comparto lo que voy aprendiendo en el día a día como desarrollador web.
Un problema bastante común que nos pasa a los desarrolladores cuando comenzamos a trabajar en Django,
<!--more-->
es que los archivos CSS y las
imágenes que subimos mediante formularios en nuestra aplicación, no los podemos visualizar.

En modo desarrollo casi siempre nos funciona todo de maravillas, con solo agregar unas pocas configuraciones podemos tener todo listo.
Aclarar que Django sabe cuando estamos en modo desarrollo o en modo producción de nuestra aplicación por la variable Debug que hay en
el archivo settings.py

<img src="/assets/img/posts/debugTrue.png">

## Pasos para visualizar archivos estáticos en modo desarrollo
1- En nuestro settings.py agregar unas variables que tendrá la dirección donde estarán los css, js, imagenes de nuestra aplicación.
``` python
STATIC_URL = '/static/' 
STATIC_ROOT = os.path.join(BASE_DIR, 'static') 
MEDIA_ROOT = os.path.join(BASE_DIR, 'uploaded_files')
MEDIA_URL = '/files/'
```
**STATIC_URL = '/static/'** #URL en el navegador desde donde se van a cargar los archivos.

**STATIC_ROOT = os.path.join(BASE_DIR, 'static')** #Carpeta fisica desde donde se van a leer los archivos por django server.

**MEDIA_ROOT = os.path.join(BASE_DIR, 'uploaded_files')** #Carpeta fisica desde donde se van a leer los archivos que se suban desde formularios por django server.

**MEDIA_URL = '/files/'** #URL en el navegador desde donde se van a cargar los archivos que se suban desde forms.

2- En el **archivo url.py principal** de nuestro proyecto, agregar una configuración para que Django sepa de donde buscar los archivos de css, js, imagenes de nuestra aplicación.
``` python
urlpatterns += static(settings.MEDIA_URL, document_root=settings.MEDIA_ROOT)
```
3- Ejecutar el comando que nos copiará todos los archivos css, js, e imágenes que tengamos en nuestro proyecto dentro de nuestros módulos 
a las carpetas físicas que configuramos anteriormente en el paso 1. Si no tienes un virtualenviroment configurado te recomiendo que veas como hacerlo , para que te sea más fácil el desarrollar en Django. <a href="https://www.youtube.com/watch?v=TqSSOhfRzTU" target="_blank">Ver video</a>
``` python
python3 manage.py collectstatic
```
4- En cada template que usamos debemos incluir lo siguiente cuando vayamos a cargar algún css, imagen o js. El caso de una imagen se vería así:
<img src="/assets/img/posts/imagenStatic.png" alt="MI imagen">

Al terminar todo el desarrollo de nuestra aplicación, debemos poner en producción, es decir subir nuestro proyecto django a un servidor en internet, digitalocean, aws, google cloud o el de nuestra preferencia y configurar un servidor web para que publique nuestro proyecto.

Yo uso NGINX por su simplicidad y ligereza.

Si subimos el proyecto así tal cual está tendríamos problemas, pues debemos colocar nuestra variable Debug a False para pasar a ambiente de 
producción. Esto causaría que nuestros archivos css, js y demás no se visualizaran y 


Es una muy breve explicación pero espero les sirva como introducción al tema.



