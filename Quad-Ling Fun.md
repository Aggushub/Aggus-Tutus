# 🧠✨ The Ultimate Cross-Language Function CheatSheet!
Because remembering every syntax is harder than remembering your Wi-Fi password 😅

Welcome to the Python 🐍 | JavaScript 💻 | Java ☕ | C# 🎮 Trilingual Function Bible — a single mega-table that bridges the gap between “Wait, how do I do this in JS again?” and “Oh right, that’s .length() not .len()!”

From Strings to OOP, Loops to Regex, Exceptions to ASCII, this doc covers it all — cleanly, clearly, and with enough caffeine energy to survive your next coding interview. ☕⚡

---

## 🧵 **1. STRING FUNCTIONS TABLE**

| Index + Name       | Description                | Python              | Java                    | JavaScript          | C#                      |
| ------------------ | -------------------------- | ------------------- | ----------------------- | ------------------- | ----------------------- |
| **1. Length**      | Count characters           | `len(s)`            | `s.length()`            | `s.length`          | `s.Length`              |
| **2. Uppercase**   | Convert to capital letters | `s.upper()`         | `s.toUpperCase()`       | `s.toUpperCase()`   | `s.ToUpper()`           |
| **3. Lowercase**   | Convert to lowercase       | `s.lower()`         | `s.toLowerCase()`       | `s.toLowerCase()`   | `s.ToLower()`           |
| **4. Trim**        | Remove side spaces         | `s.strip()`         | `s.trim()`              | `s.trim()`          | `s.Trim()`              |
| **5. Replace**     | Replace substring          | `s.replace(a,b)`    | `s.replace(a,b)`        | `s.replace(a,b)`    | `s.Replace(a,b)`        |
| **6. Split**       | Break into list            | `s.split(",")`      | `s.split(",")`          | `s.split(",")`      | `s.Split(",")`          |
| **7. Join**        | Combine list to string     | `' '.join(lst)`     | `String.join(" ", lst)` | `arr.join(" ")`     | `string.Join(" ", arr)` |
| **8. Find index**  | Find substring position    | `s.find("x")`       | `s.indexOf("x")`        | `s.indexOf("x")`    | `s.IndexOf("x")`        |
| **9. Starts with** | Check prefix               | `s.startswith("x")` | `s.startsWith("x")`     | `s.startsWith("x")` | `s.StartsWith("x")`     |
| **10. Ends with**  | Check suffix               | `s.endswith("x")`   | `s.endsWith("x")`       | `s.endsWith("x")`   | `s.EndsWith("x")`       |

---

# 🔢 **2. NUMBER FUNCTIONS TABLE**

| Index + Name           | Description        | Python          | Java                     | JavaScript      | C#                |
| ---------------------- | ------------------ | --------------- | ------------------------ | --------------- | ----------------- |
| **11. Absolute**       | Positive magnitude | `abs(x)`        | `Math.abs(x)`            | `Math.abs(x)`   | `Math.Abs(x)`     |
| **12. Round**          | Round to nearest   | `round(x)`      | `Math.round(x)`          | `Math.round(x)` | `Math.Round(x)`   |
| **13. Power**          | x raised to y      | `pow(x,y)`      | `Math.pow(x,y)`          | `Math.pow(x,y)` | `Math.Pow(x,y)`   |
| **14. Min**            | Smallest number    | `min(a,b)`      | `Math.min(a,b)`          | `Math.min(a,b)` | `Math.Min(a,b)`   |
| **15. Max**            | Largest number     | `max(a,b)`      | `Math.max(a,b)`          | `Math.max(a,b)` | `Math.Max(a,b)`   |
| **16. Convert to int** | String → int       | `int(s)`        | `Integer.parseInt(s)`    | `parseInt(s)`   | `int.Parse(s)`    |
| **17. Sum list**       | Add all elements   | `sum(lst)`      | `Arrays.stream(a).sum()` | `arr.reduce()`  | `arr.Sum()`       |
| **18. Square root**    | √x                 | `math.sqrt(x)`  | `Math.sqrt(x)`           | `Math.sqrt(x)`  | `Math.Sqrt(x)`    |
| **19. Floor**          | Round down         | `math.floor(x)` | `Math.floor(x)`          | `Math.floor(x)` | `Math.Floor(x)`   |
| **20. Ceil**           | Round up           | `math.ceil(x)`  | `Math.ceil(x)`           | `Math.ceil(x)`  | `Math.Ceiling(x)` |

---

# 🧮 **3. LIST / ARRAY FUNCTIONS TABLE**

