# 📚 Doubly Linked List: Insert Elements at the End of a Doubly Linked List

This Python program demonstrates the creation and manipulation of a **Doubly Linked List** where elements can be inserted at the **end** of the list. The program also provides a method to traverse the list and display the elements.

---

## 🎯 Aim

To write a Python program that:
- Implements a **Doubly Linked List**.
- Allows insertion of elements at the end of the list.
- Provides functionality to traverse the list and display its elements.

---

## 🧠 Algorithm

1. **Step 1:** Define a class `Node` to represent each node in the doubly linked list with attributes:
   - `item` for storing the data of the node.
   - `nref` for storing the reference to the next node.
   - `pref` for storing the reference to the previous node.

2. **Step 2:** Define a class `DoublyLinkedList` with:
   - `start_node` to point to the first node of the list.

3. **Step 3:** Define methods in the `DoublyLinkedList` class:
   - `insert_in_emptylist(data)` to insert an element when the list is empty.
   - `insert_at_end(data)` to insert elements at the end of the list.
   - `traverse_list()` to traverse the list and print the elements.

4. **Step 4:** Create an instance of `DoublyLinkedList` and use the `insert_at_end()` method to insert elements into the list.

5. **Step 5:** Use the `traverse_list()` method to print the elements of the list.

---

## 💻 Program
# Node class

# Doubly Linked List class
class DoublyLinkedList:
    def __init__(self):
        self.start_node = None

    # Insert when list is empty
    def insert_in_emptylist(self, data):
        new_node = Node(data)
        self.start_node = new_node

    # Insert at end
    def insert_at_end(self, data):
        if self.start_node is None:
            self.insert_in_emptylist(data)
            return

        new_node = Node(data)
        temp = self.start_node

        while temp.nref is not None:
            temp = temp.nref

        temp.nref = new_node
        new_node.pref = temp

    # Traverse list
    def traverse_list(self):
        if self.start_node is None:
            print("List is empty")
            return

        temp = self.start_node
        while temp is not None:
            print(temp.item, end=" ")
            temp = temp.nref
        print()


# Main program
```
# Node class
# Doubly Linked List class
class DoublyLinkedList:
    def __init__(self):
        self.start_node = None

    # Insert when list is empty
    def insert_in_emptylist(self, data):
        new_node = Node(data)
        self.start_node = new_node

    # Insert at end
    def insert_at_end(self, data):
        if self.start_node is None:
            self.insert_in_emptylist(data)
            return

        new_node = Node(data)
        temp = self.start_node

        while temp.nref is not None:
            temp = temp.nref

        temp.nref = new_node
        new_node.pref = temp

    # Traverse list
    def traverse_list(self):
        if self.start_node is None:
            print("List is empty")
            return

        temp = self.start_node
        while temp is not None:
            print(temp.item, end=" ")
            temp = temp.nref
        print()


# Main program
dll = DoublyLinkedList()

n = int(input("Enter number of elements: "))

for i in range(n):
    value = int(input("Enter value: "))
    dll.insert_at_end(value)

print("Doubly Linked List elements:")
dll.traverse_list()
```

## Sample Output
<img width="357" height="191" alt="image" src="https://github.com/user-attachments/assets/b11a8d66-dc76-4700-9742-7ab9941ac110" />

## Result
The program is exucted successfully and the output is verified

