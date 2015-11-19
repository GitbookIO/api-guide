# Access Keys

Access keys allow non-collaborator to access a private book.

#### List keys for a book

```
GET /book/:author/:book/keys/
```


###### Response

```js
{
    "list": [
        {
            "id": "564c97a917c24e09ddd8b765",
            "label": "For Aaron",
            "key": "aaron_private_key",
            "dates": {
                "created": "2015-11-19T12:22:27.765Z",
                "updated": "2015-11-19T12:22:27.765Z"
            }
        }
        ...
    ],
    "total": 15,
    "limit": 10,
    "page": 0
}
```

#### Get an access key

```
GET /book/:author/:book/keys/:id
```
