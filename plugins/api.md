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

Hooks only have access to the `<Book>` instance.

#### Book instance

The `Book` class is the central point of GitBook, it centralize all access methods. This class is defined in [book.js](https://github.com/GitbookIO/gitbook/blob/master/lib/book.js).

```js
// Access to book's configuration (book.json)
var title = book.config.get('title');
var websiteStylesheet = book.config.get('styles.website', 'default_value.css');

```
