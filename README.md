# 🔗 Doubly Linked List — String Manipulation

A **character-based doubly linked list** implemented in C++ that stores a string as a sequence of individual character nodes. Supports a full suite of string operations including concatenation, substring extraction, search, replacement, and index-based removal.

---

## 📌 About

This project was built as a data structures assignment to demonstrate the practical use of **doubly linked lists** in C++. Rather than storing a string as a primitive, each character occupies its own node with both a `next` and `previous` pointer — enabling efficient insertion, deletion, and traversal in both directions.

---

## 🛠️ How It Works

Each node stores three fields:

| Field | Role |
|-------|------|
| `info` | The character value stored in the node |
| `next` | Pointer to the next node |
| `previous` | Pointer to the previous node |

### Key Operations

| Function | Description |
|----------|-------------|
| `addtotail(char)` | Appends a character to the end of the list |
| `removefromhead()` | Removes the first character |
| `removefromtail()` | Removes the last character |
| `removalbyind(int)` | Removes the character at a given index |
| `getlength()` | Counts and prints the number of characters |
| `searchthelist(string)` | Returns the starting index of a substring, or -1 if not found |
| `subextract(int, int)` | Extracts a substring starting at index with a given length |
| `replacestring(new, old)` | Replaces all occurrences of a substring with another |
| `concatstrings(charDLL)` | Appends another doubly linked list to the current one |
| `display()` | Prints each character separated by spaces |

---

## 📁 Project Structure

```
DoublyLinkedList-String-CPP/
│
├── src/
│   └── main.cpp        # node and charDLL classes + interactive main
├── README.md           # Project documentation
├── LICENSE             # MIT License
└── .gitignore          # Ignores compiled binaries
```

---

## ▶️ How to Run

### Prerequisites
- A C++ compiler (g++, clang++, MSVC, etc.)

### Compile & Run (Linux / macOS)
```bash
g++ -o dll_string src/main.cpp
./dll_string
```

### Compile & Run (Windows)
```bash
g++ -o dll_string.exe src/main.cpp
dll_string.exe
```

---

## 🖥️ Sample Session

```
Enter string to add to list 1: Hello
Enter string to add to list 2: World
Concatenated Lists: HelloWorld

Choose a character by index to remove: 5
List after removal: HelloWorld  ← removes 'W' at index 5

Enter index and length to get substring: 0 5
Substring: Hello

Search for a string in the list: llo
Found at index 2

Enter 2 substrings to replace one with another: llo xyz
List after replacement: Hexyzorld
```

---

## 🧠 Concepts Demonstrated

- **Doubly Linked List** — bidirectional traversal via `next` and `previous` pointers
- **Character-level string storage** — each character is an independent node
- **Dynamic memory management** — manual `new`/`delete` with a destructor to prevent leaks
- **Substring search** — O(n × m) pattern matching directly on the linked list
- **In-place string replacement** — node-level unlinking and re-linking without rebuilding the list
- **Operator overloading** — `<<` operator for clean output via `cout`
- **Edge case handling** — empty list checks, head/tail removal, out-of-bounds index

---

## 📜 License

This project is open source and available under the [MIT License](LICENSE).
