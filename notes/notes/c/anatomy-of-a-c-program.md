# Anatomy of a C Program

## Basic Structure

A C program is composed of instructions organized into functions.

The `main()` function is the entry point of a C program.

A basic program can look like this:

```c
#include <stdio.h>

int main(void)
{
    printf("Hello World\n");

    return 0;
}
```

The instructions between `{` and `}` form a **block**.

## Functions

A function is followed by parentheses.

For example:

```c
main()
{
}
```

However, the standard form I am using is:

```c
int main(void)
{
    return 0;
}
```

`main` returns an `int`, which is why `int` is used before the function name.

## Case Sensitivity

C is **case-sensitive**.

This means that these are different identifiers:

```text
main
Main
MAIN
```

The same applies to variables, functions, and other identifiers.

## Header Files

Header files provide declarations and information that can be used by a program.

For example:

```c
#include <stdio.h>
```

includes the standard input/output header.

This allows us to use functions such as `printf()` and `scanf()`.

## `printf()`

`printf()` is used to produce formatted output.

Example:

```c
printf("Hello World\n");
```

## Escape Sequences

The backslash `\` is used to introduce escape sequences inside strings.

For example:

```c
printf("Hello\n");
```

`\n` represents a newline.

### Double quotes

A double quote normally marks the beginning or end of a string.

To print a double quote as part of the string, I can use:

```c
printf("Today is a \"beautiful\" day!\n");
```

The `\"` tells C that the quote is part of the string rather than the end of it.

### Backslash

To print a backslash itself:

```c
printf("\\");
```

### Percent sign

To print `%` with `printf()`, I can use:

```c
printf("100%%\n");
```

## Comments

Comments are ignored by the compiler and can be used to document code.

A block comment is written using:

```c
/*
   This is a comment.
*/
```

For a single-line comment, C also supports:

```c
// This is a comment
```

## What I practiced

I practiced writing small programs using:

* `main()`
* `#include`
* `stdio.h`
* `printf()`
* Escape sequences
* Comments
* Return values

I also solved exercises where I had to identify syntax errors and understand why certain C programs did not compile.
