---
id: 167
title: Como cambiar el título del adminsitrador de DJANGO
date: 2019-05-24T03:23:35+00:00
author: robert
layout: post
permalink: /como-cambiar-el-titulo-del-adminsitrador-de-django/
categories:
  - Django
  - How To
  - python
---
Siguiendo la serie sobre como sacar mejor provecho al administrador de DJANGO , hoy les dejo un pequeño cambio pero importante.

En la mayoría de los casos cuando comenzamos a utilizar el administrador de DJANGO que viene ya listo, es necesario **cambiar los títulos** que aparece de inicio tanto en el formulario de inicio de sesión, en la barra de título y en el listado principal, **&#8220;Django administration&#8221; o &#8220;Administración de Django&#8221;.**<figure class="wp-block-image">

<img class="wp-image-168" src="http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/05/image.png" alt="" srcset="http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/05/image.png 337w, http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/05/image-300x53.png 300w" sizes="(max-width: 337px) 100vw, 337px" /> <figcaption>Titulo de la barra superior del administrador</figcaption></figure> 

#### Como cambiar el texto &#8220;Administración de Django&#8221;

1 &#8211; En un admin.py del proyecto agregar las siguientes líneas.

<pre class="lang:python decode:true ">admin.site.site_header = "Sitio web de inventarios"
admin.site.site_title = "Portal de inventarios"
admin.site.index_title = "Bienvenidos al portal de administración"</pre>

&nbsp;

Obteniendo los siguientes resultados :<figure class="wp-block-image">

<img class="wp-image-169" src="http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/05/image-1.png" alt="" srcset="http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/05/image-1.png 489w, http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/05/image-1-300x96.png 300w" sizes="(max-width: 489px) 100vw, 489px" /> </figure> <figure class="wp-block-image">**admin.site.site_header = &#8220;Sitio web de inventarios&#8221;**</figure> 

&nbsp;

#### Cabecera y bienvenida<figure class="wp-block-image">

<img class="wp-image-170" src="http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/05/image-2.png" alt="" srcset="http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/05/image-2.png 441w, http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/05/image-2-300x83.png 300w" sizes="(max-width: 441px) 100vw, 441px" /> </figure> <figure class="wp-block-image">**admin.site.site_header = &#8220;Sitio web de inventarios&#8221;** y **admin.site.index_title = &#8220;Bienvenidos al portal de administración&#8221;**</figure> 

#### **Título de sitio**<figure class="wp-block-image">

<img class="wp-image-171" src="http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/05/Screenshot_20190523_220722.png" alt="" /> </figure> 

**admin.site.site_title = &#8220;Portal de inventarios&#8221;**

Espero les sirva y les agradecería sus comentarios.