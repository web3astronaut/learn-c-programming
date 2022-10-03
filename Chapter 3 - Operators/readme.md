# Operators

## Arithmetic Operators

There are five arithmetic operators in C. They are

| Operator | Purpose                          |
| -------- | -------------------------------- |
| +        | addition                         |
| -        | subtraction                      |
| *        | multiplication                   |
| /        | division                         |
| %        | remainder after integer division |

> **Note** - The % operator is sometimes referred to as the modulus operator. There is no exponentiation operator in C. However, there is a library function (`pow`) to carry out exponentiation.


---

## UNARY OPERATORS

C includes a class of operators that act upon a single operand to produce a new value. Such operators are known as unary operators. Unary operators usually precede their single operands, though some unary operators are written after their operands.

There are two other commonly used unary operators: The increment operator, ++, and the decrement operator, −−. The increment operator causes its operand to be increased by 1, whereas the decrement operator causes its operand to be decreased by 1. The operand used with each of these operators must be a single variable.

eg - 

```c
#include <stdio.h>

void main() {
	int i = 0;
	printf("i = %d\n",i); // 0
	printf("i = %d\n",i++); // 0
	printf("i = %d\n",i); // 1
	printf("i = %d\n",++i); // 2
}
```

The `++i`  operation first increases the value of `i` and then print the new value whereas the `i++` operation first prints the value and then increases it by 1.

Another unary operator that is worth mentioning at this time is the `sizeof` operator. This operator returns the size of its operand, in bytes. The `sizeof` operator always precedes its operand. The operand may be an expression, or it may be a cast.

```c
#include <stdio.h>

void main() {
	int i;
    float f;
    char c;
	printf("Integer  = %d\n",sizeof i);
    printf("Float  = %d\n",sizeof f);
    printf("Char  = %d\n",sizeof c);
}
```

Output - 

```bash
Integer  = 4
Float  = 4
Char  = 1
```

**Addressof operator(&):** It gives an address of a variable. It is used to return the memory address of a variable. These addresses returned by the address-of operator are known as pointers because they “point” to the variable in memory.

```c
#include <stdio.h>

void main() {
	int i = 0;
    int* ptr;
    ptr = &i;
    printf("%d",ptr); // 6422036
}
```

---

## RELATIONAL OPERATORS

Relational operators check if a specific relation between two operands is true. The result is evaluated to 1 (which means true) or 0 (which means false). This result is often used to affect control flow (via if, while, for), but can also be stored in variables.

There are four relational operators in C. They are
 | Operator | Meaning                  |
 | -------- | ------------------------ |
 | <        | less than                |
 | <=       | less than or equal to    |
 | >        | greater than             |
 | >=       | greater than or equal to |

Equality Operator closely resemble relational operators , they are

| Operator | Meaning      |
| -------- | ------------ |
| ==       | equal to     |
| !=       | not equal to |


These six operators are used to form logical expressions, which represent conditions that are either true or false.

---

## LOGICAL OPERATORS

In addition to the relational and equality operators, C contains two logical operators (also called logical connectives). They are

| Operator | Meaning |
| -------- | ------- |
| &&     | and     |
| \|\|     | or      |


---

## Conditional Operator/Ternary Operator

Simple conditional operations can be carried out with the conditional operator (? :). An expression that makes use of the conditional operator is called a conditional expression. Such an expression can be written in place of the more traditional if−else statement.

**Syntax** - 
```c
expression 1 ? expression 2 : expression 3
```

When evaluating a conditional expression,` expression 1` is evaluated first. If `expression 1` is true (i.e., if its value is nonzero), then `expression 2` is evaluated and this becomes the value of the conditional expression. However, if` expression 1` is false (i.e., if its value is zero), then `expression 3` is evaluated and this becomes the value of the conditional expression. Note that only one of the embedded expressions (either `expression 2` or `expression 3`) is evaluated when determining the value of a conditional expression.

eg -

```c
#include <stdio.h>

void main() {
	int i = 10;
    int j = (i > 5) ? 20 : 30;
    int k = (i < 5) ? 20 : 30;
    printf("%d,%d",j,k); // 20,30
}
```

The conditional operator can be nested. For example, the following code determines the bigger of three numbers:

```c
big = a > b ? (a > c ? a : c) 
			: (b > c ? b : c);
```

---
