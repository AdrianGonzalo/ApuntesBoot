# BOOTCAMP

# 2024_03_18 dia 1

    Presentaciones

    CEO: Mike

    Profesores: Manu

    Profesores adjuntos: Flors, Marta.  

    HR: Carmen

    Modelos de trabajo que usaremos para maximizar la eficiencia

        -Agil: es un enfoque de gestión de proyectos que se centra en la entrega continua de valor al final del proyecto. Este enfoque permite a los equipos responder a la incertidumbre a través de iteraciones cortas de trabajo, conocidas como sprints.

        -Scrum: es un marco dentro del enfoque Agile que se utiliza para desarrollar, entregar y mantener productos complejos. En Scrum, el trabajo se divide en pequeñas partes manejables conocidas como sprints. El progreso se rastrea y se reevalúa en reuniones diarias de Scrum.

# 2024_03_19 dia 2

    Markdown: lenguaje que tiene la finalidad de permitir crear contenido de una manera sencilla de escribir manteniendo un diseño legible

    Stack Overflow
    Chat Gpt

    2 tipos de datos

    -No Mutantes/Primitivos (Stack  memoria rapida)

        ·Numbers (numeros)

        ·Strings (cadena de texto)

        ·Boolean: representa o verdadero o falso (TRUE / FALSE)

        ·Null: ausencia de valor

        ·Undefined: representa una variable definida pero sin valor

        ·Symbol: valor unico e inmutable




    -Mutantes/Objetos (Heap  memoria compleja)

    ·Object: coleccion de pares clave-valor

        -clave: cadenas o simbolos

        -valor: cualquier tipo de dato

    ·Array: coleccion ordenada de valores

    ·Function: bloque de codigo reutilizable que se puede llamar para realizar una tarea especifica

    ·Date: instante especifico en el tiempo

    ·RegExp: Representa un patrón de búsqueda dentro de una cadena de texto

![alt text](image-2.png)

# 2024_03_20 dia 3

#### Uso del debugger

    -F10 : sigue de forma ordenada el codigo

    -F9 : se mete dentro del objeto, array...

## Uso de la terminal y sus comandos (Ctrl + J)

## Comandos de navegacion y visualizacion

    ·pwd: donde se ubica el archivo abierto

    ·ls: carpetas de usuario

    ·ls-l: fechas, permisos de las carpetas

        ·drwx
            d: directory
            r: read
            w: write
            x: execute

    ·ls-a: archivos ocultos (carpeta de usuario)

    ·cd "x": cambiar de directorio

    ·cd.. : retrocede un paso del directorio

    ·cd~ : cambia al directorio de inicio del usuario

## Comandos de Manipulacion de Archivos y Directorio 

    ·mkdir: crear carpeta

    ·mkdir -p "staff/adrian-martin":crear 2 carpetas de trabajo

    ·cp "archivo origen" "archivo destino": copia un archivo o directorio

    ·touch "staff/adrian-martin/.gitignore": crear fichero vacio ( ejemplo de fichero oculto para ocultar archivos a git)

    ·cat "staff/adrian-martin/.gitignore": ver contenido

    ·mv "archivo origen" "archivo destino: mueve archivo o directorio

    ·rm "archivo" : elimina un archivo

    ·rm -r "directorio": elimina un directorio y su contenido

## Otros comandos

    ·Ctrl + N : limpiar la terminal

    ·history: muestra historial de comandos usados

    ·man [comando]: Muestra el manual de un comando específico.

# Comandos de Git

    ·git init: inicia un repositorio en el directorio actual

    ·git add "staff/adrian-martin/.gitignore": introduce la copia en git

    ·git commit -m "comentario de que se esta haceindo ": guardar

    ·git push: sube los commits locales al origin

    ·git pull: descarga los cambios desde el repositorio remoto y losfusiona con tu rama local

    ·git fetch: descarga los cambios desde el repositorio remoto, pero no los fusiona automáticamente con tu rama local.

    ·git log: ves los commit(cambios)

    ·git clone(url): copiar en la carpeta asignada

    ·git branch: ver ramas de trabajo(main/develop...)

    ·git branch "develop": crea rama de trabajo(expl:develop)

    ·git switch "develop": cambia de rama(expl:en este caso a develop creada anteriormente)

    ·git checkout: se mete dentro de la rama creada

    ·git status: informacion de la carpeta respecto a git

    ·git rebase: combina trabajo, conjunto de commits, los copia y aplica a otro lafo

    ·git mv: mover un archivo

    ·git diff: sirve para ver cambios y comparar

    ·git merge "nombre de la rama":fusiona la rama especificada con la rama actual

    ·git reset "hash": reset el comit al commit que se indica

    ·git branch -D "nombre de la rama": borra su totalidad

## Comandos para deshacer cambios

    ·git checkout -- [archivo(s)]**: Descarta los cambios en los archivos modificados y los restaura a su último estado confirmado.

    ·git revert [hash_del_commit]**: Crea un nuevo commit que deshace los cambios introducidos por el commit especificado.

