# 🧠✨ The Ultimate Cross-Language Function CheatSheet!
Because remembering every syntax is harder than remembering your Wi-Fi password 😅

Welcome to the Python 🐍 | JavaScript 💻 | Java ☕ Trilingual Function Bible — a single mega-table that bridges the gap between “Wait, how do I do this in JS again?” and “Oh right, that’s .length() not .len()!”

From Strings to OOP, Loops to Regex, Exceptions to ASCII, this doc covers it all — cleanly, clearly, and with enough caffeine energy to survive your next coding interview. ☕⚡

---

## 🧵 STRING FUNCTIONS COMPARISON

| Index + Description                                                   | Python                  | JavaScript              | Java                      |
| --------------------------------------------------------------------- | ----------------------- | ----------------------- | ------------------------- |
| **1. Length of string — returns number of characters.**               | `len(str)`              | `str.length`            | `str.length()`            |
| **2. Convert to uppercase — makes all letters capital.**              | `str.upper()`           | `str.toUpperCase()`     | `str.toUpperCase()`       |
| **3. Convert to lowercase — makes all letters small.**                | `str.lower()`           | `str.toLowerCase()`     | `str.toLowerCase()`       |
| **4. Trim spaces — removes whitespace from both ends.**               | `str.strip()`           | `str.trim()`            | `str.trim()`              |
| **5. Replace substring — substitutes part of text with another.**     | `str.replace(old, new)` | `str.replace(old, new)` | `str.replace(old, new)`   |
| **6. Split string — divides string into list/array using delimiter.** | `str.split(delim)`      | `str.split(delim)`      | `str.split(delim)`        |
| **7. Join list/array — merges elements into single string.**          | `' '.join(list)`        | `arr.join(delim)`       | `String.join(delim, arr)` |
| **8. Find substring — returns first index of substring.**             | `str.find('x')`         | `str.indexOf('x')`      | `str.indexOf('x')`        |
| **9. Check prefix — verifies if string starts with given chars.**     | `str.startswith('x')`   | `str.startsWith('x')`   | `str.startsWith('x')`     |
| **10. Check suffix — verifies if string ends with given chars.**      | `str.endswith('x')`     | `str.endsWith('x')`     | `str.endsWith('x')`       |

---

## 🔢 NUMBER FUNCTIONS COMPARISON

| Index + Description                                         | Python                | JavaScript                      | Java                                            |
| ----------------------------------------------------------- | --------------------- | ------------------------------- | ----------------------------------------------- |
| **1. Absolute value — positive magnitude of number.**       | `abs(x)`              | `Math.abs(x)`                   | `Math.abs(x)`                                   |
| **2. Round number — rounds to nearest integer or decimal.** | `round(x, n)`         | `Math.round(x)`                 | `Math.round(x)`                                 |
| **3. Power/exponent — raises x to y.**                      | `pow(x, y)`           | `Math.pow(x, y)`                | `Math.pow(x, y)`                                |
| **4. Minimum value — smaller of numbers.**                  | `min(a,b)`            | `Math.min(a,b)`                 | `Math.min(a,b)`                                 |
| **5. Maximum value — larger of numbers.**                   | `max(a,b)`            | `Math.max(a,b)`                 | `Math.max(a,b)`                                 |
| **6. Type conversion — string → numeric.**                  | `int(x)` / `float(x)` | `parseInt(x)` / `parseFloat(x)` | `Integer.parseInt(x)` / `Double.parseDouble(x)` |
| **7. Sum of list/array.**                                   | `sum(list)`           | `arr.reduce((a,b)=>a+b)`        | `Arrays.stream(arr).sum()`                      |
| **8. Square root — √x.**                                    | `math.sqrt(x)`        | `Math.sqrt(x)`                  | `Math.sqrt(x)`                                  |
| **9. Floor value — rounds down.**                           | `math.floor(x)`       | `Math.floor(x)`                 | `Math.floor(x)`                                 |
| **10. Ceil value — rounds up.**                             | `math.ceil(x)`        | `Math.ceil(x)`                  | `Math.ceil(x)`                                  |

---

## 🧮 LIST / ARRAY FUNCTIONS COMPARISON

