# Extend Assets

Extending assets allow plugins to add css or js to the build website or ebook.


### Extending website assets

It is being done by listing the assets in the plugin's entry point. The folder `book.assets` will be copied in the final build. `book.css` and `book'js` will be listed in all HTML pages.

```js
module.exports = {
    book: {
        assets: './assets/website',
        css: [
            'mystyle.css'
        ],
        js: [
            'myfile.js
        ]
    }
};
```