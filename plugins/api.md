# Context and APIs

GitBooks provides different APIs and contexts to plugins. These APIs can vary according to the GitBook version being used, your plugin should specify the `engines.gitbook` field in `package.json` accordingly.

#### Context for Blocks and Filters

Blocks and filters have access to the same context, this context is bind to the template engine execution:

```js
{
    // Current templating syntax
    "ctx": {
        // For example, after a {% set message = "hello" %}
        "message": "hello"
    },
    
    // Book instance
    "book" <Book>,
    
    // Current generator
    "generator": "website"
}
```

#### Context for Hooks
