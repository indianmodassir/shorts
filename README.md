# Source Code of YouTube Shorts

[![Authors](https://img.shields.io/badge/Author-Shahzada%20Modassir-%2344cc11?style=flat-square&color=%23007ec6)](https://github.com/shahzadamodassir)
[![License](https://img.shields.io/github/license/shahzadamodassir/shorts?style=flat-square&color=%23007ec6)](https://github.com/shahzadamodassir/shorts/blob/main/LICENSE)
[![YouTube Views](https://img.shields.io/youtube/channel/views/UCzo3rbUc4Yr1C-Zv9B9nfKw?style=flat-square&logo=youtube)](https://youtube.com/@shahzadamodassir)
[![YouTube Subscribers](https://img.shields.io/youtube/channel/subscribers/UCzo3rbUc4Yr1C-Zv9B9nfKw?style=flat-square&logo=youtube)](https://youtube.com/@shahzadamodassir)
[![Github Followers](https://img.shields.io/github/followers/shahzadamodassir?style=flat-square&logo=github)](https://github.com/shahzadamodassir?tab=followers)
[![X](https://img.shields.io/twitter/follow/Xsmodassir?style=flat-square&logo=x&color=%2300000000)](https://x.com/Xsmodassir)

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
