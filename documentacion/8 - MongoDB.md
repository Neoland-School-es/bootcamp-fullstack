# MongoDB

* ¿Qué es el NoSQL?
* Modelo de datos en MongoDB
* Modelo de query en MongoDB
* Indexado de datos
* Bases de datos y colecciones
* Operaciones con los datos

## Conexión con MongoDB

```js
const MongoClient = require("mongodb").MongoClient;

MongoClient.connect("mongodb://localhost:27017/animals", (err, client) => {
  if (err) throw err;

  const db = client.db("animals");
  db.collection("mammals")
    .find()
    .toArray((err, result) => {
      if (err) throw err;
      console.log(result);
      client.close();
    });
});
```
