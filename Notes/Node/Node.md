# Node.js: Resumen

## ¿Qué es Node.js?

Node.js es un entorno de ejecución de JavaScript del lado del servidor. Esto significa que permite ejecutar código JavaScript fuera del navegador, en el servidor, lo que lo hace ideal para desarrollar aplicaciones escalables y de alto rendimiento.

## Características principales
```
· Asíncrono y no bloqueante:

    - Modelo de E/S no bloqueante: Node.js utiliza un modelo de entrada/salida (I/O) no bloqueante, lo que significa que puede manejar múltiples operaciones a la vez sin esperar a que una termine antes de comenzar otra.
    
    - Event Loop: Node.js gestiona operaciones asíncronas mediante un bucle de eventos que permite manejar tareas concurrentes de manera eficiente.

· Basado en el motor V8 de Google:

   - Node.js está construido sobre el motor JavaScript V8 de Google, que es conocido por su alta velocidad y eficiencia.

· Single-threaded pero altamente escalable:

   - Aunque Node.js utiliza un solo hilo (single-threaded) para ejecutar JavaScript, puede manejar muchas conexiones concurrentes gracias a su arquitectura asíncrona.

· NPM (Node Package Manager):

   - Node.js viene con NPM, el gestor de paquetes más grande del mundo para librerías de JavaScript. Esto facilita la instalación, gestión y actualización de paquetes y módulos.
```
## Usos comunes
```
· APIs RESTful: Node.js es ideal para construir APIs ligeras y eficientes que pueden manejar un alto volumen de solicitudes.

· Aplicaciones en tiempo real: Es muy utilizado para aplicaciones que requieren comunicación en tiempo real, como chats o sistemas de colaboración.

· Microservicios: Su arquitectura ligera lo hace adecuado para construir microservicios independientes y escalables.

· Aplicaciones de streaming: Debido a su naturaleza asíncrona, es excelente para manejar grandes cantidades de datos en streaming.
```
## Ventajas
```
· Alto rendimiento: Su modelo asíncrono y no bloqueante permite un manejo eficiente de múltiples conexiones simultáneas.

· Desarrollo rápido: La vasta colección de paquetes NPM y su uso de JavaScript tanto en el servidor como en el cliente facilitan y aceleran el desarrollo.

· Comunidad activa: Node.js cuenta con una comunidad grande y activa, lo que significa abundancia de recursos, tutoriales y soporte.
```
## Desventajas
```
· No apto para tareas CPU intensivas: Debido a su naturaleza single-threaded, no es ideal para tareas que requieren mucho procesamiento de CPU.

· Modelo de programación asíncrona: Puede ser complicado para desarrolladores acostumbrados a modelos de programación síncronos debido al uso intensivo de callbacks y promesas.
```


[All Documentation](https://developer.mozilla.org/es/docs/Web/API/Node)