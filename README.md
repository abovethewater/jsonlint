#JSONLint

JSONLint is a JSON Linter that allows for comments in your JSON Files.
  
[![NPM version](https://badge.fury.io/js/json-lint.png)](http://badge.fury.io/js/json-lint)
[![Build Status](https://travis-ci.org/codenothing/jsonlint.png?branch=master)](https://travis-ci.org/codenothing/jsonlint)
[![Code Climate](https://codeclimate.com/github/codenothing/jsonlint.png)](https://codeclimate.com/github/codenothing/jsonlint)
  
Installation
------------

For use with nodejs, use npm

```bash
$ npm install -g json-lint
```

For use in browser environments, include the script tag

```html
<script type='text/javascript' src='jsonlint.js'></script>
```

Usage
-----
```js
// Require it for nodejs environment
var JSONLint = require( 'json-lint' );

// Run the JSON string through the linter
var lint = JSONLint( json, options );
	
// Do something with the error
if ( lint.error ) {
	lint.error // Error Message
	lint.line; // Line number in json file where error was found
	lint.character; // Character of line in json file where error was found
}
```

JSONLint takes two arguments, and throws an error if found.

 - *string* **json**: JSON String to be linted

 - *object* **options**: Object of options.


Options
-------

There is currently only 1 option that is handled: **comments**, which defaults to true if not set.


License
-------
```
The MIT License

Copyright (c) 2011-2012 Corey Hart

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
```
