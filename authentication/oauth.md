# OAuth

All developers need to [register their application](https://www.gitbook.com/settings/developers) before getting started. A registered OAuth application is assigned a unique Client ID and Client Secret. The Client Secret should not be shared.

### 1. Redirect users to request GitBook access

```
GET https://api.gitbook.com/oauth/authorize?response_type=code&redirect_uri=<CALLBACK_URL>&client_id=<CLIENT_ID>
```


###### Parameters

| Name | Type | Description |
| -- | -- | -- |
| `client_id` | `string` | **Required**. The client ID you received from GitBook when you registered. |
| `redirect_uri` | `string` | **Required**. The URL in your app where users will be sent after authorization.  |


### 2. GitBook redirects back to your site

If the user accepts your request, GitBook redirects back to your site with a temporary code in a `code` parameter.

Exchange this for an access token:

```
POST https://api.gitbook.com/oauth/access_token
```

###### Parameters

| Name | Type | Description |
| -- | -- | -- |
| `client_id` | `string` | **Required**. The client ID you received from GitBook when you registered. |
| `client_secret` | `string` | **Required**. The client secret you received from GitBook when you registered. |
| `code` | `string` | **Required**. The code you received as a response to Step 1. |
| `grant_type` | `string` | **Required**. `authorization_code` to exchange an oauth code |

###### Response

By default, the response will take the following form:

````
access_token=e72e16c7e42f292c6912e7710c838347ae178b4a&token_type=bearer
```

`access_token` can also be returned as JSON.

### 3. Use the access token to access the API

Include it in the Authorization header

```
Authorization: Bearer OAUTH-TOKEN
```

For example, in curl you can set the Authorization header like this:

```
$ curl -H "Authorization: Bearer OAUTH-TOKEN" https://api.gitbook.com/account
```