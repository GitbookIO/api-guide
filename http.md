# HTTP API

This describes the resources that make up the official GitBook API. If you have any problems or requests please [contact support](https://www.gitbook.com/contact).

### Libraries

Some official libraries are available to easily get you started:

| Name | Language |
| ----- | ------- |
| [node-gitbook-api](https://github.com/GitbookIO/node-gitbook-api) | Node.js |
| [go-gitbook-api](https://github.com/GitbookIO/go-gitbook-api) | Go (Golang) | 



### Schema

All API access is over HTTPS, and accessed through `https://api.gitbook.com/` . All data is sent and received as **JSON**.

```raw
$ curl -i https://api.gitbook.com/author/gitbookio

HTTP/1.1 200 OK
Server: Cowboy
Connection: keep-alive
Content-Type: application/json; charset=utf-8
Content-Length: 275
Etag: W/"113-25d22777"
Date: Thu, 11 Jun 2015 14:49:26 GMT
Via: 1.1 vegur

{ ... }
```

### Error Format

Error are returned as JSON: 

```js
{
    "error": "Not found",
    "code": 404
}
```

### Pagination

Requests that return multiple items will be paginated to 50 items by default.

You can specify further pages with the `?page` parameter. For some resources, you can also set a custom page size up to 100 with the `?limit`.

Paginated results will be returned with information about the page context:

```js
{
    list: [],
    page: 0,
    limit: 100,
    total: 0
}
```


### Root Endpoint

You can issue a GET request to the root endpoint to get details about the instance:

```
curl https://api.gitbook.com
```

###### Results

```js
{
    "type":"public",
    "version":"11.7.6",
    "urls":{
        "main":"https://www.gitbook.com/",
        "api":"https://api.gitbook.com/"
    }
}
```