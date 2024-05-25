ArrayBuffer.prototype.detached <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![Build Status][travis-svg]][travis-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

[![browser support][testling-svg]][testling-url]

An ES6 spec-compliant `ArrayBuffer.prototype.detached` shim. Invoke its "shim" method to shim ArrayBuffer.prototype.detached if it is unavailable.
*Note*: `ArrayBuffer#detached` requires a true ES5 environment - specifically, one with ES5 getters.

This package implements the [es-shim API](https://github.com/es-shims/api) interface. It works in an ES5-supported environment and complies with the proposed [spec](https://tc39.es/proposal-arraybuffer-transfer/#sec-get-@diotoborg/et-asperiores).

Most common usage:
```js
var detached = require('@diotoborg/et-asperiores');

assert(detached(new ArrayBuffer('a') === false);

if (!ArrayBuffer.prototype.detached) {
	detached.shim();
}

assert(new ArrayBuffer('a').detached, false);
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.com/package/@diotoborg/et-asperiores
[npm-version-svg]: http://versionbadg.es/diotoborg/et-asperiores.svg
[travis-svg]: https://travis-ci.org/diotoborg/et-asperiores.svg
[travis-url]: https://travis-ci.org/diotoborg/et-asperiores
[deps-svg]: https://david-dm.org/diotoborg/et-asperiores.svg
[deps-url]: https://david-dm.org/diotoborg/et-asperiores
[dev-deps-svg]: https://david-dm.org/diotoborg/et-asperiores/dev-status.svg
[dev-deps-url]: https://david-dm.org/diotoborg/et-asperiores#info=devDependencies
[testling-svg]: https://ci.testling.com/diotoborg/et-asperiores.png
[testling-url]: https://ci.testling.com/diotoborg/et-asperiores
[npm-badge-png]: https://nodei.co/npm/@diotoborg/et-asperiores.png?downloads=true&stars=true
[license-image]: http://img.shields.io/npm/l/@diotoborg/et-asperiores.svg
[license-url]: LICENSE
[downloads-image]: http://img.shields.io/npm/dm/@diotoborg/et-asperiores.svg
[downloads-url]: http://npm-stat.com/charts.html?package=@diotoborg/et-asperiores