| Index + Description                 | Python               | JavaScript               | Java                        |
| ----------------------------------- | -------------------- | ------------------------ | --------------------------- |
| **1. Length — number of elements.** | `len(arr)`           | `arr.length`             | `arr.length`                |
| **2. Add element at end.**          | `arr.append(x)`      | `arr.push(x)`            | `list.add(x)`               |
| **3. Remove last element.**         | `arr.pop()`          | `arr.pop()`              | `list.remove(index)`        |
| **4. Sort ascending.**              | `arr.sort()`         | `arr.sort()`             | `Collections.sort(list)`    |
| **5. Reverse order.**               | `arr.reverse()`      | `arr.reverse()`          | `Collections.reverse(list)` |
| **6. Find index of element.**       | `arr.index(x)`       | `arr.indexOf(x)`         | `list.indexOf(x)`           |
| **7. Check presence of element.**   | `x in arr`           | `arr.includes(x)`        | `list.contains(x)`          |
| **8. Remove by value.**             | `arr.remove(x)`      | `arr.splice(index,1)`    | `list.remove(Object)`       |
| **9. Sum of all elements.**         | `sum(arr)`           | `arr.reduce((a,b)=>a+b)` | `Arrays.stream(arr).sum()`  |
| **10. Map/transform each element.** | `[x*x for x in arr]` | `arr.map(x=>x*x)`        | `list.stream().map(x->x*x)` |

---

## 🧩 **SET FUNCTIONS COMPARISON**

| Index + Description                                | Python            | JavaScript                                     | Java                                                       
| -------------------------------------------------- | ----------------- | ---------------------------------------------- | ------------------------------------- 
| **1. Create a set — unique elements only.**        | `myset = {1,2,3}` | `let myset = new Set([1,2,3])`                 | `Set<Integer> set = new HashSet<>();` |                      |
| **2. Add an element to set.**                      | `myset.add(4)`    | `myset.add(4)`                                 | `set.add(4);`                         |                      |
| **3. Remove an element.**                          | `myset.remove(2)` | `myset.delete(2)`                              | `set.remove(2);`                      |                      |
| **4. Check presence of element.**                  | `2 in myset`      | `myset.has(2)`                                 | `set.contains(2);`                    |                      |
| **5. Union — combine two sets.**                   | `set1 + set2`     | `new Set([...set1, ...set2])`                  | `set1.addAll(set2);` 
|                      |
| **6. Intersection — common elements.**             | `set1 & set2`     | `new Set([...set1].filter(x => set2.has(x)))`  | `set1.retainAll(set2);`               |                      |
| **7. Difference — elements in one but not other.** | `set1 - set2`     | `new Set([...set1].filter(x => !set2.has(x)))` | `set1.removeAll(set2);`               |                      |
| **8. Clear all elements.**                         | `myset.clear()`   | `myset.clear()`                                | `set.clear();`                        |                      |
| **9. Length/size of set.**                         | `len(myset)`      | `myset.size`                                   | `set.size();`                         |                      |
| **10. Convert to list/array.**                     | `list(myset)`     | `[...myset]`                                   | `new ArrayList<>(set);`               

---

## 🧠 **DICTIONARY / MAP FUNCTIONS COMPARISON**

| Index + Description                           | Python                      | JavaScript                            | Java                                            |
| --------------------------------------------- | --------------------------- | ------------------------------------- | ----------------------------------------------- |
| **1. Create dictionary/map.**                 | `d = {'a':1, 'b':2}`        | `let obj = {a:1, b:2}` / `new Map()`  | `Map<String, Integer> map = new HashMap<>();`   |
| **2. Access value by key.**                   | `d['a']`                    | `obj.a` / `map.get('a')`              | `map.get("a");`                                 |
| **3. Add or update key-value.**               | `d['c'] = 3`                | `obj.c = 3` / `map.set('c',3)`        | `map.put("c", 3);`                              |
| **4. Remove key-value pair.**                 | `d.pop('a')`                | `delete obj.a` / `map.delete('a')`    | `map.remove("a");`                              |
| **5. Check if key exists.**                   | `'a' in d`                  | `'a' in obj` / `map.has('a')`         | `map.containsKey("a");`                         |
| **6. Get all keys.**                          | `d.keys()`                  | `Object.keys(obj)` / `map.keys()`     | `map.keySet();`                                 |
| **7. Get all values.**                        | `d.values()`                | `Object.values(obj)` / `map.values()` | `map.values();`                                 |
| **8. Loop through key-value pairs.**          | `for k,v in d.items(): ...` | `for (let [k,v] of map) {...}`        | `for (Map.Entry<K,V> e : map.entrySet()) {...}` |
| **9. Get value with default if key missing.** | `d.get('x', 0)`             | `obj.x ?? 0` / `map.get('x') ?? 0`    | `map.getOrDefault("x", 0);`                     |
| **10. Clear all key-values.**                 | `d.clear()`                 | `map.clear()`                         | `map.clear();`                                  |

