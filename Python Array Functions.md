# Python Array Functions — Creation, Input, Functions, and Examples

---

## 1. Array Creation

Python has no built-in array data type like Java or C, but we commonly use:

* **Lists** (dynamic, flexible)
* **array module arrays** (typed arrays, efficient)
* **NumPy arrays** (if NumPy installed — powerful for numeric operations)

Here, we’ll cover **`array` module arrays** and lists.

---

### Creation of Arrays Using `array` Module

```python
import array

# Syntax: array.array(typecode, initializer_list)
# typecode examples: 'i' for integers, 'f' for floats, 'u' for Unicode chars

arr = array.array('i', [1, 2, 3, 4])
```

---

### Creation of Lists (most common)

```python
lst = [1, 2, 3, 4]
```

---

## 2. Input of Arrays

* For lists: input can be taken as space-separated values and converted
* For `array.array`, similarly convert input to list, then to array

```python
# Input for list of integers
lst = list(map(int, input("Enter integers separated by space: ").split()))

# Input for array of integers
import array
arr = array.array('i', map(int, input("Enter integers separated by space: ").split()))
```

---

## 3. Array Functions (for `array` module)

| Function           | Definition                                            | Syntax                      |
| ------------------ | ----------------------------------------------------- | --------------------------- |
| `append(x)`        | Add element `x` to the end                            | `arr.append(x)`             |
| `insert(i, x)`     | Insert element `x` at index `i`                       | `arr.insert(i, x)`          |
| `pop([i])`         | Remove and return element at index `i` (default last) | `arr.pop()` or `arr.pop(i)` |
| `remove(x)`        | Remove first occurrence of value `x`                  | `arr.remove(x)`             |
| `index(x)`         | Return index of first occurrence of `x`               | `arr.index(x)`              |
| `count(x)`         | Count occurrences of `x`                              | `arr.count(x)`              |
| `reverse()`        | Reverse the array in place                            | `arr.reverse()`             |
| `buffer_info()`    | Returns tuple(address, length) of array               | `arr.buffer_info()`         |
| `typecode`         | The type code of array                                | `arr.typecode`              |
| `extend(iterable)` | Extend array by appending elements from iterable      | `arr.extend([5,6])`         |

---

## 4. Python List Functions (common array-like functions)

| Function           | Definition                                 | Syntax                      |
| ------------------ | ------------------------------------------ | --------------------------- |
| `append(x)`        | Add element at end                         | `lst.append(x)`             |
| `insert(i, x)`     | Insert element at position                 | `lst.insert(i, x)`          |
| `pop([i])`         | Remove and return element                  | `lst.pop()` or `lst.pop(i)` |
| `remove(x)`        | Remove first occurrence of value           | `lst.remove(x)`             |
| `index(x)`         | Return index of first occurrence           | `lst.index(x)`              |
| `count(x)`         | Count occurrences of `x`                   | `lst.count(x)`              |
| `reverse()`        | Reverse list                               | `lst.reverse()`             |
| `sort()`           | Sort list in ascending order               | `lst.sort()`                |
| `extend(iterable)` | Extend list by appending iterable elements | `lst.extend([7,8])`         |

---

## 5. Complete Program Demonstrating All These (using `array` module and lists)

```python
import array

# Creating an array of integers
arr = array.array('i', [1, 2, 3, 4])
print("Initial array:", arr)  # array('i', [1, 2, 3, 4])

# append(x)
arr.append(5)
print("After append(5):", arr)  # array('i', [1, 2, 3, 4, 5])

# insert(i, x)
arr.insert(2, 10)
print("After insert(2, 10):", arr)  # array('i', [1, 2, 10, 3, 4, 5])

# pop()
popped = arr.pop()
print("After pop():", arr)  # array('i', [1, 2, 10, 3, 4])
print("Popped element:", popped)  # 5

# pop(i)
popped_index = arr.pop(2)
print("After pop(2):", arr)  # array('i', [1, 2, 3, 4])
print("Popped element at index 2:", popped_index)  # 10

# remove(x)
arr.remove(3)
print("After remove(3):", arr)  # array('i', [1, 2, 4])

# index(x)
idx = arr.index(4)
print("Index of 4:", idx)  # 2

# count(x)
cnt = arr.count(2)
print("Count of 2:", cnt)  # 1

# reverse()
arr.reverse()
print("After reverse():", arr)  # array('i', [4, 2, 1])

# buffer_info()
buf_info = arr.buffer_info()
print("Buffer info:", buf_info)  # (address, length), e.g. (139734295371904, 3)

# typecode
print("Typecode:", arr.typecode)  # 'i'

# extend(iterable)
arr.extend([7, 8])
print("After extend([7, 8]):", arr)  # array('i', [4, 2, 1, 7, 8])

print("\n--- List examples ---")

# List creation and input
lst = [1, 2, 3, 4]
print("Initial list:", lst)  # [1, 2, 3, 4]

# append(x)
lst.append(5)
print("After append(5):", lst)  # [1, 2, 3, 4, 5]

# insert(i, x)
lst.insert(2, 10)
print("After insert(2, 10):", lst)  # [1, 2, 10, 3, 4, 5]

# pop()
popped_lst = lst.pop()
print("After pop():", lst)  # [1, 2, 10, 3, 4]
print("Popped element:", popped_lst)  # 5

# pop(i)
popped_lst_i = lst.pop(2)
print("After pop(2):", lst)  # [1, 2, 3, 4]
print("Popped element at index 2:", popped_lst_i)  # 10

# remove(x)
lst.remove(3)
print("After remove(3):", lst)  # [1, 2, 4]

# index(x)
index_lst = lst.index(4)
print("Index of 4:", index_lst)  # 2

# count(x)
count_lst = lst.count(2)
print("Count of 2:", count_lst)  # 1

# reverse()
lst.reverse()
print("After reverse():", lst)  # [4, 2, 1]

# sort()
lst.sort()
print("After sort():", lst)  # [1, 2, 4]

# extend(iterable)
lst.extend([7, 8])
print("After extend([7, 8]):", lst)  # [1, 2, 4, 7, 8]
