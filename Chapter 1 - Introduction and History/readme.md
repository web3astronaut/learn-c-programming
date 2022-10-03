# Introduction and History of C

## Introduction

C is a general-purpose, structured programming language. Its instructions consist of terms that resemble algebraic expressions, augmented by certain English keywords such as `if`, `else`, `for`, `do` and `while`. In this respect C resembles other high-level structured programming languages such as Pascal and Fortran. C also contains certain additional features, however, that allow it to be used at a lower level, thus bridging the gap between machine language and the more conventional high-level languages. This flexibility allows C to be used for `systems programming` (e.g., for writing operating systems) as well as for `applications programming`.

---

## History of C

- C was originally developed in the 1970s by Dennis Ritchie at Bell Telephone Laboratories, Inc. (now a part of AT&T).
- It is an outgrowth of two earlier languages, called BCPL and B, which were also developed at Bell Laboratories.
- C was largely confined to use within Bell Laboratories until 1978, when Brian Kernighan and Ritchie published a definitive description of the language.

---

## Structure of a C Program

- Every C program consists of one or more modules called functions. One of the functions must be called `main`. 
- The program will always begin by executing the `main` function, which may access other functions.
- Any other function definitions must be defined separately, either ahead of or after `main`

**Each function must contain**:

1. A function heading, which consists of the function `name`, followed by an optional list of `arguments`, enclosed in parentheses.
2. A list of argument declarations, if arguments are included in the heading.
3. A `compound statement`, which comprises the remainder of the function.


eg-  A simple Hello World Program..

```c
#include <stdio.h>

void main() {
    printf("Hello World!");
}
```

---
