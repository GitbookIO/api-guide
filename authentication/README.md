# Authentication


### Basic Authentication

The API supports Basic Authentication as defined in [RFC2617](http://www.ietf.org/rfc/rfc2617.txt) with a few slight differences.

Requests that require authentication will return `404 Not Found`, instead of `403 Forbidden`, in some places. This is to prevent the accidental leakage of private books to unauthorized users.

##### Via Username and Password

To use Basic Authentication with the GitBook API, simply send the username and password associated with the account.

For example, if you’re accessing the API via cURL, the following command would authenticate you if you replace <username> with your GitBook username. (cURL will prompt you to enter the password.)

```
$ curl -u <username> https://api.gitbook.com/account
```

##### Via OAuth Tokens

Alternatively, you can use personal access tokens or OAuth tokens instead of your password.

```
$ curl -u <username>:<token> https://api.gitbook.com/account
```

This approach is useful if your tools only support Basic Authentication but you want to take advantage of OAuth access token security features.
