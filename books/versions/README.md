# Versions

#### List branches for a book


```
GET /book/:author/:book/versions/branches
```


###### Response

```js
[
    {
        "name": "master",
        "urls": {
            "website": "https://samypesse.gitbooks.io/how-to-create-an-operating-system/content/",
            "epub": "https://www.gitbook.com/download/epub/book/samypesse/how-to-create-an-operating-system/",
            "pdf": "https://www.gitbook.com/download/pdf/book/samypesse/how-to-create-an-operating-system/",
            "mobi": "https://www.gitbook.com/download/mobi/book/samypesse/how-to-create-an-operating-system/"
        },
        "current": true
    },
    ...
]
```


#### List tags for a book

```
GET /book/:author/:book/versions/tags
```
