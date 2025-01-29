# NodeJS

* [Instalación de Node, npm/x y nvm](../README.md#programas-necesarios)
* [Desarrollando para el servidor](https://developer.mozilla.org/en-US/docs/Learn_web_development/Extensions/Server-side)

## El motor V8 de Google y Node

* [El motor V8 de Google](https://v8.dev/)
* [Documentación de V8 en NodeJS](https://nodejs.org/docs/latest/api/v8.html)

## Creación de un paquete con node (package.json)

* [Versionado de librerías](https://developer.mozilla.org/en-US/docs/Learn_web_development/Extensions/Client-side_tools/Package_management)
* [Publicación en npm](https://www.npmjs.com/)

## Creación de un servidor simple de http

```js
// /server/index.js
var http = require('http');
var url = require("url");

http.createServer(function server_onRequest (request, response) {
    var pathname = url.parse(request.url).pathname;

    console.log("Request for " + pathname + " received.");

    response.writeHead(200, {'Content-Type': 'text/html'});
    response.write("<h1>Hello World</h1>");
    response.end();
}).listen(process.env.PORT, process.env.IP);

console.log('Server running at http://' + process.env.IP + ':' + process.env.PORT + '/');
```

## El sistema de ficheros

[Módulo filesystem (fs)](https://nodejs.org/api/fs.html)

* [Buffer](https://nodejs.org/api/buffer.html)
* [Stream](https://nodejs.org/api/stream.html)
* [Watch](https://nodejs.org/api/fs.html#fswatchfilename-options-listener)

Ejemplo de uso de **fs**: [CRUD de BBDD en archivo local al servidor](https://www.freecodecamp.org/espanol/news/como-crear-una-aplicacion-crud-de-linea-de-comandos-con-node-js/)

## Sockets

* [TCP](https://nodejs.org/api/net.html): [ejemplo de servicor TCP y cliente](https://gist.github.com/tedmiston/5935757)
* [Websockets](https://developer.mozilla.org/en-US/docs/Web/API/WebSockets_API)
  * [Ejemplo de uso con la librería ws](https://dev.to/hamzakhan/built-in-websockets-in-nodejs-2024-a-comprehensive-guide-2236)
  * [Ejemplo de uso con la librería express-ws](https://www.scaler.com/topics/expressjs-tutorial/express-websocket/)
