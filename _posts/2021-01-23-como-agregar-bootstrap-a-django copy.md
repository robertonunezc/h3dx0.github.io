---
id: 121
title: Como agregar bootstrap a DJANGO
date: 2019-06-12T04:58:01+00:00
author: robert
layout: post
permalink: /como-agregar-bootstrap-a-django/
categories:
  - Django
  - How To
  - template
  - Bootstrap
---

Con este artículo quiero enseñarte **como agregar o integrar Bootstrap a django**, un requerimiento que muchas veces es útil para desarrollar nuestro frontend de forma más rápida y usando buenas prácticas.
Para los que no lo conocen <a href="https://getbootstrap.com/" target="_blank">Bootstrap</a> es uno de los frameworks de maquetado más usados en el mundo.
<!--more-->
# Video
<iframe width="560" height="315" src="https://www.youtube.com/embed/0B-GQZaDkl0" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<br>

# Agregando Bootstrap a nuestro HTML

Existen 2 vías principales para agregar una librería externa a nuestro proyecto de DJANGO.

La primera: **descargamos y copiamos los archivos** directamente a nuestro proyecto.

La segunda: **enlazamos los archivos desde un servidor CDN.**

Al final tenemos el mismo resultado solo que cada método tiene sus ventajas. Yo personalemente en la mayoría de los proyectos web uso la vía de enlazarlos vía CDN, sobre todo por cuestiones de eficiencia y quitarle trabajo a mi servidor.

1- Vamos al sitio de <a href="https://getbootstrap.com/docs/5.0/getting-started/download/" target="_blank">Bootstrap</a> y en la **seccion de Donwload** vamos y copiamos el código para enlazar desde un servidor CDN los archivos del código.

```
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.0-beta1/dist/css/bootstrap.min.css" rel="stylesheet" crossorigin="anonymous">
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.0-beta1/dist/js/bootstrap.bundle.min.js"crossorigin="anonymous"></script>
```

2- Debemos agregar esos enlaces en nuestro base.html o en el template de nuestro proyecto de DJANGO donde querramos hacer uso de boostrap. 

<img src="/assets/img/posts/boots.png" alt="ADD_BOOTSTAP_DJANGO" style="width:100%;margin:0 auto; display:block">

Después de este paso ya nuestro proyecto DJANGO está listo para hacer uso del framework.
Debemos ir a la documentación y aprender a usar este framework. 

Tenemos muchas clases que usar para mejorar y estandarizar nuestro proyecto en cuanto a diseño.

Acá les dejo un ejemplo de como agregar bootstrap a una tabla.
```
<table class="table table-bordered table-striped">
        <thead>
        <th>Nombre</th>
        <th>Descripción</th>
        <th>Cantidad</th>
        <th>Precio</th>
        </thead>
        <tbody>        
            <tr>
                <td>Pan</td>
                <td>
                   Pan artesanal mejor calidad
                </td>
                <td>10</td>
                <td>$15.00</td>
            </tr>
        
        </tbody>
    </table>
```
El resultado es el siguiente si tuvieramos más filas en nuestro código anterior:

<img src="/assets/img/posts/table.png" alt="ADD_BOOTSTAP_DJANGO" style="width:100%;margin:0 auto; display:block">


Happy coding. 🙂
