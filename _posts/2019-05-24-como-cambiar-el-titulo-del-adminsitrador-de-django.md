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
Hoy les traigo un **forma muy sencilla** de sacar mejor provecho al administrador de DJANGO, el poder **cambiar los títulos principales** de esta importante sección .
Queremos modificar los textos tanto en el formulario de inicio de sesión, la barra de título y en el listado principal. Supongamos que tenemos un sistema de inventarios que al inicio se ve así:


![TITULO](/assets/img/posts/cambiar-titulo/TituloOriginal.png)
<p class="text-center fs12">Textos originales</p>

**Queremos que se vea de la siguiente manera:**

![TITULO](/assets/img/posts/cambiar-titulo/NuevoTitulo.png)
<p class="text-center fs12">Textos después de hacer cambios</p>

Siguiendo unos simples pasos tendremos el resultado esperado que es agregar nuestros propios textos

#### Como cambiar el texto &#8220;Administración de Django&#8221;
1 &#8211; Abrimos con nuestro editor favorito cualquier archivo **admin.py** del proyecto.

![CODIGO](/assets/img/posts/cambiar-titulo/Estructura.png)

2 &#8211; Agregamos al inicio las siguientes líneas.

```python
admin.site.site_header = "Sitio web de inventarios"
admin.site.site_title = "Portal de inventarios"
admin.site.index_title = "Bienvenidos al portal de administración"
```
Y tenemos el resultado esperado. Esos son títulos de ejemplo obviamente usted debe agregar los que su proyecto requiera.

![INICIO_SESION](/assets/img/posts/cambiar-titulo/login.png)
<p class="text-center fs12">Textos después de hacer cambios</p>

Acá les dejo un video de los pasos a seguir y su resultado.

[![PASO A PASO](http://img.youtube.com/vi/d9F8RYpAXFU/0.jpg)](http://www.youtube.com/watch?v=d9F8RYpAXFU)

Espero les sirva.