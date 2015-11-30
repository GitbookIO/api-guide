# Authentication

While the API provides multiple methods for authentication, we strongly recommend using [OAuth](./oauth.md) for production applications. The [other methods](./basic.md) provided are intended to be used for scripts or testing (i.e., cases where full OAuth would be overkill).

Third party applications that rely on GitBook for authentication should not ask for or collect GitBook credentials. Instead, they should use the OAuth web flow.