| Index + Name          | Description            | Python             | Java                     | JavaScript      | C#                 |
| --------------------- | ---------------------- | ------------------ | ------------------------ | --------------- | ------------------ |
| **21. Length**        | Count items            | `len(a)`           | `a.length`               | `a.length`      | `a.Length`         |
| **22. Add**           | Insert at end          | `a.append(x)`      | `list.add(x)`            | `a.push(x)`     | `list.Add(x)`      |
| **23. Pop**           | Remove last            | `a.pop()`          | `list.remove(idx)`       | `a.pop()`       | `list.RemoveAt(i)` |
| **24. Sort**          | Ascending order        | `a.sort()`         | `Collections.sort(a)`    | `a.sort()`      | `list.Sort()`      |
| **25. Reverse**       | Reverse order          | `a.reverse()`      | `Collections.reverse(a)` | `a.reverse()`   | `list.Reverse()`   |
| **26. Index of**      | Position of element    | `a.index(x)`       | `list.indexOf(x)`        | `a.indexOf(x)`  | `list.IndexOf(x)`  |
| **27. Contains**      | Check membership       | `x in a`           | `list.contains(x)`       | `a.includes(x)` | `list.Contains(x)` |
| **28. Remove value**  | Remove specific value  | `a.remove(x)`      | `list.remove(x)`         | `a.splice(i,1)` | `list.Remove(x)`   |
| **29. Sum list**      | Add elements           | `sum(a)`           | `stream.sum()`           | `reduce()`      | `a.Sum()`          |
| **30. Map/Transform** | Apply function to each | `[x*x for x in a]` | `stream.map()`           | `a.map()`       | `a.Select(f)`      |

---

# 🧩 **4. SET FUNCTIONS TABLE**

| Index + Name         | Description            | Python        | Java               | JavaScript      | C#                   |     
| -------------------- | ---------------------- | ------------- | ------------------ | --------------- | -------------------- | 
| **31. Create set**   | Make unique collection | `{1,2}`       | `new HashSet<>()`  | `new Set()`     | `new HashSet<int>()` |               
| **32. Add element**  | Insert value           | `s.add(x)`    | `set.add(x)`       | `set.add(x)`    | `set.Add(x)`         |               
| **33. Remove**       | Delete element         | `s.remove(x)` | `set.remove(x)`    | `set.delete(x)` | `set.Remove(x)`      |               
| **34. Contains**     | Check existence        | `x in s`      | `set.contains(x)`  | `set.has(x)`    | `set.Contains(x)`    |               
| **35. Union**        | Combine two sets       | `s1.union(s2)`| `addAll()`         | spread + Set    | `UnionWith()`        |
| **36. Intersection** | Common elements        | `s1 & s2`     | `retainAll()`      | filter          | `IntersectWith()`    |              
| **37. Difference**   | Subtract sets          | `s1 - s2`     | `removeAll()`      | filter          | `ExceptWith()`       |               
| **38. Clear**        | Empty set              | `s.clear()`   | `set.clear()`      | `set.clear()`   | `set.Clear()`        |               
| **39. Size**         | Count items            | `len(s)`      | `set.size()`       | `set.size`      | `set.Count`          |               
| **40. To list**      | Convert to list        | `list(s)`     | `new ArrayList(s)` | `[...set]`      | `s.ToList()`         |               

---

# 🗂 **5. DICTIONARY / MAP TABLE**

| Index + Name        | Description       | Python                 | Java                | JavaScript            | C#                          |
| ------------------- | ----------------- | ---------------------- | ------------------- | --------------------- | --------------------------- |
| **41. Create map**  | Key–value store   | `{'a':1}`              | `new HashMap<>()`   | `{a:1}` / `new Map()` | `new Dictionary<>()`        |
| **42. Get value**   | Access item       | `d['a']`               | `map.get("a")`      | `obj.a` / `map.get()` | `dict["a"]`                 |
| **43. Set value**   | Insert/overwrite  | `d['b']=2`             | `map.put()`         | `obj.b=2`             | `dict["b"]=2`               |
| **44. Remove key**  | Delete entry      | `d.pop(k)`             | `map.remove(k)`     | `delete obj.a`        | `dict.Remove(k)`            |
| **45. Check key**   | Exists?           | `'a' in d`             | `map.containsKey()` | `'a' in obj`          | `dict.ContainsKey()`        |
| **46. Keys**        | All keys          | `d.keys()`             | `map.keySet()`      | `Object.keys(obj)`    | `dict.Keys`                 |
| **47. Values**      | All values        | `d.values()`           | `map.values()`      | `Object.values()`     | `dict.Values`               |
| **48. Loop items**  | Iterate key-value | `for k,v in d.items()` | `entrySet()`        | `for..of map`         | `foreach(var kv in dict)`   |
| **49. Get default** | Return fallback   | `d.get(k,0)`           | `getOrDefault()`    | `obj.a ?? 0`          | `dict.GetValueOrDefault(k)` |
| **50. Clear**       | Remove all        | `d.clear()`            | `map.clear()`       | `map.clear()`         | `dict.Clear()`              |

---

# 🧱 **6. OOP TABLE**

