# Source Code of YouTube Shorts

[![Authors](https://img.shields.io/badge/Author-Shahzada%20Modassir-%2344cc11?style=flat-square&color=%23007ec6)](https://github.com/shahzadamodassir)
[![License](https://img.shields.io/github/license/shahzadamodassir/shorts?style=flat-square&color=%23007ec6)](https://github.com/shahzadamodassir/shorts/blob/main/LICENSE)
[![YouTube Views](https://img.shields.io/youtube/channel/views/UCzo3rbUc4Yr1C-Zv9B9nfKw?style=flat-square&logo=youtube)](https://youtube.com/@shahzadamodassir)
[![YouTube Subscribers](https://img.shields.io/youtube/channel/subscribers/UCzo3rbUc4Yr1C-Zv9B9nfKw?style=flat-square&logo=youtube)](https://youtube.com/@shahzadamodassir)
[![Github Followers](https://img.shields.io/github/followers/shahzadamodassir?style=flat-square&logo=github)](https://github.com/shahzadamodassir?tab=followers)
[![Javascript](https://img.shields.io/badge/JAVASCRIPT-%23F7DF1E?style=flat-square&logo=JAVASCRIPT&labelColor=%23333)](https://)
[![X](https://img.shields.io/twitter/follow/Xsmodassir?style=flat-square&logo=x&color=%2300000000)](https://x.com/Xsmodassir)


## Javascript Shorts Source
Watch all Javascript shorts video on youtube see playlist [Javascript Shorts](https://youtube.com/playlist?list=PLnnLdunPzY2s16kDzbhDfX9tAsGFRHpGJ&si=EES3tAT0i0DybXik)

### array_combine

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

```js
/**
 * Convert Decimal to Octal
 * @param {number} value
 * @returns A octal number
 */
function dec2Oct(value) {
  return parseInt(value.toString(8));
}

/**
 * Convert Octal to Decimal
 * @param {number} value
 * @returns A decimal number
 */
function oct2Dec(value) {
  return parseInt(value, 8);
}

// Example usage:
dec2Oct(299); // Outputs: 453
oct2Dec(453); // Outputs: 299
```

```js
/**
 * Create a memory unit formatter
 * @param {number} bytes
 * @return formatted memory unit
 */
function formatMemunit(bytes) {
  var factor, units = ['B', 'KB', 'MB', 'GB', 'TB', 'PB', 'EB', 'ZB', 'YB'];

  factor = Math.floor(Math.log(bytes) / Math.log(1024));

  return (Math.round(bytes / Math.pow(1024, factor) * 100) / 100) + ' ' + units[factor];
}

// Example usage:
formatMemunit()
```

```js
/**
 * Decimal to Hex Convertation
 * @param {number} num
 * @returns
 */
function dechex(num) {
  return num.toString(16);
}

/**
 * Hex to Decimal Convertation
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

### generatedOTP

[![Shorts Views](https://img.shields.io/youtube/views/_F8gi5beA5o?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/_F8gi5beA5o)
[![Shorts Likes](https://img.shields.io/youtube/likes/_F8gi5beA5o?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/_F8gi5beA5o)
[![Shorts Comments](https://img.shields.io/youtube/comments/_F8gi5beA5o?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/_F8gi5beA5o)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/_F8gi5beA5o)

**Parameters:**
- `length` [&lt;string&gt;](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#String_type)
- Returns: [&lt;int&gt;](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#number_type)

```js
/**
 * Generate Random Numeric OTP
 * @param {number} length
 * @returns A random generated OTP
 */
function generateOTP(length) {
  return String(Math.floor(Math.random() * Math.pow(10, length))).padStart(length, '0');
}

// Generate OTP of 6-digits
generateOTP(6); // Outputs: 991229
```