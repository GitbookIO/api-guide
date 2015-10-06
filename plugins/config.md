# Configuration Manifest

A plugin manifest `package.json` can also contain details about the required configuration.
Starting with GitBook **2.5.0**, the schema will be used to valid configuration during build.

The configuration schema is defined in `gitbook.config`:

```js
{
    "name": "gitbook-plugin-mytest",
    "version": "1.0.0",
    "engines": {
        "gitbook": ">=2.5.0
    },
    "gitbook": {
        "config": [
            {
                "key": "myConfigKey",
                "type": "string",
                "value": "it's the default value",
                "description": "It defines my awesome config!"
            }
        ]
    }
}
```

### Schema

`gitbook.config` should be a list of objects with the following properties:

|  | Description | Required? |
| -- | -- | -- |
| **key** | Unique key for the configuration | Yes |
| **type** | Type of the configuration, it can be `string`, `array`, or `number`; default is `string` | No |
| **description** | Help message shown in the editor and during validation | No |
| **value** | Default value used during build | No |



