# # 🔍 Singly Linked List-To Search an Element in a Linked List

This project contains a simple implementation of a **singly linked list** in Python, allowing insertion and searching of elements.

---

## 🎯 Aim

To write a Python program to search for a given element in a singly linked list using object-oriented programming principles.

---

## 🧠 Algorithm

1. **Define a Node class** with `data` and `next` attributes.
2. **Define a LinkedList class** with:
   - A `head` pointer initialized to `None`.
   - A `push()` method to add elements at the beginning.
   - A `search()` method to check whether a given value exists.
3. Create a `LinkedList` instance.
4. Insert the elements **10, 30, 11, 21, 14** using `push()` (which results in reverse order).
5. Read an integer input from the user.
6. Use `search()` to check if the element exists in the list.
7. Output **"Yes"** if found, else **"No"**.

---

## 💻 Program
```
# Node class
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None


# Linked List class
class LinkedList:
    def __init__(self):
        self.head = None

    # Push (insert at beginning)
    def push(self, data):
        new_node = Node(data)
        new_node.next = self.head
        self.head = new_node

    # Search element
    def search(self, key):
        temp = self.head

        while temp is not None:
            if temp.data == key:
                return True
            temp = temp.next

        return False


# Main program
ll = LinkedList()

# Insert elements (10, 30, 11, 21, 14) using push
ll.push(10)
ll.push(30)
ll.push(11)
ll.push(21)
ll.push(14)

# Take input from user
key = int(input("Enter element to search: "))

# Search and display result
if ll.search(key):
    print("Yes")
else:
    print("No")
```
## Sample Output
<img width="360" height="302" alt="image" src="https://github.com/user-attachments/assets/06c48285-6df8-4584-80ee-1ac74c22d4e4" />

## Result
The program is exucted successfully and the output is verified
