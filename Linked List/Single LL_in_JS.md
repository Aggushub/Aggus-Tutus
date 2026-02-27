
# 🧠 Learning Linked Lists in JavaScript  
### 📅 Date: 23/06/2025  
### 📚 Course: Udemy – Mastering Data Structures with JavaScript

---

## 🚀 Introduction

On 23rd June 2025, I explored one of the core fundamentals of Data Structures — **Linked Lists** — using **JavaScript** as part of a Udemy course. This hands-on journey helped me understand how nodes work, how to connect them dynamically, and how to perform various operations on them like insertion, deletion, searching, and traversal.

This file documents my learning progress, includes code, and a detailed breakdown of all key operations I implemented from scratch.

---

## 🧩 Summary of Linked List Operations

| Operation       | Description                                                                 | Example                                           |
|----------------|-----------------------------------------------------------------------------|---------------------------------------------------|
| `append(val)`   | Adds a node to the end of the list                                          | `list.append(10)` → Adds `10` at tail             |
| `prepend(val)`  | Adds a node to the beginning of the list                                    | `list.prepend(20)` → Adds `20` at head            |
| `insert(val, i)`| Inserts a node at a given index (or at end if `-1` or last index)           | `list.insert(30, 2)`                              |
| `traverse()`    | Prints all elements in order                                                | `list.traverse()` → logs all node values          |
| `search(val)`   | Returns `true` if value exists in list, else `false`                        | `list.search(10)`                                 |
| `get(i)`        | Gets the node at the given index                                            | `list.get(1)` → returns Node at index 1           |
| `set(i, val)`   | Updates the value of the node at the given index                           | `list.set(2, 99)` → sets index 2 value to 99      |
| `pop()`         | Removes and returns the last node                                           | `list.pop()` → removes tail                       |
| `popFirst()`    | Removes and returns the first node                                          | `list.popFirst()`                                 |
| `remove(i)`     | Removes a node at a specified index                                         | `list.remove(2)`                                  |
| `deleteAll()`   | Clears the entire list                                                      | `list.deleteAll()`                                |
| `toString()`    | Returns a string representation like `10->20->30`                          | `list.toString()`                                 |

---

## 📘 Code Implementation (JavaScript)

