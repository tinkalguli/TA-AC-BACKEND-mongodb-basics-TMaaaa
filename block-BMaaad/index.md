writeCode

Write command to

- List collections from a database.

```js
show collections
```

- create a new collection in your country database which you created recently.

```js
db.createCollections("The_new_collection")
```

Write code to:-

- crate a database named `weather`

```js
use weather
```
- create a capped collection named `temperature` with maximum of 3 documents and try inserting more than 3 to see the result.

```js
db.createCollection("temperature", {capped: true, size : 10000})
db.temperature.insert({place: "Guwahati", state: "Assam", dist: "Kamrup"})
```
- create a simple collection named `humidity`

```js
db.createCollection("humidity")
```
- check whether `temperature` collection is capped or not ?

```js
db.temperature.stats()["capped"]
```

- Delete `humidity` collection and then the entire database(weather).

```js
db.humidity.drop()
db.dropDatabase()
```