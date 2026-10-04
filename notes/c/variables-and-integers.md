# Variables and Integers in C

## Variables

A variable is a named object used to store a value of a particular type.

For example:

```c
int age;
```

Here, `age` is a variable of type `int`.

A variable can then be assigned a value:

```c
age = 20;
```

It can also be initialized when it is declared:

```c
int age = 20;
```

## Variable Names

Variable names should describe what the variable represents.

For example:

```c
int age;
int account_number;
int total;
```

Using `_` can make multiple-word names easier to read.

## Declaration Before Use

Variables should be declared before they are used.

For example:

```c
int number;

number = 10;
```

## Assignment

A variable can be assigned to another variable.

```c
int first = 10;
int second;

second = first;
```

The value stored in `first` is copied to `second`.

## Integers

The `int` type is used to represent integer values.

For example:

```c
int number = 10;
int temperature = -5;
```

Integers can be positive, negative, or zero when using a signed integer type.

## Integer Arithmetic

Basic arithmetic operations can be performed with integers:

```text
+   addition
-   subtraction
*   multiplication
/   division
%   remainder
```

An important thing I learned is that when integer operands are used in integer division, the result is also an integer.

## `printf()` and Integers

The `%d` format specifier can be used to print an `int`.

```c
int number = 10;

printf("%d\n", number);
```

## `scanf()`

`scanf()` can be used to read input from the user.

For an `int`, I can write:

```c
int number;

scanf("%d", &number);
```

The `&` provides the address of the variable so that `scanf()` can store the input there.

This is different from simply passing the value of the variable.

## Using Variables in Calculations

I practiced two different ways of performing calculations.

The result can be used directly:

```c
int n1, n2;

scanf("%d%d", &n1, &n2);

printf("%d\n", n1 + n2);
```

Or the result can first be stored in another variable:

```c
int n1, n2;
int sum;

scanf("%d%d", &n1, &n2);

sum = n1 + n2;

printf("%d\n", sum);
```

This reminded me of the way I used variables in Python.

# Integer Types and Modifiers

C provides different integer types and modifiers.

Some of the modifiers I studied are:

* `short`
* `long`
* `signed`
* `unsigned`

For example:

```c
short int age;
long int account_number;
unsigned int value;
```

Some type combinations can also be written in shorter forms:

```c
short age;
long account_number;
unsigned value;
```

## `short` and `long`

The exact size of integer types depends on the C implementation.

`short` is guaranteed to be at least 16 bits, while `long` is guaranteed to be at least 32 bits.

Therefore, I should not assume that `short` is always exactly 2 bytes or `long` is always exactly 4 bytes.

## Format Specifiers

Different integer types use different format specifiers.

Examples:

```text
int             %d
unsigned int    %u
short int       %hd
long int        %ld
unsigned long   %lu
```

Example:

```c
short age;
long account_number;

scanf("%hd", &age);
scanf("%ld", &account_number);

printf("%hd\n", age);
printf("%ld\n", account_number);
```

## Signed and Unsigned

Signed integers can represent negative and non-negative values.

For example:

```c
int temperature = -10;
```

Unsigned integers cannot represent negative values.

```c
unsigned int value = 10;
```

The range of values depends on the type's representation and size.

An `int` is signed by default, so writing:

```c
int number;
```

is equivalent to:

```c
signed int number;
```

when the default signed integer type is intended.

## `sizeof`

The `sizeof` operator can be used to determine the size of a type or expression in bytes.

For example:

```c
#include <stdio.h>

int main(void)
{
    printf("%zu\n", sizeof(char));
    printf("%zu\n", sizeof(int));
    printf("%zu\n", sizeof(float));
    printf("%zu\n", sizeof(double));

    return 0;
}
```

The result depends on the implementation and platform.

`sizeof` returns a value of type `size_t`, which is why `%zu` is the appropriate format specifier in modern C.

## What I learned

Studying variables and integer types made me realize that C requires more attention to how values are represented.

I started thinking not only about the value stored in a variable, but also about:

* Its type
* Its size
* Its range
* How it is represented
* How input is stored
* How arithmetic behaves

This led me to study `unsigned` integers and what happens when they reach their maximum value.
