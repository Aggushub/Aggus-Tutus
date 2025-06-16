# JavaScript Array & String Functions

This is the a complete rundown of all built‑in JavaScript String and Array methods. First you’ll find, for each, its signature, a brief definition and a one‑line example. After that is a single JS program that invokes every method, with each call’s expected output shown in a comment.

## String Methods

| Method                                         | Description                                                            | Example                                      |
| ---------------------------------------------- | ---------------------------------------------------------------------- | -------------------------------------------- |
| `str.length`                                   | Number of UTF‑16 code units in the string                              | `"hi".length // 2`                           |
| `str.charAt(i)`                                | Character at index `i`                                                 | `"abc".charAt(1) // "b"`                     |
| `str.charCodeAt(i)`                            | UTF‑16 code of char at index `i`                                       | `"A".charCodeAt(0) // 65`                    |
| `str.codePointAt(i)`                           | Unicode code point at index `i` (handles astral symbols)               | `"😊".codePointAt(0) // 128522`              |
| `str.concat(...strings)`                       | Concatenate one or more strings                                        | `"a".concat("b","c") // "abc"`               |
| `str.endsWith(substr[, length])`               | `true` if string (or its first `length` chars) ends with `substr`      | `"test.js".endsWith(".js") // true`          |
| `str.includes(substr[, pos])`                  | `true` if `substr` occurs at or after position `pos`                   | `"hello".includes("ll") // true`             |
| `str.indexOf(substr[, pos])`                   | Index of first `substr` at or after `pos`, or `-1`                     | `"banana".indexOf("na") // 2`                |
| `str.lastIndexOf(substr[, pos])`               | Index of last `substr` before or at `pos`, or `-1`                     | `"banana".lastIndexOf("na") // 4`            |
| `str.localeCompare(other[, locales, options])` | Returns –1/0/1 comparing lexically under locale rules                  | `"a".localeCompare("b") // -1`               |
| `str.match(regexp)`                            | Array of matches (or `null`)                                           | `"a1b2".match(/\d/) // ["1"]`                |
| `str.matchAll(regexp)`                         | Iterator of all match objects                                          | `Array.from("a1b2".matchAll(/\d/g)) // [..]` |
| `str.normalize([form])`                        | Unicode normalization                                                  | `"\u00E9".normalize("NFD") // "é"`          |
| `str.padEnd(len[, pad])`                       | Pad string on right to length `len` with `pad`                         | `"42".padEnd(4,"0") // "4200"`               |
| `str.padStart(len[, pad])`                     | Pad string on left to length `len` with `pad`                          | `"5".padStart(3,"0") // "005"`               |
| `str.repeat(count)`                            | Repeat the string `count` times                                        | `"ab".repeat(3) // "ababab"`                 |
| `str.replace(regexpOrStr, newSub)`             | First match replaced (RegExp or string)                                | `"foo".replace("o","0") // "f0o"`            |
| `str.replaceAll(regexpOrStr, newSub)`          | All matches replaced                                                   | `"foo".replaceAll("o","0") // "f00"`         |
| `str.search(regexp)`                           | Index of first match of `regexp`, or `-1`                              | `"a1b2".search(/\d/) // 1`                   |
| `str.slice(start[, end])`                      | Substring from `start` up to (but not including) `end`                 | `"hello".slice(1,4) // "ell"`                |
| `str.split([sep[, limit]])`                    | Split into array by `sep` (string or regex), up to `limit` parts       | `"a,b,c".split(",") // ["a","b","c"]`        |
| `str.startsWith(substr[, pos])`                | `true` if string at or after `pos` starts with `substr`                | `"js".startsWith("j") // true`               |
| `str.substring(start[, end])`                  | Like `slice` but swaps args if `start>end` and treats negatives as `0` | `"hello".substring(1,4) // "ell"`            |
| `str.toLocaleLowerCase([locales])`             | Lowercase under locale rules                                           | `"İ".toLocaleLowerCase("tr") // "i̇"`        |
| `str.toLocaleUpperCase([locales])`             | Uppercase under locale rules                                           | `"ß".toLocaleUpperCase("de") // "SS"`        |
| `str.toLowerCase()`                            | Convert all to lowercase                                               | `"HeLLo".toLowerCase() // "hello"`           |
| `str.toUpperCase()`                            | Convert all to uppercase                                               | `"HeLLo".toUpperCase() // "HELLO"`           |
| `str.trim()`                                   | Remove whitespace from both ends                                       | `"  hi  ".trim() // "hi"`                    |
| `str.trimStart()` / `str.trimLeft()`           | Remove whitespace from start                                           | `"  hi".trimStart() // "hi"`                 |
| `str.trimEnd()` / `str.trimRight()`            | Remove whitespace from end                                             | `"hi  ".trimEnd() // "hi"`                   |
| `str.toString()`                               | Returns the primitive string value                                     | `new String("x").toString() // "x"`          |
| `str.valueOf()`                                | Same as `toString()`                                                   | `"x".valueOf() // "x"`                       |

