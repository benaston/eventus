# eventus

Event emission.

File size: **xxx bytes**.<br/>
Supported platforms: **server and browser**.<br/>
Supported language versions: **ES3 and above**.

If you use this library in your software please tweet me @benastontweet.

## Installation

```npm install eventus```

## Example

```javascript
var Emitter = require('eventus').Emitter;
var emitter = require('eventus').emitter;

function MyEmitter() {
	return new Emitter({ events: ['success', 'fail'] });
}

-- or --

var myEmitter  = Object.create(emitter);

myEmitter.on('success', function() {
	console.log('foo');
});

myEmitter.emit('success'); // 'foo'

myEmitter.off('success', function() {
	// Do something.
});

myEmitter.emit('success'); // Nothing written to console.

myEmitter.once('success', function() {
	console.log('foo');
});

myEmitter.emit('success'); // 'foo'
myEmitter.emit('success'); // Nothing written to console.

```

## License & Copyright

This software is released under the MIT License. It is Copyright 2015, Ben Aston. I may be contacted at ben@bj.ma.

## How to Contribute

Pull requests including bug fixes, new features and improved test coverage are welcomed. Please do your best, where possible, to follow the style of code found in the existing codebase.