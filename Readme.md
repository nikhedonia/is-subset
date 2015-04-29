[![Coveralls – test coverage
](https://img.shields.io/coveralls/studio-b12/is-subset.svg?style=flat-square)
](https://coveralls.io/r/studio-b12/is-subset)
 [![Travis – build status
](https://img.shields.io/travis/studio-b12/is-subset/master.svg?style=flat-square)
](https://travis-ci.org/studio-b12/is-subset)
 [![David – status of dependencies
](https://img.shields.io/david/studio-b12/is-subset.svg?style=flat-square)
](https://david-dm.org/studio-b12/is-subset)
 [![Code style: airbnb
](https://img.shields.io/badge/code%20style-airbnb-blue.svg?style=flat-square)
](https://github.com/airbnb/javascript)
 [![Stability: experimental
](https://img.shields.io/badge/stability-experimental-red.svg?style=flat-square)
](https://nodejs.org/api/documentation.html#documentation_stability_index)




is-subset
=========

**Check if an object is contained within another one.**




Installation
------------

```sh
$ npm install is-subset
```




Usage
-----

1) Import the module:

```js
import isSubset from 'is-subset/module';

// …or:
var isSubset = require('is-subset');
```

2) These are true:

```js
isSubset(
  {a: 1, b: 2},
  {a: 1}
);

isSubset(
  {a: 1, b: {c: 3, d: 4}, e: 5},
  {a: 1, b: {c: 3}}
);

isSubset(
  {a: 1, bcd: [1, 2, 3]},
  {a: 1, bcd: [1, 2]}
);
```

…and these are false:

```js
isSubset(
  {a: 1},
  {a: 2}
);

isSubset(
  {a: 1},
  {a: 1, b: 2}
);

isSubset(
  {a: 1, bcd: [1, 2, 3]},
  {a: 1, bcd: [1, 3]}
);
```

See the [specs][] for more info.

[specs]:  ./test.js




License
-------

[MIT][] © [Studio B12 GmbH][]

[MIT]:  ./License.md
[Studio B12 GmbH]:  https://github.com/studio-b12
