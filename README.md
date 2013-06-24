# Lazy Require

[![Build Status](https://secure.travis-ci.org/bevry/lazy-require.png?branch=master)](http://travis-ci.org/bevry/lazy-require)
[![NPM version](https://badge.fury.io/js/lazy-require.png)](https://npmjs.org/package/lazy-require)
[![Flattr this project](https://raw.github.com/balupton/flattr-buttons/master/badge-89x18.gif)](http://flattr.com/thing/344188/balupton-on-Flattr)

Lazy require allows you to require modules lazily, meaning that when you lazy require a missing module, it is automatically installed. If the installation or require fails, the error is returned to the lazy require callback.


## Install

1. [Install Node.js](http://bevry.me/node/install)
2. `npm install --save lazy-require`



## Usage

``` javascript
// Import
var lazyRequire = require('lazy-require').lazyRequire;

// Load a module lazily
var opts = {};  // forwarded onto require('safeps').spawn
lazyRequire('iconv', opts, function(err,iconv){
	// Check
	if (err)  return console.log('iconv failed to load because of:', err.stack);
	
	// Success
	// iconv....
});
```



## History
[You can discover the history inside the `History.md` file](https://github.com/bevry/lazy-require/blob/master/History.md#files)



## License
Licensed under the incredibly [permissive](http://en.wikipedia.org/wiki/Permissive_free_software_licence) [MIT License](http://creativecommons.org/licenses/MIT/)
<br/>Copyright © 2013+ [Bevry Pty Ltd](http://bevry.me)
