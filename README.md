# CFG Playground

## Overview

CFG Playground is a web-based interactive tool for exploring **Context-Free Grammars (CFGs)** and fundamental parsing techniques from the Theory of Computation. It enables users to define grammars, evaluate input strings, and visualize parsing behavior through structured representations.

The platform is designed to support both **conceptual learning** and **practical experimentation**, bridging the gap between formal language theory and implementation.

---

## Key Features

### Grammar Definition

* Supports user-defined CFG productions using standard notation
* Handles multiple production rules and alternatives
* Includes editable grammar input interface

### Preset Grammars

* Arithmetic expressions
* Balanced parentheses
* Palindromes
* Ambiguous grammars

### CYK Parsing Engine

* Implements the **Cocke–Younger–Kasami (CYK) algorithm**
* Uses dynamic programming for efficient string validation
* Determines membership of a string in the language ( L(G) )

### Visualization Modules

* **CYK Table**: Displays step-by-step parsing table construction
* **Parse Tree**: Represents hierarchical derivation structure
* **Derivation View**: Shows production expansion sequences

### Input Validation

* Accepts user-defined input strings
* Provides deterministic output:

  * Accepted (string ∈ language)
  * Rejected (string ∉ language)

---

## Theoretical Foundations

* Context-Free Grammars (CFG)
* Chomsky Normal Form (CNF)
* CYK Parsing Algorithm
* Parse Trees and Derivations
* Grammar Ambiguity

---

## System Architecture

The system is composed of the following core components:

* **Grammar Parser**: Processes and validates production rules
* **CYK Engine**: Executes bottom-up parsing using CNF-compatible grammars
* **Visualization Layer**: Renders tables, trees, and derivations
* **User Interface**: Facilitates interaction and real-time feedback

---

## Limitations

* The CYK algorithm requires grammars to be in **Chomsky Normal Form (CNF)**
* Non-CNF grammars may result in incorrect parsing outcomes
* Current implementation provides limited diagnostic feedback for rejected inputs

---

## Future Enhancements

* Automated CNF conversion
* Detailed error diagnostics for invalid strings
* Stepwise CYK execution visualization
* Enhanced grammar validation and feedback
* Export functionality for parse trees and derivations

---

## Installation

```bash
git clone https://github.com/your-username/cfg-playground.git
cd cfg-playground
npm install
npm start
```

---

## Use Case

CFG Playground is intended for:

* Students studying formal languages and automata theory
* Educators demonstrating parsing algorithms
* Developers experimenting with grammar-based systems

---

