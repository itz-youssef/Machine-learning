# 🧠 Assembly Instruction Emulator in C++

This project is a **simple emulator for a virtual assembly-like instruction set**, written in C++. It simulates a CPU's behavior by handling instructions, registers, and memory. The emulator accepts input through a file or terminal and displays register and memory states with a clean and colored terminal interface.

---

## 📌 Overview

The program mimics basic machine instruction handling by parsing 4-character hexadecimal instructions, each consisting of:
- **1st character**: Opcode (operation code)
- **Next 3 characters**: Operand (usually a memory or register address)

It currently:
- Loads and stores instructions
- Extracts opcodes and addresses
- Displays a 256-byte memory space (00 to FF)
- Displays 16 general-purpose registers (`R00` to `R0F`)
- Uses color-coded output to enhance readability

---

## 🛠️ Features

- 📄 **Load instructions from a `.txt` file**
- ⌨️ **Type instructions manually via terminal**
- 📌 **Parse and display operation codes (opcodes) and program counters**
- 🧠 **Simulated memory of 256 bytes with hex addressing**
- 🧮 **16 registers (`R00` to `R0F`) initialized to `00`**
- 🎨 **Colorful terminal UI using ANSI escape codes**

---

## 📁 File Structure

| File / Class | Description |
|--------------|-------------|
| `Get`        | Static class to load and parse instructions from file or terminal |
| `UI`         | Handles menu, user interaction, and display of memory/registers |
| `main.cpp`   | Main entry point (not shown in this version but should call `Main_Menu()`) |
| `reg`        | `map<string, string>` to hold register values |
| `Mem`        | `map<string, string>` to simulate 256 bytes of memory |
| `instructions` | `vector<string>` holding all raw instructions |
| `operations`   | Parsed operation codes from instructions |
| `PC`          | Program counters extracted from instructions |

---

## 🧪 Sample Input (from File)

A `.txt` file like this:

A0F3
B120
C000




Will be parsed as:
- `A`: Operation code
- `0F3`: Program counter / operand

---

## 🖥️ Terminal Menu

```text
1- Load instruction file
2- Type instructions
3- Exit



🧭 Future Enhancements
 Implement instruction execution (e.g., LOAD, STORE, ADD)

 Instruction validation

 Support for labels, jumps, and flags

 Clock cycle simulation

 GUI-based memory visualizer (optional)