# 2024_03_21 dia 4

    Git WorkFlolw: recomendacion de como usar GIt para realizar el trabajo de manera productiva.

#### Cambiar fichero (gitignore) y subir a git

    1. hacer las modificaciones

    2. git status  (para comprobar) 

    3. git add "staff/adrian-martin/.gitignore"

    4. git status  (para comprobar)

    5. git commit -m "edit St_Storage #7"

    6. git log  (para ver si el commit se ha guardado)

    7. git push

#### Cambiar nombre carpeta y subir cambios

    1. renombrar carpeta

    2. git add

    3. git status  (para comprobar)

    4. git commit -m "edit the name"

    5. git log para ver si el commit se ha guardado

    6. git push

#### Quitar ultimo commit

    1. git log

    2. copiar codigo del commit que queremos cambiar (origin)
    
    3. git reset y pegamos el codigo

    4. limpar

    5. git status

# 2024_03_25 dia 5

#### Metodos de estudio

    · Metodo Phomodoro: método de gestión de tiempo que sugiere trabajar en intervalos de 25 minutos, sin interrupción ni distracciones, y añadir tiempos de descanso de 5 minutos.

    · Metodo del patito: consiste en explicar en voz alta a un patito de goma cada línea de código y el por qué la estamos usando. 

Console.dir(): muestra una lista interactiva de las propiedades del objeto JavaScript especificado

#### Document

    ·querySelector(): selecciona un elemento ya existente ('tittle'...)

    ·createElement(): crea un elemento en el html ('h2', 'p'...)

    ·appendChild(): agregar nuevos elementos a un documento existente o para mover un elemento de la página.

# 2024_03_26 dia 6

### Code workspace/isdi-parttime-202403/ entra al code con la carpeta desde terminal

#### Como hacer un reset

    1. copiamos el hash de donde queremos partir

    2. reset + hash

    3. git log para comprobar


Para renombrar un commit ya renombrado usamos --amend -m ""

#### Box Model 2 tipos de cajas

(Estas caracteristicas se refieren al modo como se comporta la caja en terminos de flujo de página y en relacion con otras cajas)

    ·Caja en bloque:

        · fuerza un salto de linea al llegar al final de la linea
        
        · se respetan las propiedades width y heigth

        · el relleno, el margen y el borde mantienen a los otros elementos alejados de la caja

        · la caja se extendera en direccion de la linea para llenar todo el espacio disponible, la caja sera tan ancha como su contenedor

        . Ejml: <h1>, <p>....

    ·Caja en linea:

        · la caja no fuerza ningun salto de linea

        · las propiedades width y heigth nop se aplican 

        · se aplica relleno, margen y bordes verticales, pero no mantienen alejadas otras cajas de linea 

        · se aplica relleno, margen y bordes horizontales y mantienen alejadas otras cajsa en linea

        ·Ejml: <span>, <a>...

Favicon: es una pequeña imagen asociada con una página o sitio web en particular.

### Enagrama de Client-Server

![alt text](image-1.png)

### Libreria de Css, Html y Js   Mozilla Mmdn

# 2024_03_27 dia 7

## Continuamos con el trabajo de del cV haciendolo todo en Js

#### Poner estilos desde Js: 

    ·document.body.style.textDecoration = 'overline''underline'

    ·classList.add('overline'...)

#### Poner tipografia desde JS

    ·let fontLink = document.createElement('link')

    ·fontLink.href = 'url'

    ·fontLink.rel = 'stylesheet'

    ·document.head.appendChild(fontLink)
    
#### Poner el * de css desde Js

    ·let style = document.createElement('style')

    ·style.innerHTML = 'body { background-color: black; margin: 5vw; font-family: Workbench; color: greenyellow;}

        ⬆ en la misma linea

    .document.head.appendChild(style)

### Git Fetch

El comando git fetch descarga confirmaciones, archivos y referencias desde un repositorio remoto a su repositorio local. Buscar es lo que haces cuando quieres ver en qué han estado trabajando todos los demás.

# 2024_03_28 dia 8

## CSS Colornames

Pagina para ver los colores propios de Css, los navegadores modernos  admiten 140 nombres de colores.

## FlexBox 

Flexbox es un método de diseño de página unidimensional para compaginar elementos en filas o columnas.

    ·Eje principal:

        -flex-direction:
            
            -row: el eje principal correra a lo largo de la fila segun la direccion de linea

            -row-reverse: el eje principal correra a lo largo de la fila segun la direccion de linea

            -column: el eje principal correrá desde el borde superior de la página hasta el final, segun la direccion del bloque

            -column-reverse: el eje principal correrá desde el borde superior de la página hasta el final, segun la direccion del bloque

    ·Eje cruzado: El eje cruzado va perpendicular al eje principal

## Uso de Snippets en F12 de navegador

# Tarea Finde 29-1 (4dias)

    - CHECK  Terminar el resumen de los dias de la semana 

    - CHECK  Seguir FreeCodeCamp

    - CHECK  Terminar ranas

    - CHECK  Terminar regar jardin

    - CHECK  Pasar CV a js 

    - CHECK  Hacer resumen de display, flex, position, gap, justify, align...

    - CHECK  Terminar cerdito y demas 

    - CHECK  Intentar ejercicio de recursion

    - CHECK  Poner bonito y ordenado los markdown

