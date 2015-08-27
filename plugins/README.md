# Create and publish a plugin

A GitBook plugin is a node package published on NPM that follow a defined convention.

## Structure

#### package.json

The `package.json` contains general information about your plugin (name, version, description, ...):

```
{
    "name": "gitbook-plugin-mytest",
    "version": "0.0.1",
    "description": "This is my first GitBook plugin",
    "engines": {
        "gitbook": ">1.x.x"
    }
}
```

You can learn more about `package.json` from the [NPM documentation](https://docs.npmjs.com/files/package.json).

The **package name** must begin with `gitbook-plugin-` and the **package engines** should contains `gitbook`.

#### index.js

The `index.js` is main entry point of your plugin:

```js
module.exports = {
    // Map of hooks
    hooks: {},
    
    // Map of new blocks
    blocks: {},
    
    // Map of new filters
    filters: {}
};
```

## Publish your plugin

GitBook plugins are published and installed from [NPM](https://www.npmjs.com).

To publish a new plugin, you need to create an account on [npmjs.com](https://www.npmjs.com) then publish it from the command line:

```
$ npm publish
```
