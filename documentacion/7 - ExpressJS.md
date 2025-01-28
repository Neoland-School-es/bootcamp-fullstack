# ExpressJS

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

WIP

* https://developer.auth0.com/resources/code-samples/api/express/basic-authorization
* https://permify.co/post/oauth-20-implementation-nodejs-expressjs/
* https://www.reddit.com/r/node/comments/1aervdx/oauth_20_implementation_in_nodejs_express/
* https://merlino.agency/blog/step-by-step-how-to-implement-oauth2-server-in-expressjs

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
