<div align="center">

# 🔗 Linked List in C

### A clean and simple **Doubly Linked List** implementation written in C  
This project demonstrates how to **insert**, **delete**, **display**, and **clear data** in a linked list structure.

<br>

![C](https://img.shields.io/badge/Language-C-blue?style=for-the-badge&logo=c)
![Data Structure](https://img.shields.io/badge/Data%20Structure-Doubly%20Linked%20List-orange?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

</div>

---

## 📌 Project Overview

This project was built to help explain the basic concept of a **Doubly Linked List** using the C programming language.

Unlike a singly linked list, a doubly linked list allows each node to point in two directions:

- `next` points to the next node
- `prev` points to the previous node

This makes the list more flexible because data can be accessed, inserted, and deleted from both directions.

The program uses three main pointers:

| Pointer | Purpose |
|---|---|
| `head` | Points to the first node in the list |
| `tail` | Points to the last node in the list |
| `curr` | Works as a helper pointer for traversal and searching |

---

## ✨ Key Features

✅ Insert data at the front of the list  
✅ Insert data at the back of the list  
✅ Insert data after a specific value  
✅ Delete data from the front of the list  
✅ Delete data from the back of the list  
✅ Delete data by a specific value  
✅ Clear all data from the list  
✅ Display the linked list from front to back  

---

## 🧠 Concepts Used

This project covers several important concepts in C programming and data structures:

- `struct` for creating a node
- `next` and `prev` pointers
- Dynamic memory allocation using `malloc()`
- Memory cleanup using `free()`
- Linked list traversal
- Handling an empty list
- Handling a list with only one node
- Insert and delete operations in a doubly linked list

---

## 🏗️ Node Structure

Each node in this program contains three main parts:

```c
struct tnode
{
    int x;
    struct tnode *next;
    struct tnode *prev;
};
```

Explanation:

| Part | Description |
|---|---|
| `x` | Stores an integer value |
| `next` | Points to the next node |
| `prev` | Points to the previous node |

---

## ⚙️ Function Breakdown

| Function | Description |
|---|---|
| `push_front(int value)` | Adds a new node to the front of the list |
| `push_back(int value)` | Adds a new node to the back of the list |
| `push_mid(int value, int searchKey)` | Adds a new node after a specific value |
| `delete_front()` | Removes the first node from the list |
| `delete_back()` | Removes the last node from the list |
| `delete_mid(int searchKey)` | Removes a node based on a specific value |
| `clearData()` | Removes all nodes from the list |
| `printList()` | Displays every value in the list |

---

## 🔄 Program Flow

The program starts by inserting several values into the linked list:

```c
push_front(11);
push_back(90);
push_front(78);
push_back(50);
```

Initial list result:

```text
78 11 90 50
```

After that, the program performs several insert and delete operations:

```text
Insert after 90  -> 78 11 90 22 50
Insert after 78  -> 78 18 11 90 22 50
Delete front     -> 18 11 90 22 50
Delete back      -> 18 11 90 22
Delete 90        -> 18 11 22
Delete all       -> There is No Data
```

---

## 🖥️ Sample Output

```text
PUSH DATA
List: 78 11 90 50

Insert after 90
List: 78 11 90 22 50

Insert after 78
List: 78 18 11 90 22 50

Delete front
List: 18 11 90 22 50

Delete back
List: 18 11 90 22

Delete 90
List: 18 11 22

Delete all
There is No Data
```

---

## 🚀 How to Run the Program

### 1. Clone the repository

```bash
git clone https://github.com/aphroditemoon/Linked-List.git
cd Linked-List
```

### 2. Compile the program

If your file uses the `.c` extension, run:

```bash
gcc Tugas.c -o linkedlist
```

If your file is named `Tugas` or `Tugas.txt`, run:

```bash
gcc -x c Tugas -o linkedlist
```

or:

```bash
gcc -x c Tugas.txt -o linkedlist
```

### 3. Run the program

For Windows:

```bash
linkedlist
```

For Linux or macOS:

```bash
./linkedlist
```

---

## 📂 Repository Structure

```text
Linked-List/
│
├── Tugas
└── README.md
```

---

## 📊 Simple Visualization

Example of a doubly linked list:

```text
NULL <- [78] <-> [11] <-> [90] <-> [50] -> NULL
```

After running:

```c
push_mid(22, 90);
```

The list becomes:

```text
NULL <- [78] <-> [11] <-> [90] <-> [22] <-> [50] -> NULL
```

---

## 🎯 Project Goals

The main goal of this project is to strengthen the understanding of linked list operations, especially how data is inserted, deleted, displayed, and managed through pointers in C.

By understanding this project, learners can build a stronger foundation for more advanced data structures such as:

- Stack
- Queue
- Tree
- Graph
- Hash Table

---

## 📝 Future Improvements

A few possible improvements for this project:

- Add an interactive menu for user input
- Add a search feature
- Display the list from back to front using the `prev` pointer
- Add memory allocation validation after `malloc()`
- Improve the output format to make it more user-friendly

---

## 👨‍💻 Author

**Erlangga Putra Mahardika**  
Repository: `Linked-List`

---

<div align="center">

### ⭐ Thanks for checking out this project!

If you find this project helpful, feel free to give it a star.

</div>
