
# Iteration Statements/Loops

## _`For`_ loop

The for statement is the most commonly used looping statement in C. 
This statement includes an expression that specifies an initial value for an index, another expression that determines whether or not the loop is continued, and a third expression that allows the index to be modified at the end of each pass. 
The general form of the for statement is 

```c
for (expression 1; expression 2; expression 3) statement
```

where `expression 1` is used to initialize some parameter (called an index) that controls the looping action, `expression 2` represents a condition that must be true for the loop to continue execution, and `expression 3` is used to alter the value of the parameter initially assigned by` expression 1`. Typically, expression 1 is an _assignment expression_, expression 2 is a _logical expression_ and expression 3 is a _unary expression_ or an assignment expression.

The looping action will continue as long as the value of `expression 2` is not zero, that is, as long as the logical condition represented by `expression 2` is true.

eg - 

```c
#include <stdio.h>

void main() {
	for(int i = 0; i < 11; ++i) printf("%d\n",i);
}
```

Output - 

```bash
0
1
2
3
4
5
6
7
8
9
10
```

---

## _`While`_ loop

The while statement is used to carry out looping operations, in which a group of statements is executed repeatedly, until some condition has been satisfied. 

The general form of the while statement is 

```c
while (expression) statement
```

The `statement` will be executed repeatedly, as long as the `expression` is true.

eg - 

```c
#include <stdio.h>

void main() {
	int count;
    while (count < 5) {
        printf("Hello World\n");
        count++;
    }
}
```

Output  - 

```bash
Hello World
Hello World
Hello World
Hello World
Hello World
```

---

## _`Do-While`_ loop

When a loop is constructed using the while statement described above the test for continuation of the loop is carried out at the beginning of each pass.
Sometimes, however, it is desirable to have a loop with the test for continuation at the end of each pass. This can be accomplished by means of the do - while statement. 

The general form of the do - while statement is 

```c
do statement while (expression);
```


in this loop the statement is executed at least once.

eg - 

```c
#include <stdio.h>

void main() {
	int count;
    do {
        printf("Hello World\n");
    } while (count < 0);
}
```

Here even though the while condition evaluates to false we get output in the console as the statement is executed before the check.

Output - 

```bash
Hello World
```

---

## Infinite Loops

A loop is said to be an infinite loop if the control enters but never leaves the body of the loop. This happens when the test condition of the loop never evaluates to **false**.

Example:

```c
for (int i = 0; i >= 0; ) {
 /* body of the loop where i is not changed*/
}
```


In a for loop, the condition statement optional. In this case, the condition is always true vacuously, leading to an infinite loop.

```c
for (;;)
{
 /* body of the loop */
}
```

---
