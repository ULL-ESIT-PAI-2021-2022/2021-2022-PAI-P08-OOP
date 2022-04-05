# Práctica 8. Programación Orientada a Objetos en Javascript
### Factor de ponderación: 7

### Objetivos
Los objetivos de esta práctica son:
* Poner en práctica metodologías y conceptos de Programación Orientada a Objetos en JavaScript.

### Rúbrica de evaluacion del ejercicio
Se señalan a continuación los aspectos más relevantes (la lista no es exhaustiva)
que se tendrán en cuenta a la hora de evaluar esta práctica:
* Se valorará la realización de las diferentes tareas que se proponen
* El comportamiento del programa debe ajustarse a lo solicitado en este enunciado.
* Capacidad de la programadora de introducir cambios en el programa desarrollado.
* Deben usarse estructuras de datos adecuadas para representar los diferentes elementos que intervienen en el problema
* Acreditar que se sabe generar informes de cubrimiento de código utilizando tanto 
[Jest](https://jestjs.io/)
como
[CodeCov](https://docs.codecov.com/docs)
* Ante la presencia de bugs, el alumnado sabe utilizar el depurador de Visual Studio Code
* Saber corregir bugs en un programa utilizando el depurador de Visual Studio Code
* Ser capaz de desarrollar tests unitarios para sus programas utilizando 
[Jest](https://jestjs.io/)
* Acreditar su capacidad para configurar y utilizar 
[ESLint](https://eslint.org/)
  y que es capaz de trabajar con la misma en Visual Studio Code.
* El código ha de estar documentado con 
[JSDoc](https://jsdoc.app/). 
  y que es capaz de generar documentación para sus programas utilizando la herramienta.
  Haga que la documentación del programa generada con JSDoc esté disponible a través de una web alojada en su máquina IaaS de la asignatura.
* Acreditar que sabe depurar sus programas usando Visual Studio Code.
* Ser capaz de resolver problemas de la plataforma Exercism, subiendo sus soluciones a la misma.
* Acreditar que es capaz de desarrollar y ejecutar programas simples de la plataforma Jutge
* Se comprobará que el código que el alumnado escribe se adhiere a las reglas de la 
[Guía de Estilo de Google para Javascript](https://google.github.io/styleguide/jsguide.html).
* Acreditar que es capaz de editar ficheros de forma remota en su VM usando Visual Studio
  Code (VSC)

### Indicaciones de caracter general
En esta práctica y las siguientes se promoverá el uso del paradigma orientado a objetos.
Así pues los programas estarán organizados en torno a clases que se han de implementar usando la sintaxis para
clases de JavaScript y poniendo en práctica los principios de abstracción y encapsulamiento característicos 
de la Programación Orientada a Objetos.
Vigile siempre el tipo de visibilidad que elige para los atributos (properties) de sus clases
y tenga en cuenta tanto las reglas de 
[estilo](https://google.github.io/styleguide/jsguide.html#features-classes)
como las 
[etiquetas JSDoc](https://stackoverflow.com/questions/41715994/how-to-document-ecma6-classes-with-jsdoc)
relacionadas con el constructo 'class'.

Configure para esta práctica una página web que sirva de índice para mostrar la documentación generada por
JSDoc para todos los programas que desarrolle.

Configure un fichero `package.json` en el directorio raíz de su repositorio de modo que ejecutando 
`npm install` queden instaladas todas las dependencias de su proyecto.
Revise la información en
[What is the file package.json?](https://nodejs.org/en/knowledge/getting-started/npm/what-is-the-file-package-json/#:~:text=All%20npm%20packages%20contain%20a,as%20handle%20the%20project's%20dependencies.).

### 1.- La clase *Clock*
En este ejercicio se propone desarrollar un módulo ES6 que implemente una clase `Clock` 
para representar un reloj digital con horas y minutos. No es necesario contemplar segundos.

La clase no ha de usar en modo alguno objetos 
[Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)
de JavaScript y se desarrollará usando la sintaxis para clases de JavaScript y poniendo en práctica los principios de
abstracción y encapsulamiento característicos de la Programación Orientada a Objetos.

La clase ha de contener un método *toString()* que permita imprimir en pantalla un objeto *Clock* en el
formato `hh:mm`.
La clase ha de contemplar métodos que permitan sumar y restar minutos a un objeto *Clock*.
Análogamente, dos objetos que representen la misma hora deben ser iguales entre sí.
Incluya discrecionalmente cualesquiera otras operaciones que considere adecuadas como métodos en la clase `Complejo`.

Previo a la implementación de la clase, diseñe y desarrolle un conjunto de tests para probar el correcto
funcionamiento de todos los métodos de la clase.

Encapsule la clase en un módulo que exporte la misma hacia otros programas clientes que pudieran utilizarla.

Desarrolle un programa *cliente* que utilice la clase *Clock* e instancie objetos de esa clase:
```javascript
const horaActual = new Clock(11, 59);
console.log(horaActual.toString());   // 11:59h
```

### 2.- La clase *Complejo*
Un
[número complejo](https://es.wikipedia.org/wiki/N%C3%BAmero_complejo)
puede representarse como la suma de un número real y un número imaginario, de la forma `a + bi` donde el
término `a` es la parte real, `b` la parte imaginaria e `i` la
[unidad imaginaria](https://es.wikipedia.org/wiki/Unidad_imaginaria).

En este ejercicio se propone desarrollar un módulo ES6 que implemente una clase `Complejo` que permita operar con números complejos.
La clase se desarrollará usando la sintaxis para clases de JavaScript y poniendo en práctica los principios de
abstracción y encapsulamiento característicos de la Programación Orientada a Objetos.

La clase ha de contener al menos métodos que permitan las siguientes operaciones con números complejos:

* `print` Imprimir un número complejo 
* `add` Sumar 
* `sub` Restar
* `mul` Multiplicar
* `div` Dividir
* `abs` Calcular el valor absoluto
* `conj` Calcular el conjugado de un número complejo

Incluya discrecionalmente cualesquiera otras operaciones que considere adecuadas como métodos en la clase `Complejo`.

Previo a la implementación de la clase, diseñe y desarrolle un conjunto de tests para probar el correcto
funcionamiento de todos sus métodos.

Desarrolle un programa cliente `complejos.js` que permita operar con números complejos y haga uso de la clase `Complejo` que diseñe.
El programa cliente definirá un par de números complejos `-1-5i` y `1+i` y realice todas las operaciones
anteriores utilizando ambos números como operandos.


### Ejercicios de Exercism
Resuelva los siguientes problemas ejecutando los tests correspondientes a cada uno de ellos hasta conseguir
que todos pasen correctamente. 
Una vez que lo logre, suba su solución a Exercism.
* [Strain](https://exercism.org/tracks/javascript/exercises/strain). 
  Las funciones que ha de programar, *keep()* y *discard()* toman ambas dos parámetros, 
  un array y una función booleana (un predicado) y devuelven un array que contiene (keep) o no (discard) los elementos del array de entrada para los que el predicado es cierto.
* [Yacht](https://exercism.org/tracks/javascript/exercises/yacht)
  Si analiza el programa que realiza los tests (`yacht.spec.js`) observará que la función *score()* ha de tener dos parámetros: 
  un array con las puntuaciones de los lanzamientos de 5 dados y una cadena (string) con el nombre de la jugada y ha de devolver 
  la puntuación correspondiente a esa jugada.

## Referencias
* [Using ES modules in Node.js](https://blog.logrocket.com/es-modules-in-node-today/)
* [CodeCov](https://docs.codecov.com/docs)
* [Jest](https://jestjs.io/)
* [ESLint](https://eslint.org/)
* [JSDoc](https://jsdoc.app/)
* [The Modern Javascript Tutorial](https://javascript.info)
* [PAI Code Examples](https://github.com/ULL-ESIT-PAI-2021-2022/PAI-class-code-examples/tree/master/src)
* [Google JavaScript Style Guide](https://google.github.io/styleguide/jsguide.html)