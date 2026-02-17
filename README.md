# 🔗 Doubly Linked List Implementation

This repository contains a professional-grade implementation of a **Doubly Linked List** in [Language, e.g., Java], strictly adhering to the standard `List` Interface. This project is designed for educational purposes to demonstrate pointer management and interface contracts.

---

## 🧐 What is a Doubly Linked List?

A **Doubly Linked List (DLL)** is a linear data structure where each element (node) contains a data field and **two references** (pointers):
1.  **Next:** Points to the subsequent node.
2.  **Prev:** Points to the preceding node.

This bidirectional nature allows for traversal in both directions (forward and backward) and more efficient deletions if a pointer to the node is already known.

---

## 🛠️ Interface Implementation: `List<T>`

By implementing the `List` interface, this class guarantees the following standard behaviors:

* **`add(T element)`**: Appends an element to the end of the list.
* **`add(int index, T element)`**: Inserts an element at a specific position.
* **`get(int index)`**: Retrieves an element by its position.
* **`remove(int index)`**: Removes the element at the specified position.
* **`size()`**: Returns the current number of elements.
* **`isEmpty()`**: Checks if the list contains any elements.
* **`clear()`**: Removes all elements from the list.

---

## 📊 Efficiency Analysis

The Doubly Linked List offers significant advantages for insertions and deletions at both ends of the list:

| Operation | Time Complexity (Big O) | Description |
| :--- | :---: | :--- |
| **Insert at Head/Tail** | $O(1)$ | Direct access via head/tail pointers. |
| **Delete at Head/Tail** | $O(1)$ | No shifting required (unlike Arrays). |
| **Access by Index** | $O(n)$ | Must traverse from head or tail. |
| **Search** | $O(n)$ | Linear scan required. |
| **Space Complexity** | $O(n)$ | Each node stores two additional pointers. |

---

## 💻 Code Example

```java
// Example usage of the implementation
List<String> names = new DoublyLinkedList<>();

names.add("Alice");
names.add("Bob");
names.add(1, "Charlie"); // Insert in the middle

System.out.println("First element: " + names.get(0));
System.out.println("List size: " + names.size());