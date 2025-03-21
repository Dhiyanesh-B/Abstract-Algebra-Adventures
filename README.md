# Abstract-Algebra-Adventures

## Overview
This Python project provides a comprehensive tool for analyzing algebraic structures such as groups, rings, and their properties. It includes functions to check various mathematical properties and relationships between sets under different operations.

## Features
- Group Theory Analysis:
  - Closure verification
  - Associativity checking
  - Identity element detection
  - Inverse element identification
  - Commutativity testing
  - Cyclic group detection
  - Subgroup enumeration
  - Coset calculations (left and right)
  - Normal subgroup verification

- Ring Theory Analysis:
  - Ring property verification
  - Commutative ring checking
  - Unity element identification
  - Unit element enumeration
  - Zero divisor detection
  - Subring identification
  - Ideal verification

## Requirements
- Python 3.x
- Required libraries:
  - sympy (`pip install sympy`)
  - operator (standard library)
  - itertools (standard library)

## Installation
1. Clone the repository:
```bash
git clone https://github.com/Dhiyanesh-B/Abstract-Algebra-Adventures.git
```
Or download the ZIP and extract it.

## Usage

### Example: Check if a set forms a group under addition modulo 4
tset = [0, 1, 2, 3]
is_group(tset, '+', 4)  # Returns 1 if it's a group, 0 if not

### Example: Check if a set forms a ring
tset = [0, 1, 2, 3]
is_ring(tset, '+', '*', 4, 4)  # Checks ring properties with addition and multiplication

### Example: Find subgroups
subgroup(tset, '+', 4)  # Returns list of all subgroups

### Working with matrices
matrix_set = [
    [1, 0],  # Identity matrix
    [0, 1],
    [1, 1],  # Another 2x2 matrix
    [0, 0]   # Zero matrix
]

### Check if matrices form a group under addition
group_result = is_group(matrix_set, '+', 2)  # Modulo 2 addition
print("Matrices form group:", bool(group_result))

### Check if matrices form a ring
ring_result = is_ring(matrix_set, '+', '*', 2, 2)  # Addition and multiplication mod 2
print("Matrices form ring:", bool(ring_result))

### Find identity element
identity_elem = identity(matrix_set, '+', 2)
print("Identity element:", identity_elem)

## Supported Operations
The following operations are supported via the ops dictionary:

- +: Addition
- -: Subtraction
- *: Multiplication
- /: Division
- %: Modulus
- ^: XOR

## Key Functions
- is_group(tset, opr, mod): Checks if a set forms a group
- is_ring(tset, opr1, opr2, mod1, mod2): Checks if a set forms a ring
- subgroup(tset, opr, mod): Finds all subgroups
- left_coset(tset, opr, mod, subset): Calculates left cosets
- right_coset(tset, opr, mod, subset): Calculates right cosets
- commutative(tset, opr, mod): Checks commutativity
- cyclic(tset, opr, mod): Identifies cyclic generators
- identity(tset, opr, mod): Finds the identity element

## Team Members
1. Dhiyanesh B
2. [Dipankar T V](https://github.com/dipankar272)

---
⭐ **If you like this project, give it a star!** ⭐
