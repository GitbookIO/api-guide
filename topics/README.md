# Topics

#### List topics

```
GET /topics
```

###### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| `q` | `string` | The search keywords, as well as any qualifiers. |


###### Response

```js
{
    "list": [
        {
            "id": "programming",
            "name": "Programming",
            "books": 320
        }
        ...
    ],
    "total": 76,
    "limit": 10,
    "page": 0
}
```

#### Get specific topic

```
GET /topic/:id
```
