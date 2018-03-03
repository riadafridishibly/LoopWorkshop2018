# List of Topics - Day 1

* [String](#string)
    * [String Printing](#string-printing)
* [Integer](#integer)
    * [Integer Declaration](#integer-declaration)
    * [Integer Initialization](#integer-initialization)
    * [Integer Printing](#integer-printing)
    * [Sum of two Integers](#sum-of-two-integers)
* [Float](#float)
    * [Float Declaration](#float-declaration)
    * [Float Initialization](#float-initialization)
    * [Float Printing](#float-printing)
* [Char](#char)
    * [Char Declaration](#char-declaration)
    * [Char Initialization](#char-initialization)
    * [Char Printing](#char-printing)
* [Special Topic](#special-topic)
    * [Integer Division](#integer-division)

## String

### What?

Sequence of characters. `"abcd"`, `"0123"`.
Notice double quotes. It's important. Anything inside **double quotes** is a string.

### String Printing

Simply put your string inside double quotes. And print it.

```c
printf("Hello, World!");

printf("My string");

printf("Sakib Khan");

printf("0123456789");

printf("!@#@$#%");

```

OK. Then How to print Escape char? I mean let's print Newline.

```c
printf("Hello\nWorld!"); // notice \n
```

`\n` means Newline Char. Run this program. And notice this change.

What if I wanna print `Hello` inside ``""`` quote.


```c
printf("\"Hello\""); // \"  Hello \" this means escape them.
```

Try this without `backslash` and try to understand the errors.


## Integer

### What?

Numbers. Like `1`, `0`, `-12312`, `1505000`. Notice There is no double quotes.

### Integer Declaration

```c
int myInteger;
int rollNumber;
```

Don't start variable name with numbers or any other character except `_` (**underscore**).

```c
int 9k;  // error: don't do this.
int k9;  // do this

int this_is_my_int;  // do this
```

### Integer Initialization

```c
int x = 777; // value 777 is assigned to x

int y;
y = 71231; // you can do this too
```

Don't use **uninitialized** variables.

```c
int x;
int y;

y = x + 1; // please don't do this. Because x is uninitialized
           // What is the value of x?
           // Who knows! Maybe some garbage value.
```

### Integer Printing

Use `%d` format specifier.

```c
printf("%d", 123); // 123 is an Integer. Print it

int x = 707;   // 707 is assigned to x

printf("%d", x); // x is an integer. Print it
```

### Sum of two integers

```c
int a, b, c; // declaration

a = 7; // assignment
b = 8; // assignment

c = a + b; // first compiler calculates (a + b)
           // then the calculated value is assigned to c

printf("Sum is %d", c);

printf("Sum is %d", a + b); // you can do this too
                            // one less variable

a = a + b; // this is also valid.
           // a is modified. (a + b) calculated first.
           // then value is assigned to a
           // awakward. isn't it?

printf("Sum is %d", a); // because now a contains sum of a and b
                        // a is no more 7
```


## Float

### What?
Floating point number. Examples:

PI: `3.14159265`
CGPA: `2.95`, `4.0000000123` If you don't get the joke yet. Don't worry.

### Float Declaration

```c
float f;
float my_float;

int   x; // x is an int
float x; // Bro. You can't use same name twice.

```

### Float Initialization
Like an integer.

```c
int x = 6; // an Integer

float a = 3.22;
float b = 3.;
float c = 5.f;
```

### Float Printing
Use `%f` format specifier.

```c
printf("%f", 3.12312);
printf("CGPA %f\n", 3.99);
```

## Char

### What?

Single character. `a`, `1`, `#`, `)` All are characters. Notice the single quote. You may wanna see the [ASCII Table](https://www.asciitable.com/).


### Char Declaration
Like any other int or float.

```c
char ch;
ch = 'a';  // notice single quote. This is important.
```

### Char Initialization

```c
char a = 'k';
char b = '#';
```

### Char Printing
Use `%c` format specifier.

```c
printf("%c", 'a');
printf("%c", '#');
```

## Special Topic

### Integer Division

What is the result of `5 / 3` ?

```c
printf("%f", 5 / 3);  // not correct

printf("%f", 5.0      / 3); // correct
printf("%f", 5.f      / 3); // correct
printf("%f", 5.       / 3); // correct
printf("%f", (float)5 / 3); // correct
```

