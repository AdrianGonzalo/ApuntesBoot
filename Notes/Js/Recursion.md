# RECURSION JS
## Que es?
La recursion es cuando una función sigue llamandose a si misma, hasta que ya no tiene que hacerlo

El caso base es la condicion que le dice a la funcion cuando dejar de llamarse a si misma

## Ejemplos de Recursion

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

### Que ha pasado?

Lo primero que se hizo fue definir el *caso base* porque la funcion necesita saber cuando dejara de llamarse a si misma  ⬇
```
if (numero === 0) {
        return;
    }
```
Sino le decimos a la funcion cuando detenerse pasara algo llamado stackoverflow, la pila se va a llenar de funciones que se estan llamando, pero no regresan

La parte de recursión sucede en la línea 7
```
return cuentaAtras(numero - 1);
```
Donde le decimos a la funcion que siga regresando, pero reduciendo sus entradas cada vez que regresa.

Paso a paso esto es lo que sucede:
```
1// La entrada actual es 5
2// Es 5 igual a 0 ?
3// No, Ok entonces imprime 5 en la consola.
4// Se llama asi misma de nuevo con el numero - 1 O 5 - 1;
5// La entrada principal es 4
6// Es 4 igual a 0 ?
7// No, Ok entonces imprime 4 en la consola.
8// Repite hasta que la entrada sea 0, y asi la función deja de llamarse a si misma.
```
Ejemplos y explicacion sacados de [freeCodeCamp](https://www.freecodecamp.org/espanol/news/como-entender-recursividad-en-javascript/)