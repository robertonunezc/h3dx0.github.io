---
id: 56
title: Flexbox, conceptos básicos (flex-direction)
date: 2018-02-13T04:10:54+00:00
author: robert
layout: post
permalink: /conceptos-basicos-en-flexbox/
categories:
  - CSS3
  - HTML5
tags:
  - flex-direction
  - flexbox
  - main-axis
---
Continuando con la serie de este artículo sobre **Flexbox** estaremos viendo los conceptos principales que debemos tener en cuenta a la hora de maquetar nuestros layouts con esta técnica en especial la propiedad **flex-direction** y los axis. Sino lo leíste  [aquí hay una introducción](http://localhost/~h3dx0/wordpress/comenzando-con-flexbox-css/) para comenzar a usar esta técnica de forma muy fácil.

## Los dos ejes o axis de Flexbox:

Para comenzar a trabajar con flexbox se debe tener en cuenta que para acomodar los elementos se hace en base a los  2 ejes o axis que existen, el **main axis** y el **cross axis .** Siendo el main axis la principal y que es definida por la propiedad **flex-direction.**

<figure id="attachment_57" aria-describedby="caption-attachment-57" style="width: 501px" class="wp-caption alignnone"><img class="wp-image-57 size-full" title="main axis" src="http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/02/main_axis.png" alt="Flex-direction main axis" width="501" height="77" srcset="http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/02/main_axis.png 501w, http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/02/main_axis-300x46.png 300w" sizes="(max-width: 501px) 100vw, 501px" /><figcaption id="caption-attachment-57" class="wp-caption-text">main axis</figcaption></figure>

Al definir la propiedad **flex-direction: row,** estamos diciéndole a nuestro contenedor que acomode los elementos uno al lado del otro, es decir nuestro **main-axis será ubicado horizontalmente** lo cual debemos tener en cuenta porque muchas **otras propiedades dependen de la definición de los axis.**

Este es el contenedor de los elementos del menú.

<pre class="lang:default decode:true" title="flex-direction html">&lt;nav&gt;
  &lt;ul&gt;
    &lt;li&gt;&lt;a href="#"&gt;Inicio&lt;/a&gt;&lt;/li&gt;
    &lt;li&gt;&lt;a href="#"&gt;Quienes somos&lt;/a&gt;&lt;/li&gt;
    &lt;li&gt;&lt;a href="#"&gt;Servicios&lt;/a&gt;&lt;/li&gt;
    &lt;li&gt;&lt;a href="#"&gt;Contacto&lt;/a&gt;&lt;/li&gt;
  &lt;/ul&gt;
&lt;/nav&gt;</pre>

CSS aplicado.

<pre class="lang:css decode:true" title="css">nav{
  background: #008492;  
}

ul{
  display:flex;
  flex-direction:row;

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

Si ya leyeron el [artículo anterior](http://localhost/~h3dx0/wordpress/comenzando-con-flexbox-css/) pueden notar que no hay cambios en cuanto al resultado que esperamos, en este caso cada elemento del menú se coloca uno al lado del otro. Esto sucede pues al definir en el **ul la propiedad display:flex,** el comportamiento de los elementos hijos por **default es flex-direction:row,** por lo que no es necesario definir la propiedad si queremos que su comportamiento sea el establecido.

## Valores de aceptados por flex-direction

Para manipular los axis de nuestro contenedor  flex-direction acepta los siguientes valores:

  * `row`
  * `row-reverse`
  * `column`
  * `column-reverse```

<p class="">
  Así se vería nuestro menú aplicando los distintos valores a esta propiedad
</p>

###  row-reverse

<img class="size-full wp-image-66" src="http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/02/Firefox_Screenshot_2018-02-14T03-28-45.768Z.png" alt="flex-direction:row-reverse" width="808" height="62" srcset="http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/02/Firefox_Screenshot_2018-02-14T03-28-45.768Z.png 808w, http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/02/Firefox_Screenshot_2018-02-14T03-28-45.768Z-300x23.png 300w, http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/02/Firefox_Screenshot_2018-02-14T03-28-45.768Z-768x59.png 768w" sizes="(max-width: 808px) 100vw, 808px" /> 

###  column

<img class="size-full wp-image-64" src="http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/02/columns.png" alt="flex-direction:column" width="428" height="237" srcset="http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/02/columns.png 428w, http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/02/columns-300x166.png 300w" sizes="(max-width: 428px) 100vw, 428px" /> 

###  column-reverse

<img class="alignnone size-full wp-image-67" src="http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/02/Firefox_Screenshot_2018-02-14T03-31-29.538Z.png" alt="" width="251" height="183" /> 

En las imágenes anteriores se puede ver claramente como afecta el orden de los elementos al aplicar los distintos valores a  **flex-direction.**

&nbsp;

## Cross axis

El cross axis es el eje encargado de acomodar los elementos perpendicularmente al main axis, por lo que tenemos que tener en cuenta la orientación del mismo dado que dependen uno de otro.

> Si el main axis está orientado a column o column-reverse el cross axis estará afectando los elementos horizontalmente.

Acá les dejo un codepen para que puedan practicar los conceptos y valores aprendidos.