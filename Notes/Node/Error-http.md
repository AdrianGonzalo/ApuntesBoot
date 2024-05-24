# Códigos de Estado HTTP

## 100 - 199: Informativos

1. **100 - Continue (Continuar)**: Indica que el servidor ha recibido los encabezados de solicitud y que el cliente debería proceder a enviar el cuerpo de la solicitud.

2. **101 - Switching Protocols (Cambiar Protocolos)**: Indica que el servidor está cambiando los protocolos según la solicitud del cliente.

3. **102 - Processing (Procesando)**: Informa al cliente que el servidor ha recibido la solicitud y la está procesando, pero aún no ha completado la acción requerida.

4. **103 - Early Hints (Indicios tempranos)**: Permite retornar algunos encabezados de respuesta antes de que la respuesta final sea enviada, lo cual puede ser útil para ciertos casos de optimización de rendimiento.

## 200 - 299: Éxito

1. **200 - OK (Correcto)**: Indica que la solicitud fue exitosa y el servidor ha devuelto los datos solicitados correctamente.

2. **201 - Created (Creado)**: Indica que la solicitud ha tenido éxito y ha resultado en la creación de un nuevo recurso.

3. **202 - Accepted (Aceptado)**: Indica que la solicitud ha sido aceptada para procesamiento, pero el proceso puede no haber sido completado.

4. **204 - No Content (Sin contenido)**: Indica que la solicitud se ha procesado correctamente, pero no hay contenido para devolver en la respuesta.

5. **206 - Partial Content (Contenido parcial)**: Indica que la solicitud GET ha sido exitosa y el servidor está devolviendo solo una parte del recurso debido a una solicitud de rango.

## 300 - 399: Redirecciones

1. **300 - Multiple Choices (Múltiples opciones)**: Indica que hay múltiples opciones para el recurso solicitado. El agente del usuario o el usuario debe elegir una de ellas.

2. **301 - Moved Permanently (Movido permanentemente)**: Indica que el recurso solicitado ha sido movido permanentemente a una nueva URL. La nueva URL se proporciona en el encabezado `Location` de la respuesta.

3. **302 - Found (Encontrado)**: Indica que el recurso solicitado reside temporalmente en una URL diferente. No se debería actualizar la URL en los índices.

4. **303 - See Other (Ver otro)**: Indica que el cliente debe realizar una solicitud GET a otra URL para obtener el recurso.

5. **304 - Not Modified (No modificado)**: Indica que el recurso no ha sido modificado desde la última solicitud. Permite el uso de la versión almacenada en caché del recurso.

6. **307 - Temporary Redirect (Redirección temporal)**: Similar al 302, pero especifica que el método de solicitud no debe cambiar.

7. **308 - Permanent Redirect (Redirección permanente)**: Similar al 301, pero el método de solicitud original debe ser utilizado en la nueva URL.

## 400 - 499: Errores del Cliente

1. **400 - Bad Request (Solicitud incorrecta)**: Indica que el servidor no puede o no procesará la solicitud debido a un error del cliente (por ejemplo, una sintaxis mal formada).

2. **401 - Unauthorized (No autorizado)**: Indica que la solicitud requiere autenticación del usuario. Si ya se ha proporcionado autenticación, el servidor puede responder con este código si las credenciales no son válidas.

3. **403 - Forbidden (Prohibido)**: Indica que el servidor entiende la solicitud, pero se niega a autorizarla.

4. **404 - Not Found (No encontrado)**: Indica que el servidor no pudo encontrar el recurso solicitado.

5. **405 - Method Not Allowed (Método no permitido)**: Indica que el método especificado en la solicitud no está permitido para el recurso identificado.

6. **406 - Not Acceptable (No aceptable)**: Indica que el servidor no puede generar una respuesta que sea aceptable para el cliente según los encabezados de aceptación enviados en la solicitud.

7. **408 - Request Timeout (Tiempo de espera de la solicitud)**: Indica que el servidor agotó el tiempo de espera para la solicitud.

8. **409 - Conflict (Conflicto)**: Indica que la solicitud no puede ser completada debido a un conflicto con el estado actual del recurso.

9. **410 - Gone (Desaparecido)**: Indica que el recurso solicitado ya no está disponible y no lo estará nuevamente.

10. **413 - Payload Too Large (Carga útil demasiado grande)**: Indica que la solicitud es mayor que los límites definidos por el servidor.

11. **414 - URI Too Long (URI demasiado larga)**: Indica que la URI proporcionada era demasiado larga para ser procesada por el servidor.

12. **415 - Unsupported Media Type (Tipo de medio no soportado)**: Indica que el formato de la entidad solicitada no es compatible con el servidor.

13. **429 - Too Many Requests (Demasiadas solicitudes)**: Indica que el cliente ha enviado demasiadas solicitudes en un periodo de tiempo dado.

## 500 - 599: Errores del Servidor

1. **500 - Internal Server Error (Error interno del servidor)**: Indica que el servidor encontró una condición inesperada que le impidió cumplir con la solicitud.

2. **501 - Not Implemented (No implementado)**: Indica que el servidor no reconoce el método de solicitud o carece de la capacidad para completarlo.

3. **502 - Bad Gateway (Puerta de enlace incorrecta)**: Indica que el servidor, actuando como una puerta de enlace o proxy, recibió una respuesta inválida del servidor upstream.

4. **503 - Service Unavailable (Servicio no disponible)**: Indica que el servidor no está disponible temporalmente, generalmente debido a sobrecarga o mantenimiento.

5. **504 - Gateway Timeout (Tiempo de espera de la puerta de enlace)**: Indica que el servidor, actuando como una puerta de enlace o proxy, no recibió una respuesta a tiempo del servidor upstream.
6. **505 - HTTP Version Not Supported (Versión HTTP no soportada)**: Indica que el servidor no soporta la versión del protocolo HTTP utilizada en la solicitud.

7. **507 - Insufficient Storage (Almacenamiento insuficiente)**: Indica que el servidor no puede almacenar la representación necesaria para completar la solicitud.

8. **508 - Loop Detected (Bucle detectado)**: Indica que el servidor detectó un bucle infinito al procesar una solicitud con WebDAV.

9. **511 - Network Authentication Required (Autenticación de red requerida)**: Indica que el cliente necesita autenticarse para obtener acceso a la red.



[All Documentation](https://developer.mozilla.org/es/docs/Web/HTTP/Status)