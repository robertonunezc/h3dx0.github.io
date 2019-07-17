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

Para alinear los elementos nuestro contenedor acepta 4 propiedades fundamentales

  * justify-content
  * align-items
  * align-self

Estas propiedades colocarán los elementos dependiendo  de como se hubiese definido nuestro main-axis, [aquí](http://localhost/~h3dx0/wordpress/conceptos-basicos-en-flexbox/) puedes darle una revisada a este tema.  
<img class="aligncenter wp-image-75 size-full" title="AxisFlexbox" src="http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/02/AxisFlexbox.png" alt="AxisFlexbox" width="640" height="400" srcset="http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/02/AxisFlexbox.png 640w, http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/02/AxisFlexbox-300x188.png 300w" sizes="(max-width: 640px) 100vw, 640px" /> 

&nbsp;

## justify-content:

Esta propiedad será la encargada de organizar los elementos dentro de nuestro contenedor a través del main-axis (de forma horizontal en el caso de la imagen).

Valores aceptados:

### **justify-content: flex-start;**

[codepen\_embed height=&#8221;265&#8243; theme\_id=&#8221;0&#8243; slug\_hash=&#8221;PRemLd&#8221; default\_tab=&#8221;result&#8221; user=&#8221;h3dx0&#8243;]See the Pen <a href=&#8217;https://codepen.io/h3dx0/pen/PRemLd/&#8217;>ju-co:flsart</a> by Robert (<a href=&#8217;https://codepen.io/h3dx0&#8242;>@h3dx0</a>) on <a href=&#8217;https://codepen.io&#8217;>CodePen</a>.[/codepen_embed]

Al aplicar esta propiedad puede que no se vea ningún efecto de inicio dado que nuestro menú en el ejemplo ya tiene asignada la propiedad **flex-direction: row** desde un inicio acomodando los elementos uno al lado del otro,  lo que se quiere lograr es que los elementos se acomoden donde comienza el contenedor que en este caso es de izquierda a derecha.

### **justify-content: center;**

[codepen\_embed height=&#8221;265&#8243; theme\_id=&#8221;0&#8243; slug\_hash=&#8221;ZxoKNb&#8221; default\_tab=&#8221;result&#8221; user=&#8221;h3dx0&#8243;]See the Pen <a href=&#8217;https://codepen.io/h3dx0/pen/ZxoKNb/&#8217;>justcont:center</a> by Robert (<a href=&#8217;https://codepen.io/h3dx0&#8242;>@h3dx0</a>) on <a href=&#8217;https://codepen.io&#8217;>CodePen</a>.[/codepen_embed]

Aplicando esta propiedad vemos como todos los elementos se centran teniendo en cuenta el main-axis que en este caso es en forma horizontal.

### **justify-content: flex-end;**

[codepen\_embed height=&#8221;265&#8243; theme\_id=&#8221;0&#8243; slug\_hash=&#8221;gezWJd&#8221; default\_tab=&#8221;result&#8221; user=&#8221;h3dx0&#8243;]See the Pen <a href=&#8217;https://codepen.io/h3dx0/pen/gezWJd/&#8217;>justcont:flexend</a> by Robert (<a href=&#8217;https://codepen.io/h3dx0&#8242;>@h3dx0</a>) on <a href=&#8217;https://codepen.io&#8217;>CodePen</a>.[/codepen_embed]

Flex-end nos ayuda a alinear nuestros elementos al final de nuestro contenedor en este caso hacia la derecha. Lo que anteriormente lograríamos usando floats.

&nbsp;

### **justify-content: space-between;**

[codepen\_embed height=&#8221;265&#8243; theme\_id=&#8221;0&#8243; slug\_hash=&#8221;JLvNQN&#8221; default\_tab=&#8221;result&#8221; user=&#8221;h3dx0&#8243;]See the Pen <a href=&#8217;https://codepen.io/h3dx0/pen/JLvNQN/&#8217;>jcspace-btween</a> by Robert (<a href=&#8217;https://codepen.io/h3dx0&#8242;>@h3dx0</a>) on <a href=&#8217;https://codepen.io&#8217;>CodePen</a>.[/codepen_embed]

Space-between es una de las propiedades que más me gustan, dada la facilidad con que se pueden dar espacios exactos (ayudándonos con el diseño responsivo en muchos casos) entre los elementos que estamos colocando. Esta propiedad coloca los elementos hacia los extremos de nuestro contenedor y el espacio restante los distribuye con los demás elementos.

### **justify-content: space-around;**

[codepen\_embed height=&#8221;265&#8243; theme\_id=&#8221;0&#8243; slug\_hash=&#8221;xWjdvq&#8221; default\_tab=&#8221;result&#8221; user=&#8221;h3dx0&#8243;]See the Pen <a href=&#8217;https://codepen.io/h3dx0/pen/xWjdvq/&#8217;>jc:space-around</a> by Robert (<a href=&#8217;https://codepen.io/h3dx0&#8242;>@h3dx0</a>) on <a href=&#8217;https://codepen.io&#8217;>CodePen</a>.[/codepen_embed]

Space-around así como space-between nos ayuda a distribuir de forma equitativa el espacio entre nuestros elementos, a diferencia de de la propiedad anterior , crea espacios iguales entre todos los elementos así como con los límites de nuestro contenedor.

## Alinear elementos según cross-axis

### align-items:

Esta propiedad será la encargada de organizar los elementos dentro de nuestro contenedor a través del cross-axis (de forma vertical en el caso de la imagen).

### Valores aceptados:``

### align-items: flex-start:

###<img class="alignnone size-full wp-image-89" src="http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/02/ag-start.png" alt="" width="640" height="400" srcset="http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/02/ag-start.png 640w, http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/02/ag-start-300x188.png 300w" sizes="(max-width: 640px) 100vw, 640px" /> 

### align-items: flex-end;

<img class="alignnone size-full wp-image-92" src="http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/02/ag-end-1.png" alt="" width="640" height="400" srcset="http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/02/ag-end-1.png 640w, http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/02/ag-end-1-300x188.png 300w" sizes="(max-width: 640px) 100vw, 640px" /> 

### align-items: center;

<img class="alignnone wp-image-93 size-full" src="http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/02/ag-center.png" alt="alinear elementos" width="640" height="400" srcset="http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/02/ag-center.png 640w, http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/02/ag-center-300x188.png 300w" sizes="(max-width: 640px) 100vw, 640px" /> 

### align-items: strech;

<img class="alignnone wp-image-95 size-full" src="http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/02/ag-strech-1.png" alt="alinear elementos" width="640" height="400" srcset="http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/02/ag-strech-1.png 640w, http://localhost/~h3dx0/wordpress/wp-content/uploads/2018/02/ag-strech-1-300x188.png 300w" sizes="(max-width: 640px) 100vw, 640px" /> 

Estas son las principales propiedades para poder controlar la ubicación de todos los elementos dentro de nuestro contenedor. Muchas de estas propiedades están sujetas a como orientemos nuestros main-axis y cross-axis. Estas son algunos de los resultados que ahora con flexbox se puede lograr de forma mas sencilla.

Muchas gracias por su lectura. Espero que les sirva este artículo para que puedan comenzar a usar estas fantásticas propiedades y atributos.

No lo dudes y regálame un simple GRACIAS.