---

## Array Methods

| Method                                         | Description                                                      | Example                                                |
| ---------------------------------------------- | ---------------------------------------------------------------- | ------------------------------------------------------ |
| `Array.isArray(obj)`                           | `true` if `obj` is an Array                                      | `Array.isArray([]) // true`                            |
| `arr.length`                                   | Number of elements                                               | `[1,2].length // 2`                                    |
| `arr.concat(...values)`                        | Returns new array by concatenating `values` (arrays or elements) | `[1].concat(2,[3]) // [1,2,3]`                         |
| `arr.copyWithin(target, start[, end])`         | Copy a slice of itself within the same array                     | `[1,2,3,4].copyWithin(0,2) // [3,4,3,4]`               |
| `arr.entries()`                                | Returns iterator of `[index, value]` pairs                       | `Array.from([5,6].entries()) // [[0,5],[1,6]]`         |
| `arr.every(fn[, thisArg])`                     | `true` if `fn` returns truthy for **all** elements               | `[2,4].every(x=>x%2==0) // true`                       |
| `arr.fill(value[, start[, end]])`              | Fill elements with `value` from `start` to `end`                 | `[1,2,3].fill(0,1) // [1,0,0]`                         |
| `arr.filter(fn[, thisArg])`                    | New array of elements where `fn` returns truthy                  | `[1,2,3].filter(x=>x>1) // [2,3]`                      |
| `arr.find(fn[, thisArg])`                      | First element where `fn` returns truthy, or `undefined`          | `[1,2,3].find(x=>x>1) // 2`                            |
| `arr.findIndex(fn[, thisArg])`                 | Index of first match for `fn`, or `-1`                           | `[1,2,3].findIndex(x=>x>1) // 1`                       |
| `arr.flat([depth])`                            | Flatten nested arrays up to `depth` (default 1)                  | `[1,[2,[3]]].flat() // [1,2,[3]]`                      |
| `arr.flatMap(fn[, thisArg])`                   | Map each then flatten result by one level                        | `[1,2].flatMap(x=>[x,x]) // [1,1,2,2]`                 |
| `arr.forEach(fn[, thisArg])`                   | Invoke `fn` for each element (no return value)                   | `[].forEach(x=>console.log(x))`                        |
| `arr.includes(value[, fromIndex])`             | `true` if array contains `value`                                 | `[1,2].includes(2) // true`                            |
| `arr.indexOf(searchElement[, fromIndex])`      | Index of first `searchElement`, or `-1`                          | `[1,2,1].indexOf(1,1) // 2`                            |
| `arr.join([sep])`                              | Join elements into string with separator `sep`                   | `[1,2,3].join("-") // "1-2-3"`                         |
| `arr.keys()`                                   | Iterator of indices                                              | `Array.from([].keys()) // []`                          |
| `arr.lastIndexOf(searchElement[, fromIndex])`  | Last index of `searchElement`, or `-1`                           | `[1,2,1].lastIndexOf(1) // 2`                          |
| `arr.map(fn[, thisArg])`                       | New array with results of calling `fn` on each element           | `[1,2].map(x=>x*x) // [1,4]`                           |
| `arr.pop()`                                    | Remove and return last element                                   | `[1,2,3].pop() // 3`                                   |
| `arr.push(...elements)`                        | Append elements, returns new length                              | `let a=[1]; a.push(2) // 2 and a=[1,2]`                |
| `arr.reduce(fn[, init])`                       | Reduce to single value from left                                 | `[1,2,3].reduce((a,b)=>a+b,0) // 6`                    |
| `arr.reduceRight(fn[, init])`                  | Same as `reduce` but from right                                  | `[1,2,3].reduceRight((a,b)=>a-b) // -4`                |
| `arr.reverse()`                                | Reverse in place, returns the array                              | `[1,2,3].reverse() // [3,2,1]`                         |
| `arr.shift()`                                  | Remove and return first element                                  | `[1,2,3].shift() // 1`                                 |
| `arr.slice([start[, end]])`                    | Extract subarray (non‑destructive)                               | `[1,2,3].slice(1,3) // [2,3]`                          |
| `arr.some(fn[, thisArg])`                      | `true` if `fn` returns truthy for **any** element                | `[1,2,3].some(x=>x>2) // true`                         |
| `arr.sort([compareFn])`                        | Sort in place (strings by UTF‑16 by default, or via `compareFn`) | `[2,1,3].sort() // [1,2,3]`                            |
| `arr.splice(start[, deleteCount[, ...items]])` | Change contents by removing/inserting elements                   | `[1,2,3].splice(1,1,9) // returns [2] and arr=[1,9,3]` |
| `arr.toLocaleString([locales,options])`        | Locale‑sensitive string of elements                              | `[1234].toLocaleString("de") // "1.234"`               |
| `arr.toString()`                               | String of elements separated by commas                           | `[1,2,3].toString() // "1,2,3"`                        |
| `arr.unshift(...elements)`                     | Insert at front, returns new length                              | `let b=[2]; b.unshift(1) // 2 and b=[1,2]`             |
| `arr.values()`                                 | Iterator of values                                               | `Array.from([1,2].values()) // [1,2]`                  |
| `arr[@@iterator]()`  – same as `values()`      | Default iterator for `for…of`                                    | `for(let x of [1,2])…`                                 |

