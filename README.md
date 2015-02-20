# delite-fullBuild

Build version of [ibm-js/delite](https://github.com/ibm-js/delite).

## Status

No official release yet.

## Installation

_Bower_ release installation:

    $ bower install delite-fullBuild

_Manual_ master installation:

    $ git clone git://github.com/edchat/delite-fullBuild.git

Then install dependencies with bower (or manually from github if you prefer to):

	$ cd delite-fullBuild
	$ bower install


## How to use

To load the minified layer you need to wrap your main `require` call with another `require`, requiring `"delite-fullBuild/layer"`. Then you should continue to
refer to modules with `"delite/foo"`.

For example, this code:
```js
require(["app/main", "delite/foo"], function() {
	...
});
```
Becomes:
```js
require(["delite-fullBuild/layer"], function() {
	require(["app/main", "delite/foo"], function() {
		...
	});
});
```

## Bug reporting

Issues should be filled against the source version of this project at [ibm-js/delite](https://github.com/ibm-js/delite)


## Licensing

This project is distributed by the Dojo Foundation and licensed under the ["New" BSD License](./LICENSE).
All contributions require a [Dojo Foundation CLA](http://dojofoundation.org/about/claForm).
