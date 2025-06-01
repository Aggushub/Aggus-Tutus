## ✅ Linked List in Python with All Operations & Definitions

```python
# Node class: represents each element in the list
class Node:
    def __init__(self, data):
        self.data = data  # Holds the data
        self.next = None  # Points to the next node

# LinkedList class with all operations
class LinkedList:
    def __init__(self):
        self.head = None  # Initially the list is empty

    # ➤ 1. Insert at End
    # Adds a new node to the end of the list
    def insert_at_end(self, data):
        new_node = Node(data)
        if not self.head:
            self.head = new_node
            return
        temp = self.head
        while temp.next:
            temp = temp.next
        temp.next = new_node

    # ➤ 2. Insert at Beginning
    # Adds a new node at the start of the list
    def insert_at_beginning(self, data):
        new_node = Node(data)
        new_node.next = self.head
        self.head = new_node

    # ➤ 3. Insert at a Specific Position (0-based)
    # Inserts a node at a given position in the list
    def insert_at_position(self, index, data):
        if index == 0:
            self.insert_at_beginning(data)
            return
        new_node = Node(data)
        temp = self.head
        for _ in range(index - 1):
            if temp is None:
                print("Position out of bounds.")
                return
            temp = temp.next
        new_node.next = temp.next
        temp.next = new_node

    # ➤ 4. Delete by Value
    # Deletes the first node containing the given value
    def delete_by_value(self, value):
        temp = self.head
        prev = None
        while temp and temp.data != value:
            prev = temp
            temp = temp.next
        if temp is None:
            print("Value not found.")
            return
        if prev is None:
            self.head = temp.next
        else:
            prev.next = temp.next

    # ➤ 5. Delete by Position
    # Deletes the node at a given index
    def delete_at_position(self, index):
        if self.head is None:
            print("List is empty.")
            return
        temp = self.head
        if index == 0:
            self.head = temp.next
            return
        prev = None
        for _ in range(index):
            prev = temp
            temp = temp.next
            if temp is None:
                print("Position out of bounds.")
                return
        prev.next = temp.next

    # ➤ 6. Search
    # Checks if a value exists in the list
    def search(self, key):
        temp = self.head
        while temp:
            if temp.data == key:
                return True
            temp = temp.next
        return False

    # ➤ 7. Display
    # Prints all elements in the list
    def display(self):
        temp = self.head
        while temp:
            print(temp.data, end=" -> ")
            temp = temp.next
        print("None")

    # ➤ 8. Get Size
    # Returns the total number of nodes
    def get_size(self):
        count = 0
        temp = self.head
        while temp:
            count += 1
            temp = temp.next
        return count

# ➤ 9. Example usage
if __name__ == "__main__":
    ll = LinkedList()

    print("Inserting at end:")
    ll.insert_at_end(10)
    ll.insert_at_end(20)

    print("Inserting at beginning:")
    ll.insert_at_beginning(5)

    print("Inserting at position 1:")
    ll.insert_at_position(1, 15)

    print("Linked List:")
    ll.display()  # Output: 5 -> 15 -> 10 -> 20 -> None

    print("Deleting value 10:")
    ll.delete_by_value(10)
    ll.display()  # Output: 5 -> 15 -> 20 -> None

    print("Deleting at position 0:")
    ll.delete_at_position(0)
    ll.display()  # Output: 15 -> 20 -> None

    print("Searching for 20:", ll.search(20))  # Output: True
    print("Size of the list:", ll.get_size())  # Output: 2
```

---

### 📌 Summary of Operations

| Operation           | Method Name             | Description                     |
| ------------------- | ----------------------- | ------------------------------- |
| Insert at End       | `insert_at_end()`       | Add a node at the end           |
| Insert at Beginning | `insert_at_beginning()` | Add a node at the start         |
| Insert at Position  | `insert_at_position()`  | Insert node at given index      |
| Delete by Value     | `delete_by_value()`     | Remove node by value            |
| Delete by Position  | `delete_at_position()`  | Remove node at index            |
| Search              | `search()`              | Check if a value is in the list |
| Display             | `display()`             | Print all values in the list    |
| Get Size            | `get_size()`            | Count the number of nodes       |

---
