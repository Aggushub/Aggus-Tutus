### ✅ **Java Code: Linked List with All Operations + Definitions**

```java
class LinkedList {
    // Inner class representing a node in the list
    class Node {
        int data;
        Node next;

        Node(int d) {
            data = d;
            next = null;
        }
    }

    // Head pointer of the linked list
    private Node head = null;

    // ➤ 1. Insert at End
    // Adds a new node with given data at the end of the list
    public void insertAtEnd(int data) {
        Node newNode = new Node(data);
        if (head == null) {
            head = newNode;
            return;
        }
        Node curr = head;
        while (curr.next != null) {
            curr = curr.next;
        }
        curr.next = newNode;
    }

    // ➤ 2. Insert at Beginning
    // Adds a new node at the start of the list
    public void insertAtBeginning(int data) {
        Node newNode = new Node(data);
        newNode.next = head;
        head = newNode;
    }

    // ➤ 3. Insert at Specific Position (0-based index)
    // Inserts a node at a specific index in the list
    public void insertAtPosition(int index, int data) {
        if (index == 0) {
            insertAtBeginning(data);
            return;
        }

        Node newNode = new Node(data);
        Node curr = head;
        for (int i = 0; curr != null && i < index - 1; i++) {
            curr = curr.next;
        }

        if (curr == null) {
            System.out.println("Position out of bounds.");
            return;
        }

        newNode.next = curr.next;
        curr.next = newNode;
    }

    // ➤ 4. Delete by Value
    // Deletes the first node that contains the specified value
    public void deleteByValue(int data) {
        if (head == null) return;

        if (head.data == data) {
            head = head.next;
            return;
        }

        Node curr = head;
        while (curr.next != null && curr.next.data != data) {
            curr = curr.next;
        }

        if (curr.next == null) {
            System.out.println("Value not found.");
        } else {
            curr.next = curr.next.next;
        }
    }

    // ➤ 5. Delete by Position
    // Deletes the node at a specific position (index)
    public void deleteAtPosition(int index) {
        if (head == null) return;

        if (index == 0) {
            head = head.next;
            return;
        }

        Node curr = head;
        for (int i = 0; curr != null && i < index - 1; i++) {
            curr = curr.next;
        }

        if (curr == null || curr.next == null) {
            System.out.println("Position out of bounds.");
            return;
        }

        curr.next = curr.next.next;
    }

    // ➤ 6. Search
    // Searches for a specific value in the list
    public boolean search(int key) {
        Node curr = head;
        while (curr != null) {
            if (curr.data == key) return true;
            curr = curr.next;
        }
        return false;
    }

    // ➤ 7. Display
    // Prints all elements in the list
    public void display() {
        Node curr = head;
        while (curr != null) {
            System.out.print(curr.data + " -> ");
            curr = curr.next;
        }
        System.out.println("NULL");
    }

    // ➤ 8. Get Size
    // Returns the number of nodes in the list
    public int getSize() {
        int count = 0;
        Node curr = head;
        while (curr != null) {
            count++;
            curr = curr.next;
        }
        return count;
    }

    // ➤ 9. Main method to test all operations
    public static void main(String[] args) {
        LinkedList list = new LinkedList();

        System.out.println("Inserting at end:");
        list.insertAtEnd(10);
        list.insertAtEnd(20);

        System.out.println("Inserting at beginning:");
        list.insertAtBeginning(5);

        System.out.println("Inserting at position 1:");
        list.insertAtPosition(1, 15); // Insert 15 at position 1

        list.display();  // 5 -> 15 -> 10 -> 20 -> NULL

        System.out.println("Deleting value 10:");
        list.deleteByValue(10);
        list.display();  // 5 -> 15 -> 20 -> NULL

        System.out.println("Deleting at position 0:");
        list.deleteAtPosition(0);
        list.display();  // 15 -> 20 -> NULL

        System.out.println("Searching for 20: " + list.search(20)); // true
        System.out.println("Size of list: " + list.getSize());       // 2
    }
}
```

---

### 💡 Summary Table of Operations

| Operation           | Method Name           | Description                             |
| ------------------- | --------------------- | --------------------------------------- |
| Insert at End       | `insertAtEnd()`       | Add node at the tail of the list        |
| Insert at Beginning | `insertAtBeginning()` | Add node at the start of the list       |
| Insert at Position  | `insertAtPosition()`  | Add node at any index                   |
| Delete by Value     | `deleteByValue()`     | Remove first occurrence of a value      |
| Delete by Position  | `deleteAtPosition()`  | Remove node at a specific index         |
| Search              | `search()`            | Find whether a value exists in the list |
| Display             | `display()`           | Print the full list                     |
| Get Size            | `getSize()`           | Count the number of nodes in the list   |

---

