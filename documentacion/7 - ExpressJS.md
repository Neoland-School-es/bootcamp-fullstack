# [ExpressJS](https://developer.mozilla.org/en-US/docs/Learn_web_development/Extensions/Server-side/Express_Nodejs)

## Instalación

```bash
npm install --save express
```

Ejemplo de uso:

```js
// /server/index.express.js
const express = require('express')
const app = express()
const port = 3000

app.get('/', (req, res) => {
  res.send('Hello World!')
})

app.listen(port, () => {
  console.log(`Example app listening on port ${port}`)
})
```

[Habilitar reinicio del servidor tras los cambios con Nodemon](https://developer.mozilla.org/en-US/docs/Learn_web_development/Extensions/Server-side/Express_Nodejs/skeleton_website#enable_server_restart_on_file_changes)

```bash
npm install --save-dev nodemon
```

Modificar los scripts de inicio, para Linux/MAC:

```json
"scripts": {
  "start": "node ./bin/www",
  "devstart": "nodemon ./bin/www",
  "serverstart": "DEBUG=express-locallibrary-tutorial:* npm run devstart"
}
```

Y para Windows:

```json
"scripts": {
  "serverstart": "SET DEBUG=express-locallibrary-tutorial:* & npm run devstart"
}
```

## [Gestión de rutas](https://expressjs.com/en/guide/routing.html)

```js
// /server/router.express.js
const express = require('express')
const app = express()

// respond with "hello world" when a GET request is made to the homepage
app.get('/', (req, res) => {
  res.send('hello world')
})

// POST method route
app.post('/', (req, res) => {
  res.send('POST request to the homepage')
})
```

## [Middlewares](https://expressjs.com/en/guide/writing-middleware.html)

Identificación de usuarios por medio del protocolo de autorización OAuth2

* [OpenID-Connect with Google](https://permify.co/post/oauth-20-implementation-nodejs-expressjs/)
  * [Check comments](https://www.reddit.com/r/node/comments/1aervdx/oauth_20_implementation_in_nodejs_express/)
* [OAuth2 with Express](https://merlino.agency/blog/step-by-step-how-to-implement-oauth2-server-in-expressjs)

## [Gestión de errores](https://expressjs.com/en/guide/error-handling.html)

## Creación de APIs como endpoints REST

Métodos de envío y recogida de datos:

* GET
* POST
* PUT
* DELETE

```js
// /server/index.express.js
const express = require('express')
const app = express()
const port = 3000

app.get('/', (req, res) => {
  res.send('Hello World!')
})
// CREATE
app.post('/users', (req, res) => {
  res.send('User created!')
})
// READ
app.get('/users', (req, res) => {
  res.send('Users\' list')
})
// UPDATE
app.put('/users/:id', (req, res) => {
  res.send('User updated!')
})
// DELETE
app.delete('/users/:id', (req, res) => {
  res.send('User deleted!')
})
```

## [Uso de plantillas](https://expressjs.com/en/guide/using-template-engines.html)

* [Pug](https://www.npmjs.com/package/pug)
* [Handlebars](https://www.npmjs.com/package/handlebars)
* [EJS](https://www.npmjs.com/package/ejs)
