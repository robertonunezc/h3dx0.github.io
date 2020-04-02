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

En la mayoría de los casos cuando comenzamos a utilizar el administrador de DJANGO que viene ya listo, es necesario **cambiar los títulos** que aparece de inicio tanto en el formulario de inicio de sesión, en la barra de título y en el listado principal.

#### Como cambiar el texto &#8220;Administración de Django&#8221;
1 &#8211; En un admin.py del proyecto agregar las siguientes líneas.
```python
admin.site.site_header = "Sitio web de inventarios"
admin.site.site_title = "Portal de inventarios"
admin.site.index_title = "Bienvenidos al portal de administración"
```
Esos son títulos de ejemplo obviamente usted debe agregar los que quiere que aparezcan.

Espero les sirva.