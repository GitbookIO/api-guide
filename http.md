# HTTP API

This describes the resources that make up the official GitBook API. If you have any problems or requests please [contact support](https://www.gitbook.com/contact).

#### Schema

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


#### Authentication

There is currently only one way to authenticate through GitBook API: **Basic Auth**.

Requests that require authentication will return `404 Not Found`, instead of `403 Forbidden`, in some places. This is to prevent the accidental leakage of private books to unauthorized users.

```
$ curl -u "username:token" https://api.gitbook.com/books/
```

#### Error Format

Error are returned as JSON: 

```js
{
    "error": "Not found",
    "code": 404
}
```

#### Pagination

Requests that return multiple items will be paginated to 30 items by default.

You can specify further pages with the `?skip` parameter. For some resources, you can also set a custom page size up to 100 with the `?limit`.

Paginated results will be returned with information about the page context:

```js
{
    list: [],
    skip: 0,
    limit: 100,
    total: 0
}
```