---

## 🧱 OOP CONCEPTS COMPARISON

| Index + Description                             | Python                | JavaScript               | Java                       |
| ----------------------------------------------- | --------------------- | ------------------------ | -------------------------- |
| **1. Define class — create user-defined type.** | `class Person:`       | `class Person {}`        | `class Person {}`          |
| **2. Create object.**                           | `p = Person()`        | `const p = new Person()` | `Person p = new Person();` |
| **3. Constructor — initialize object.**         | `def __init__(self):` | `constructor() {}`       | `Person() {}`              |
| **4. Inheritance — derive subclass.**           | `class B(A):`         | `class B extends A`      | `class B extends A`        |
| **5. Override parent method.**                  | `def show(self):`     | `show() {}`              | `@Override void show()`    |
| **6. Encapsulation — restrict access.**         | `_var` (protected)    | `#var` (private)         | `private int x;`           |
| **7. Polymorphism — many forms.**               | Dynamic typing        | Overriding               | Overloading + Overriding   |
| **8. Abstraction — hide internal details.**     | ABC classes           | Abstract/interface       | Abstract/interface         |
| **9. Static method — class-level function.**    | `@staticmethod`       | `static myFunc()`        | `static void func()`       |
| **10. Getter/Setter.**                          | `@property`           | `get x()` / `set x(v)`   | `getX()` / `setX()`        |

---

## 🧩 CONSTRUCTORS COMPARISON

| Index + Description                    | Python                   | JavaScript         | Java                      |
| -------------------------------------- | ------------------------ | ------------------ | ------------------------- |
| **1. Constructor definition.**         | `def __init__(self):`    | `constructor()`    | `ClassName() {}`          |
| **2. Auto called on object creation.** | `p = Person()`           | `new Person()`     | `new Person()`            |
| **3. Default values supported.**       | `def __init__(self,x=0)` | `constructor(x=0)` | Overloading with defaults |
| **4. Overloading constructors.**       | Not supported            | Not supported      | Supported                 |
| **5. Calling parent constructor.**     | `super().__init__()`     | `super()`          | `super()`                 |

---

## 📁 FILE HANDLING COMPARISON

| Index + Description                   | Python                  | JavaScript                     | Java                                              |
| ------------------------------------- | ----------------------- | ------------------------------ | ------------------------------------------------- |
| **1. Open file for read/write.**      | `open('file.txt', 'r')` | `fs.readFileSync('file.txt')`  | `FileReader fr = new FileReader("file.txt");`     |
| **2. Read contents.**                 | `file.read()`           | `fs.readFileSync('f','utf-8')` | `BufferedReader br.readLine()`                    |
| **3. Write to file.**                 | `file.write("text")`    | `fs.writeFileSync('f','text')` | `FileWriter fw.write("text")`                     |
| **4. Close file.**                    | `file.close()`          | (Auto handled)                 | `fw.close()`                                      |
| **5. With block — auto closes file.** | `with open('f') as f:`  | `await fs.promises.readFile()` | `try-with-resources` (`try(FileReader fr=...){}`) |

---

## 🔁 LOOPS COMPARISON

| Index + Description                              | Python               | JavaScript             | Java                   |
| ------------------------------------------------ | -------------------- | ---------------------- | ---------------------- |
| **1. For loop — iterate over sequence.**         | `for i in list:`     | `for(let i of arr)`    | `for(int i: arr)`      |
| **2. While loop — repeat while condition true.** | `while condition:`   | `while(condition){}`   | `while(condition){}`   |
| **3. Range-based loop — numeric sequence.**      | `for i in range(5):` | `for(let i=0;i<5;i++)` | `for(int i=0;i<5;i++)` |
| **4. Break — exit loop early.**                  | `break`              | `break`                | `break`                |
| **5. Continue — skip current iteration.**        | `continue`           | `continue`             | `continue`             |

