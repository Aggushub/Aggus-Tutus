## ✅ Linked List in C with All Operations & Definitions

```c
#include <stdio.h>
#include <stdlib.h>

// Define a node of the linked list
struct Node {
    int data;
    struct Node* next;
};

struct Node* head = NULL; // Global head pointer

// ➤ 1. Insert at the End
// Adds a node to the end of the list
void insertAtEnd(int value) {
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = value;
    newNode->next = NULL;

    if (head == NULL) {
        head = newNode;
        return;
    }

    struct Node* temp = head;
    while (temp->next != NULL)
        temp = temp->next;

    temp->next = newNode;
}

// ➤ 2. Insert at the Beginning
// Adds a node at the start of the list
void insertAtBeginning(int value) {
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = value;
    newNode->next = head;
    head = newNode;
}

// ➤ 3. Insert at a Specific Position
// Inserts a node at the given index (0-based)
void insertAtPosition(int pos, int value) {
    if (pos == 0) {
        insertAtBeginning(value);
        return;
    }

    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = value;

    struct Node* temp = head;
    for (int i = 0; temp != NULL && i < pos - 1; i++) {
        temp = temp->next;
    }

    if (temp == NULL) {
        printf("Position out of bounds.\n");
        free(newNode);
        return;
    }

    newNode->next = temp->next;
    temp->next = newNode;
}

// ➤ 4. Delete by Value
// Removes the first node that contains the given value
void deleteByValue(int value) {
    struct Node* temp = head;
    struct Node* prev = NULL;

    while (temp != NULL && temp->data != value) {
        prev = temp;
        temp = temp->next;
    }

    if (temp == NULL) {
        printf("Value not found.\n");
        return;
    }

    if (prev == NULL)
        head = temp->next;
    else
        prev->next = temp->next;

    free(temp);
}

// ➤ 5. Delete by Position
// Removes the node at a specific position
void deleteAtPosition(int pos) {
    if (head == NULL) return;

    struct Node* temp = head;

    if (pos == 0) {
        head = head->next;
        free(temp);
        return;
    }

    struct Node* prev = NULL;
    for (int i = 0; temp != NULL && i < pos; i++) {
        prev = temp;
        temp = temp->next;
    }

    if (temp == NULL) {
        printf("Position out of bounds.\n");
        return;
    }

    prev->next = temp->next;
    free(temp);
}

// ➤ 6. Search
// Searches the list for a given value
int search(int value) {
    struct Node* temp = head;
    while (temp != NULL) {
        if (temp->data == value)
            return 1;
        temp = temp->next;
    }
    return 0;
}

// ➤ 7. Display the list
void display() {
    struct Node* temp = head;
    while (temp != NULL) {
        printf("%d -> ", temp->data);
        temp = temp->next;
    }
    printf("NULL\n");
}

// ➤ 8. Count Nodes
int getSize() {
    int count = 0;
    struct Node* temp = head;
    while (temp != NULL) {
        count++;
        temp = temp->next;
    }
    return count;
}

// ➤ 9. Main function to test operations
int main() {
    insertAtEnd(10);
    insertAtEnd(20);
    insertAtBeginning(5);
    insertAtPosition(1, 15);  // 5 -> 15 -> 10 -> 20

    printf("Linked List: ");
    display();

    deleteByValue(10);
    printf("After deleting 10: ");
    display();

    deleteAtPosition(0);
    printf("After deleting position 0: ");
    display();

    printf("Search for 20: %s\n", search(20) ? "Found" : "Not Found");
    printf("Size of list: %d\n", getSize());

    return 0;
}
```

---

### 💡 Summary Table

| Operation           | Function Name         | Description                   |
| ------------------- | --------------------- | ----------------------------- |
| Insert at End       | `insertAtEnd()`       | Adds node at end              |
| Insert at Beginning | `insertAtBeginning()` | Adds node at start            |
| Insert at Position  | `insertAtPosition()`  | Adds node at specified index  |
| Delete by Value     | `deleteByValue()`     | Removes node with given value |
| Delete by Position  | `deleteAtPosition()`  | Removes node at a given index |
| Search              | `search()`            | Finds value in list           |
| Display             | `display()`           | Prints all nodes              |
| Count Nodes         | `getSize()`           | Returns total number of nodes |

---
