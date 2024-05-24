# Errores HTTP

Los codigos de estado respuesta HTTP indican si se ha completado ssatisfactoriamente una solicitud HTTP especifica, se agrupan en cinco clases:

    1. Respuestas informativas ( 100 - 199 )
    2. Respuestas astisfactorias ( 200 - 299 )
    3. Redirecciones ( 300 - 399 )
    4. Errores de los clientes ( 400 - 499 )
    5. Errores del servidor ( 500 - 599 )

## Respuestas informativas

### 100 - Continue

Indica que el servidor ha recibido los encabezados de solicitud y que el cliente deberia proceder a enviar el cuerpo

### 101 - Switching Protocols

Indica que el servidor esta cambiando los protocolos segun la solicitud del cliente

### 102 - Processing

Se utiliza para informar al cliente que el servidor ha recibido la solicitud y la esta procesando, pero aun no ha completado la accion requerida

### 103 - Early Hints

Se utiliza para retornar algunos encabezados de respuesta antes de que la respuesta final sea enviada

## Respuestas sarisfactorias (mas comunes)

### 200 - OK

Indica que la solicitud fue exitosa y el servidor ha devuelto los datos solicitados correctamente

### 201 - Created

Se utiliza para indicar que la solicitud ha tenido exito y ha resultado en la creacion de un nuevo recurso

### 202 - Accepted

Indica que la solicitudha sido aceptada para procesamiento, pero puedo no haber sido completado

### 204 - No Content

Se utiliza para indicar que la solicitud se ha procesado correctamente, pero no hay copntenido para devolver

### 206 - Partial Content

Indica que la solicitud GET ha sido exitosa y el servidor esta devolviendo solo una parte del recurso debido a una solicitud de rango

WIP

[All Documentation](https://developer.mozilla.org/es/docs/Web/HTTP/Status)