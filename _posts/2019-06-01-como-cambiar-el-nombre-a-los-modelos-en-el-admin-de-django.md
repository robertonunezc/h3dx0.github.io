---
id: 184
title: Como cambiar el nombre a los modelos en el admin de DJANGO
date: 2019-06-01T23:39:30+00:00
author: robert
layout: post
permalink: /como-cambiar-el-nombre-a-los-modelos-en-el-admin-de-django/
categories:
  - Django
  - How To
  - python
tags:
  - admindjango
  - django
  - python
---
En numerosas ocaciones debemos **mostrar los nombres de nuestros modelos en español**, si el cliente final hará interacción con el administrador de DJANGO. Esto puede ser un problema si nos gusta definir y hacer la programación de nuestro **sistema en inglés, para mantener estándares** o simplemente el **nombre del modelo es algo más abastracto** que su homólogo en la vida real o su **terminación plural no es la correcta** como la imagen que muestro a continuación, por lo que necesitamos **cambiar sus nombre de los modelos** para que **se vean correctamente** en el administrador.

<img class="size-full wp-image-185 aligncenter" src="http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/06/Firefox_Screenshot_2019-06-01T23-22-24.607Z.png" alt="Cambiar Nombre Modelo Django" width="413" height="81" srcset="http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/06/Firefox_Screenshot_2019-06-01T23-22-24.607Z.png 413w, http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/06/Firefox_Screenshot_2019-06-01T23-22-24.607Z-300x59.png 300w" sizes="(max-width: 413px) 100vw, 413px" /> 

## Solución

&nbsp;

Para resolver esta situación y poder mostrar en el adminsitrador de DJANGO los nombres que nosotros querramos simplemente basta con **definir 1 propiedad a nuestro modelo.**

Esta propiedad es **verbose\_name\_plural = &#8220;NOMBRE EN PLURAL&#8221;<img class="aligncenter size-full wp-image-186" src="http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/06/Screenshot_20190601_182644.png" alt="Propiedad Verbose" width="738" height="165" srcset="http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/06/Screenshot_20190601_182644.png 738w, http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/06/Screenshot_20190601_182644-300x67.png 300w" sizes="(max-width: 738px) 100vw, 738px" />**

Como muestra la imagen, vamos a nuestro modelo y definimos en la **subclase Meta: la propiedad verbose\_name\_plural**

<img class="aligncenter size-full wp-image-187" src="http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/06/Firefox_Screenshot_2019-06-01T23-31-27.993Z.png" alt="Estado de cuenta" width="615" height="47" srcset="http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/06/Firefox_Screenshot_2019-06-01T23-31-27.993Z.png 615w, http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/06/Firefox_Screenshot_2019-06-01T23-31-27.993Z-300x23.png 300w" sizes="(max-width: 615px) 100vw, 615px" /> 

Teniendo como resultado en nuestro administrador la imagen anterior.

&nbsp;

Espero les sirva este artículo y no dude en dejar un comentario o cualquier duda sobre DJANGO.

Dando [clic aquí](http://localhost/~h3dx0/wordpress/category/django/) podrás ver otros tips interesantes sobre **DJANGO**.

También pudes suscribirte a **mi boletín(sección derecha de la web)** y te enterarás primero que nadie cuando publique un nuevo artículo.

&nbsp;

&nbsp;

&nbsp;