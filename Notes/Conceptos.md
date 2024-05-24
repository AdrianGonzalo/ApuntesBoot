# CONCEPTOS

## Console
El metodo Console proporciona varios metodos para la salida de informacion en la consola del navegador o en la consola de desarrollo de herramientas.
```
.log() => Imprime mensajes de registro en la consola

.debug() => Imprime mensajes de depuracion en la consola

.info() => Muestra un mensaje de informacion en la pantalla

.error() => Muestra un mensaje de error en la consola

.table() => Muestra una tabla a partir de un objeto o matriz

.clear() => Borra la consola
```
## TDD-Test-Driven-Development
Test-Driven-Development (TDD) se refiere a un estilo de programacion en el que tres actividades estan estrechamente entrelazadas: codificacion, pruebas y diseño
## Git Fetch
El comando git fetch descarga confirmaciones, archivos y referencias desde un repositorio remoto a su repositorio local. Buscar es lo que haces cuando quieres ver en qué han estado trabajando todos los demás.
[imagen](https://www.google.com/imgres?q=Git%20Fetch&imgurl=https%3A%2F%2Fwac-cdn.atlassian.com%2Fdam%2Fjcr%3Af8458bba-d80a-457e-98f5-3544679eb16b%2F01%2520Synchronize%2520origin%2520with%2520git%2520fetch.svg%3FcdnVersion%3D1528&imgrefurl=https%3A%2F%2Fwww.atlassian.com%2Fgit%2Ftutorials%2Fsyncing%2Fgit-fetch&docid=w0CoHIUVUPe_vM&tbnid=3l4h1E1tKFSbsM&vet=12ahUKEwjt9NWZtKiFAxWkQEEAHYvkAL4QM3oECBkQAA..i&w=800&h=377&hcb=2&ved=2ahUKEwjt9NWZtKiFAxWkQEEAHYvkAL4QM3oECBkQAA)
## IIFF-Immediately-invoked-Function-Expression
Es una tecnica utilizada mucho en ES% para implementar el patron de diseño de "modulo", la idea es `envolver` tu modulo en una funcion que es inmediatamnete ejecutada
```
(function loop(count){

  if (count > 3)
    return

  console.log(count)

  loop(count + 1)

  if (count === 0)

})(0)
```
## Node
NOde.js es un entorno en tiempo de ejecucion multiplataforma, de codigo abioerto, para la capa del servidor basado en el lenguaje de programacion javaScript
## Loops
Event loop es un bucle interno de JavaScript que se encarga de manejar la cola de tareas pendientes y ejecutarlas de manera secuencial.
```
(function loop(count){
  console.log('loop', 'start', count)

  if (count > 3)
    return

  console.log(count)

  loop(count + 1)

  if (count === 0)
    return function(message) { console.log(message)}

  console.log('loop', 'end', count)
})(0)('end loop')

VM414:2 loop start 0
VM414:7 0
VM414:2 loop start 1
VM414:7 1
VM414:2 loop start 2
VM414:7 2
VM414:2 loop start 3
VM414:7 3
VM414:2 loop start 4
VM414:14 loop end 3
VM414:14 loop end 2
VM414:14 loop end 1
VM414:12 end loop
```
## Call Stack
Un Call Stack es un mecanismo para que un interprete realice un seguimiento de en que lugar se llama a multiples funciones, que funcion se esta ejecutando actualmente y que funciones son llamadas desde esa funcion 
```
function saludar() {
  // [1] Código
  diHola();
  // [2] Código
}
function diHola() {
  return "!Hola!";
}

// Invocar la función `saludar`
saludar();

// [3] Código
```
## Callback
Una función de callback es una función que se pasa a otra función como un argumento, que luego se invoca dentro de la función externa para completar algún tipo de rutina o acción.
```
function saludar(nombre) {
  alert("Hola " + nombre);
}

function procesarEntradaUsuario(callback) {
  var nombre = prompt("Por favor ingresa tu nombre.");
  callback(nombre);
}

procesarEntradaUsuario(saludar);
```
## Recursion
La recursion es cuando una función sigue llamandose a si misma, hasta que ya no tiene que hacerlo.El caso base es la condicion que le dice a la funcion cuando dejar de llamarse a si misma
Lo primero es entender lo que queremos que haga nuestro programa
```
Cuenta regresiva desde un número dado hasta el número más pequeño, restando 1 cada vez que pasa por el bucle.

Dado el numero 5, deberia de ser algo asi:

  5
  4
  3
  2
  1

Ejemplo de lo anterior con recursión

  let cuentaAtras = numero => {
      //base case
      if (numero === 0) {
          return;
      }
      console.log(numero);
      return cuentaAtras(numero - 1);
  };
  console.log(cuentaAtras(5)) // 5, 4, 3, 2, 1
```
## Closure
El uso del CLosure es algo confuso debido a que es "invisible", aprender closure es mas sobre identificar caundo se usa que aprender un nuevo concepto en si
```
function miFuncion() {
    let count = 1
    function contador() {
        console.log(count)
    }
    contador() // imprime 1
}
```
Ahora tenemos una funcion `contador` que utiliza un `valor` que fue declarado fuera de esa funcion `count`, y un valor `count` que fue declarado en la funcion `miFuncion` pero que es usado dentro de la funcion `contador`
## Hosting
El Hosting se refiere al comportamiento de la declaraciones de variables, funciones y clases que se mueven a la parte superior, todo antes de la ejecucion del codigo, a su vez nos permite utilizar funciones, variables y clases antes de que sean declaradas

+ Hosting con VAR

Cuando el intérprete hace hoisting de una variable declarada con var, inicializa su valor a undefined
```
console.log(foo); // undefined

var foo = 'bar';

console.log(foo); // "bar"
```
+ Hosting con Const y Let

...
## Lexical Scope
El lexical Scope es un concepto fundamental en programacion, que determina la accesibilidad de varialbes y funciones dentro de un programa.

Esta determinado por la ubicacion de variables y funciones en el codigo y permanece igual durante toda la ejecucion del programa.

Se pude acceder a las variables globales desde cualquier lugar dentro del programa, mientras que las variables locales solo e puede acceder dentro de la funcion o bloque en el que estan definidas

**Variables Globales**: Son variables que se definen fuera de las funciones, cualquier funcion puede acceder a ellas directamente.

    
    let name = "John"; // Global variable 
  
    function sayHello() { 
        console.log("Hello " + name); 
    } 
        
    sayHello(); // Output: "Hello John"
    
**Variables Locales**: Son variables que se definen dentro de funciones, solo se pueden usar dentro de las funciones que los definen.

    function sayHello() { 
    let name = "John"; // Local variable 
    
    console.log("Hello " + name); 
    } 
        
    sayHello(); // Output: "Hello John" 
        
    console.log(name);  
    // Output: Uncaught ReferenceError: name is not defined
# InstanceOF
Permite verificar si un objeto pertenece a una clase determinada
```
color1 = new String("verde");
color1 instanceof String; // devuelve verdadero (true)
color2 = "coral";
color2 instanceof String; // devuelve falso (color2 no es un objeto String)
```
# TypeOF
Devuelve una cadena que indica el tipo del operador sin evaluarlo
```
typeof miFuncion === "function";
typeof forma === "string";
typeof 4 === "number";
typeof noExiste === "undefined";
typeof true === "boolean";
typeof null === "object";
```
# Funciones Constructoras
El constructor Function crea un nuevo objeto Function
```
const sum = new Function('a', 'b', 'return a + b');

console.log(sum(2, 6));
// Expected output: 8
```
# Operador condicional TERNARIO
El operador condicional (ternario) es el único operador en JavaScript que tiene tres operandos. Este operador se usa con frecuencia como atajo para la instrucción if
```
condición ? expr1 : expr2

condición -> Una expresión que se evalúa como true o false.

expr1, expr2 -> Expresión con valores de algún tipo.
```