---

## Example Program

```javascript
// — String demo —
let s = "  Hello, JS!  ";
console.log(s.length);                   // 14
console.log(s.charAt(2));                // "H"
console.log(s.charCodeAt(2));            // 72
console.log(String.fromCodePoint(128522)); // "😊"
console.log(s.concat(" Welcome."));      // "  Hello, JS!   Welcome."
console.log(s.endsWith("!  "));          // true
console.log(s.includes("JS"));           // true
console.log(s.indexOf("JS"));            // 9
console.log(s.lastIndexOf(" "));         // 13
console.log("a".localeCompare("b"));     // -1
console.log("a1b2".match(/\d/g));        // ["1","2"]
console.log(Array.from("a1b2".matchAll(/\d/g))); // [ ["1"], ["2"] ]
console.log("\u00E9".normalize("NFD"));  // "é"
console.log("42".padStart(4,"0"));       // "0042"
console.log("42".padEnd(4,"0"));         // "4200"
console.log("ha".repeat(3));             // "hahaha"
console.log("foo".replace("o","0"));     // "f0o"
console.log("foo".replaceAll("o","0"));  // "f00"
console.log("a1b2".search(/\d/));        // 1
console.log("hello".slice(1,4));         // "ell"
console.log("a,b,c".split(","));         // ["a","b","c"]
console.log("JS".startsWith("J"));       // true
console.log("hello".substring(1,4));     // "ell"
console.log("HeLLo".toLowerCase());      // "hello"
console.log("HeLLo".toUpperCase());      // "HELLO"
console.log("  hi  ".trim());            // "hi"
console.log("  hi".trimStart());         // "hi"
console.log("hi  ".trimEnd());           // "hi"
console.log(new String("x").toString()); // "x"
console.log("x".valueOf());              // "x"

// — Array demo —
console.log(Array.isArray([1,2]));       // true
let arr = [1,2,3,4,5];
console.log(arr.length);                 // 5
console.log(arr.concat(6,[7,8]));        // [1,2,3,4,5,6,7,8]
console.log([1,2,3,4].copyWithin(0,2));  // [3,4,3,4]
console.log(Array.from([5,6].entries())); // [[0,5],[1,6]]
console.log([2,4].every(x=>x%2==0));     // true
console.log([1,2,3].fill(0,1));          // [1,0,0]
console.log([1,2,3].filter(x=>x>1));     // [2,3]
console.log([1,2,3].find(x=>x>1));       // 2
console.log([1,2,3].findIndex(x=>x>1));  // 1
console.log([1,[2,[3]]].flat());         // [1,2,[3]]
console.log([1,2].flatMap(x=>[x,x]));    // [1,1,2,2]
[1,2,3].forEach(x=>{});                  // (no output)
console.log([1,2].includes(2));          // true
console.log([1,2,1].indexOf(1,1));       // 2
console.log([1,2,3].join("-"));          // "1-2-3"
console.log(Array.from([].keys()));       // []
console.log([1,2,1].lastIndexOf(1));     // 2
console.log([1,2].map(x=>x*x));          // [1,4]
console.log([1,2,3].pop());              // 3
let a=[1]; console.log(a.push(2), a);    // 2 [1,2]
console.log([1,2,3].reduce((a,b)=>a+b,0)); // 6
console.log([1,2,3].reduceRight((a,b)=>a-b)); // -4
console.log([1,2,3].reverse());          // [3,2,1]
console.log([1,2,3].shift());            // 1
console.log([1,2,3].slice(1,3));         // [2,3]
console.log([1,2,3].some(x=>x>2));       // true
console.log([2,1,3].sort());             // [1,2,3]
let sp = [1,2,3]; console.log(sp.splice(1,1,9), sp); // [2] [1,9,3]
console.log([1234].toLocaleString("de")); // "1.234"
console.log([1,2,3].toString());         // "1,2,3"
let b=[2]; console.log(b.unshift(1), b); // 2 [1,2]
console.log(Array.from([1,2].values())); // [1,2]
for (let v of [1,2]) console.log(v);     // 1<br>// 2
```
