# Unix Shell in C

A lightweight command-line shell built from scratch in C for a university systems programming module. It reads commands, runs programs, and keeps its own state between sessions, much like the shells we use every day.

## Overview

The shell works as a classic read, parse, execute loop. Each line you type is split into tokens, checked against the built-in commands, and, if it isn't one, launched as an external program in a child process.

## What It Can Do

**Running programs**
Any program found on the PATH can be launched. The shell creates a child process with `fork`, replaces it with the requested program using `exec`, and waits for it to finish with `wait`.

**Built-in commands**

| Command | Purpose |
|---|---|
| `cd` | Change directory (relative or absolute paths) |
| `getpath` | Show the current PATH |
| `setpath` | Replace the PATH with a new one |
| `history` | View and reuse previous commands |
| `alias` | Create a shortcut for a command |
| `unalias` | Remove an existing alias |

**Saved state**
Command history and aliases are written to disk, so they are still there the next time you start the shell.

**Input handling**
Input is tokenised carefully, and invalid commands, bad arguments and failed lookups produce clear error messages instead of crashing the shell.

## Built With

- **C** (POSIX system calls)
- **Linux**
- Key ideas: process control, environment variables, file I/O

## Getting Started

```bash
# Build
make

# Run
./shell
```

## What This Project Taught Me

- How a shell really works under the hood, from process creation to waiting on children
- Writing a tokeniser and command parser by hand, without libraries doing the work
- Reading and modifying environment variables such as PATH and HOME from code
- Saving and reloading data with file I/O so the shell remembers its state
- Splitting a C program into small, reusable modules that are easier to maintain
