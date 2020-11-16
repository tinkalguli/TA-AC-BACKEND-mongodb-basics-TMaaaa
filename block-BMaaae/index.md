writeCode

Write code to:-

- create a database named `sports`.

```js
use sports
```

- list all databases present in local mongod server.

```js
show dbs
```

- create 3 collections named `cricket`, `football`, `TT` in sports databse.

```js
db.createCollection("cricket")
db.createCollection("football")
db.createCollection("TT")
```

- add multiple players in those collections which should have fields like `name`, `age` and `email` and `bid_price`.

```js
db.cricket.insertMany([
  { name: "Ram",
    age : 15, 
    email: "xyz@gmail.com", 
    bid_price : 9000
  },
  {
    name: "Lil", 
    age : 45, 
    email: "fgg@gmail.com", 
    bid_price : 7000
  },
  {
    name: "Dil", 
    age : 34, 
    email: "hjj@gmail.com", 
    bid_price : 6000
  }
])

db.football.insertMany([
  {
    name: "John", 
    age : 23, 
    email: "kjh@gmail.com", 
    bid_price : 3000
  },
  {
    name: "Arti", 
    age : 21, 
    email: "sdf@gmail.com", 
    bid_price : 9000
  }
])

db.TT.insertMany([
  {
    name: "Susmita", 
    age : 43, 
    email: "asd@gmail.com", 
    bid_price : 5000
  },
  {
    name: "Rahul", 
    age : 34, 
    email: "rth@gmail.com", 
    bid_price : 10000
  }
])
```

- list all collections in sports database.

```js
show collections
```

- rename `TT` collection to `tennis`.

```js
db.TT.renameCollection("tennis")
```

- create a capped collection called `khokho` which should have max 3 documents.
  Try inserting more than 3 and see what happens?

```js
db.createCollection( "log", { capped: true, size: 10000, max : 3} )
````
  - size is required when capped is true
  - I have inserting more than 3 and when I check the collection there are only 3 documents

- check whether a collection is capped or not?

```
db.mycollection.stats()["capped"]
```

- drop all documents from `football` collection.

```js
db.football.remove()
```

- delete cricket collection completely.

```js
db.cricket.drop()
```

- delete sports database.

```js
db.dropDatabase()
```

- check which database you are connected to ?

```js
db
```

- connect to test database

```js
use test
```
