writeCode

Write code to:-

- create a database named `mountains`

```js
use mountains
```

- a collection inside that database named `himalayas`

```js
db.createCollection("himalayas")
```

- insert 1 document into that collection `{name: 'Dhauldhar range', height: '4000 mtrs'}`

```js
db.himalayas.insert({
    name: 'Dhauldhar range', 
    height: '4000 mtrs'
})
```

- insert multiple document using insertMany command

```js
db.himalayas.insertMany([
    {
        name: 'Dhauldhar range', 
        height: '4000 mtrs'
    },
    {
        name: 'Dhauldhar range', 
        height: '9000 mtrs'
    },
    {
        name: 'Brahmaputra range', 
        height: '5000 mtrs'
    },
    {
        name: 'Yamuna range', 
        height: '7000 mtrs'
    }
])
```

- find all documents from mountains

```js
db.himalayas.find()
```

- find a single document using name

```js
db.himalayas.findOne({ name: 'Dhauldhar range' })
```