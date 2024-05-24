# Metodos de Peticion HTTP

Http define un conjunto de metodos de peticion para indicar la accion que se desea realizar para un recurso determinado:

### GET

El metodo GET se utiliza para recuperar datos

```
app.get('/', (req, res) => {

  res.send('Hola, mundo!');
});

```
### HEAD

El metodo HEAD pide una respuesta identica a la de una peticion GET, pero sin el cuerpo de la respuesta
```
app.head('/', (req, res) => {

        // Establecer algunos encabezados de respuesta

  res.set({
    'Content-Type': 'text/plain',
    'Custom-Header': 'CustomValue'
  });

        // Enviar una respuesta sin cuerpo

  res.end();
});
```
### POST

El metodo POST se utiliza para enviar una entidad a un recurso en especifico
```
app.post('/data', (req, res) => {

  const receivedData = req.body;
  console.log('Datos recibidos:', receivedData);

        // Enviar una respuesta de éxito

  res.send('Datos recibidos correctamente');
});
```
### PUT

El metodo PUT reemplaza todas las representaciones actuales del recurso de destino con la carga util de la peticion
```
app.put('/update', (req, res) => {

  const updatedData = req.body;
  console.log('Datos actualizados:', updatedData);

        // Enviar una respuesta de éxito

  res.send('Datos actualizados correctamente');
});
```
### DELETE

El metodo DELETE borra un recurso en especifico
```
app.delete('/delete/:id', (req, res) => {

  const { id } = req.params;
  console.log(`Recurso con ID ${id} eliminado`);

        // Enviar una respuesta de éxito

  res.send(`Recurso con ID ${id} eliminado correctamente`);
});
```
### CONNECT 

El metodo CONNECT establece un túnel hacia el servidor identificado por el recurso
```
        // Crear un servidor HTTP

const server = http.createServer((req, res) => {

  res.writeHead(200, { 'Content-Type': 'text/plain' });
  res.end('Servidor HTTP\n');

});

        // Manejar la solicitud CONNECT

server.on('connect', (req, clientSocket, head) => {

  const { port, hostname } = new url.URL(`http://${req.url}`);
  console.log(`Conectando a ${hostname}:${port}`);

        // Conectar a la dirección de destino

  const serverSocket = net.connect(port || 80, hostname, () => {

    clientSocket.write('HTTP/1.1 200 Connection Established\r\n' +
                       'Proxy-agent: Node.js-Proxy\r\n' +
                       '\r\n');

    serverSocket.write(head);
    serverSocket.pipe(clientSocket);
    clientSocket.pipe(serverSocket);
  });

        // Manejar errores de socket

  clientSocket.on('error', (err) => {

    console.error('Cliente Socket Error:', err);
    serverSocket.end();
  });

  serverSocket.on('error', (err) => {

    console.error('Servidor Socket Error:', err);
    clientSocket.end();
  });
});
```
### OPTIONS

El metodo OPTIONS es utilizado para describir las opciones de comunicacion para el recurso de destino
```
        // Middleware para permitir solicitudes CORS

app.use((req, res, next) => {

  res.setHeader('Access-Control-Allow-Origin', '*');
  res.setHeader('Access-Control-Allow-Methods', 'OPTIONS, GET, POST, PUT, DELETE');
  res.setHeader('Access-Control-Allow-Headers', 'Content-Type');
  next();
});

        // Ruta para manejar solicitudes OPTIONS

app.options('/', (req, res) => {

  res.sendStatus(200);
});
```
### TRACE

El metodo TRACE realiza una prueba de bucle de retorno de mensaje a lo largo de la ruta al recurso de destino
```
        // Middleware para permitir solicitudes CORS

app.use((req, res, next) => {

  res.setHeader('Access-Control-Allow-Origin', '*');
  res.setHeader('Access-Control-Allow-Methods', 'TRACE, GET, POST, PUT, DELETE');
  res.setHeader('Access-Control-Allow-Headers', 'Content-Type');
  next();
});

        // Ruta para manejar solicitudes TRACE

app.trace('/', (req, res) => {

  const requestHeaders = req.headers;
  res.status(200).json({ headers: requestHeaders });
});
```
### PATCH

El metodo PATCH es utilizado para aplicar modificaciones parciales a un recurso
```
        // Ruta para manejar solicitudes PATCH al recurso

app.patch('/resource', (req, res) => {

        // Obtener los datos de la solicitud PATCH

  const patchData = req.body;

        // Aplicar las modificaciones al recurso

  Object.assign(resource, patchData);

        // Enviar una respuesta con el recurso modificado

  res.json(resource);
});
```


[All Documentation](https://developer.mozilla.org/es/docs/Web/HTTP/Methods)


