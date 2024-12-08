# Source Code of YouTube Shorts

<a href="https://github.com/shahzadamodassir"><img src="https://img.shields.io/badge/Author-Shahzada%20Modassir-%2344cc11?style=flat-square"/></a>
<a href="LICENSE"><img src="https://img.shields.io/github/license/shahzadamodassir/shorts?style=flat-square"/></a>

<a href="https://github.com/shahzadamodassir/shorts/stargazers"><img src="https://img.shields.io/github/stars/shahzadamodassir/shorts?style=flat-square"/></a>
<a href="https://github.com/shahzadamodassir/shorts/graphs/contributors"><img src="https://img.shields.io/github/contributors/shahzadamodassir/shorts?style=flat-square" alt="Contributors"></a>

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
