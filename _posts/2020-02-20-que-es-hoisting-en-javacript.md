---
id: 98
title: Que es hoisting en javascript
date: 2020-02-20
author: robert
layout: post
permalink: /que-es-hoisting-en-javascript/
categories:
- Javascript
- Frontend
tags:
- javascript
- frontend
- arrays
---
Hola y bienvenidos a este rinconcito de internet donde comparto lo que voy aprendiendo en el día a día como desarrollador web.
Hoy quisiera hacerles una breve introducción a uno de los conceptos que enfrentamos cuando comenzamos a aprender JAVASCRIPT y el es HOSTING.
<!--more-->

## ¿Que es HOISTING?

Hoisting es un problema que ocurre cuando se declaran variables después de usarlas, me dirán muchos eso es imposible no tiene sentido, pero si puede ocurrir y el motor de JS lo permite, pongo un ejemplo:
```javascript
console.log(mensaje);
var mensaje = “Hola a todos”;
```

Este código no arroja error,  esto se debe a que la declaración de la variable se hace primero en el motor de JS y posteriormente se ejecuta la asignación de los valores a la misma. 

```javascript
var mensaje;
console.log(mensaje);
mensaje = “Hola a todos”;
```
En esa secuencia es  como  se ejecuta el código y a ese comportamiento se le llama HOISTING.

### Como evitar el HOISTING?

La principal medida es usar **let** y **const** para crear nuestras variables a la hora de programar en JS.
Otra regla general que podemos optar es siempre declarar nuestras variables al inicio de nuestro scope, esto nos va a ayudar a evitar el hoisting en caso que usemos var para declarar las variables.

```javascript
let libreria = “Alamos”;
let cantidadLibros = 50;
const descuento = 10;
```

Es una muy breve explicación pero espero les sirva como introducción al tema.



