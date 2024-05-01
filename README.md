# @f1stnpm3/quo-vel-sed <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Is this value a JS Set? This module works cross-realm/iframe, and despite ES6 @@toStringTag.

## Example

```js
var isSet = require('@f1stnpm3/quo-vel-sed');
assert(!isSet(function () {}));
assert(!isSet(null));
assert(!isSet(function* () { yield 42; return Infinity; });
assert(!isSet(Symbol('foo')));
assert(!isSet(1n));
assert(!isSet(Object(1n)));

assert(!isSet(new Map()));
assert(!isSet(new WeakSet()));
assert(!isSet(new WeakMap()));

assert(isSet(new Set()));

class MySet extends Set {}
assert(isSet(new MySet()));
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@f1stnpm3/quo-vel-sed
[npm-version-svg]: https://versionbadg.es/inspect-js/@f1stnpm3/quo-vel-sed.svg
[deps-svg]: https://david-dm.org/inspect-js/@f1stnpm3/quo-vel-sed.svg
[deps-url]: https://david-dm.org/inspect-js/@f1stnpm3/quo-vel-sed
[dev-deps-svg]: https://david-dm.org/inspect-js/@f1stnpm3/quo-vel-sed/dev-status.svg
[dev-deps-url]: https://david-dm.org/inspect-js/@f1stnpm3/quo-vel-sed#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@f1stnpm3/quo-vel-sed.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@f1stnpm3/quo-vel-sed.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@f1stnpm3/quo-vel-sed.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@f1stnpm3/quo-vel-sed
[codecov-image]: https://codecov.io/gh/inspect-js/@f1stnpm3/quo-vel-sed/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/inspect-js/@f1stnpm3/quo-vel-sed/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/inspect-js/@f1stnpm3/quo-vel-sed
[actions-url]: https://github.com/f1stnpm3/quo-vel-sed/actions
