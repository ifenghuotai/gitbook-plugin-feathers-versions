## gitbook-plugin-feathers-versions

[![Greenkeeper badge](https://badges.greenkeeper.io/feathersjs/gitbook-plugin-feathers-versions.svg)](https://greenkeeper.io/)

> This is a modified version of [Versions](https://plugins.gitbook.com/plugin/versions)

Display a `<select>` with other versions of your gitbook that you have specified in your `book.json` file.

### Usage with gitbook.com

When your book is hosted on [GitBook.com](https://www.gitbook.com), the plugin can access a listing of versions using the [GitBook API](http://developer.gitbook.com/books/versions/).

Put this in your book.json:

```js
{
    "plugins": [ "feathers-versions" ],
    "pluginsConfig": {
        "versions": {
            "gitbookConfigURL": "https://raw.githubusercontent.com/feathersjs/feathers-docs/master/book.json",
            "options": [
                {
                    "value": "https://docs.feathersjs.com",
                    "text": "Latest Stable (Auk)"
                },
                {
                    "value": "https://legacy.docs.feathersjs.com",
                    "text": "Legacy (Pre-Auk)"
                }
            ]
        }
    }
}
```

A `<select>` element will be created with the given `options` and placed at the top of the book summary. When the user selects one of the options, they are taken to that URL.

The `gitbookConfigURL` variable is a publicly accessible URL to your `book.json`. If this is present, the plugin will fetch the latest config when the page loads, so even older versions of your book will have updated `options`.

### Credits

Original work by [@mjackson](https://github.com/mjackson).
