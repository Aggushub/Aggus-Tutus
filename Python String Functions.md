## Python String Functions with Definitions, Syntax, and Examples

### 1. **len()**

* **Definition**: Returns the length of a string.
* **Syntax**: `len(string)`

### 2. **lower()**

* **Definition**: Converts all characters to lowercase.
* **Syntax**: `string.lower()`

### 3. **upper()**

* **Definition**: Converts all characters to uppercase.
* **Syntax**: `string.upper()`

### 4. **capitalize()**

* **Definition**: Capitalizes the first character.
* **Syntax**: `string.capitalize()`

### 5. **title()**

* **Definition**: Capitalizes the first character of each word.
* **Syntax**: `string.title()`

### 6. **strip()**

* **Definition**: Removes leading and trailing whitespace.
* **Syntax**: `string.strip()`

### 7. **lstrip()**

* **Definition**: Removes leading whitespace.
* **Syntax**: `string.lstrip()`

### 8. **rstrip()**

* **Definition**: Removes trailing whitespace.
* **Syntax**: `string.rstrip()`

### 9. **replace()**

* **Definition**: Replaces a substring with another.
* **Syntax**: `string.replace(old, new)`

### 10. **find()**

* **Definition**: Returns the first index of a substring or -1.
* **Syntax**: `string.find(sub)`

### 11. **index()**

* **Definition**: Returns the index of a substring, raises error if not found.
* **Syntax**: `string.index(sub)`

### 12. **split()**

* **Definition**: Splits string into a list.
* **Syntax**: `string.split(sep)`

### 13. **join()**

* **Definition**: Joins elements of a list into a string.
* **Syntax**: `sep.join(list)`

### 14. **count()**

* **Definition**: Returns number of occurrences of a substring.
* **Syntax**: `string.count(sub)`

### 15. **startswith()**

* **Definition**: Checks if string starts with substring.
* **Syntax**: `string.startswith(sub)`

### 16. **endswith()**

* **Definition**: Checks if string ends with substring.
* **Syntax**: `string.endswith(sub)`

### 17. **isalpha()**

* **Definition**: Checks if all characters are alphabetic.
* **Syntax**: `string.isalpha()`

### 18. **isdigit()**

* **Definition**: Checks if all characters are digits.
* **Syntax**: `string.isdigit()`

### 19. **isalnum()**

* **Definition**: Checks if all characters are alphanumeric.
* **Syntax**: `string.isalnum()`

### 20. **isspace()**

* **Definition**: Checks if all characters are whitespace.
* **Syntax**: `string.isspace()`

### Complete Program Demonstrating All

```python
s = "  Hello World  "

print(len(s))  # 15
print(s.lower())  # "  hello world  "
print(s.upper())  # "  HELLO WORLD  "
print(s.capitalize())  # "  hello world  "
print(s.title())  # "  Hello World  "
print(s.strip())  # "Hello World"
print(s.lstrip())  # "Hello World  "
print(s.rstrip())  # "  Hello World"
print(s.replace("World", "Python"))  # "  Hello Python  "
print(s.find("World"))  # 8
print(s.index("World"))  # 8
print(s.split())  # ['Hello', 'World']
print("-".join(["Python", "Rocks"]))  # "Python-Rocks"
print(s.count("l"))  # 3
print(s.startswith("  H"))  # True
print(s.endswith("  "))  # True
print("Hello".isalpha())  # True
print("123".isdigit())  # True
print("Hello123".isalnum())  # True
print("   ".isspace())  # True
```

Each output is provided as a comment. Run this in any Python interpreter to test them all!
