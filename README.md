# CFG Playground

A web-based interactive system for constructing, transforming, and parsing **Context-Free Grammars (CFGs)** using the **CYK (Cocke–Younger–Kasami) algorithm**, with real-time visualization of parsing structures.

---

## Overview

CFG Playground provides an environment to:

* Define custom grammars
* Automatically convert them into **Chomsky Normal Form (CNF)**
* Parse input strings using CYK
* Visualize internal parsing steps through:

  * CYK table construction
  * Parse trees
  * Stepwise derivations

The system is designed to make formal parsing algorithms observable and testable.

---

## Core Capabilities

### 1. Grammar Processing

* Accepts CFG input using standard production notation
* Parses and normalizes rules internally
* Converts arbitrary CFG into **CNF (on-the-fly)** 

### 2. CYK Parsing Engine

* Implements bottom-up dynamic programming
* Builds a triangular CYK table
* Tracks backpointers for reconstruction of parse structures

### 3. Visualization System

#### CYK Table

* Incremental cell computation animation
* Highlights:

  * Active computation cell
  * Filled entries
  * Final acceptance state

#### Parse Tree

* Dynamically generated from backpointers
* Tree layout algorithm with proper spacing and hierarchy

#### Derivation View

* Step-by-step expansion of sentential forms
* Supports:

  * Manual navigation
  * Auto-play traversal

---

## Features

* Preset grammars:

  * Arithmetic expressions
  * Balanced parentheses
  * Palindromes
  * (a^n b^n) language
  * Ambiguous grammar

* Real-time CNF display

* Token-based input parsing (space-separated symbols)

* Status feedback system (Accepted / Rejected / Errors)

---

## Architecture

The system consists of four main components:

| Component           | Responsibility                          |
| ------------------- | --------------------------------------- |
| Grammar Parser      | Parses user input into structured rules |
| CNF Converter       | Transforms CFG into valid CNF form      |
| CYK Engine          | Performs parsing and table computation  |
| Visualization Layer | Renders table, tree, and derivation     |

---

## Algorithmic Flow

1. Parse input grammar
2. Convert grammar to CNF
3. Tokenize input string
4. Initialize CYK table (length = 1 substrings)
5. Fill table for increasing substring lengths
6. Check if start symbol derives full string
7. If accepted:

   * Build parse tree
   * Generate derivation steps

---

## Limitations

* CNF conversion does not fully optimize all edge cases (e.g., epsilon-heavy grammars)
* Grammar validation is permissive (invalid structures may silently degrade results)
* Error feedback is minimal for rejected strings

---

## Installation

```bash
git clone https://github.com/your-username/cfg-playground.git
cd cfg-playground
open index.html


## Usage

1. Select a preset or define a custom grammar
2. Enter a space-separated input string
3. Click **Parse**
4. Explore:

   * CYK Table
   * Parse Tree
   * Derivation Steps

## Example

**Input Grammar**
S → A B  
A → a  
B → b  


**Input String**
a b

**Output**
✓ Accepted — string ∈ L(G)

## Future Improvements

* Strong grammar validation with error diagnostics
* Better CNF conversion (epsilon & unit optimization)
* Support for ambiguous parse trees (multiple trees)
* Export functionality (JSON / SVG)
* Step-by-step CYK explanation mode


