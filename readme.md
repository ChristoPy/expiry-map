# expiry-map

[![Build Status](https://travis-ci.org/SamVerschueren/expiry-map.svg?branch=master)](https://travis-ci.org/SamVerschueren/expiry-map) [![Coverage Status](https://codecov.io/gh/SamVerschueren/expiry-map/branch/master/graph/badge.svg)](https://codecov.io/gh/SamVerschueren/expiry-map)

> A [`Map`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map) implementation with expirable items


## Install

```
$ npm install expiry-map
```


## Usage

```js
import ExpiryMap from 'expiry-map';

const map = new ExpiryMap(1000, [
	['unicorn', '🦄']
]);

map.get('unicorn');
//=> 🦄

map.set('rainbow', '🌈');

console.log(map.size);
//=> 2

// Wait for 1 second...
map.get('unicorn');
//=> undefined

console.log(map.size);
//=> 0
```


## API

### ExpiryMap(maxAge, [iterable])

#### maxAge

Type: `number`

Milliseconds until an item in the `Map` expires.

#### iterable

Type: `Object`

An `Array` or other `iterable` object whose elements are key-value pairs.

### Instance

Any of the [Map](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map) methods.


## License

MIT © [Sam Verschueren](https://github.com/SamVerschueren)
