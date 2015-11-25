# Contents

These API methods let you retrieve the contents of files within a book.

#### Get contents


```
GET /book/:author/:book/contents/:file
```

###### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| `file` | `string` | Path of the file to retrieve (with `.json` extension) |


###### Response

```js
{
    "progress": {
        ...
    },
    "sections": [
        {
            "type": "normal",
            "content": "<h1>My Awesome book</h1>"
        }
    ],
    "langs": []
}
```