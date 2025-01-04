# Source Code of YouTube Shorts

[![Authors](https://img.shields.io/badge/Author-Shahzada%20Modassir-%2344cc11?style=flat-square&color=%23007ec6)](https://github.com/indianmodassir)
[![License](https://img.shields.io/github/license/indianmodassir/shorts?style=flat-square&color=%23007ec6)](https://github.com/indianmodassir/shorts/blob/main/LICENSE)
[![YouTube Views](https://img.shields.io/youtube/channel/views/UCzo3rbUc4Yr1C-Zv9B9nfKw?style=flat-square&logo=youtube)](https://youtube.com/@indianmodassir)
[![YouTube Subscribers](https://img.shields.io/youtube/channel/subscribers/UCzo3rbUc4Yr1C-Zv9B9nfKw?style=flat-square&logo=youtube)](https://youtube.com/@indianmodassir)
[![Github Followers](https://img.shields.io/github/followers/indianmodassir?style=flat-square&logo=github)](https://github.com/indianmodassir?tab=followers)
[![X](https://img.shields.io/twitter/follow/Xsmodassir?style=flat-square&logo=x&color=%2300000000)](https://x.com/Xsmodassir)

## Used Coding Languages in YT Shorts

- [Javascript](#javascript-yt-shorts-source-code)

## Web Shorts HTML, CSS or JavaScript

Watch all Web shorts video on youtube see playlist [JavaScript Shorts](https://www.youtube.com/playlist?list=PLnnLdunPzY2t2iQ7X8BAUh4s8Yx-2KR7z)

### Draggable List

[![Shorts Views](https://img.shields.io/youtube/views/ZxOHPXOZ4q8?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/ZxOHPXOZ4q8)
[![Shorts Likes](https://img.shields.io/youtube/likes/ZxOHPXOZ4q8?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/ZxOHPXOZ4q8)
[![Shorts Comments](https://img.shields.io/youtube/comments/ZxOHPXOZ4q8?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/ZxOHPXOZ4q8)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/ZxOHPXOZ4q8)

[Download](https://)

### Bounce Loader

[![Shorts Views](https://img.shields.io/youtube/views/0nlHZn1Q4Gk?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/0nlHZn1Q4Gk)
[![Shorts Likes](https://img.shields.io/youtube/likes/0nlHZn1Q4Gk?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/0nlHZn1Q4Gk)
[![Shorts Comments](https://img.shields.io/youtube/comments/0nlHZn1Q4Gk?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/0nlHZn1Q4Gk)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/0nlHZn1Q4Gk)

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    * {
      padding: 0;
      margin: 0;
      box-sizing: border-box;
    }

    body {
      width: 100vw;
      height: 100vh;
    }

    body {
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .bounce-loader {
      display: flex;
      width: 24px;
      height: 40px;
      justify-content: space-between;
    }

    .bounce-loader span {
      border-radius: 10px;
      width: 6px;
      height: 100%;
      background-color: #a6a6a6;
      animation: loading 0.6s var(--i) ease-in-out infinite;
    }

    @keyframes loading {
      0%, 100% {
        transform: scaleY(0.2);
        opacity: 0.8;
      }

      50% {
        transform: scaleY(1);
        opacity: 1;
      }
    }
  </style>
</head>
<body>

  <div class="bounce-loader">
    <span style="--i: 0s"></span>
    <span style="--i: 0.15s"></span>
    <span style="--i: 0.3s"></span>
  </div>
  
</body>
</html>
```

## Javascript YT Shorts Source Code

Watch all JavaScript shorts video on youtube see playlist [JavaScript Shorts](https://www.youtube.com/playlist?list=PLnnLdunPzY2srl1Iy4xHkKWaGQ-CUepNk)

### memoize

[![Shorts Views](https://img.shields.io/youtube/views/N_qQc43ZKds?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/N_qQc43ZKds)
[![Shorts Likes](https://img.shields.io/youtube/likes/N_qQc43ZKds?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/N_qQc43ZKds)
[![Shorts Comments](https://img.shields.io/youtube/comments/N_qQc43ZKds?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/N_qQc43ZKds)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/N_qQc43ZKds)

```js
/**
 * Speed up your code with memoization!
 * 🚀 Caching results for faster performance!
 * @param {function} fn
 * @param {function} func
 * @returns A callback Function
 */
function memoize(fn, func) {
  let result, key, cache = new Map();

  return function() {
    key = JSON.stringify(arguments);

    // If key in cache, then return the cached result
    return cache.has(key) ? (
      result = cache.get(key),
      func(result),
      result

    // Otherwise
    ) : (
      result = fn(...arguments),
      cache.set(key, result),
      result
    );
  };
}

// Example usage:

// For example, This is your big Handler
let bigHandler = (end) => {
  for(let i = 0; i < end; i++) {}
  console.log("\nFrom Handler: " + end);
  return end;
};

let memoizedAdd = memoize(bigHandler,
  // Optional argument
  // This func will be invoked when data is loaded from the cache
  function(res) {
    console.log("\nFrom Cache: " + res);
  });

// Testing with Outputs:
console.time();
memoizedAdd(100000000);
console.timeEnd();

console.time();
memoizedAdd(100000000);
console.timeEnd();

console.time();
memoizedAdd(500000000);
console.timeEnd();

console.time();
memoizedAdd(500000000);
console.timeEnd();
```

### cloneDeep

[![Shorts Views](https://img.shields.io/youtube/views/iybtOI8yJgk?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/iybtOI8yJgk)
[![Shorts Likes](https://img.shields.io/youtube/likes/iybtOI8yJgk?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/iybtOI8yJgk)
[![Shorts Comments](https://img.shields.io/youtube/comments/iybtOI8yJgk?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/iybtOI8yJgk)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/iybtOI8yJgk)

```js
/**
 * Function to perform deep cloning of an object or array
 * @param {object|array} obj
 * @returns The cloned array or object
 */
function cloneDeep(obj) {
  if (obj === null || typeof obj !== 'object') {
    return obj;
  }

  let clone = Array.isArray(obj) ? [] : {},
    key;

  for(key in obj) {
    if (obj.hasOwnProperty(key)) {
      clone[key] = cloneDeep(obj[key]);
    }
  }

  return clone;
}

// Example usage:
const orig = {
  name: 'modassir',
  details: {age: 22, addr: 'RFJ'},
  hobbies: ['coding', 'reading']
};

const copied = cloneDeep(orig);
copied.details.age = 23;
copied.hobbies[1] = 'travelling';

// Outputs:
console.log('Original:', orig);
console.log('Copied:', copied);
```

### debounce

[![Shorts Views](https://img.shields.io/youtube/views/VItEOPa7b58?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/VItEOPa7b58)
[![Shorts Likes](https://img.shields.io/youtube/likes/VItEOPa7b58?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/VItEOPa7b58)
[![Shorts Comments](https://img.shields.io/youtube/comments/VItEOPa7b58?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/VItEOPa7b58)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/VItEOPa7b58)

```js
/**
 * debounce function to limit the rate at which a function is invoked
 * @param {function} fn
 * @param {number} delay
 */
function debounce(fn, delay) {
  let id;
  return function() {
    // Clear previous timeout,
    // to reset the delay
    clearTimeout(id);

    // Set a new timeout
    id = setTimeout(fn, delay || 1000, ...arguments);
  };
}

// Example usage:

const searchHandler = (search) => {
  console.log('Fetching database with query:' + search);
};

// swd -> search with debounce
let swd = debounce(searchHandler);

// Call without debounce
swd('ja');
swd('java');
swd('javasc');
swd('javascri');
swd('javascript');
```

### Serialize

[![Shorts Views](https://img.shields.io/youtube/views/HOVlf_olxTc?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/HOVlf_olxTc)
[![Shorts Likes](https://img.shields.io/youtube/likes/HOVlf_olxTc?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/HOVlf_olxTc)
[![Shorts Comments](https://img.shields.io/youtube/comments/HOVlf_olxTc?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/HOVlf_olxTc)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/HOVlf_olxTc)

```js
/**
 * Serialize an array of form elements or a set of
 * key/values into a query string
 */
function serialize(data, trad) {
  let prefix, s = [],
    add = function(key, val) {
      s[s.length] = encodeURIComponent(key) + '=' +
        encodeURIComponent(val == null ? '' : val);
    };

  if (data == null) return '';

  // [['key','value']] or [{name: '', value: ''}]
  if (Array.isArray(data)) {
    for(prefix of data) {
      add(
        prefix[0] || prefix.name,
        prefix[1] || prefix.value
      );
    }
  } else {
    // Encode params recursively.
    // {name: {...}, key: [...]} or {key: value}
    for(prefix in data) {
      makeParams(prefix, data[prefix], trad, add);
    }
  }

  return s.join('&');
}

function makeParams(prefix, mixed, trad, add) {
  let name, rbracket = /\[\]$/;

  if (Array.isArray(mixed)) {
    // Serialize array item.
    mixed.forEach(function(v, i) {
      trad || rbracket.test(prefix) ? add(prefix, v) :
        makeParams(
          prefix + '[' + (typeof v == 'object' && v != null ? i : '') + ']',
          v,
          trad,
          add
        );
    });
  } else if (!trad && typeof mixed === 'object') {
    // Serialize object item.
    for(name in mixed) {
      makeParams(prefix + '[' + name + ']', mixed[name], trad, add);
    }
  } else {
    // Serialize scalar item.
    add(prefix, mixed);
  }
}

// Example usage:
let data = {id: 3, email: 'example@gmai.com', pass: 12354};
let arr = [['name', 'modassir'], {name: 'age', value: 22}];
let obj = {id: 1, param: {one:1, two: 2}, index: [1,2,3,4,5]};

// Outputs:
serialize(data);      // Outputs: id=3&email=example%40gmai.com&pass=12354
serialize(arr);       // Outputs: name=modassir&age=22
serialize(obj);       // Outputs: id=1&param%5Bone%5D=1&param%5Btwo%5D=2&index%5B%5D=1&index%5B%5D=2&index%5B%5D=3&index%5B%5D=4&index%5B%5D=5
serialize(obj, true); // Outputs: id=1&param=%5Bobject%20Object%5D&index=1&index=2&index=3&index=4&index=5
```

### ArrayUnique

[![Shorts Views](https://img.shields.io/youtube/views/JQG5HDsVM_g?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/JQG5HDsVM_g)
[![Shorts Likes](https://img.shields.io/youtube/likes/JQG5HDsVM_g?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/JQG5HDsVM_g)
[![Shorts Comments](https://img.shields.io/youtube/comments/JQG5HDsVM_g?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/JQG5HDsVM_g)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/JQG5HDsVM_g)

```js
/**
 * Function to remove duplicate elements from an array.
 * @param {array} arr 
 * @param {boolean} isRef 
 * @returns Unique Array
 */
function ArrayUnique(arr, isRef) {
  // Create a new array of unique elements
  let unique = [...new Set(arr)];

  // If isRef, Modify the original array by reference
  if (isRef) {
    // First we will empty the original array
    arr.length = 0;

    // Now we will push the unique array into the original array
    [].push.apply(arr, unique);
  }

  return unique;
}

// Example usage with outputs
let arr = [1,2,3,4,1,2,3,4,1,2,3,4];
ArrayUnique(arr);       // Outputs: [1,2,3] Return a new array without modified in original array
ArrayUnique(arr, true); // Outputs: [1,2,3] Return a new array with modified original array by reference
```

### upm (User Password Manager) Library

[![Shorts Views](https://img.shields.io/youtube/views/D06gC1fyjgY?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/D06gC1fyjgY)
[![Shorts Likes](https://img.shields.io/youtube/likes/D06gC1fyjgY?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/D06gC1fyjgY)
[![Shorts Comments](https://img.shields.io/youtube/comments/D06gC1fyjgY?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/D06gC1fyjgY)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/D06gC1fyjgY)

Create a `storage.json` file on current working directory
```json
{}
```

Then create `upm.js` Javascript Library File on current working directory
```js
const upm = {}; // user password manager
const path = 'storage.json';
const fs = require('fs');

/**
 * Gets password, If user exists in storage
 * @param {string} username 
 * @returns 
 */
upm.get = function(username) {
  return (this.getAll()[username] || {}).password;
}

/**
 * Returns all saved storage data
 * @returns All storage data
 */
upm.getAll = function() {
  return JSON.parse(fs.readFileSync(path, {encoding: 'utf8'}));
}

/**
 * Save new password, If user does not exists
 * @param {string} username 
 * @param {string} password 
 * @returns true or undefined
 */
upm.save = function(username, password) {
  let date = (new Date).toLocaleString(),
    storage = this.getAll();

  if (!this.get(username)) {
    if (password) storage[username] = {password, date};
    fs.writeFileSync(path, JSON.stringify(storage, null, 2));
    return true;
  }
}

// Example usage:

// Save Password in Storage
upm.save('GmailPass', '123@gmail');
upm.save('FBPass', '123@facebook');
upm.save('InstaPass', '123@insta');

// View all saved data
upm.getAll();

// Get Passwword of Specific User
upm.get('GmailPass');
upm.get('InstaPass');
```

### encrypt and decrypt

[![Shorts Views](https://img.shields.io/youtube/views/8j_JdzFA5A4?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/8j_JdzFA5A4)
[![Shorts Likes](https://img.shields.io/youtube/likes/8j_JdzFA5A4?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/8j_JdzFA5A4)
[![Shorts Comments](https://img.shields.io/youtube/comments/8j_JdzFA5A4?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/8j_JdzFA5A4)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/8j_JdzFA5A4)

```js
const crypto = require('crypto');

/**
 * Encrypts the given data using AES-256-GCM encryption algorithm
 * @param {string} data
 * @param {key} key
 * @returns {string} Encrypted plainText
 */
function encrypt(data, key) {
  let encrypted, cipher, tag,
    iv = crypto.randomBytes(16);

  key = crypto.createHash('sha256').update(key).digest();
  cipher = crypto.createCipheriv('AES-256-GCM', key, iv);

  encrypted = cipher.update(data, 'utf-8', 'base64');
  encrypted += cipher.final('base64');

  return btoa(JSON.stringify({
    data: encrypted,
    iv: iv.toString('base64'),
    tag: cipher.getAuthTag().toString('base64')
  }));
}

/**
 * Decrypts the encrypted data using AES-256-GCM algorithm
 * @param {string} encdata
 * @param {string} key
 * @returns {string} Decrypted plainText
 */
function decrypt(encdata, key) {
  let decrypted, decipher,
    {data, iv, tag} = JSON.parse(atob(encdata));

  key = crypto.createHash('sha256').update(key).digest();

  decipher = crypto.createDecipheriv('AES-256-GCM', key, Buffer.from(iv, 'base64'));
  decipher.setAuthTag(Buffer.from(tag, 'base64'));

  decrypted = decipher.update(data, 'base64', 'utf-8');
  decrypted += decipher.final('utf-8');

  return decrypted;
}

// Example usage:
let key = 'example-key'; // private key

let encMsg = encrypt('Your secret message?', key); // Outputs: eyJkYXRhIjoidzkzVGVPRDJwYzREUWVYUjRXeVJQU1FxWGZrPSIsIml2IjoiWlNpSVNmanNPcFBic0dvTGJUOUJDZz09IiwidGFnIjoiSkVFUDBBeGdkRUlnRVNyekNTZUJidz09In0=
decrypt(encMsg);                                   // Outputs: Your secret message?
```

### hasPassword and verifyPassword

[![Shorts Views](https://img.shields.io/youtube/views/9_soeaSaccs?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/9_soeaSaccs)
[![Shorts Likes](https://img.shields.io/youtube/likes/9_soeaSaccs?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/9_soeaSaccs)
[![Shorts Comments](https://img.shields.io/youtube/comments/9_soeaSaccs?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/9_soeaSaccs)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/9_soeaSaccs)

```js
const crypto = require('crypto');

/**
 * Create a password hash with salt hashing SHA-256 algorithm
 * @param {string} password 
 * @param {string} salt [optional]
 * @returns {string} Hashed Password
 */
function hashPassword(password, salt) {
  // Generate Salt
  salt = salt || crypto.randomBytes(16).toString('hex');
  let hash = salt + crypto.createHmac('sha256', salt).update(password).digest('hex');
  return hash;
}

/**
 * Checks if the given hash matches the given options
 * @param {string} password 
 * @param {string} hash 
 * @returns {boolean} Verified for true Otherwise false
 */
function verifyPassword(password, hash) {
  // Extract salt from given hash
  let salt = hash.slice(0, 32);
  return hashPassword(password, salt) === hash;
}

// Example usage:
let hash = hashPassword('123@pass'); // Outputs: Random => 8d0f5aa4fdfec0895a9e796420ffb9eeb223c9f04777e96d8038591378a535f662edfd6f9e3a49c64ca423bc38106125
verifyPassword('123@pass', hash);    // Outputs: true
verifyPassword('123@Pass', hash);    // Outputs: false
verifyPassword('pass@123', hash);    // Outputs: false
```

### toggleCase

[![Shorts Views](https://img.shields.io/youtube/views/5kPF4bQecWU?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/5kPF4bQecWU)
[![Shorts Likes](https://img.shields.io/youtube/likes/5kPF4bQecWU?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/5kPF4bQecWU)
[![Shorts Comments](https://img.shields.io/youtube/comments/5kPF4bQecWU?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/5kPF4bQecWU)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/5kPF4bQecWU)

```js
/**
 * Converts a string with a specified separator into tOGGLE cASE format.
 * @param {string} str
 * @param {string} sep
 * @returns {string} tOGGLE cASE format
 */
function toggleCase(str, sep = " ") {
  let regex = new RegExp("([^" + sep + "]+)", "g");

  // Converting str to tOGGLE cASE
  return str.replace(regex, (_, w) => w[0].toLowerCase() + w.slice(1).toUpperCase());
}

// Example usage:
let str = 'Hello World hello:world hello_world';

toggleCase(str);        // Outputs: hELLO wORLD hELLO:WORLD hELLO_WORLD
toggleCase(str, ': _'); // Outputs: hELLO wORLD hELLO:wORLD hELLO_wORLD
toggleCase(str, ': _'); // Outputs: tOGGLE cASE
toggleCase(str, ':_');  // Outputs: hELLO WORLD HELLO:wORLD HELLO_wORLD
```

### generatePassword

[![Shorts Views](https://img.shields.io/youtube/views/b9rw-DEwgj4?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/b9rw-DEwgj4)
[![Shorts Likes](https://img.shields.io/youtube/likes/b9rw-DEwgj4?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/b9rw-DEwgj4)
[![Shorts Comments](https://img.shields.io/youtube/comments/b9rw-DEwgj4?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/b9rw-DEwgj4)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/b9rw-DEwgj4)

```js
/**
 * Generates a Random strong password (e.g., CRsAB0f%XUGY)
 * @param {number} Password length
 * @returns The Random Password
 */
function generatePassword(len) {
  let chars = 'abcdefghijklmnopqrstuvwxyz',
    num = 1234567890,
    password = '',
    i = 0;

    // Concating num, Upper alpha and special chars
    chars += num + chars.toUpperCase() + '!@#$%^&*()';
    len = +len || 8;

  // Generating random password
  for(; i < len; i++) {
    password += chars[Math.floor(Math.random() * chars.length)];
  }

  return password;
}

// Example usage:
generatePassword();   // Outputs: CRsAB0f%XUGY
generatePassword(12); // Outputs: ayrYcu%Pu$Ka
```

### findLongest and findShortest

[![Shorts Views](https://img.shields.io/youtube/views/MDumTQ543O4?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/MDumTQ543O4)
[![Shorts Likes](https://img.shields.io/youtube/likes/MDumTQ543O4?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/MDumTQ543O4)
[![Shorts Comments](https://img.shields.io/youtube/comments/MDumTQ543O4?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/MDumTQ543O4)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/MDumTQ543O4)

```js
/**
 * Find the longest string value in an Array
 * @param {}
 * @returns The longest string
 */
function findLongest(arr) {
  return arr.reduce((max, val) => (
    max.length < val.length && (max = val),
    max
  ), arr[0] + '');
}

/**
 * Find the shortest string value in an Array
 * @param {}
 * @returns The shortest string
 */
function findShortest(arr) {
  return arr.reduce((min, val) => (
    min.length > val.length && (min = val),
    min
  ), arr[0] + '');
}

// Example usage:
let arr = ['Hello', 'How are you?', 'Welcome to you', 'Thanks'];

findLongest(arr);  // Outputs: Welcome to you
findShortest(arr); // Outputs: Hello
```

### strShuffle

[![Shorts Views](https://img.shields.io/youtube/views/kOB_yygDwIY?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/kOB_yygDwIY)
[![Shorts Likes](https://img.shields.io/youtube/likes/kOB_yygDwIY?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/kOB_yygDwIY)
[![Shorts Comments](https://img.shields.io/youtube/comments/kOB_yygDwIY?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/kOB_yygDwIY)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/kOB_yygDwIY)

```js
/**
 * shuffles a string. One permutation of all possible is created.
 * @param {string} str The input string.
 * @returns {string} Randomly shuffles a string
 */
function strShuffle(str) {
  let arr = str.split(''),
    i = arr.length - 1,
    rIndex;

  // Shuffle Algorithm
  for(; i > 0; i--) {
    rIndex = Math.floor(Math.random() * (i + 1));

    // Swap the current element with the random element
    [arr[i], arr[rIndex]] = [arr[rIndex], arr[i]];
  }

  return arr.join('');
}

// Example usage:
strShuffle('Hello'); // Outputs: olelH
```

### jsonEncode and jsonDecode

[![Shorts Views](https://img.shields.io/youtube/views/5uURC9ItBEQ?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/5uURC9ItBEQ)
[![Shorts Likes](https://img.shields.io/youtube/likes/5uURC9ItBEQ?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/5uURC9ItBEQ)
[![Shorts Comments](https://img.shields.io/youtube/comments/5uURC9ItBEQ?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/5uURC9ItBEQ)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/5uURC9ItBEQ)

```
/**
 * Converts a JavaScript value to a JavaScript Object Notation (JSON) string.
 * @param {any} value           [required]
 * @param {any} replacer        [optional]
 * @param {string|number} space [optional]
 * @returns {string} The JSON string representation of the object.
 */
function jsonEncode(value, replacer, space) {
  try {
    return JSON.stringify(value, replacer, space);
  } catch(e) {
    throw new Error('Error encoding object: ' + e);
  }
}

/**
 * Converts a JavaScript Object Notation (JSON) string into an object.
 * @param {string} json [required]
 * @param {any} reviver [optional]
 * @returns {object} The decoded Javascript object
 */
function jsonDecode(json, reviver) {
  try {
    return JSON.parse(json, reviver);
  } catch(e) {
    throw new Error('Error decoding JSON: ' + e);
  }
}

// Example usage with output:

let obj = {name: 'Modassir', age: 23, Indian: true};

// Encoding the object to a JSON string
let json = jsonEncode(obj);  // Outputs: '{"name":"Modassir","age":23,"Indian":true}'

// Decoding the JSON string back to a JavaScript object
jsonDecode(json); // Outputs: {name: 'Modassir', age: 23, Indian: true}
```

### wordCount

[![Shorts Views](https://img.shields.io/youtube/views/LkZgDWlKauU?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/LkZgDWlKauU)
[![Shorts Likes](https://img.shields.io/youtube/likes/LkZgDWlKauU?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/LkZgDWlKauU)
[![Shorts Comments](https://img.shields.io/youtube/comments/LkZgDWlKauU?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/LkZgDWlKauU)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/LkZgDWlKauU)

```js
/**
 * Return information about words used in a string
 * @param {string} str The string
 * @param {number} format Specify the return value of this function. The current supported values
 * @param {string} chars A list of additional characters which will be considered as 'word'
 * @returns Information about words
 */
function wordCount(str, format = 0, chars) {
  let regstr = new RegExp("([a-z-0-9" + (chars || "") + "]+)", "gi"),
    ret = [0, [], {}][format],
    result;

  while((result = regstr.exec(str))) {
    if (format === 0) ret++;
    else if (format === 1) ret.push(result[0]);
    else ret[result.index] = result[0];
  }

  return ret;
}

// Example usage:
let str = 'one:two three-four five_six seven$eight nine%ten';

wordCount(str);           // Outputs: 9
wordCount(str, 0, '$:%'); // Outputs: 6
wordCount(str, 1);        // Outputs: ['one', 'two', 'three-four', 'five', 'six', 'seven','eight', 'nine', 'ten']
wordCount(str, 1, '$:%'); // Outputs: [ 'one:two', 'three-four', 'five', 'six', 'seven$eight', 'nine%ten' ]
wordCount(str, 2);        // Outputs: {'0': 'one','4': 'two','8': 'three-four','19': 'five','24': 'six','28': 'seven','34': 'eight','40': 'nine','45': 'ten'}
wordCount(str, 2, '$:%'); // Outputs: {'0': 'one:two','8': 'three-four','19': 'five','24': 'six','28': 'seven$eight','40': 'nine%ten'}
```

### speech2text

[![Shorts Views](https://img.shields.io/youtube/views/zW_zEscP1bU?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/zW_zEscP1bU)
[![Shorts Likes](https://img.shields.io/youtube/likes/zW_zEscP1bU?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/zW_zEscP1bU)
[![Shorts Comments](https://img.shields.io/youtube/comments/zW_zEscP1bU?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/zW_zEscP1bU)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/zW_zEscP1bU)

```js
/**
* Text to Speech using SpeechSynthesisUtterance and SpeechSynthesis API
* @param {string} text target text for speech
*/
function text2speech(text) {
 let speech = new window.SpeechSynthesisUtterance(text),
   synthesis = window.speechSynthesis;

 // Optional: Set language of speech
 speech.lang = 'en-US';

 // Optional: Set pitch and rate of speech
 speech.pitch = 1;
 speech.rate = 1;
 
 // Start speech
 synthesis.speak(speech);
}

// Example usage:
speech2text('Hello viewers, how are you?');
```

### cmdout

[![Shorts Views](https://img.shields.io/youtube/views/rdfFyUhKUys?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/rdfFyUhKUys)
[![Shorts Likes](https://img.shields.io/youtube/likes/rdfFyUhKUys?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/rdfFyUhKUys)
[![Shorts Comments](https://img.shields.io/youtube/comments/rdfFyUhKUys?style=flat-square&logo=youtube)](https://www.youtube.com/shorts/rdfFyUhKUys)

Watch video shorts on youtube click: [Watch Now](https://www.youtube.com/shorts/rdfFyUhKUys)

```js
/**
 * cmdout To highlight text or background color in cmd/terminal
 * @param {string} text Target text to highlight
 * @param {boolean} setBg true for background otherwise text highlight
 * @param {boolean} bold true for bold otherwise normal
 * @param {array} color Don't use, Internal use only [private]
 * @returns The highlightable text format
 */
function cmdout(text, setBg, bold, color) {
  let ansi = `\x1b[${setBg ? 48 : 38};2;${color.join(';')}m`;

  if (bold) ansi = `\x1b[1m${ansi}`;
  if (setBg) text = `\x20${text}\x20`;

  return `${ansi}${text}\x1b[0m`;
}

Object.assign(cmdout, {
  blue: function(text, setBg, bold) {
    return cmdout(text, setBg, bold, [8, 48, 218]);
  },
  green: function(text, setBg, bold) {
    return cmdout(text, setBg, bold, [19, 161, 14]);
  },
  aqua: function(text, setBg, bold) {
    return cmdout(text, setBg, bold, [58, 150, 221]);
  },
  red: function(text, setBg, bold) {
    return cmdout(text, setBg, bold, [197, 15, 31]);
  },
  purple: function(text, setBg, bold) {
    return cmdout(text, setBg, bold, [136, 23, 152]);
  },
  yellow: function(text, setBg, bold) {
    return cmdout(text, setBg, bold, [193, 156, 0]);
  },
  white: function(text, setBg, bold) {
    return cmdout(text, setBg, bold, [204, 204, 204]);
  },
  gray: function(text, setBg, bold) {
    return cmdout(text, setBg, bold, [118, 118, 118]);
  }
});

// Example usage:
cmdout.yellow('Like', true, true) + cmdout.blue('Subscribe', true, true); // Outputs:
cmdout.red('Hello World!', false, true);                                  // Outputs:
cmdout.red('Hello World!', true, true);                                   // Outputs:
cmdout.yellow('Hello World!', false, true);                               // Outputs:
cmdout.yellow('Hello World!', true, true);                                // Outputs:
cmdout.blue('Hello World!', false, true);                                 // Outputs:
cmdout.red('Thanks', true, true) + cmdout.yellow('Watching', true, true); // Outputs:
```

### getType

[![Shorts Views](https://img.shields.io/youtube/views/i2azCn225nE?style=flat-square&logo=youtube)](https://youtube.com/shorts/i2azCn225nE)
[![Shorts Likes](https://img.shields.io/youtube/likes/i2azCn225nE?style=flat-square&logo=youtube)](https://youtube.com/shorts/i2azCn225nE)
[![Shorts Comments](https://img.shields.io/youtube/comments/i2azCn225nE?style=flat-square&logo=youtube)](https://youtube.com/shorts/i2azCn225nE)

Watch video shorts on youtube click: [Watch Now](https://youtube.com/shorts/i2azCn225nE)

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
