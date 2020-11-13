---
id: 193
title: Como agregar un logo al administador de DJANGO
date: 2019-06-12T04:58:01+00:00
author: robert
layout: post
permalink: /como-agregar-un-logo-al-administador-de-django/
categories:
  - Admin
  - Django
  - How To
  - python
---

Con este artículo quiero enseñarte **como agregar un logo al adminstrador de django**, un requerimiento que muchas veces es útil para darle un toque personal a esta sección tan importante . Puedes ver el video explicativo dando clic <a href="https://youtu.be/wbpeWareO00" target="_blank">aquí</a>
La mayoría de los proyectos web en la actualidad necesitan que su información sea dinámica y facilemente modificable por el cliente o los encargados de realizar esta tarea. 
 <!--more-->

Aquí es donde entra en juego el **administrador de DJANGO**  y casi siempre hay que hacerle las **modificaciones visuales** para que se adapte a nuestro cliente.

Una de estas adecuaciones es [cambiar el título del mismo](/como-cambiar-el-titulo-del-adminsitrador-de-django/) por uno personalizado o simplemente agregar el logo de nuestro cliente. **¿Como cambiamos el título por nuestro logo?**

## SOLUCIÓN

1- En la raíz de nuestro proyecto debemos **crear una estructura de carpetas  TEMPLATES/ADMIN.**

<img class="aligncenter" title="EstructuraProyecto" src="/assets/img/posts/agregar-logo/estructura_proyecto.png" alt="EstructuraProyecto" width="340" height="400" sizes="(max-width: 640px) 100vw, 640px" /> 

2- En esta carpeta admin el **copiar el archivo base_site.html.** Este archivo se encuentra en el directorio donde **se instaló DJANGO como librería,** acá les dejo una captura de mi proyecto, donde uso un virtual enviroment para que puedan tener como referencia donde encontrar este archivo. Normalmente es dentro del virtual enviroment otra carpeta que se llama **site-packages** y después la estructura que muestro en la imagen. En ese directorio están todas las vistas usadas por el administrador.


<img class="aligncenter" title="ArchivosDjango" src="/assets/img/posts/agregar-logo/django.png" alt="ArchivosDjango" width="340" height="500" sizes="(max-width: 640px) 100vw, 640px" /> 


3- **Editar el base_site.html** copiado en la estructura de **TEMPLATES/ADMIN** creada y agregar los

```python
load staticfiles
```
y en el bloque 
```python
block branding
```
hacer las modificaciones que querramos para dejar el header como nos guste.

**RESULTADO**
<img class="aligncenter" title="ArchivosDjango" src="/assets/img/posts/agregar-logo/html_final.png" alt="ArchivosDjango"  sizes="(max-width: 640px) 100vw, 640px" /> 

<img class="aligncenter" title="LogoAdministradorDjango" src="/assets/img/posts/agregar-logo/admin_logo.png" alt="LogoAdministradorDjango"  sizes="(max-width: 640px) 100vw, 640px" /> 

Este es el principio para hacer cualquier modificación al administrador, el proceso es sobreescribir los archivos .html o .css que tiene el core de DJANGO con nuestras modificaciones. Proximamente estaré escribiendo más artículos sobre esta poderoza herramienta que DJANGO nos brinda.

Happy coding. 🙂
