
# Array.prototype

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


+ Filter:  Crea un nuevo array con todos los elementos que cumplan la condición implementada por la función dada.

    Callback: Función que comprueba cada elemento del array para ver si cumple la condición, retorna true si el elemento la cumple o en caso contrario retornará false. Acepta tres parámetros:

        currentValue: Elemento actual siendo procesado en el array

        index(opcional): El índice del elemento actual siendo procesado en el array

        array(opcional): El array sobre el que se llama filter

    Retorno: Un nuevo array con los elementos que cumplen la condición.


+ Push:  Añade uno o mas elementos al final de un array y devuelve la nueva longitud del array

    Retorno: La nueva propiedad length del objeto sobre el cual se efectuo la llamada


+ Pop:  Elimina el último elemento de un array y lo devuelve, este metodo cambia la longitud del array

    Retorno: El elemento que ha sido eliminado del array, undefined si esta vacio


+ Find:  Devuelve el primer elemento del array que cumple la funcion de prueba proporcionada, sino devuelve undefined

    Callback: Función a ejecutar en cada uno de los valores del array hasta que devuelve true, indicando que el elemento que la cumple fue encontrado.Recibe tres argumentos:

        element: El elemento actual que se esta procesando en el array

        index(opcional): El indice del elemento actual que se esta procesando en el array

        array(opcional): El array sobre el que se llama find

    Retorno: El valor del primer elemento del array que cumple la función de prueba proporcionada; de lo contrario, devuelve undefined.


+ FindIndex:  Devuelve el primer elemento del array que cumple la funcion de prueba proporcionada, sino devuelve -1

    Callback: Función a ejecutar en cada uno de los valores del array hasta que devuelve true, indicando que el elemento que la cumple fue encontrado.Recibe tres argumentos:

        element: El elemento actual que se esta procesando en el array

        index(opcional): El indice del elemento actual que se esta procesando en el array

        array(opcional): El array findIndex() de donde fue llamado

    Retorno: El valor del primer elemento del array que cumple la función de prueba proporcionada; de lo contrario, devuelve -1.


+ IndexOf:  Retorna el primer índice en el que se puede encontrar un valor especificado dado en el array, o retorna -1 si el elemento no esta presente

        element: El elemento a encontrar en el array

        index(opcional): Indica el índice por el que se comienza la busqueda

            _Por defecto es 0, se busca en todo el array

            _Si es mayor o igual a la longitud del array, devuelve -1

            _Si el valor es negativo, se toma restando posiciones desde el final del array

    Retorno: El primer indice del elemento en la matriz; -1 si no se encuentra


+ Unshift: Agrega  uno o mas elementos al inicio del array, y devuelve la nueva longitud del array

        element: Elementos a agregar al inicio del array

    Retorno: La nueva propiedad length del objeto sobre el cual el método fue llamado.


+ Includes: Determina si una matriz incluye un determinado elemento, devulve true o false segun corresponda

        element: Elementos a agregar al inicio del array

        fromIndex(opcional): Posicion en la matriz, donde se debe comenzar a buscar el element; el primer caracter a buscar se encuentra en element. Un valor negativo inicia la búsqueda desde array.length + element en adelande

    Retorno: La nueva propiedad length del objeto sobre el cual el método fue llamado.


+ Every:  Devuelve el primer elemento del array que cumple la funcion de prueba proporcionada, sino devuelve -1

    Callback: Una función para probar cada elemento; recibe tres argumentos:

        element: El elemento actual que se esta procesando en el array

        index(opcional): El índice del elemento actual del arreglo que está siendo procesado.

        array(opcional): El arreglo sobre el cual fue llamado every.

    Retorno: Devuelve true si la funcion de devolucion de llamada devuelve un valor de truthy para cada elemento de la matriz, de lo contrario false


+ Splice:  Cambia el contenido de un array eliminando elementos existentes y/o agregando elementos nuevos

        start: Un entero indicando el número de elementos a eliminar del array antiguo

            Si deleteCount se omite, o su valor es mayor que arr.length - start, entonces todos los elementos desde start hastsa el final seran eliminados

            Si deleteCount es igual a 0 o negativo, no se eliminara ningun elemento

        item1, item2, ...(opcional): Los elementos que se agregan al array, empezando en el indice start, sino se especifican ningun elemento, splice unicamente eliminara elementos del array

    Retorno: Devulve un array que contiene los elementos eliminados, sino se ha eliminado ningun elemento, devolvera un array vacio


+ Slice:  Devuelve una copia de una parte del array dentro de un nuevo array empezando por inicio hasta fin

        Inicio: Indice donde empieza la extraccion, el primer elemento corresponde con el indice 0

        Fin: Indice que marca el final de la extraccion

    Retorno: Un nuevo array con los valores extraidos