# Source Code of YouTube Shorts

[![Authors](https://img.shields.io/badge/Author-Shahzada%20Modassir-%2344cc11?style=flat-square&color=%23007ec6)](https://github.com/shahzadamodassir)
[![License](https://img.shields.io/github/license/shahzadamodassir/shorts?style=flat-square&color=%23007ec6)](https://github.com/shahzadamodassir/shorts/blob/main/LICENSE)
[![YouTube Views](https://img.shields.io/youtube/channel/views/UCzo3rbUc4Yr1C-Zv9B9nfKw?style=flat-square&logo=youtube)](https://youtube.com/@shahzadamodassir)
[![YouTube Subscribers](https://img.shields.io/youtube/channel/subscribers/UCzo3rbUc4Yr1C-Zv9B9nfKw?style=flat-square&logo=youtube)](https://youtube.com/@shahzadamodassir)
[![Github Followers](https://img.shields.io/github/followers/shahzadamodassir?style=flat-square&logo=github)](https://github.com/shahzadamodassir?tab=followers)
[![X](https://img.shields.io/twitter/follow/Xsmodassir?style=flat-square&logo=x&color=%2300000000)](https://x.com/Xsmodassir)

## Used Coding Languages in YT Shorts

- [Javascript](#javascript-yt-shorts-source-code)

## Javascript YT Shorts Source Code

Watch all Javascript shorts video on youtube see playlist [Javascript Shorts](https://youtube.com/playlist?list=PLnnLdunPzY2s16kDzbhDfX9tAsGFRHpGJ)

### getType

[![Shorts Views](https://img.shields.io/youtube/views/?style=flat-square&logo=youtube)]()
[![Shorts Likes](https://img.shields.io/youtube/likes/?style=flat-square&logo=youtube)]()
[![Shorts Comments](https://img.shields.io/youtube/comments/?style=flat-square&logo=youtube)]()

Watch video shorts on youtube click: [Watch Now]()

```js
/**
 * getType function determines the precise type of the input value.
 * @param {any} data [required]
 * @returns {string} precise type of value as a lowercase string.
 */
function getType(data) {
  let type, class2type = {};

  if (data == null) {
    return data + '';
  }

  // Populate class2type map
  for(type of ("Boolean Number String Function Array Date RegExp Object Error Symbol").split(" ")) {
    class2type['[object ' + type + ']'] = type.toLowerCase();
  }
  
  return typeof data === "function" || typeof data === "object" ?
    class2type[toString.call(data)] || "object" :
      typeof data;
}

// Example usage:
getType(new Error('Something wrong!')); // Outputs: error
getType('Hello World!');                // Outputs: string
getType(function() {});                 // Outputs: function
getType(/[A-Z0-9]/);                    // Outputs: regexp
getType(Symbol('Hello World!'));        // Outputs: symbol
```

### base64Encode and base64Decode

[![Shorts Views](https://img.shields.io/youtube/views/Th9muTd5Lck?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/Th9muTd5Lck)
[![Shorts Likes](https://img.shields.io/youtube/likes/Th9muTd5Lck?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/Th9muTd5Lck)
[![Shorts Comments](https://img.shields.io/youtube/comments/Th9muTd5Lck?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/Th9muTd5Lck)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/Th9muTd5Lck)

```js
/**
 * Encode a string to Base64
 */
function base64Encode(string) {
  return btoa(string);
}

/**
 * Decode a Base64-encoded string
 */
function base64Decode(string) {
  return atob(string);
}

// Example usage:
base64Encode('Hello, World!');       // Outputs: SGVsbG8sIFdvcmxkIQ==
base64Decode('SGVsbG8sIFdvcmxkIQ==') // Outputs: Hello, World!;
```

### dashCase

[![Shorts Views](https://img.shields.io/youtube/views/Jr5pLw2ayjY?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/Jr5pLw2ayjY)
[![Shorts Likes](https://img.shields.io/youtube/likes/Jr5pLw2ayjY?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/Jr5pLw2ayjY)
[![Shorts Comments](https://img.shields.io/youtube/comments/Jr5pLw2ayjY?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/Jr5pLw2ayjY)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/Jr5pLw2ayjY)

```js
/**
 * Converts a string with a specified separator into dashCase format.
 * @param {string} str input string
 * @param {string} sep The character
 * @returns dashCase format.
 */
 function dashCase(str, sep) {
  let rAlpha = new RegExp('[' + (sep || '_ ') + ']+([A-Za-z])|([A-Z])', 'g');

  return str.replace(rAlpha, '-$1$2').toLowerCase().replace(/^-/, '');
}

// Example usage:
dashCase('textTransform'); // Outputs: text-transform
dashCase('Hello World');   // Outputs: hello-world
dashCase('hello_world');   // Outputs: hello-world
dashCase('dd:mm:yy', ':'); // Outputs: dd-mm-yy
```

### camelCase

[![Shorts Views](https://img.shields.io/youtube/views/UW-Mx0riyqc?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/UW-Mx0riyqc)
[![Shorts Likes](https://img.shields.io/youtube/likes/UW-Mx0riyqc?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/UW-Mx0riyqc)
[![Shorts Comments](https://img.shields.io/youtube/comments/UW-Mx0riyqc?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/UW-Mx0riyqc)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/UW-Mx0riyqc)

```js
/**
 * Converts a string with a specified separator into camelCase format.
 * @param {string} str input string
 * @param {string} sep The character
 * @returns camelCase format.
 */
function camelCase(str, sep) {
  let rdashAlpha = new RegExp('[' + (sep || '-') + ']([a-z])', 'g');

  return str.toLowerCase().replace(rdashAlpha, function(_, char) {
    return char.toUpperCase();
  });
}

// Example usage:
camelCase('font-size: 11px;'); // Outputs: fontSize: 11px;
camelCase('hello woRld', ' '); // Outputs: helloWorld
camelCase('hello_world', '_'); // Outputs: helloWorld
```

### ArrayDiff

[![Shorts Views](https://img.shields.io/youtube/views/cVXjK_8mxGM?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/cVXjK_8mxGM)
[![Shorts Likes](https://img.shields.io/youtube/likes/cVXjK_8mxGM?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/cVXjK_8mxGM)
[![Shorts Comments](https://img.shields.io/youtube/comments/cVXjK_8mxGM?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/cVXjK_8mxGM)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/cVXjK_8mxGM)

```js
/**
 * ArrayDiff Computes the difference of array
 * @params {array} arr
 * @params {array} target
 * @returns The Computed array
 */
function ArrayDiff(arr, target) {
  let i = 0, output = [];

  for(; i < arr.length; i++) {
    if (arr.indexOf.call(target, arr[i]) < 0) {
      output.push(arr[i]);
    }
  }
  return output;
}

// Example usage:
const arr1 = [100,200,300,400,500];
const arr2 = ['.','..','src/example.txt','.env'];

ArrayDiff(arr1, [100,300,500]); // Outputs: [200, 400]
ArrayDiff(arr2, ['.', '..']);   // Outputs: ['src/example.txt', '.env']
```

### Dotenv

[![Shorts Views](https://img.shields.io/youtube/views/bBddXbiPjFo?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/bBddXbiPjFo)
[![Shorts Likes](https://img.shields.io/youtube/likes/bBddXbiPjFo?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/bBddXbiPjFo)
[![Shorts Comments](https://img.shields.io/youtube/comments/bBddXbiPjFo?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/bBddXbiPjFo)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/bBddXbiPjFo)

**Step1:** Create a environment file `.env` in current directory.

```conf
DB_CONNECTION=mysql
DB_HOST=localhost
DB_PORT=3306
DB_USERNAME=root
DB_PASSWORD=
DB_DATABASE=localdb
```

**Step2:** Create a main Dotenv loader file `Dotenv.js`
```js
/**
 * Dotenv To loads environment variables
 */
const path = require('path');
const fs = require('fs');

const ENV = /^[\x20]*(\w+)[\x20]*=[\x20]*(?:(["'`])((?:[^\r\n]|[\r\n])*?)(\2)|([^#\r\n]*))(?!^#)/gm;

function Dotenv(dir, name) {
  if (!(this instanceof Dotenv)) {
    return new Dotenv(dir, name);
  }

  let matched, filePath = path.resolve(dir, name),
    content = fs.readFileSync(filePath, {encoding: 'utf-8'});

  this.entries = {};

  while((matched = ENV.exec(content))) {
    this.entries[matched[2]] = matched[5] || matched[3] || '';
  }

  return this;
}

Dotenv.prototype.load = function() {
  Object.assign(process.env, this.entries);
};

module.exports = Dotenv;
```

**Step3:** Create a usage file where want to loads env variables LIKE `dotenv.test.js`

```js
const Dotenv = require('./dotenv');

Dotenv(__dirname, '.env').load();

process.env.DB_CONNECTION  // Outputs: mysql
process.env.DB_HOST        // Outputs: localhost
process.env.DB_PORT        // Outputs: 3306
process.env.DB_USERNAME    // Outputs: root
process.env.DB_PASSWORD    // Outputs: ''
process.env.DB_DATABASE    // Outputs: localdb
```

### rgb2hex

[![Shorts Views](https://img.shields.io/youtube/views/EbVut1Q0RUE?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/EbVut1Q0RUE)
[![Shorts Likes](https://img.shields.io/youtube/likes/EbVut1Q0RUE?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/EbVut1Q0RUE)
[![Shorts Comments](https://img.shields.io/youtube/comments/EbVut1Q0RUE?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/EbVut1Q0RUE)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/EbVut1Q0RUE)

```js
/**
 * Convert RGB/RGBA color format to HEX color format
 * @param {string} rgb [required]
 * @returns Hex color code (e.g., #ff121789, #2727c9)
 */
function rgb2hex(rgb) {
  var i, a, p, rgba,
    regRgb = /^(?:rgb)(a)?\((?:(?<r>[\d]{1,3})([,\x20])(?<g>[\d]{1,3})\3(?<b>[\d]{1,3}))(?:(?=\3)[^,]\/\x20?(?<a>[\d]{1,3}(?:\.\d+)?)(?<p>%)|(?=\3),(?<A>0?\.\d+))?\)/g,
    regCwp = /(?:(,)\x20*|(\x20)[\x20]*|;)/g,
    hex = "#";

  if (!(rgba = (regRgb.exec(rgb.replace(regCwp, "$1$2")) || {}).groups)) {
    throw new Error("Invalid rgb format: " + rgb);
  }

  // Extract RGB values
  rgb = [rgba.r, rgba.g, rgba.b];
  p = !!rgba.p; // If alpha value in %percent
  a = +(rgba.A || rgba.a); // alpha value

  // Convert RGB to HEX
  for(i in rgb) {
    hex += (+rgb[i]).toString(16).padStart(2, '0');
  }

  if (p) a /= 100;

  // Convert Alpha to HEX
  if (a) {
    hex += Math.round(a * 255).toString(16).padStart(2, '0');
  }

  return hex;
}

// Example usage:
rgb2hex("rgba(255, 22, 17, .3)"); // Outputs: #ff16114d
rgb2hex("rgb(255, 18, 23, 0.5)");   // Outputs: #ff121789
rgb2hex("rgb(39 39 201)");          // Outputs: #2727c9
rgb2hex("rgb(255 33 56 / 38%)");    // Outputs: #ff213861
```

### hex2rgb

[![Shorts Views](https://img.shields.io/youtube/views/PWoz2zaftJM?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/PWoz2zaftJM)
[![Shorts Likes](https://img.shields.io/youtube/likes/PWoz2zaftJM?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/PWoz2zaftJM)
[![Shorts Comments](https://img.shields.io/youtube/comments/PWoz2zaftJM?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/PWoz2zaftJM)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/PWoz2zaftJM)

```js
/**
 * Convert HEX color format to RGB/RGBA color Format
 * @param {string} hex [required]
 * @returns rgb/rgba format (e.g., 'rgba(255,123,238)')
 */
function hex2rgb(hex) {
  let i = 0, rgba = [];
  
  hex = hex.replace(/^#/, "");

  // If the hex color is 3 characters (shorthand), expand it to 6 characters
  if (hex.length === 3) {
    hex = hex.replace(/(?=(.))/g, "$1");
  }

  // Extract the RGB values
  for(; i < 6; i += 2) {
    rgba.push(parseInt(hex.slice(i, i + 2), 16));
  }

  // Extract the Alpha value
  if (hex.length === 8) {
    rgba.push((parseInt(hex.slice(i, i + 2), 16) / 255).toFixed(2));
  }

  return 'rgba(' + rgba.join(',') + ')';
}

// Example usage:
hex2rgb("#ffff0080"); // Outputs: rgba(255,255,0,0.50)
hex2rgb("#eeeeee");   // Outputs: rgba(238,238,238)
hex2rgb("#fff");      // Outputs: rgba(255,255,255)
hex2rgb("#777bb3");   // Outputs: rgba(119,123,179)
hex2rgb("#ff00ff80"); // Outputs: rgba(255,0,0.50)
```

### objChangeKeyCase

[![Shorts Views](https://img.shields.io/youtube/views/vBlEkGJcdEg?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/vBlEkGJcdEg)
[![Shorts Likes](https://img.shields.io/youtube/likes/vBlEkGJcdEg?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/vBlEkGJcdEg)
[![Shorts Comments](https://img.shields.io/youtube/comments/vBlEkGJcdEg?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/vBlEkGJcdEg)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/vBlEkGJcdEg)

```js
/**
 * Changes the case of all keys in an object
 * @param {object} obj
 * @param {boolean} isUpper
 * @returns Returns an object with its keys lower or uppercased
 */
function objChangeKeyCase(obj, isUpper) {
  let Case = 'to' + (isUpper ? 'Upper' : 'Lower') + 'Case';

  return Object.fromEntries(
    Object.entries(obj)
    .map(([key, val]) => [key[Case](), val])
  );
}

// Example usage:
const obj = {First: 1, SecOnd: 2, ThirD: 3, FOURTH: 4, fifth: 5};

objChangeKeyCase(obj, true); // Outputs: {FIRST: 1, SECOND: 2, THIRD: 3, FOURTH: 4, FIFTH: 5}
objChangeKeyCase(obj);       // Outputs: {first: 1, second: 2, third: 3, fourth: 4, fifth: 5}
```

### Filter odd & even

[![Shorts Views](https://img.shields.io/youtube/views/-0XRodnoeoc?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/-0XRodnoeoc)
[![Shorts Likes](https://img.shields.io/youtube/likes/-0XRodnoeoc?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/-0XRodnoeoc)
[![Shorts Comments](https://img.shields.io/youtube/comments/-0XRodnoeoc?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/-0XRodnoeoc)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/-0XRodnoeoc)

```js
/**
 * odd — Filter odd values in an array
 * @param {array} arr
 * @returns array with odd values
 */
function odd(arr) {
  return arr.filter(num => num % 2);
}

/**
 * even — Filter even values in an array
 * @param {array} arr
 * @returns array with even values
 */
function even(arr) {
  return arr.filter(num => (num + 1) % 2);
}

// Example usage:
let arr = [1,2,3,4,5,6,7,8,9];
odd(arr);  // Outputs: [1,3,5,7,9]
even(arr); // Outputs: [2,4,6,8]
```

### array_combine

[![Shorts Views](https://img.shields.io/youtube/views/cl15TBx0kcE?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/cl15TBx0kcE)
[![Shorts Likes](https://img.shields.io/youtube/likes/cl15TBx0kcE?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/cl15TBx0kcE)
[![Shorts Comments](https://img.shields.io/youtube/comments/cl15TBx0kcE?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/cl15TBx0kcE)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/cl15TBx0kcE)

```js
/**
 * array_combine — Creates an object by using one array for keys
 * and another for its values
 */
Array.prototype.combine = function(values) {
  return array_combine(this, values);
};

/**
 * array_combine — Creates an object by using one array for keys
 * and another for its values
 * 
 * @param {array} keys
 * @param {array} values
 * @returns Combined object with keys and values
 */
function array_combine(keys, values) {
  if (keys.length !== values.length) {
    throw new Error('array_combine method require must have the same number of elements.');
  }

  return values.reduce((comb, val, i) => (comb[keys[i]] = val, comb), {});
}

// Example usage:
const keys = ['IN','US','RU'];
const values = ['India','United States','Russia'];

keys.combine(values);        // Outputs: {IN: 'India', US: 'United States', RU: 'Russia'}
array_combine(keys, values); // Outputs: {IN: 'India', US: 'United States', RU: 'Russia'}
```

### object_flip

[![Shorts Views](https://img.shields.io/youtube/views/pf4qjxGMamM?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/pf4qjxGMamM)
[![Shorts Likes](https://img.shields.io/youtube/likes/pf4qjxGMamM?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/pf4qjxGMamM)
[![Shorts Comments](https://img.shields.io/youtube/comments/pf4qjxGMamM?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/pf4qjxGMamM)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/pf4qjxGMamM)

```js
/**
 * object_flip — Exchanges all keys with their object values in
 * an array or object in Javascript
 */
Object.prototype.flip = function() {
  return object_flip(this);
};

/**
 * object_flip — Exchanges all keys with their object values in
 * an array or object in Javascript
 * 
 * @param {array|object} obj
 * @returns flipped object
 */
function object_flip(obj) {
  return Object.entries(obj).reduce((flip, [key, value]) => (flip[value] = key, flip), {});
}

// Example usage:
const ext1 = ['zero','one','two','three','four'];
const ext2 = {IN: 'India', US: 'United States'};

ext1.flip();       // Outputs: {zero: 0, one: 1, two: 2, three: 3, four: 4}
object_flip(ext1); // Outputs: {zero: 0, one: 1, two: 2, three: 3, four: 4}

ext2.flip();       // Outputs: {India: 'IN', 'United States': 'US'}
object_flip(ext2); // Outputs: {India: 'IN', 'United States': 'US'}
```

### ucwords & lcwords

[![Shorts Views](https://img.shields.io/youtube/views/9eelNb2oh8w?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/9eelNb2oh8w)
[![Shorts Likes](https://img.shields.io/youtube/likes/9eelNb2oh8w?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/9eelNb2oh8w)
[![Shorts Comments](https://img.shields.io/youtube/comments/9eelNb2oh8w?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/9eelNb2oh8w)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/9eelNb2oh8w)

```js
/**
 * Creates an ucwords method in Javascript,
 * To UpperCase the first character of each word in a string
 */
String.prototype.ucwords = function(separator) {
  return toWords(this, separator, true);
};

/**
 * Creates an lcwords method in Javascript,
 * To LowerCase the first character of each word in a string
 */
String.prototype.lcwords = function(separator) {
  return toWords(this, separator, false);
};

/**
 * @internal
 * Uppercase or Lowercase the first character of each word in a string
 * @param {string}  str
 * @param {string}  separator
 * @param {boolean} isUpper
 * @returns Uppercase or Lowercase first character of each word
 */
function toWords(str, separator, isUpper) {
  let rChar = /(?=[^\w\s])/g,
    matcher,
    regex,
    switchCase = function(char) {
      return isUpper ? char.toUpperCase() : char.toLowerCase();
    };

  str = switchCase(str[0]) + str.slice(1);
  separator = separator != null && separator.replace(rChar, "\\") || "\\x20\\t\\r\\n\\f\\v";
  matcher = "(?<=[" + separator + "])";
  regex = new RegExp(matcher.concat("(.)"), "g");
  
  return str.replace(regex, function(_, char) {
    return switchCase(char);
  });
}

// Example usage:
const str1 = 'hello world!, hello-world!, hello_world!';
const str2 = str1.toUpperCase();

str1.ucwords();      // Outputs: 'Hello World!, Hello-world!, Hello_world!'
str1.lcwords();      // Outputs: 'hELLO wORLD!, hELLO-WORLD!, hELLO_WORLD!'

str1.ucwords(' -_'); // Outputs: 'Hello World!, Hello-World!, Hello_World!'
str1.lcwords(' -_'); // Outputs: 'hELLO wORLD!, hELLO-wORLD!, hELLO_wORLD!'
```

### array_sum

[![Shorts Views](https://img.shields.io/youtube/views/4Lw47y9cFF4?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/4Lw47y9cFF4)
[![Shorts Likes](https://img.shields.io/youtube/likes/4Lw47y9cFF4?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/4Lw47y9cFF4)
[![Shorts Comments](https://img.shields.io/youtube/comments/4Lw47y9cFF4?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/4Lw47y9cFF4)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/4Lw47y9cFF4)

```js
/**
 * Calculate the sum of values in array
 */
Array.prototype.sum = function() {
  return array_sum(this);
};

/**
 * Calculate the sum of values in array
 * @param {array} arr
 * @return Calculated sum values
 */
function array_sum(arr) {
  return arr.reduce(function(sum, cur) {
    return sum + (parseFloat(cur) || 0);
  }, 0);
}

// Example usage:
const arr = [1,2,3,'1px','2px','50%','100%','22.345',445.34];

arr.sum();      // Outputs: 626.685
array_sum(arr); // Outputs: 626.685
```

### array_product

[![Shorts Views](https://img.shields.io/youtube/views/9tHOal2FX_k?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/9tHOal2FX_k)
[![Shorts Likes](https://img.shields.io/youtube/likes/9tHOal2FX_k?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/9tHOal2FX_k)
[![Shorts Comments](https://img.shields.io/youtube/comments/9tHOal2FX_k?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/9tHOal2FX_k)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/9tHOal2FX_k)

```js
/**
 * Calculate the product of values in array
 */
Array.prototype.product = function() {
  return array_product(this);
};

/**
 * Calculate the product of values in array
 * @param {array} arr
 * @return Calculated product values
 */
function array_product(arr) {
  return arr.reduce(function(product, cur) {
    return (product * (parseFloat(cur) || 0)).toFixed(2);
  }, 1);
}

// Example usage:
const arr = [1,2,3,'3px','5px','55.23%','32.44'];

arr.product();      // Outputs: 161249.51
array_product(arr); // Outputs: 161249.51
```

### max & min

[![Shorts Views](https://img.shields.io/youtube/views/X3QqTG3W6E0?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/X3QqTG3W6E0)
[![Shorts Likes](https://img.shields.io/youtube/likes/X3QqTG3W6E0?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/X3QqTG3W6E0)
[![Shorts Comments](https://img.shields.io/youtube/comments/X3QqTG3W6E0?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/X3QqTG3W6E0)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/X3QqTG3W6E0)

```js
/**
 * min — Array to look through or first value to compare Find lowest value
 * @param {array} arr
 * @returns lowest value
 */
function min(arr) {
  return Math.min.apply(null, arr);
}

/**
 * max — Array to look through or first value to compare Find heighest value
 * @param {array} arr
 * @returns heighest value
 */
function max(arr) {
  return Math.max.apply(null, arr);
}

// Example usage:
const arr = [100,343,232,433,54544,33,3343,23];
min(arr); // Outputs: 23
max(arr); // Outputs: 54544
```

### randomEmoji

[![Shorts Views](https://img.shields.io/youtube/views/1UZ9Io92YDA?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/1UZ9Io92YDA)
[![Shorts Likes](https://img.shields.io/youtube/likes/1UZ9Io92YDA?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/1UZ9Io92YDA)
[![Shorts Comments](https://img.shields.io/youtube/comments/1UZ9Io92YDA?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/1UZ9Io92YDA)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/1UZ9Io92YDA)

```js
/**
 * @function randomEmoji To Generates a random emoji
 * @returns Random Emoji (e.g., 😴, 😍, 😯)
 */
function randomEmoji() {
  let startCodePoint = 0x1F601,
    endCodePoint = 0x1F64F,
    emoji = [];

  for(; startCodePoint < endCodePoint; startCodePoint++) {
    emoji.push(String.fromCodePoint(startCodePoint));
  }

  return emoji[
    Math.floor(Math.random() * emoji.length)
  ];
}

// Example usage:
randomEmoji(); // Outputs: 😍
```

### randomEmail

[![Shorts Views](https://img.shields.io/youtube/views/XYLPpxCsHO8?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/XYLPpxCsHO8)
[![Shorts Likes](https://img.shields.io/youtube/likes/XYLPpxCsHO8?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/XYLPpxCsHO8)
[![Shorts Comments](https://img.shields.io/youtube/comments/XYLPpxCsHO8?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/XYLPpxCsHO8)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/XYLPpxCsHO8)

```js
/**
 * randomEmail — Generates a random fake email
 * @param {string} domain [optional]
 * @returns random fake email address
 */
function randomEmail(domain) {
  let suffix = Math.floor(Math.random() * Math.pow(4, 6)),
    alpha = 'abcdefghijklmnopqrstuvwxyz',
    username = '',
    i = 0;

  domain = suffix + '@' + (domain || 'gmail.com');

  for(; i < 12; i++) {
    username += alpha[Math.floor(Math.random() * alpha.length)];
  }

  return username + domain;
}

// Example usage:
randomEmail();           // Outputs: 'psskyxrmtyve762@gmail.com'
randomEmail('user.com'); // Outputs: 'psskyxrmtyve762@user.com'
```

### dateFormat

[![Shorts Views](https://img.shields.io/youtube/views/hBXIMoK1Fmo?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/hBXIMoK1Fmo)
[![Shorts Likes](https://img.shields.io/youtube/likes/hBXIMoK1Fmo?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/hBXIMoK1Fmo)
[![Shorts Comments](https://img.shields.io/youtube/comments/hBXIMoK1Fmo?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/hBXIMoK1Fmo)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/hBXIMoK1Fmo)

```js
/**
 * dateFormat — Create a Local date/time formatter
 * @param {string} format
 * @return Formatted Local date/time
 */
function dateFormat(format) {
  var rformat = /(?<!\\)[dLmntyYhHgGisaA]|\\([a-z])/g,

    date = new Date(),
    n = date.getMonth() + 1,
    Y = date.getFullYear(),
    i = date.getMinutes(),
    G = date.getHours(),
    s = date.getSeconds(),

    formats = {G, n, Y,
      t: new Date(Y, n, 0).getDate(),
      s: s <= 9 ? s + '0' : s,
      L: date.getDate(),
      g: G % 12 || 12,
      i: i <= 9 ? i + '0' : i,
      a: G >= 12 ? 'pm' : 'am'
    };

  Object.assign(formats, {
    H: (formats.G <= 9 ? '0' : '') + formats.G,
    h: (formats.g <= 9 ? '0' : '') + formats.g,
    m: (formats.n <= 9 ? '0' : '') + formats.n,
    d: (formats.L <= 9 ? '0' : '') + formats.L,
    y: formats.Y % 100,
    A: formats.a.toUpperCase()
  });

  return format.replace(rformat, function(f, c) {
    return c || formats[f];
  });
}

// Example usage:
dateFormat('d-m-y h:i:s a'); // Outputs: 09-12-24 11:45:48 pm
dateFormat('d-m-Y h:i:s A'); // Outputs: 09-12-2024 11:45:48 PM
dateFormat('L n Y H:i:s A'); // Outputs: 9 12 2024 23:45:48 PM
dateFormat('d/m/Y');         // Outputs: 09/12/2024
dateFormat('H:i:s A');       // Outputs: 23:45:48 PM
dateFormat('h');             // Outputs: 11 hours
dateFormat('i');             // Outputs: 45 minutes
dateFormat('s');             // Outputs: 48 seconds
dateFormat('a');             // Outputs: pm
dateFormat('d/m/Y h:i:s');   // Outputs: 09/12/2024 11:45:48
```

### generateIP

[![Shorts Views](https://img.shields.io/youtube/views/aLW3bmSRAKs?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/aLW3bmSRAKs)
[![Shorts Likes](https://img.shields.io/youtube/likes/aLW3bmSRAKs?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/aLW3bmSRAKs)
[![Shorts Comments](https://img.shields.io/youtube/comments/aLW3bmSRAKs?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/aLW3bmSRAKs)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/aLW3bmSRAKs)

```js
/**
 * generateIP — Generate random fake IP address
 * @returns Random fake IP address
 */
function generateIP() {
  var i = 0, ip = '';

  for(; i < 4; i++) {
    ip += Math.floor(Math.random() * 256);
    if (i < 3) ip += '.';
  }
  return ip;
}

// Example usage:
generateIP(); // Outputs: '131.167.104.164'
```

### getFlag

[![Shorts Views](https://img.shields.io/youtube/views/YGGHUDv3pvw?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/YGGHUDv3pvw)
[![Shorts Likes](https://img.shields.io/youtube/likes/YGGHUDv3pvw?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/YGGHUDv3pvw)
[![Shorts Comments](https://img.shields.io/youtube/comments/YGGHUDv3pvw?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/YGGHUDv3pvw)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/YGGHUDv3pvw)

```js
/**
 * getFlag — To create a country flag generator using regional indicator symbols
 * @param {string} code
 * @return country flag
 */
function getFlag(code) {
  return code.replace(/[a-z]/gi, function(char) {
    return String.fromCodePoint(char.toUpperCase().charCodeAt() - 65 + 127462);
  });
}

// Example usage:
getFlag('IN'); // Outputs: 🇮🇳
getFlag('us'); // Outputs: 🇺🇸
getFlag('Ru'); // Outputs: 🇷🇺
getFlag('nK'); // Outputs: 🇳🇰
```

### str2bin & bin2str

[![Shorts Views](https://img.shields.io/youtube/views/9yoKPiN0LTU?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/9yoKPiN0LTU)
[![Shorts Likes](https://img.shields.io/youtube/likes/9yoKPiN0LTU?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/9yoKPiN0LTU)
[![Shorts Comments](https://img.shields.io/youtube/comments/9yoKPiN0LTU?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/9yoKPiN0LTU)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/9yoKPiN0LTU)

```js
/**
 * str2bin — Convert String to Binary
 * @param {string} str
 * @returns Binary code
 */
function str2bin(str) {
  return str.replace(/./gs, rcFunc(true)).trim();
}

/**
 * bin2str — Convert Binary to String
 * @param {string} bin
 * @returns Readable text
 */
function bin2str(bin) {
  return bin.replace(/[01]+[\x20]?/g, rcFunc(false));
}

/**
 * rcFunc — Replace Callback Function
 * @param {boolean} encoding
 * @return Binary or Readable text
 */
function rcFunc(encoding) {
  return function(m) {
    return encoding ? m.charCodeAt().toString(2).padStart(8, '0') + ' ' : String.fromCharCode(parseInt(m, 2));
  };
}

// Example usage:
str2bin('Welcome to my YT Channel');
// Outputs: 01010111 01100101 01101100 01100011 01101111 01101101 01100101 00100000 01110100 01101111 00100000 01101101 01111001 00100000 01011001 01010100 00100000 01000011 01101000 01100001 01101110 01101110 01100101 01101100

bin2str('01010111 01100101 01101100 01100011 01101111 01101101 01100101 00100000 01110100 01101111 00100000 01101101 01111001 00100000 01011001 01010100 00100000 01000011 01101000 01100001 01101110 01101110 01100101 01101100');
// Outputs: 'Welcome to my YT Channel'
```

### decbin & bindec

[![Shorts Views](https://img.shields.io/youtube/views/20v-hCx7fok?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/20v-hCx7fok)
[![Shorts Likes](https://img.shields.io/youtube/likes/20v-hCx7fok?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/20v-hCx7fok)
[![Shorts Comments](https://img.shields.io/youtube/comments/20v-hCx7fok?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/20v-hCx7fok)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/20v-hCx7fok)

```js
/**
 * decbin — Convert Decimal to Binary
 * @param {number} num
 * @returns Binary format 0101011
 */
function decbin(num) {
  return num.toString(2);
}

/**
 * bindec — Convert Binary to Decimal
 * @param {string} bin
 * @returns decimal number
 */
function bindec(bin) {
  return parseInt(bin, 2);
}

// Example usage:
decbin(348374347384);                              // Outputs: '101000100011100101110101010111001111000'
bindec('101000100011100101110101010111001111000'); // Outputs: 348374347384
```

### dechex & hexdec

[![Shorts Views](https://img.shields.io/youtube/views/YBjTnFVOXEE?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/YBjTnFVOXEE)
[![Shorts Likes](https://img.shields.io/youtube/likes/YBjTnFVOXEE?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/YBjTnFVOXEE)
[![Shorts Comments](https://img.shields.io/youtube/comments/YBjTnFVOXEE?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/YBjTnFVOXEE)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/YBjTnFVOXEE)

```js
/**
 * dechex — Decimal to Hex Convertation
 * @param {number} num
 * @returns
 */
function dechex(num) {
  return num.toString(16);
}

/**
 * hexdec — Hex to Decimal Convertation
 * @param {string} hex
 * @returns
 */
function hexdec(hex) {
  return parseInt(hex, 16);
}

// Example usage:
dechex(16777215); // Outputs: 'ffffff'
hexdec('ffffff'); // Outputs: 16777215
```

### formatMemunit

[![Shorts Views](https://img.shields.io/youtube/views/TeawybFGvzk?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/TeawybFGvzk)
[![Shorts Likes](https://img.shields.io/youtube/likes/TeawybFGvzk?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/TeawybFGvzk)
[![Shorts Comments](https://img.shields.io/youtube/comments/TeawybFGvzk?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/TeawybFGvzk)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/TeawybFGvzk)

```js
/**
 * formatMemunit — Create a memory unit formatter
 * @param {number} bytes
 * @return formatted memory unit
 */
function formatMemunit(bytes) {
  var factor, units = ['B', 'KB', 'MB', 'GB', 'TB', 'PB', 'EB', 'ZB', 'YB'];

  factor = Math.floor(Math.log(bytes) / Math.log(1024));

  return (Math.round(bytes / Math.pow(1024, factor) * 100) / 100) + ' ' + units[factor];
}

// Example usage:
formatMemunit(583462344);        // Outputs: 556.43 MB
formatMemunit(43223);            // Outputs: 42.21 KB
formatMemunit(432);              // Outputs: 432 B
formatMemunit(8274264242473);    // Outputs: 7.53 TB
formatMemunit(13462490534);      // Outputs: 12.54 GB
formatMemunit(3346249053473485); // Outputs: 2.97 PB
```

### dec2Oct & oct2Dec

[![Shorts Views](https://img.shields.io/youtube/views/q5I141s3CiA?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/q5I141s3CiA)
[![Shorts Likes](https://img.shields.io/youtube/likes/q5I141s3CiA?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/q5I141s3CiA)
[![Shorts Comments](https://img.shields.io/youtube/comments/q5I141s3CiA?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/q5I141s3CiA)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/q5I141s3CiA)

```js
/**
 * dec2oct — Convert Decimal to Octal
 * @param {number} value
 * @returns A octal number
 */
function dec2oct(value) {
  return parseInt(value.toString(8));
}

/**
 * oct2dec — Convert Octal to Decimal
 * @param {number} value
 * @returns A decimal number
 */
function oct2dec(value) {
  return parseInt(value, 8);
}

// Example usage:
dec2oct(299); // Outputs: 453
oct2dec(453); // Outputs: 299
```

### generatedOTP

[![Shorts Views](https://img.shields.io/youtube/views/SYq9KRBvBmw?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/SYq9KRBvBmw)
[![Shorts Likes](https://img.shields.io/youtube/likes/SYq9KRBvBmw?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/SYq9KRBvBmw)
[![Shorts Comments](https://img.shields.io/youtube/comments/SYq9KRBvBmw?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/SYq9KRBvBmw)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/SYq9KRBvBmw)

```js
/**
 * generateOTP — Generate Random Numeric OTP
 * @param {number} length
 * @returns A random generated OTP
 */
function generateOTP(length) {
  return String(Math.floor(Math.random() * Math.pow(10, length))).padStart(length, '0');
}

// Generate OTP of 6-digits
generateOTP(6); // Outputs: 991229
```
