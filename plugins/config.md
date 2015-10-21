# Configuration Manifest

A plugin manifest `package.json` can also contain details about the required configuration.
Starting with GitBook **2.5.0**, the schema will be used to valid configuration during build.

The configuration schema is defined in the `gitbook` field of the `package.json`:

```js
{
    "name": "gitbook-plugin-mytest",
    "version": "1.0.0",
    "engines": {
        "gitbook": ">=2.5.0
    },
    "gitbook": {
        "properties": {
            "myConfigKey": {
                "type": "string",
                "default": "it's the default value",
                "description": "It defines my awesome config!"
            }
        }
    }
}
```

This field follow the [JSON-Schema](http://json-schema.org) guidelines.

Examples:

- [sitemap](https://github.com/GitbookIO/plugin-sitemap/blob/master/package.json)
- [fontsettings](https://github.com/GitbookIO/plugin-fontsettings/blob/master/package.json)



