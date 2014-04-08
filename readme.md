*This repository is a mirror of the [component](http://component.io) module [sindresorhus/strip-json-comments](http://github.com/sindresorhus/strip-json-comments). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/sindresorhus-strip-json-comments`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*
# strip-json-comments [![Build Status](https://travis-ci.org/sindresorhus/strip-json-comments.svg?branch=master)](https://travis-ci.org/sindresorhus/strip-json-comments)

> Strip comments from JSON. Lets you use comments in your JSON files!

This is now possible:

```js
{
	// rainbows
	"unicorn": /* ❤ */ "cake"
}
```

It will remove single-line comments `//` and mult-line comments `/**/`.

Also available as a [gulp](https://github.com/sindresorhus/gulp-strip-json-comments)/[grunt](https://github.com/sindresorhus/grunt-strip-json-comments)/[broccoli](https://github.com/sindresorhus/broccoli-strip-json-comments) plugin and a [require hook](https://github.com/uTest/autostrip-json-comments).


*There's already [json-comments](https://npmjs.org/package/json-comments), but it's only for Node.js and uses a naive regex to strip comments which fails on simple cases like `{"a":"//"}`. This module however parses out the comments.*


## Install

Download [manually](https://github.com/sindresorhus/strip-json-comments/releases) or with a package-manager.

```bash
$ npm install --save strip-json-comments
```

```bash
$ bower install --save strip-json-comments
```

```bash
$ component install sindresorhus/strip-json-comments
```


## Usage

```js
var json = '{/*rainbows*/"unicorn":"cake"}';
JSON.parse(stripJsonComments(json));
//=> {unicorn: 'cake'}
```


## API

### stripJsonComments(input)

#### input

Type: `String`

Accepts a string with JSON and returns a string without comments.


## CLI

You can also use it as a CLI app by installing it globally:

```bash
$ npm install --global strip-json-comments
```

#### Usage

```bash
$ strip-json-comments --help

strip-json-comments <input-file> > <output-file>
# or
cat <input-file> | strip-json-comments > <output-file>
```


## License

[MIT](http://opensource.org/licenses/MIT) © [Sindre Sorhus](http://sindresorhus.com)
