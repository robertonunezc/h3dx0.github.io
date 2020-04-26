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

![TITULO](/assets/img/posts/cambiar-nombre-modelos/ModeloOriginal.png)
<p class="text-center fs12">Modelo Products</p>
En nuestra apliación tenemos un modelo llamado Products y queremos que aparezca en el administrador el nombre como Productos.

## Solución

Para resolver esta situación y poder mostrar en el adminsitrador de DJANGO los nombres que nosotros querramos simplemente basta con **definir 1 propiedad a nuestro modelo.**

Esta propiedad es **verbose\_name\_plural = &#8220;NOMBRE EN PLURAL&#8221;**

Como muestra la imagen, vamos a nuestro modelo y definimos en la **subclase Meta: la propiedad verbose\_name\_plural**

![MODELO_PLURAL](/assets/img/posts/cambiar-nombre-modelos/ModeloPlural.png)

Teniendo como resultado en nuestro administrador la imagen anterior.

![MODELO_PLURAL](/assets/img/posts/cambiar-nombre-modelos/ModeloFinal.png)

Espero les sirva este artículo y no dude en dejar un comentario o cualquier duda sobre DJANGO.

Dando [clic aquí](https://www.youtube.com/channel/UCDbGgmXz39F1tkF2rThehlQ) podrás ver otros tips interesantes sobre **DJANGO**.

Puedes ver un video del paso a paso para hacer este cambio en tu proyecto

[![PASO A PASO](http://img.youtube.com/vi/mHcUXQ2M2ko/0.jpg)](http://www.youtube.com/watch?v=mHcUXQ2M2ko)

Espero les sirva.