# 2024_04_2 dia 9


## Hosting

El Hosting se refiere al comportamiento de la declaraciones de variables, funciones y clases que se mueven a la parte superior, todo antes de la ejecucion del codigo, a su vez nos permite utilizar funciones, variables y clases antes de que sean declaradas

### Hosting con VAR

Cuando el intérprete hace hoisting de una variable declarada con var, inicializa su valor a undefined
```
console.log(foo); // undefined

var foo = 'bar';

console.log(foo); // "bar"
```
### Hosting con Const y Let

...

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

Es decir, tenemos un **clousure**

### IIFE - Immediately-invoked Function Expression

Es una tecnica utilizada mucho en ES% para implementar el patron de diseño de "modulo", la idea es `envolver` tu modulo en una funcion que es inmediatamnete ejecutada

Informacion sacada de [freeCodeCamp](https://www.freecodecamp.org/espanol/news/que-es-un-closure-en-javascript/)


# 2024_04_3 dia 10
Ejemplos de loop y callback

## Metodos de Array 

+ ForEach: Ejecuta la función indicada una vez por cada elemento del array.

    Callback: Funcion a ejecutar por cada elemento, que recibe 3 argumnetos:

        currentValue: Elemento actual siendo procesado en el array

        index(opcional): El índice del elemento actual siendo procesado en el array

        array(opcional): El vector en el que forEach() esta siendo aplicado

    Retorno: Undefined


+ Map:  Crea un nuevo array con los resultados de la llamada a la función indicada aplicados a cada uno de sus elementos.

    Callback: Función que producirá un elemento del nuevo array, recibe tres argumentos:

        currentValue: Elemento actual siendo procesado en el array

        index(opcional): El índice del elemento actual siendo procesado en el array

        array(opcional): El array sobre el que se llama map.

    Retorno: Un nuevo array en la que cada elemento es el resultado de ejecutar callback.


# 2024_04_4 dia 11

Copilot AI: es un asistente virtual de inteligencia artificial desarrollado por Microsoft que está disponible en Windows 11

Web components: Los componentes web son un conjunto de características que actualmente están siendo añadidas por el W3C a las especificaciones HTML y DOM de forma que permite la creación de widgets o componentes reutilizables en documentos y aplicaciones web.

Console.assert(): Aparece un mensaje de error en la consola si la afirmación es falsa. Si la afirmación es verdadera, no aparecerá nada.

# Tarea Finde 5-7 (3dias)

    - CHECK  Terminar el resumen de los dias de la semana 

    - CHECK  Seguir FreeCodeCamp

    - CHECK  Repasar recursion

    - CHECK  Crear md de conceptos

    - CHECK  Crear md de metodos de array

    - CHECK  Hacer el print-dom-tree again

    - CHECK  TSeguir dibujando

    - CHECK  Intentar metgodos

# 2024_04_8 dia 12

Arguments: Es un objeto similar a Array accesible dentro de funciones que contiene los valores de los argumentos pasados a esa función.

TC39: Es el lugar donde cualquiera puede proponer un cambio para mejorar javaScript

# 2024_04_9 dia 13

Ternaty operator: Un operador ternario evalúa la condición de prueba y ejecuta un bloque de código basado en el resultado de la condición.

+ Slice:  Devuelve una copia de una parte del array dentro de un nuevo array empezando por inicio hasta fin

        Inicio: Indice donde empieza la extraccion, el primer elemento corresponde con el indice 0

        Fin: Indice que marca el final de la extraccion

    Retorno: Un nuevo array con los valores extraidos

# 2024_04_10 dia 14

# Operador condicional Ternario
```
condición ? expr1 : expr2
```
Condicion: expresion que se evalua como true o false
expr1... expresion con valores de algun tipo

### Descripcion

Si la `condicion` es `true`, el operador retornara el valor de `expr1`; de lo contrario, devuelve `expr2`.
```
"La Cuota es de:  " + (isMember ? "$2.00" : "$10.00");
```
# Funciones Constructoras

Una función Constructora es un “template” o estructura pre-armada de un objeto con sus propiedades preparados para asignarles un valor.
```
function Person(name, age){
    this.name = name
    this.age = age
}

Person.prototype
{}

var p = new Person ('Peter',21)
p
Person { name: 'Peter', age: 21}

var e = new Person ('Esme', 22)
e
Person {name: 'Esme', age: 22}

var j = new Person ('Jesus', 28)
j
Person {name: 'Jesus', age: 28}

Person.prototype.fart = function() { return this.name + ': 💨'}
p.fart
'Peter: 💨'

Person.prototype.pee = function() { return this.name + ': 💦'}
p.pee
'Peter: 💦'

Person.prototype.poo = function() { return this.name + ': 💩'}
p.poo
'Peter: 💩'
```
# 2024_04_10 dia 14