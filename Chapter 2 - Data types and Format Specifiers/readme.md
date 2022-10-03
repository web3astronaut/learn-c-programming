# Data Types and Format Specifiers

## Format Specifiers

Format specifiers define the type of data to be printed on standard output. You need to use format specifiers whether you're printing formatted output with `printf()` or  accepting input with `scanf()`.


| SPECIFIER | USED FOR                                           |
| --------- | -------------------------------------------------- |
| %c        | a single character                                 |
| %s        | a string                                           |
| %hi       | short (signed)                                     |
| %hu       | short (unsigned)                                   |
| %Lf       | long double                                        |
| %n        | prints nothing                                     |
| %d        | a decimal integer (assumes base 10)                |
| %i        | a decimal integer (detects the base automatically) |
| %o        | an octal (base 8) integer                          |
| %x        | a hexadecimal (base 16) integer                    |
| %p        | an address (or pointer)                            |
| %f        | a floating point number for floats                 |
| %u        | int unsigned decimal                               |
| %e        | a floating point number in scientific notation     |
| %E        | a floating point number in scientific notation     |
| %\%       | the % symbol                                       |


---

## Data Types

Range of a int and char depends on the no of bits it holds 

Range - [-2<sup>n-1</sup> to 2<sup>n-1</sup> - 1]  where n is the number of bits.

```c
#include <stdio.h>
#include <limits.h>

void main() {
    printf("Range of a unsigned char is [0 , %u]\n",UCHAR_MAX);
    printf("Range of a signed char is [%d, %d]\n",SCHAR_MIN,SCHAR_MAX);
    printf("Range of a char is [%d,%d]\n\n",CHAR_MIN,CHAR_MAX);
    printf("Range of a signed short is [%hd, %hd]\n", SHRT_MIN, SHRT_MAX);
    printf("Range of a unsigned short is [%hu, %hu]\n\n", 0, USHRT_MAX);
    printf("Range of a signed int is [%d,%d]\n",INT_MIN,INT_MAX);
    printf("Range of a unsigned int is [%u,%u]\n\n",0,UINT_MAX);
    printf("Range of a signed long is [%ld,%ld]\n",LONG_MIN,LONG_MAX);
    printf("Range of a unsigned long is [%lu,%lu]\n",0,ULONG_MAX);
    printf("Range of a signed long long is [%lli,%lli]\n",LLONG_MIN,LLONG_MAX);
    printf("Range of a unsigned long long is [%llu,%llu]\n",0,ULLONG_MAX);
    
}
```

**Output** -

```bash
Range of a unsigned char is [0 , 255]
Range of a signed char is [-128, 127]
Range of a char is [-128,127]

Range of a signed short is [-32768, 32767]
Range of a unsigned short is [0, 65535]

Range of a signed int is [-2147483648,2147483647]
Range of a unsigned int is [0,4294967295]

Range of a signed long is [-2147483648,2147483647]
Range of a unsigned long is [0,4294967295]
Range of a signed long long is [-9223372036854775808,9223372036854775807]
Range of a unsigned long long is [0,18446744073709551615]
```


Integer types also accept octal numbers

> An octal integer constant can consist of any combination of digits taken from the set 0 through 7. However the first digit must be 0, in order to identify the constant as an octal number.

eg- 

0    01   0743    077777

---

### Floating-Point Constants

A floating-point constant is a base-10 number that contains either a decimal point or an exponent (or both).

eg - 
0
0.2     875.254     2E-8     0.005e-9      1.666E+7      0.121212e12

3 x 10<sup>5</sup> can be written as follows

1. 300000.
2. 3e5
3. 3e+5
4. 3E5
5. 0.3e6
6. 0.3E6
7. 30E4

---

### Character Constants

A character constant is a single character, enclosed in apostrophes (i.e., single quotation marks).

eg- 
`A`, `x` , `3` , `?` , ` `

Character constants have integer values that are determined by the computer’s particular character set. Thus, the value of a character constant may vary from one computer to another.

---

### String Constants

A string constant consists of any number of consecutive characters (including none), enclosed in (double) quotation marks.

eg- 

"white","254-785-9655" ,etc.

---

### SYMBOLIC CONSTANTS

A symbolic constant is a name that substitutes for a sequence of characters. The characters may represent a numeric constant, a character constant or a string constant. Thus, a symbolic constant allows a name to appear in place of a numeric constant, a character constant or a string. When a program is compiled, each occurrence of a symbolic constant is replaced by its corresponding character sequence.


**Syntax** - 
```c
#define name value
```

eg - 

```c
#define PI 3.141593
#define PRICE 400
```

---
