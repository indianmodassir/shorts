# Source Code of YouTube Shorts

[![Authors](https://img.shields.io/badge/Author-Shahzada%20Modassir-%2344cc11?style=flat-square&color=%23007ec6)](https://github.com/shahzadamodassir)
[![License](https://img.shields.io/github/license/shahzadamodassir/shorts?style=flat-square&color=%23007ec6)](https://github.com/shahzadamodassir/shorts/blob/main/LICENSE)
[![YouTube Views](https://img.shields.io/youtube/channel/views/UCzo3rbUc4Yr1C-Zv9B9nfKw?style=flat-square&logo=youtube)](https://youtube.com/@shahzadamodassir)
[![YouTube Subscribers](https://img.shields.io/youtube/channel/subscribers/UCzo3rbUc4Yr1C-Zv9B9nfKw?style=flat-square&logo=youtube)](https://youtube.com/@shahzadamodassir)
[![Github Followers](https://img.shields.io/github/followers/shahzadamodassir?style=flat-square&logo=github)](https://github.com/shahzadamodassir?tab=followers)
[![X](https://img.shields.io/twitter/follow/Xsmodassir?style=flat-square&logo=x&color=%2300000000)](https://x.com/Xsmodassir)

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
