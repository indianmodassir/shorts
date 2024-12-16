# Source Code of YouTube Shorts

[![Authors](https://img.shields.io/badge/Author-Shahzada%20Modassir-%2344cc11?style=flat-square&color=%23007ec6)](https://github.com/shahzadamodassir)
[![License](https://img.shields.io/github/license/shahzadamodassir/shorts?style=flat-square&color=%23007ec6)](https://github.com/shahzadamodassir/shorts/blob/main/LICENSE)
[![YouTube Views](https://img.shields.io/youtube/channel/views/UCzo3rbUc4Yr1C-Zv9B9nfKw?style=flat-square&logo=youtube)](https://youtube.com/@shahzadamodassir)
[![YouTube Subscribers](https://img.shields.io/youtube/channel/subscribers/UCzo3rbUc4Yr1C-Zv9B9nfKw?style=flat-square&logo=youtube)](https://youtube.com/@shahzadamodassir)
[![Github Followers](https://img.shields.io/github/followers/shahzadamodassir?style=flat-square&logo=github)](https://github.com/shahzadamodassir?tab=followers)
[![X](https://img.shields.io/twitter/follow/Xsmodassir?style=flat-square&logo=x&color=%2300000000)](https://x.com/Xsmodassir)

## Used Coding Languages in YT Shorts

- [Javascript](#javascript-shorts-source)

## Javascript YT Shorts Source Code

Watch all Javascript shorts video on youtube see playlist [Javascript Shorts](https://youtube.com/playlist?list=PLnnLdunPzY2s16kDzbhDfX9tAsGFRHpGJ&si=EES3tAT0i0DybXik)

### base64Encode and base64Decode

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

### objChangeKeyCase

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

[![Shorts Views](https://img.shields.io/youtube/views/tDIaHnmRUVk?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/tDIaHnmRUVk)
[![Shorts Likes](https://img.shields.io/youtube/likes/tDIaHnmRUVk?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/tDIaHnmRUVk)
[![Shorts Comments](https://img.shields.io/youtube/comments/tDIaHnmRUVk?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/tDIaHnmRUVk)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/tDIaHnmRUVk)

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
odd([1,2,3,4,5,6,7,8,9]);  // Outputs: [1,3,5,7,9]
even([1,2,3,4,5,6,7,8,9]); // Outputs: [2,4,6,8]
```

### array_combine

[![Shorts Views](https://img.shields.io/youtube/views/bAblJ4y5hJ0?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/bAblJ4y5hJ0)
[![Shorts Likes](https://img.shields.io/youtube/likes/bAblJ4y5hJ0?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/bAblJ4y5hJ0)
[![Shorts Comments](https://img.shields.io/youtube/comments/bAblJ4y5hJ0?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/bAblJ4y5hJ0)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/bAblJ4y5hJ0)

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

[![Shorts Views](https://img.shields.io/youtube/views/x_2Xrx0mRAE?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/x_2Xrx0mRAE)
[![Shorts Likes](https://img.shields.io/youtube/likes/x_2Xrx0mRAE?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/x_2Xrx0mRAE)
[![Shorts Comments](https://img.shields.io/youtube/comments/x_2Xrx0mRAE?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/x_2Xrx0mRAE)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/x_2Xrx0mRAE)

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

[![Shorts Views](https://img.shields.io/youtube/views/Zxu9qnMsD1U?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/Zxu9qnMsD1U)
[![Shorts Likes](https://img.shields.io/youtube/likes/Zxu9qnMsD1U?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/Zxu9qnMsD1U)
[![Shorts Comments](https://img.shields.io/youtube/comments/Zxu9qnMsD1U?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/Zxu9qnMsD1U)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/Zxu9qnMsD1U)

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

[![Shorts Views](https://img.shields.io/youtube/views/HSArJzJtVgc?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/HSArJzJtVgc)
[![Shorts Likes](https://img.shields.io/youtube/likes/HSArJzJtVgc?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/HSArJzJtVgc)
[![Shorts Comments](https://img.shields.io/youtube/comments/HSArJzJtVgc?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/HSArJzJtVgc)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/HSArJzJtVgc)

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

[![Shorts Views](https://img.shields.io/youtube/views/RjDFracRCmQ?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/RjDFracRCmQ)
[![Shorts Likes](https://img.shields.io/youtube/likes/RjDFracRCmQ?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/RjDFracRCmQ)
[![Shorts Comments](https://img.shields.io/youtube/comments/RjDFracRCmQ?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/RjDFracRCmQ)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/RjDFracRCmQ)

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

### min

[![Shorts Views](https://img.shields.io/youtube/views/7qU-UC0WGkk?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/7qU-UC0WGkk)
[![Shorts Likes](https://img.shields.io/youtube/likes/7qU-UC0WGkk?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/7qU-UC0WGkk)
[![Shorts Comments](https://img.shields.io/youtube/comments/7qU-UC0WGkk?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/7qU-UC0WGkk)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/7qU-UC0WGkk)

```js
/**
 * min — Array to look through or first value to compare Find lowest value
 * @param {array} arr
 * @returns lowest value
 */
function min(arr) {
  return Math.min.apply(null, arr);
}

// Example usage:
const arr = [100,343,232,433,54544,33,3343,23];
min(arr); // Outputs: 23
```

### max

[![Shorts Views](https://img.shields.io/youtube/views/kfmyvgnnlZs?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/kfmyvgnnlZs)
[![Shorts Likes](https://img.shields.io/youtube/likes/kfmyvgnnlZs?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/kfmyvgnnlZs)
[![Shorts Comments](https://img.shields.io/youtube/comments/kfmyvgnnlZs?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/kfmyvgnnlZs)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/kfmyvgnnlZs)

```js
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
max(arr); // Outputs: 54544
```

### randomEmail

[![Shorts Views](https://img.shields.io/youtube/views/vHgV_T1q0hE?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/vHgV_T1q0hE)
[![Shorts Likes](https://img.shields.io/youtube/likes/vHgV_T1q0hE?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/vHgV_T1q0hE)
[![Shorts Comments](https://img.shields.io/youtube/comments/vHgV_T1q0hE?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/vHgV_T1q0hE)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/vHgV_T1q0hE)

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

[![Shorts Views](https://img.shields.io/youtube/views/kzw4tcyawsw?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/kzw4tcyawsw)
[![Shorts Likes](https://img.shields.io/youtube/likes/kzw4tcyawsw?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/kzw4tcyawsw)
[![Shorts Comments](https://img.shields.io/youtube/comments/kzw4tcyawsw?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/kzw4tcyawsw)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/kzw4tcyawsw)

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

[![Shorts Views](https://img.shields.io/youtube/views/rIjJNEvGFuY?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/rIjJNEvGFuY)
[![Shorts Likes](https://img.shields.io/youtube/likes/rIjJNEvGFuY?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/rIjJNEvGFuY)
[![Shorts Comments](https://img.shields.io/youtube/comments/rIjJNEvGFuY?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/rIjJNEvGFuY)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/rIjJNEvGFuY)

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

[![Shorts Views](https://img.shields.io/youtube/views/ITzY9kYAU14?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/ITzY9kYAU14)
[![Shorts Likes](https://img.shields.io/youtube/likes/ITzY9kYAU14?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/ITzY9kYAU14)
[![Shorts Comments](https://img.shields.io/youtube/comments/ITzY9kYAU14?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/ITzY9kYAU14)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/ITzY9kYAU14)

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

[![Shorts Views](https://img.shields.io/youtube/views/W8ywsnTuHhM?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/W8ywsnTuHhM)
[![Shorts Likes](https://img.shields.io/youtube/likes/W8ywsnTuHhM?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/W8ywsnTuHhM)
[![Shorts Comments](https://img.shields.io/youtube/comments/W8ywsnTuHhM?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/W8ywsnTuHhM)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/W8ywsnTuHhM)

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

[![Shorts Views](https://img.shields.io/youtube/views/2UM3izWLY1g?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/2UM3izWLY1g)
[![Shorts Likes](https://img.shields.io/youtube/likes/2UM3izWLY1g?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/2UM3izWLY1g)
[![Shorts Comments](https://img.shields.io/youtube/comments/2UM3izWLY1g?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/2UM3izWLY1g)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/2UM3izWLY1g)

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

[![Shorts Views](https://img.shields.io/youtube/views/OhcF8UKjOqg?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/OhcF8UKjOqg)
[![Shorts Likes](https://img.shields.io/youtube/likes/OhcF8UKjOqg?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/OhcF8UKjOqg)
[![Shorts Comments](https://img.shields.io/youtube/comments/OhcF8UKjOqg?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/OhcF8UKjOqg)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/OhcF8UKjOqg)

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

[![Shorts Views](https://img.shields.io/youtube/views/vwZbs_sPTMI?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/vwZbs_sPTMI)
[![Shorts Likes](https://img.shields.io/youtube/likes/vwZbs_sPTMI?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/vwZbs_sPTMI)
[![Shorts Comments](https://img.shields.io/youtube/comments/vwZbs_sPTMI?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/vwZbs_sPTMI)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/vwZbs_sPTMI)

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
formatMemunit()
```

### dec2Oct & oct2Dec

[![Shorts Views](https://img.shields.io/youtube/views/Zdi064NgvjM?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/Zdi064NgvjM)
[![Shorts Likes](https://img.shields.io/youtube/likes/Zdi064NgvjM?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/Zdi064NgvjM)
[![Shorts Comments](https://img.shields.io/youtube/comments/Zdi064NgvjM?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/Zdi064NgvjM)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/Zdi064NgvjM)

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

[![Shorts Views](https://img.shields.io/youtube/views/_F8gi5beA5o?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/_F8gi5beA5o)
[![Shorts Likes](https://img.shields.io/youtube/likes/_F8gi5beA5o?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/_F8gi5beA5o)
[![Shorts Comments](https://img.shields.io/youtube/comments/_F8gi5beA5o?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/_F8gi5beA5o)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/_F8gi5beA5o)

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
