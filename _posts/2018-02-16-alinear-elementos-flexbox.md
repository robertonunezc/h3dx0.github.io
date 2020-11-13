---
id: 73
title: Alinear elementos en el contenedor con flexbox
date: 2018-02-16T04:26:14+00:00
author: robert
layout: post
permalink: /alinear-elementos-flexbox/
categories:
  - CSS3
  - HTML5
tags:
  - flexbox
  - maquetado
  - web
---
Continuando con la serie de artículos sobre como **maquetar en css** con flexbox, hoy tendremos como objetivo el **aprender a alinear elementos** dentro de un contenedor.
Una de las funciones o posibiliades que más me llamó la antención al comenzar a trabajar con flexbox fue la facilidad para poder acomodar o alinear elementos, tanto horizontalmente, verticalmente como cada elemento por separado.
 <!--more-->

Para alinear los elementos nuestro contenedor acepta 4 propiedades fundamentales

  * justify-content
  * align-items
  * align-self


Puedes ver el video demostrativo en este enlace.

[![PASO A PASO](http://img.youtube.com/vi/PRbfXcKxR8M/0.jpg)](https://youtu.be/PRbfXcKxR8M)


Estas propiedades colocarán los elementos dependiendo  de como se hubiese definido nuestro main-axis, [aquí](/conceptos-basicos-en-flexbox/) puedes darle una revisada a este tema.  
<img class="aligncenter wp-image-75 size-full" title="AxisFlexbox" src="/assets/img/posts/alinear-flexbox/AxisFlexbox.png" alt="AxisFlexbox" width="640" height="400" sizes="(max-width: 640px) 100vw, 640px" /> 

&nbsp;

## justify-content:

Esta propiedad será la encargada de organizar los elementos dentro de nuestro contenedor a través del main-axis (de forma horizontal en el caso de la imagen).

Valores aceptados:

### **justify-content: flex-start;**
<p class="codepen" data-height="299" data-theme-id="light" data-default-tab="css,result" data-user="h3dx0" data-slug-hash="PRemLd" data-preview="true" style="height: 299px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="ju-co:flsart">
  <span>See the Pen <a href="https://codepen.io/h3dx0/pen/PRemLd">
  ju-co:flsart</a> by Robert (<a href="https://codepen.io/h3dx0">@h3dx0</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>


Al aplicar esta propiedad puede que no se vea ningún efecto de inicio dado que nuestro menú en el ejemplo ya tiene asignada la propiedad **flex-direction: row** desde un inicio acomodando los elementos uno al lado del otro,  lo que se quiere lograr es que los elementos se acomoden donde comienza el contenedor que en este caso es de izquierda a derecha.

### **justify-content: center;**

<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="css,result" data-user="h3dx0" data-slug-hash="ZxoKNb" data-preview="true" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="justcont:center">
  <span>See the Pen <a href="https://codepen.io/h3dx0/pen/ZxoKNb">
  justcont:center</a> by Robert (<a href="https://codepen.io/h3dx0">@h3dx0</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

Aplicando esta propiedad vemos como todos los elementos se centran teniendo en cuenta el main-axis que en este caso es en forma horizontal.

### **justify-content: flex-end;**

<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="css,result" data-user="h3dx0" data-slug-hash="gezWJd" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="justcont:flexend">
  <span>See the Pen <a href="https://codepen.io/h3dx0/pen/gezWJd">
  justcont:flexend</a> by Robert (<a href="https://codepen.io/h3dx0">@h3dx0</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

Flex-end nos ayuda a alinear nuestros elementos al final de nuestro contenedor en este caso hacia la derecha. Lo que anteriormente lograríamos usando floats.

&nbsp;

### **justify-content: space-between;**

<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="css,result" data-user="h3dx0" data-slug-hash="JLvNQN" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="jcspace-btween">
  <span>See the Pen <a href="https://codepen.io/h3dx0/pen/JLvNQN">
  jcspace-btween</a> by Robert (<a href="https://codepen.io/h3dx0">@h3dx0</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

Space-between es una de las propiedades que más me gustan, dada la facilidad con que se pueden dar espacios exactos (ayudándonos con el diseño responsivo en muchos casos) entre los elementos que estamos colocando. Esta propiedad coloca los elementos hacia los extremos de nuestro contenedor y el espacio restante los distribuye con los demás elementos.

### **justify-content: space-around;**

<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="css,result" data-user="h3dx0" data-slug-hash="xWjdvq" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="jc:space-around">
  <span>See the Pen <a href="https://codepen.io/h3dx0/pen/xWjdvq">
  jc:space-around</a> by Robert (<a href="https://codepen.io/h3dx0">@h3dx0</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

Space-around así como space-between nos ayuda a distribuir de forma equitativa el espacio entre nuestros elementos, a diferencia de de la propiedad anterior , crea espacios iguales entre todos los elementos así como con los límites de nuestro contenedor.

## Alinear elementos según cross-axis

### align-items:

Esta propiedad será la encargada de organizar los elementos dentro de nuestro contenedor a través del cross-axis (de forma vertical en el caso de la imagen).

### Valores aceptados:

### align-items: flex-start:

<img class="alignnone size-full wp-image-89" src="/assets/img/posts/alinear-flexbox/ag-start.png" alt="" width="640" height="400" sizes="(max-width: 640px) 100vw, 640px" /> 

### align-items: flex-end;

<img class="alignnone wp-image-93 size-full" src="/assets/img/posts/alinear-flexbox/ag-end.png" alt="alinear elementos" width="640" height="400" sizes="(max-width: 640px) 100vw, 640px" /> 

### align-items: center;

<img class="alignnone wp-image-93 size-full" src="/assets/img/posts/alinear-flexbox/ag-center.png" alt="alinear elementos" width="640" height="400" sizes="(max-width: 640px) 100vw, 640px" /> 

### align-items: strech;

<img class="alignnone wp-image-95 size-full" src="/assets/img/posts/alinear-flexbox/ag-strech.png" alt="alinear elementos" width="640" height="400" sizes="(max-width: 640px) 100vw, 640px" /> 

Estas son las principales propiedades para poder controlar la ubicación de todos los elementos dentro de nuestro contenedor. Muchas de estas propiedades están sujetas a como orientemos nuestros main-axis y cross-axis. Estas son algunos de los resultados que ahora con flexbox se puede lograr de forma mas sencilla.

Muchas gracias por su lectura. Espero que les sirva este artículo para que puedan comenzar a usar estas fantásticas propiedades y atributos.

No lo dudes y regálame un simple GRACIAS.