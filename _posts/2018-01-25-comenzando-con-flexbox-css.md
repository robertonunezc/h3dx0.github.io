---
id: 34
title: Comenzando con CSS Flexbox layout
date: 2018-01-25T23:37:28+00:00
author: robert
layout: post
permalink: /comenzando-con-flexbox-css/
categories:
  - CSS3
  - HTML5
tags:
  - css3
  - flexbox
  - grid
  - layout
  - maquetado
  - tutorial
---
Hola a todos, muchas gracias por darte una vuelta a este artículo en el cual aprenderás como iniciar el **maquetado con flexbox** y así darle un impulso a tus conocimientos de frontend web para dejar atrás viejas e inútiles técnicas de maquetado con **CSS3.** Comenzamos&#8230;
 <!--more-->
## ¿Que es?

**CSS flexbox layout** es una tecnología o modelo de CSS3 implementada por los navegadores actuales. Tiene como objetivo ayudar a los desarrolladores a crear layouts de sitios web de manera más fácil, reutilizable y eficiente.

## ¿Por qué usarlo?

Porque la vida serás mas sencilla a la hora de maquetar  Viene a resolver muchos problemas que anteriormente se tenían que solucionar de forma poco ortodoxa, creando hacks y código poco legible. Con flexbox muchos problemas de posicionamiento de elementos, ordenamiento de los mismo se puede lograr de manera muy sencilla.

## ¿Como usarlo?

Vamos a crear un menú para nuestro sitio con los enlaces de comunes

Nuestro código HTML se vería así:

<pre class="lang:xhtml decode:true" title="Menu">&lt;nav&gt;
  &lt;ul&gt;
    &lt;li&gt;&lt;a href="#"&gt;Inicio&lt;/a&gt;&lt;/li&gt;
    &lt;li&gt;&lt;a href="#"&gt;Quienes somos&lt;/a&gt;&lt;/li&gt;
    &lt;li&gt;&lt;a href="#"&gt;Servicios&lt;/a&gt;&lt;/li&gt;
    &lt;li&gt;&lt;a href="#"&gt;Contacto&lt;/a&gt;&lt;/li&gt;
  &lt;/ul&gt;
&lt;/nav&gt;</pre>

Nuestro CSS de inicio para dar un poco de estilos sería algo así:

<pre class="lang:css decode:true" title="CSS Inicio">nav {
  background: #008492;  
}
ul &gt; li &gt; a {
  color:#fff;
  text-decoration: none;
}
li {
  list-style:none;
}</pre>

El resultado sería algo como esto

<img class="size-full wp-image-47" src="http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/01/Firefox_Screenshot_2018-01-30T02-51-28.619Z.png" alt="ResultadoSinFlexbox" width="317" height="97" srcset="http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/01/Firefox_Screenshot_2018-01-30T02-51-28.619Z.png 317w, http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/01/Firefox_Screenshot_2018-01-30T02-51-28.619Z-300x92.png 300w" sizes="(max-width: 317px) 100vw, 317px" /> 

Aquí es donde entra **flexbox** al rescate **evitando** el uso de **floats** y **clearfix.**

Agregando solamente esta línea  a nuestro ejemplo tenemos un resultado mucho mejor

<pre class="lang:css decode:true " title="DisplayFlex">ul {
  display:flex;
}</pre>

<img class="wp-image-46 size-full" title="ResultadoConFlexbox" src="http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/01/Firefox_Screenshot_2018-01-30T02-49-38.166Z.png" alt="ResultadoConFlexbox" width="743" height="62" srcset="http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/01/Firefox_Screenshot_2018-01-30T02-49-38.166Z.png 743w, http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/01/Firefox_Screenshot_2018-01-30T02-49-38.166Z-300x25.png 300w, http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/01/Firefox_Screenshot_2018-01-30T02-49-38.166Z-740x62.png 740w" sizes="(max-width: 743px) 100vw, 743px" /> 

Al agregar esta simple línea  al contenedor de los elementos que se quieren acomodar aplicando **FLEXBOX**,  el contenedor reorganizará sus elementos hijos colocándolos uno al lado del otro, como si usáramos los incómodos **float.** Este comportamiento se ejecutará de forma similar en cualquier caso que se aplique el display:flex;

Este es el primer paso para comenzar a utilizar FLEXBOX, debemos detectar nuestro **elemento padre o contenedor** y **agregar** la propiedad **display:flex.**

A continuación el código completo del ejemplo CSS. Donde la parte fundamental y objetivo es la línea 6.

<pre class="lang:css decode:true" title="Final">nav{
  background: #008492;  
}

ul{
  display:flex;// Contenedor que usa FLEXBOX
}

ul &gt; li {
    margin:10px;
}
ul &gt; li &gt; a{
  color:#fff;
  text-decoration: none;
}
li {
  list-style:none;
}</pre>

Acá les dejo otro ejemplo que ilustra muy bien el uso sencillo de FLEXBOX. Imaginen que estamos creando un sitio de ecommerce y estamos desarrollando la vista donde se muestran los productos.

Le dejo el CODEPEN para no hacer más extenso el artículo. Prueben quitando el display:flex y verán la difrencia.



Espero les sea de utilidad este artículo, es simplemente el inicio ya que flexbox tiene muchas más aplicaciones que veremos en otros artículos proximamente.

No dudes en dejar un comentario. Un gracias o feedback siempre es bienvenido y dá mucho ánimo.