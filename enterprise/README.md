# Enterprise

#### Endpoint URLs

All API endpoints are prefixed with the following URL: `http(s)://hostname/api/`.


#### Root Endpoint

You can issue a GET request to the root endpoint to get details about the instance:

```
curl https://gitbook.mycompany.com/api/
```

###### Results

```js
{
    "type":"enterprise",
    "version":"11.7.6",
    "urls":{
        "main":"https://gitbook.mycompany.com/",
        "api":"https://gitbook.mycompany.com/api/"
    }
}
```