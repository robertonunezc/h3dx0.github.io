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

Con este artículo quiero enseñarte **como agregar un logo al adminstrador de django**, un requerimiento que muchas veces es útil para darle un toque personal a esta sección tan importante .

La mayoría de los proyectos web en la actualidad necesitan que su información sea dinámica y facilemente modificable por el cliente o los encargados de realizar esta tarea. Aquí es donde entra en juego el **administrador de DJANGO** y casi siempre hay que hacerle las **modificaciones visuales** para que se adapte a nuestro cliente.

Una de estas adecuaciones es [cambiar el título del mismo](http://localhost/~h3dx0/wordpress/como-cambiar-el-titulo-del-adminsitrador-de-django/) por uno personalizado o simplemente agregar el logo de nuestro cliente. **¿Como cambiamos el título por nuestro logo?**

## SOLUCIÓN

1- En la raíz de nuestro proyecto debemos **crear una estructura de carpetas  TEMPLATES/ADMIN.**
<!-- 
<img class="aligncenter size-full wp-image-194" src="http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/06/estructura_carpetas.png" alt="estructura_carpetas" width="339" height="160" srcset="http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/06/estructura_carpetas.png 339w, http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/06/estructura_carpetas-300x142.png 300w" sizes="(max-width: 339px) 100vw, 339px" />  -->

2- En esta carpeta admin el **copiar el archivo base_site.html.** Este archivo se encuentra en el directorio donde **se instaló DJANGO como librería,** acá les dejo una captura de mi proyecto, donde uso un virtual enviroment para que puedan tener como referencia donde encontrar este archivo. En ese directorio están todas las vistas usadas por el administrador.
<!-- img class="aligncenter size-full wp-image-195" src="http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/06/django_admin_dir.png" alt="django_admin_dir" width="357" height="891" srcset="http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/06/django_admin_dir.png 357w, http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/06/django_admin_dir-120x300.png 120w, http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/06/django_admin_dir-300x749.png 300w" sizes="(max-width: 357px) 100vw, 357px"  -->

3- **Editar el base_site.html** copiado en la estructura de **TEMPLATES/ADMIN** creada y agregar los

<pre class="">*load staticfiles *</pre>

y en el bloque ** block branding ** hacer las modificaciones que querramos para dejar el header como nos guste.

Acá les dejo como agregar una imagen previante **coipada a nuestro directorio de statics/images/**
<!-- 
<img class="aligncenter size-full wp-image-198" src="http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/06/Screenshot_20190611_222243.png" alt="" width="1064" height="271" srcset="http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/06/Screenshot_20190611_222243.png 1064w, http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/06/Screenshot_20190611_222243-300x76.png 300w, http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/06/Screenshot_20190611_222243-768x196.png 768w, http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/06/Screenshot_20190611_222243-1024x261.png 1024w" sizes="(max-width: 1064px) 100vw, 1064px" />  -->

&nbsp;

La imagen anterior muestra el código del archivo base_site.html después de **cambiar el texto que viene por defecto y agregar nuestro logo.** En la imagen que sigue se ve eol resultado después de haber agregado un logo(imagen que se desee ) al administrador.
<!-- 
<img class="aligncenter size-full wp-image-199" src="http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/06/Screenshot_2019-06-11-Bienvenidos-al-portal-de-administración-Portal.png" alt="" width="1904" height="60" srcset="http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/06/Screenshot_2019-06-11-Bienvenidos-al-portal-de-administración-Portal.png 1904w, http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/06/Screenshot_2019-06-11-Bienvenidos-al-portal-de-administración-Portal-300x9.png 300w, http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/06/Screenshot_2019-06-11-Bienvenidos-al-portal-de-administración-Portal-768x24.png 768w, http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/06/Screenshot_2019-06-11-Bienvenidos-al-portal-de-administración-Portal-1024x32.png 1024w" sizes="(max-width: 1904px) 100vw, 1904px" />  -->

Este es el principio para hacer cualquier modificación al administrador, el proceso es sobreescribir los archivos .html o .css que tiene el core de DJANGO con nuestras modificaciones. Proximamente estaré escribiendo más artículos sobre esta poderoza herramienta que DJANGO nos brinda.

No dudes en **dejar cualquier comentario** que tengas sobre los artículos, son mis primeros y debo pulir muchos detalles pero que mejor **si cuento con tu ayuda.** Espero tu comentario.

Happy coding. 🙂