---

## 🔀 SWITCH / MATCH COMPARISON

| Index + Description                    | Python                       | JavaScript                       | Java                             |                       |
| -------------------------------------- | ---------------------------- | -------------------------------- | -------------------------------- | --------------------- |
| **1. Conditional branching by value.** | `match value:` / `case 'x':` | `switch(value){case 'x':break;}` | `switch(value){case 'x':break;}` |                       |
| **2. Default case — fallback option.** | `case _:`                    | `default:`                       | `default:`                       |                       |
| **3. Multi-value case.**               | `case ('a'                   | 'b'):`                           | `case 'a': case 'b':`            | `case 'a': case 'b':` |

---

## 🔍 REGEX (REGULAR EXPRESSIONS)

| Index + Description             | Python            | JavaScript              | Java                                        |
| ------------------------------- | ----------------- | ----------------------- | ------------------------------------------- |
| **1. Import regex module.**     | `import re`       | (Built-in: `/pattern/`) | `import java.util.regex.*;`                 |
| **2. Match pattern.**           | `re.match(p,t)`   | `/p/.test(t)`           | `Pattern.matches(p,t)`                      |
| **3. Search pattern anywhere.** | `re.search(p,t)`  | `t.match(/p/)`          | `Matcher m = Pattern.compile(p).matcher(t)` |
| **4. Find all matches.**        | `re.findall(p,t)` | `t.match(/p/g)`         | Use matcher with loop                       |
| **5. Replace pattern.**         | `re.sub(p,rep,t)` | `t.replace(/p/g,rep)`   | `t.replaceAll(p,rep)`                       |

---

## ⚠️ EXCEPTION HANDLING COMPARISON

| Index + Description                           | Python                         | JavaScript                     | Java                               |
| --------------------------------------------- | ------------------------------ | ------------------------------ | ---------------------------------- |
| **1. Try block — code that may throw error.** | `try:`                         | `try {}`                       | `try {}`                           |
| **2. Catch/Except — handle error.**           | `except Exception as e:`       | `catch(e){}`                   | `catch(Exception e){}`             |
| **3. Finally — always runs.**                 | `finally:`                     | `finally {}`                   | `finally {}`                       |
| **4. Raise/Throw exception.**                 | `raise ValueError("msg")`      | `throw new Error("msg")`       | `throw new Exception("msg")`       |
| **5. Custom exception class.**                | `class MyErr(Exception): pass` | `class MyErr extends Error {}` | `class MyErr extends Exception {}` |
| **6. Multiple exception handling.**           | `except (A,B):`                | `catch(e){}` with type check   | Multiple `catch` blocks            |
| **7. Assertion — validate condition.**        | `assert x>0`                   | `console.assert(x>0)`          | `assert x>0;`                      |
| **8. Try with resources (auto close).**       | `with open() as f:`            | N/A                            | `try(FileReader f=...){}`          |
| **9. Nested try.**                            | Supported                      | Supported                      | Supported                          |
| **10. Custom message print.**                 | `print(e)`                     | `console.error(e.message)`     | `e.getMessage()`                   |

---

## 🔡 ASCII & CHARACTER OPERATIONS

| Index + Description               | Python          | JavaScript                | Java                         |
| --------------------------------- | --------------- | ------------------------- | ---------------------------- |
| **1. Convert char → ASCII code.** | `ord('A')` → 65 | `'A'.charCodeAt(0)`       | `(int)'A'`                   |
| **2. Convert ASCII code → char.** | `chr(65)` → 'A' | `String.fromCharCode(65)` | `(char)65`                   |
| **3. Check character type.**      | `'A'.isalpha()` | `/[A-Z]/.test('A')`       | `Character.isLetter('A')`    |
| **4. Lowercase to uppercase.**    | `'a'.upper()`   | `'a'.toUpperCase()`       | `Character.toUpperCase('a')` |
| **5. Uppercase to lowercase.**    | `'A'.lower()`   | `'A'.toLowerCase()`       | `Character.toLowerCase('A')` |

---

