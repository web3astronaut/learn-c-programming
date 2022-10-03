# Functions

## Introduction

A `function` is a self-contained program segment that carries out some specific, well-defined task. Every C program consists of one or more functions . One of these functions must be called `main`. Execution of the program will always begin by carrying out the instructions in main. Additional functions will be subordinate to main, and perhaps to one another.

Generally, _a function will process information that is passed to it from the calling portion of the program, and return a single value_. Information is passed to the function via special identifiers called `arguments` (also called `parameters`), and returned via the `return` statement. Some functions, however, accept information but do not return anything (as, for example, the library function printf), whereas other functions (e.g., the library function scanf) return multiple values.

---

## Defining a Function

The first line of a function definition contains the `type specification` of the value returned by the function, followed by the function name, and (optionally) a `set of arguments`, separated by commas and enclosed in parentheses. Each argument is preceded by its associated type declaration. An empty pair of parentheses must follow the function name if the function definition does not include any arguments.

**Syntax** -

```c
data-type name(type 1 arg 1, type 2 arg 2, . . ., type n arg n)
```

Example:

```c
#include <stdio.h>

int add(int _num1,int _num2) {
    return _num1+_num2;
}

void main() {
    int sum = add(24,86);
    printf("%d",sum); // 110
}
```

---

## Accessing a Function

A function can be _accessed_ (i.e., called) by specifying its name, followed by a list of arguments enclosed in parentheses and separated by commas. If the function call does not require any arguments, an empty pair of parentheses must follow the name of the function.

---

## Recursion

_Recursion_ is a process by which a function calls itself repeatedly, until some specified condition has been satisfied. The process is used for repetitive computations in which each action is stated in terms of a previous result.

Example - Calculating Factorials

```c
#include <stdio.h>

long int factorial(int n) {
    if (n <=1) return 1;
    else return (n * factorial(n - 1));
}

void main() {
    printf("%d\n", factorial(5)); // 120
}
```

---
