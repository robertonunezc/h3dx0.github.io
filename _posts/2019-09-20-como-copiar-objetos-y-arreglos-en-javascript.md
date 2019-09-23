---
id: 146
title: Como copiar objetos y arreglos en javascript
date: 2019-09-19T02:45:30+00:00
author: robert
layout: post
permalink: /como-copiar-objetos-y-arreglos-en-javascript/
categories:
- Javascript
- Arreglos
- Frontend
- How To
tags:
- javascript
- frontend
- arreglos
- arrays
---
Hace unos días trabajando en un proyecto con VueJS tuve la necesidad de ver como copiar un arreglo para modificarlo en 
el componente hijo.(Si no conoces VueJS, date una vuelta por su web, es una librería increible para Javascript).

En Javascript los arreglos y objetos son creados por referencia, esto quiere decir lo siguiente.

```javascript
let frutas = ["platano", "fresa"]
let mercado = frutas
console.log(frutas, mercado)

mercado[2] = "manzanas"

console.log(frutas, mercado)

Array(3) [ "platano", "fresa", "manzanas" ]

Array(3) [ "platano", "fresa", "manzanas" ]
```
Aquí tenemos el problema, el arreglo frutas original también se modificó, por lo que necesitamos hacer que las copias de nuestro arreglo de frutas sean independientes.

## Solución
```javascript
let frutas2 = [].concat(frutas)
frutas2[3] = "peras"
console.log(frutas, frutas2)

Array(3) [ "platano", "fresa", "manzanas" ] 
Array(4) [ "platano", "fresa", "manzanas", "peras" ]
````
## Solución 2 usando Spread Operator de ES6
```javascript
const frutas3 = [...frutas]
frutas3[3] = "peras"
console.log(frutas, frutas3)

Array(3) [ "platano", "fresa", "manzanas" ] 
Array(4) [ "platano", "fresa", "manzanas", "peras" ]
````
<a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax" target="_blakn">
	Aquí
</a> les dejo el enlace de la explicación detallada de Spread Operator. 

## Una más
```javascript
const frutas4 = Array.from(frutas)
frutas4[3] = "mango"
console.log(frutas, frutas4)
Array(3) [ "platano", "fresa", "manzanas" ] 
Array(4) [ "platano", "fresa", "manzanas", "mango" ]
````
Si quieren investigar más sobre *Array.from* este es el <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/from">enlace</a>

Hasta aquí vimos varias vias de copiar arreglos para modificarlos nuevos.


Con los objetos tenemos el mismo problema pues se copian pero se mantiene la referencia entre
los objetos creados.

## Problema
```javascript

let persona = {
	nombre: 'Juan',
	edad: 25,
}
let persona2 = persona
console.log(persona, persona2)

persona2.nombre = "Pedro"
console.log(persona, persona2)

Object { nombre: "Pedro", edad: 25 } 
Object { nombre: "Pedro", edad: 25 }
````
Vemos como al modificar nuestro objeto *persona2* el objeto original *persona* también es modificado.
## Solución

```javascript

const persona3 = JSON.parse(JSON.stringify(persona));
persona3.nombre = "Pedro";
console.log(persona, persona3)

//Resultado
Object { nombre: "Juan", edad: 25 }
Object { nombre: "Pedro", edad: 25 }
````
Hay otras soluciones pero para mi esta es la que mejor me ha funcionado.

Espero les sea útil y cualquier comentario es bienvenido. 🙂

