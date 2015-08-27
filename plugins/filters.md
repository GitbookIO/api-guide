# Extend Filters

Filters are essentially functions that can be applied to variables. They are called with a pipe operator (`|`) and can take arguments.

```
{{ foo | title }}
{{ foo | join(",") }}
{{ foo | replace("foo", "bar") | capitalize }}
```

### Defining a new filter

Plugins can extend filters by defining custom functions in their entry point under the `filters` scope.

A filter function takes as first argument the content to filter, and should return the new content.

```js
module.exports = {
    filters: {
        hello: function(name) {
            return 'Hello '+name;
        }
    }
};
```

The filter `hello` can then be used in the book:

```
{{ "Aaron"|hello }}, how are you?
```
