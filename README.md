# tcomb-postcss

Extends the [`tcomb`](https://github.com/gcanti/tcomb) library with [`PostCSS`](https://github.com/postcss/postcss) irreducible node types.

The following types are added to tcomb:
- [`Container`](https://github.com/postcss/postcss/blob/master/lib/container.es6)
- [`Root`](https://github.com/postcss/postcss/blob/master/lib/root.es6)
- [`Rule`](https://github.com/postcss/postcss/blob/master/lib/rule.es6)
- [`AtRule`](https://github.com/postcss/postcss/blob/master/lib/at-rule.es6)
- [`Decl`](https://github.com/postcss/postcss/blob/master/lib/declaration.es6)
- [`Comment`](https://github.com/postcss/postcss/blob/master/lib/comment.es6)
- [`Warning`](https://github.com/postcss/postcss/blob/master/lib/warning.es6)

## Usage

```js
var t = require('tcomb-postcss');
var postcss = require('postcss');

var root = postcss.parse('a{}');
t.Root.is(root); // true
t.Rule.is(root.first); // true
t.AtRule.is(root.first); // false
```
