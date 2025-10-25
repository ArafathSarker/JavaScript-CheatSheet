# JavaScript Cheatsheet

## 1. 🔹 Strings
```javascript
let str = "hello world";

str.length                 // length of string
str.charAt(i) / str[i]     // character at index
str.substring(start, end)  // substring
str.slice(start, end)      // substring (supports negative indices)
str.substr(start, len)     // substring (deprecated)
str.indexOf("word")        // first position
str.lastIndexOf("word")    // last position
str.includes("word")       // check contains
str.startsWith("he")       // check start
str.endsWith("ld")         // check end
str.toUpperCase(), str.toLowerCase()  // case conversion
str.trim()                 // remove spaces (start+end)
str.trimStart(), str.trimEnd() // remove leading/trailing spaces
str.replace("old", "new")  // replace first match
str.replaceAll("old", "new") // replace all
str.split(" ")             // split into array
str.repeat(n)              // repeat string
```
## 2. 🔹 Numbers & Math
```javascript
let x = 42.7;

Math.abs(x)                // absolute
Math.floor(x), Math.ceil(x), Math.round(x), Math.trunc(x) // rounding
Math.pow(a, b), Math.sqrt(x)  // power, square root
Math.max(a, b, ...), Math.min(a, b, ...) // min/max
Math.random()              // random [0,1)
Math.sin(x), Math.cos(x), Math.tan(x) // trigonometry

parseInt("42"), parseFloat("42.7")  // string → number
Number("42"), Number("42.5")        // conversion
isNaN(val), isFinite(val)           // checks
```
## 3. 🔹 Arrays
```javascript
let arr = [1, 2, 3, 4];

arr.length                 // size
arr.push(x), arr.pop()     // add/remove end
arr.shift(), arr.unshift(x) // remove/add front
arr.concat(arr2)           // join arrays
arr.slice(start, end)      // copy part
arr.splice(start, deleteCount, ...items) // insert/remove
arr.indexOf(x), arr.lastIndexOf(x) // search index
arr.includes(x)            // check existence
arr.reverse()              // reverse
arr.sort()                 // sort lexically
arr.sort((a, b) => a - b)  // numeric sort
arr.join(",")              // array → string
Array.from(str)            // string → array
arr.flat(depth)            // flatten nested arrays
arr.fill(val, start, end)  // fill with value
```

## 4. 🔹 Array Iteration (🔥 super important)
```javascript
arr.forEach(fn)   // loop
arr.map(fn)       // transform
arr.filter(fn)    // filter elements
arr.reduce(fn, init) // reduce to single value
arr.find(fn)      // first match
arr.findIndex(fn) // index of first match
arr.every(fn)     // check all true
arr.some(fn)      // check if any true
```

## 5. 🔹 Objects
```javascript
let obj = { name: "Arafath", age: 21 };

Object.keys(obj)          // array of keys
Object.values(obj)        // array of values
Object.entries(obj)       // array of [key, value]
Object.assign(target, source) // copy properties
delete obj.key            // remove key
obj.hasOwnProperty("key") // check property
```
## 6. 🔹 JSON
```javascript
JSON.stringify(obj)   // object → JSON string
JSON.parse(str)       // JSON string → object
```

## 7. 🔹 Dates
```javascript
let d = new Date();

d.getFullYear(), d.getMonth(), d.getDate() // year, month(0-11), day
d.getHours(), d.getMinutes(), d.getSeconds() // time
d.toISOString(), d.toDateString(), d.toTimeString() // formats
Date.now()            // timestamp (ms since 1970)
```
## 8. 🔹 Functions & Utils
```javascript
typeof val           // type of value
Array.isArray(arr)   // check array
isNaN(x), isFinite(x) // number checks
eval(str)            // evaluate string as JS (⚠️ dangerous)
```

## 9. 🔹 DOM (Browser-specific)
```javascript
document.getElementById("id");
document.querySelector(".class");
document.querySelectorAll("div");

element.innerHTML = "text";
element.textContent = "text";
element.style.color = "red";

element.addEventListener("click", fn);
```

## 10. 🔹 Async / Promises / Fetch
```javascript
setTimeout(fn, ms)     // run later
setInterval(fn, ms)    // repeat

Promise.resolve(val);
Promise.reject(err);

fetch(url)
  .then(res => res.json())
  .then(data => console.log(data))
  .catch(err => console.error(err));

async function getData() {
  let res = await fetch(url);
  let data = await res.json();
  console.log(data);
}
```
# 11. 🔹 Examples
## Example 1: Basic usage
```javascript
let str = "Hello, world!";
let index = str.search("world");
console.log(index);  // Output: 7
```
## Example 2: Using a regular expression
```javascript
let str = "I have 2 apples and 5 oranges.";
let index = str.search(/\d+/); // \d+ matches one or more digits
console.log(index);  // Output: 7
```
## Example 3: Case-insensitive search
```javascript
let str = "JavaScript is fun!";
let index = str.search(/javascript/i); // 'i' makes it case-insensitive
console.log(index);  // Output: 0
```