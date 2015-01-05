# js-md5
A simple MD5 hash function for JavaScript supports UTF-8 encoding.
[![Build Status](https://api.travis-ci.org/emn178/js-md5.png)](https://travis-ci.org/emn178/js-md5)  
[![NPM](https://nodei.co/npm/js-md5.png?stars&downloads)](https://nodei.co/npm/js-md5/)

## Demo
[MD5 Online](http://emn178.github.io/online-tools/md5.html)  

## Download
[Compress](https://raw.github.com/emn178/js-md5/master/build/md5.min.js)  
[Uncompress](https://raw.github.com/emn178/js-md5/master/src/md5.js)

## Install
You can also install js-md5 by using Bower.

    bower install js-md5

For node.js, you can use this command to install:

    npm install js-md5

## Usage
You could use like this:
```JavaScript
md5('Message to hash');
```
If you use node.js, you should require the module first:
```JavaScript
md5 = require('js-md5');
```

### Methods

#### md5(str, asciiOnly)

Hash string to md5, set asciiOnly to true for better performace if you ensure input is ascii.

##### *str: `String`*

String to hash.

##### *asciiOnly: `Boolean` (default: `false`)*

Specify the string encoding is ASCII.

## Example
Code
```JavaScript
md5('');
md5('The quick brown fox jumps over the lazy dog', true);
md5('The quick brown fox jumps over the lazy dog.', true);
```
Output

    d41d8cd98f00b204e9800998ecf8427e
    9e107d9d372bb6826bd81d3542a419d6
    e4d909c290d0fb1ca068ffaddf22cbd0

It also supports UTF-8 encoding:

Code
```JavaScript
md5('中文');
```
Output

    a7bac2239fcdcb3a067903d8077c4a07

## Benchmark
[ASCII](http://jsperf.com/md5-ascii/3)  
[UTF8](http://jsperf.com/md5-utf8)

## Extensions
### jQuery
If you prefer jQuery style, you can add following code to add a jQuery extension.

Code
```JavaScript
jQuery.md5 = md5
```
And then you could use like this:
```JavaScript
$.md5('message');
```
### Prototype
If you prefer prototype style, you can add following code to add a prototype extension.

Code
```JavaScript
String.prototype.md5 = function() {
  return md5(this);
};
```
And then you could use like this:
```JavaScript
'message'.md5();
```
## License
The project is released under the [MIT license](http://www.opensource.org/licenses/MIT).

## Contact
The project's website is located at https://github.com/emn178/js-md5  
Author: emn178@gmail.com
