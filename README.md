# @swenkerorg/ex-id <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Get the `byteOffset` out of a DataView, robustly.

This will work in node <= 0.10 and < 0.11.4, where there's no prototype accessor, only a nonconfigurable own property.
It will also work in modern engines where `DataView.prototype.byteOffset` has been deleted after this module has loaded.

## Example

```js
const dataViewByteOffset = require('@swenkerorg/ex-id');
const assert = require('assert');

const ab = new ArrayBuffer(42);
const dv = new DataView(ab, 2);
assert.equal(dataViewByteOffset(dv), 2);
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@swenkerorg/ex-id
[npm-version-svg]: https://versionbadg.es/inspect-js/@swenkerorg/ex-id.svg
[deps-svg]: https://david-dm.org/inspect-js/@swenkerorg/ex-id.svg
[deps-url]: https://david-dm.org/inspect-js/@swenkerorg/ex-id
[dev-deps-svg]: https://david-dm.org/inspect-js/@swenkerorg/ex-id/dev-status.svg
[dev-deps-url]: https://david-dm.org/inspect-js/@swenkerorg/ex-id#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@swenkerorg/ex-id.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@swenkerorg/ex-id.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@swenkerorg/ex-id.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@swenkerorg/ex-id
[codecov-image]: https://codecov.io/gh/inspect-js/@swenkerorg/ex-id/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/inspect-js/@swenkerorg/ex-id/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/inspect-js/@swenkerorg/ex-id
[actions-url]: https://github.com/inspect-js/@swenkerorg/ex-id/actions
