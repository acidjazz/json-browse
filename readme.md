# json-browse

*json-browse* is a jQuery plugin for easily displaying JSON objects by transforming them into HTML.

Features:
- Syntax highlighting
- Collapse and expand child nodes on click
- Clickable links
- Easily readable and minimal DOM structure

Check out the [demo page](http://rawgit.com/acidjazz/json-browse/master/demo.html)!

## Usage

Import `jquery.json-browse.js` and `jquery.json-browse.css` in your application.

Then just call the `jsonBrowse()` method and pass your JSON data in argument:
```html
<pre id="json-renderer" class="json-body"></pre>
```

```js
var data = {
  "foobar": "foobaz"
};
$('#json-renderer').jsonBrowse(data);
```

## Options

The `jsonBrowse` method accepts an optional `options` hash as a second argument:

- `collapsed` (boolean, default: `false`): all nodes are collapsed at html generation.
- `withQuotes` (boolean, default: `false`): all JSON keys are surrounded with double quotation marks (`{"foobar": 1}` instead of `{foobar: 1}`).

Example:

```js
$('#json-renderer').jsonBrowse(data, {collapsed: true, withQuotes: true});
```
