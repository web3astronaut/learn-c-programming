# Selection Statements

## `if ()` Statements

One of the simplest ways to control program flow is by using if selection statements. Whether a block of code is to be executed or not to be executed can be decided by this statement.

Example:

```c
if (a > 1) {
 puts("a is larger than 1");
}
```

---

## `switch ()` Statements

The `switch` statement causes a particular group of statements to be chosen from several available groups. The selection is based upon the current value of an expression which is included within the switch` `statement. 

The general form of the switch statement is

```c
switch (expression) {
	case expression_1:
		statement 1;
		statement 2;
	case expression_2:
		statement 3;
		statement 4;
}
```

where _expression 1_, _expression 2_, . . . , _expression m_ represent constant, integer-valued expressions. Usually, each of these expressions will be written as either an `integer constant` or a `character constant`.

Example:

```c
#include <stdio.h>

void main() {
    int num;
	switch(num = getchar()) {
        case '1': 
            puts("\nNumber selected is 1");
            break;
        case '2': 
            puts("\nNumber selected is 2");
            break;
        case '3': 
            puts("\nNumber selected is 3");
            break;
        default : puts("\nNumber selected is other than 1 or 2 or 3");
    };
}
```



---

## The `break` Statement 

The break statement is used to terminate loops or to exit from a switch. It can be used within a for, while, do - while, or switch statement. The break statement is written simply as

```c
break;
```

---

## The `continue` Statement

The `continue` statement is used to bypass the remainder of the current pass through a loop. The loop does not terminate when a `continue` statement is encountered. Rather, the remaining loop statements are skipped and the computation proceeds directly to the next pass through the loop.

Example:

```c
#include <stdio.h>

void main() {
    int x;
    do {
        scanf("%f", &x);
        if (x < 0) {
            printf("ERROR - NEGATIVE VALUE FOR X");
            continue;
        };
    } while (x <= 100);
}
```

Suppose we provide a negative input the loop will continue again and again until the input is a positive value and in that case the loop will end.


---

## `if () ... else` statements and syntax

While if performs an action only when its condition evaluate to true, if / else allows you to specify the different actions when the condition true and when the condition is false.

We can also chain if-else statements to make a ladder eg-

```c
#include <stdio.h>

void main() {
    int x;
    printf("Enter Number :");
    scanf("%d", &x);

    if (x < 0) {
        puts("\nNumber is Negative");
    } else if (x > 0 && x < 100) {
        puts("\nNumber is Between 0 and 100");
    } else {
        puts("\nNumber is greater than or equal to 100");
    }
}
```


---