| Index + Name             | Description           | Python          | Java         | JavaScript      | C#            |
| ------------------------ | --------------------- | --------------- | ------------ | --------------- | ------------- |
| **51. Class definition** | Create blueprint      | `class A:`      | `class A {}` | `class A {}`    | `class A {}`  |
| **52. Constructor**      | Initialize object     | `__init__`      | `A()`        | `constructor()` | `A()`         |
| **53. Object create**    | Make instance         | `A()`           | `new A()`    | `new A()`       | `new A()`     |
| **54. Inheritance**      | Extend parent         | `class B(A)`    | `extends`    | `extends`       | `class B : A` |
| **55. Override method**  | Replace parent method | redefine        | `@Override`  | redefine        | `override`    |
| **56. Encapsulation**    | Hide data             | `_var`          | `private`    | `#var`          | `private`     |
| **57. Static method**    | Class-level method    | `@staticmethod` | `static`     | `static`        | `static`      |
| **58. Getter**           | Read value            | `@property`     | `get()`      | `get()`         | `get;`        |
| **59. Setter**           | Write value           | `@value.setter` | `set()`      | `set()`         | `set;`        |

---

# 📁 **7. FILE HANDLING TABLE**

| Index + Name       | Desc         | Python     | Java             | JS                  | C#                    |
| ------------------ | ------------ | ---------- | ---------------- | ------------------- | --------------------- |
| **60. Open file**  | Read file    | `open()`   | `FileReader`     | `fs.readFileSync()` | `File.ReadAllText()`  |
| **61. Read file**  | Read content | `.read()`  | `BufferedReader` | `.readFileSync()`   | `File.ReadAllText()`  |
| **62. Write file** | Write text   | `.write()` | `FileWriter`     | `writeFileSync()`   | `File.WriteAllText()` |
| **63. Close file** | Close stream | `.close()` | `.close()`       | auto                | auto                  |

---

# 🔁 **8. LOOPS TABLE**

| Index              | Description          | Python             | Java               | JavaScript          | C#                      |
| ------------------ | -------------------- | ------------------ | ------------------ | ------------------- | ----------------------- |
| **64. For loop**   | Index-based          | `for i in range()` | `for(int i...)`    | `for(let i...)`     | `for(int i...)`         |
| **65. For-each**   | Loop items           | `for x in lst`     | `for(Type x:list)` | `for(let x of arr)` | `foreach(var x in lst)` |
| **66. While loop** | Loop until condition | `while(cond)`      | `while(cond)`      | `while(cond)`       | `while(cond)`           |
| **67. Break**      | Exit loop            | `break`            | `break`            | `break`             | `break`                 |
| **68. Continue**   | Skip iteration       | `continue`         | `continue`         | `continue`          | `continue`              |

---

# 🔀 **9. SWITCH / MATCH TABLE**

| Index           | Desc         | Python     | Java        | JS          | C#          |
| --------------- | ------------ | ---------- | ----------- | ----------- | ----------- |
| **69. Switch**  | Multi-branch | `match x:` | `switch(x)` | `switch(x)` | `switch(x)` |
| **70. Case**    | Match value  | `case 1:`  | `case 1:`   | `case 1:`   | `case 1:`   |
| **71. Default** | Fallback     | `_:`       | `default:`  | `default:`  | `default:`  |

---

# 🔍 **10. REGEX TABLE**

| Index            | Description        | Python         | Java                | JS             | C#                |
| ---------------- | ------------------ | -------------- | ------------------- | -------------- | ----------------- |
| **72. Match**    | First match        | `re.match()`   | `Pattern.matcher()` | `str.match()`  | `Regex.Match()`   |
| **73. Search**   | Find anywhere      | `re.search()`  | `matcher.find()`    | `regex.test()` | `Regex.IsMatch()` |
| **74. Find all** | List all matches   | `re.findall()` | `matcher.group()`   | `matchAll()`   | `Regex.Matches()` |
| **75. Replace**  | Substitute pattern | `re.sub()`     | `replaceAll()`      | `replace()`    | `Regex.Replace()` |

---

# ⚠️ **11. EXCEPTION HANDLING TABLE**

| Index                  | Desc            | Python     | Java        | JS          | C#          |
| ---------------------- | --------------- | ---------- | ----------- | ----------- | ----------- |
| **76. Try**            | Test code       | `try:`     | `try{}`     | `try{}`     | `try{}`     |
| **77. Except / Catch** | Handle error    | `except:`  | `catch(){}` | `catch(){}` | `catch{}`   |
| **78. Finally**        | Always executes | `finally:` | `finally{}` | `finally{}` | `finally{}` |
| **79. Throw**          | Raise error     | `raise`    | `throw`     | `throw`     | `throw`     |

---

# 🔡 **12. ASCII TABLE**

| Index                | Description          | Python     | Java       | JS                        | C#         |
| -------------------- | -------------------- | ---------- | ---------- | ------------------------- | ---------- |
| **80. Char → ASCII** | Get ASCII code       | `ord('A')` | `int('A')` | `'A'.charCodeAt(0)`       | `(int)'A'` |
| **81. ASCII → Char** | Convert code to char | `chr(65)`  | `(char)65` | `String.fromCharCode(65)` | `(char)65` |

---
