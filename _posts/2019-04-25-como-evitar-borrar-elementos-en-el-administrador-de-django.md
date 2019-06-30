---
id: 145
title: Como evitar borrar elementos en el administrador de Django
date: 2019-04-25T02:45:30+00:00
author: robert
layout: post
permalink: /como-evitar-borrar-elementos-en-el-administrador-de-django/
# categories:
#   - Django
#   - How To
# tags:
#   - admindjango
#   - backend
#   - django
#   - howto
#   - python
---
Hola a todos y muchas gracias por llegar a mi blog. Espero este artículo te sea de utilidad.

En varios proyectos por cuestiones de manejo de información histórica , nuestro cliente nos comenta que **no se pueden borrar ciertos datos** una ves que ya están en el sistema.

Cuando hacemos nuestro administrador desde cero no hay problemas pues controlamos todo el proceso de creación pero si se desea utilizar el **administrador que DJANGO** nos brinda por cuestiones de agilizar tiempos o cualquier otra razón, este por defecto **nos da la opción de eliminar los registros de los modelos que tenemos.**<figure class="wp-block-image">

<img src="http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/04/Firefox_Screenshot_2019-04-25T02-20-59.578Z.png" alt="Listado Django por defecto" class="wp-image-146" srcset="http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/04/Firefox_Screenshot_2019-04-25T02-20-59.578Z.png 466w, http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/04/Firefox_Screenshot_2019-04-25T02-20-59.578Z-300x115.png 300w" sizes="(max-width: 466px) 100vw, 466px" /> <figcaption>Listado Django</figcaption></figure> 

Como nos muestra la imagen anterior **podemos borrar los datos** usando el ckeckbox y el select de acciones.

## Solución  


En el **archivo admin.py** de nuestro proyecto donde tenemos registrado el modelo debemos agregar lo siguiente:

**from miproyecto.admin import NonDeleteAdmin  
admin.site.register(MiModelo, NonDeleteAdmin)** 

Quedando así el administrador donde se eliminan los checkbox y el select para la acción de borrar.<figure class="wp-block-image">

<img src="http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/04/Firefox_Screenshot_2019-04-25T02-25-53.747Z.png" alt="evitar borrar datos administrador django" class="wp-image-147" srcset="http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/04/Firefox_Screenshot_2019-04-25T02-25-53.747Z.png 468w, http://localhost/~h3dx0/wordpress/wp-content/uploads/2019/04/Firefox_Screenshot_2019-04-25T02-25-53.747Z-300x110.png 300w" sizes="(max-width: 468px) 100vw, 468px" /> <figcaption>Listado sin opción de eliminar.</figcaption></figure> 

Espero les sea útil y cualquier comentario es bienvenido. 🙂