```js
// Node class representing each element in the list
class Node {
    constructor(value) {
        this.value = value;
        this.next = null;
    }
}

// LinkedList class
class LinkedList {
    constructor() {
        this.head = null;
        this.tail = null;
        this.length = 0;
    }

    // Add to end
    append(value) {
        const newNode = new Node(value);
        if (this.length === 0) {
            this.head = newNode;
            this.tail = newNode;
        } else {
            this.tail.next = newNode;
            this.tail = newNode;
        }
        this.length++;
    }

    // Add to beginning
    prepend(value) {
        const newNode = new Node(value);
        if (this.length === 0) {
            this.head = newNode;
            this.tail = newNode;
        } else {
            newNode.next = this.head;
            this.head = newNode;
        }
        this.length++;
    }

    // Insert at specific index
    insert(value, index) {
        const newNode = new Node(value);
        if (index < -1 || index > this.length) {
            return false;
        } else if (this.length === 0 || index === 0) {
            this.prepend(value);
        } else if (index === -1 || index === this.length) {
            this.append(value);
        } else {
            let tempNode = this.head;
            for (let i = 0; i < index - 1; i++) {
                tempNode = tempNode.next;
            }
            newNode.next = tempNode.next;
            tempNode.next = newNode;
            this.length++;
        }

        return this.toString();
    }

    // Print all values
    traverse() {
        let current = this.head;
        while (current !== null) {
            console.log(current.value);
            current = current.next;
        }
    }

    // Search for a value
    search(target) {
        let current = this.head;
        while (current !== null) {
            if (current.value === target) {
                return true;
            }
            current = current.next;
        }
        return false;
    }

    // Remove node at given index
    remove(index) {
        if (index === -1 || index === this.length - 1) {
            return this.pop();
        } else if (index === 0) {
            return this.popFirst();
        } else if (index >= this.length || index < -1) {
            return null;
        } else {
            const prevNode = this.get(index - 1);
            const poppedNode = prevNode.next;
            prevNode.next = poppedNode.next;
            poppedNode.next = null;
            this.length--;
            return poppedNode;
        }
    }

    // Get node at index
    get(index) {
        if (index === -1) return this.tail;
        if (index < 0 || index >= this.length) return null;

        let current = this.head;
        for (let i = 0; i < index; i++) {
            current = current.next;
        }
        return current;
    }

    // Set value at index
    set(index, value) {
        const node = this.get(index);
        if (node) {
            node.value = value;
            return true;
        }
        return false;
    }

    // Remove first node
    popFirst() {
        if (this.length === 0) return false;

        const poppedNode = this.head;
        if (this.length === 1) {
            this.head = null;
            this.tail = null;
        } else {
            this.head = this.head.next;
            poppedNode.next = null;
        }
        this.length--;
        return poppedNode;
    }

    // Clear the list
    deleteAll() {
        this.head = null;
        this.tail = null;
        this.length = 0;
    }

    // Remove last node
    pop() {
        if (this.length === 0) return false;

        let poppedNode = this.tail;

        if (this.length === 1) {
            this.head = null;
            this.tail = null;
        } else {
            let temp = this.head;
            while (temp.next !== this.tail) {
                temp = temp.next;
            }
            this.tail = temp;
            this.tail.next = null;
        }

        this.length--;
        return poppedNode;
    }

    // Convert to string representation
    toString() {
        let tempNode = this.head;
        let result = '';
        while (tempNode !== null) {
            result += tempNode.value;
            if (tempNode.next !== null) {
                result += '->';
            }
            tempNode = tempNode.next;
        }
        return result;
    }
}



// Testing the linked list

let newLinkedList = new LinkedList();
newLinkedList.append(10);
newLinkedList.append(20);
newLinkedList.append(30);
newLinkedList.prepend(50);
newLinkedList.insert(40, 3);
newLinkedList.traverse();              // 50 10 20 40 30
console.log(newLinkedList.search(20)); // true
console.log(newLinkedList.get(2));     // Node { value: 20, next: Node }
console.log(newLinkedList.set(1, 40)); // true
console.log(newLinkedList.popFirst()); // Node with value 50 removed
console.log(newLinkedList.pop());      // Node with value 30 removed
console.log(newLinkedList.remove(2));  // Node with value 40 removed
newLinkedList.deleteAll();             // List is now empty






let newLinkedList = new LinkedList();

newLinkedList.append(10);
newLinkedList.append(20);
newLinkedList.append(30);
// List: 10 -> 20 -> 30

newLinkedList.prepend(50);
// List: 50 -> 10 -> 20 -> 30

newLinkedList.insert(40, 3); // Insert 40 at index 3
// List: 50 -> 10 -> 20 -> 40 -> 30

newLinkedList.traverse();
// Output:
// 50
// 10
// 20
// 40
// 30

console.log(newLinkedList.search(20)); // true

console.log(newLinkedList.get(2)); // Node { value: 20, next: Node { value: 40, next: [Node] } }

console.log(newLinkedList.set(1, 40)); // true
// Now list: 50 -> 40 -> 20 -> 40 -> 30

console.log(newLinkedList.popFirst()); // Node with value 50 removed
// List: 40 -> 20 -> 40 -> 30

console.log(newLinkedList.pop()); // Node with value 30 removed
// List: 40 -> 20 -> 40

console.log(newLinkedList.remove(2)); // Node with value 40 removed
// List: 40 -> 20

newLinkedList.deleteAll();
// List is now empty

console.log(newLinkedList.toString()); // ''

/*
Final Output Comments from Operations:
traverse():
50
10
20
40
30

search(20): true

get(2): Node { value: 20, next: Node { value: 40, next: [Node] } }

set(1, 40): true

popFirst(): Node { value: 50, next: null }

pop(): Node { value: 30, next: null }

remove(2): Node { value: 40, next: null }

toString(): ''
*/

````

---

## 🙌 My Learning Takeaway

This was a strong reinforcement of how data is structured, stored, and accessed in memory using linked nodes. Understanding pointer manipulation and memory-safe operations like `pop()` and `insert()` has strengthened my understanding of dynamic data structures — an essential skill for interviews and real-world applications.
