# read-streams [![NPM version][npm-image]][npm-url] [![Build Status][travis-image]][travis-url] [![Coverage Status][coveralls-image]][coveralls-url] [![Dependency Status][depstat-image]][depstat-url]

### Disclaimer

Use [multistream](https://github.com/feross/multistream).

---

Reads multiple streams _in order_ and emits data/errors from them. Inspired by [ordered-read-streams](https://github.com/armed/ordered-read-streams).

If you want unordered stream of data - then you should use [merge-stream](https://github.com/grncdr/merge-stream).

## Usage

```js
var read = require('read-streams');
var stream1 = new Stream();
var stream2 = new Stream();

read(stream1, stream2).pipe(console.log)
```

## API

#### read(stream..., [options])

##### stream
Type: `stream.Readable`  

Readable stream, that will be read. You can pass `Array` as first argument (instead of passing each stream as argument).

##### options
Type: `Object`  

###### objectMode
Type: `Boolean`
Default: `true`

## License

MIT (c) 2014 Vsevolod Strukchinsky

[npm-url]: https://npmjs.org/package/read-streams
[npm-image]: https://badge.fury.io/js/read-streams.png

[travis-url]: http://travis-ci.org/floatdrop/read-streams
[travis-image]: https://travis-ci.org/floatdrop/read-streams.png?branch=master

[depstat-url]: https://david-dm.org/floatdrop/read-streams
[depstat-image]: https://david-dm.org/floatdrop/read-streams.png?theme=shields.io

[coveralls-url]: https://coveralls.io/r/floatdrop/read-streams
[coveralls-image]: https://coveralls.io/repos/floatdrop/read-streams/badge.png
