# Unix Shell

A Unix-style shell written in C as part of a university systems programming project. 

The shell supports the execution of external programs together with a range of built-in commands including changing directories, history management, aliases, and environment path configuration.

---

## 🚀 Features

* **Process Management:** Execution of external programs using process creation via `fork`, `exec`, and `wait`.
* **Built-in Commands:** Native support for `cd`, `getpath`, `setpath`, `history`, `alias`, and `unalias`.
* **Environment Management:** Full PATH and HOME environment configuration with both relative and absolute directory navigation.
* **Persistence:** Persistent command history and alias tracking across sessions.
* **Robust Parsing:** Advanced command parsing and tokenisation alongside comprehensive error handling for invalid commands and user input.

---

## 🛠️ Technologies Used

* **Language:** C
* **API/Standard:** POSIX
* **Platform:** Linux
* **Concepts:** Process Management, System Calls, File I/O Persistence

---

## 🧠 What I Learned

This project provided a deep, practical understanding of how Unix shells function internally. Key takeaways included:
* Mastering low-level **process creation** and synchronization.
* Implementing structured **command parsing** and string tokenisation algorithms.
* Managing **environment variables** programmatically.
* Handling **file persistence** in C to maintain user state across sessions.
* Strengthening overall systems programming practices and writing highly modular, maintainable C code.