##0x11. C - printf team project
###Description
This project is a group project aimed at implementing the printf function in C language. The function is designed to produce output according to a format.
###Usage
To use the printf function, first clone the repository using the following command:

git clone https://github.com/<username>/printf.git

After cloning, navigate to the repository directory and compile the source files using your preferred C compiler. For example, using gcc:

gcc -Wall -Werror -Wextra -pedantic *.c -o printf

You can then use the printf function in your C code by including the holberton.h header file and calling the function as follows:

#include "holberton.h"

int main(void)
{
    _printf("Hello, %s!\n", "world");
    return (0);
}

###Conversion Specifiers
The following conversion specifiers have been implemented:
%c: prints a single character
%s: prints a string of characters
%%: prints a percent sign
%d, %i: prints a signed integer
%u: prints an unsigned integer
%o: prints an octal integer
%x, %X: prints a hexadecimal integer
###Custom Conversion Specifiers
The following custom conversion specifiers have been implemented:
%b: prints an unsigned integer in binary form
%S: prints a string of characters, printing non-printable ASCII characters in the format \x, followed by the ASCII code value in hexadecimal
%r: prints a string of characters in reverse order
%R: prints a string of characters with the ROT13 substitution cipher applied
###Flags, Width and Precision
The following flags, width and precision modifiers have been implemented:
+: prints a sign for positive numbers after the % character.
space: prints a space for positive numbers after the % character when a sign isn't printed
#: adds the prefix 0 for octal numbers and 0x or 0X for hexadecimal numbers
0: pads the output with zeros to the left of the value.
-: left-aligns the output in the field width.
*: replaces the width or precision field with the integer argument immediately following the format string.
##Length Modifiers
The following length modifiers are handled for non-custom conversion specifiers:
l: for long integer types
h: for short integer types
##Field Width
The field width can be specified using a positive integer value. If the output is less than the specified width, it will be padded with spaces (or zeros if the 0 flag is used).
##Precision
The precision can be specified using a period followed by a positive integer value. This is used to specify the maximum number of characters to be printed for strings, or the minimum number of digits to be printed for integers.

###Examples

#include "holberton.h"

int main(void)
{
    char c = 'H';
    char *str = "Hello, world!";
    int num = 8;

    _printf("%c\n", c);
    /* Output: H */

    _printf("%s\n", str);
    /* Output: Hello, world! */

    _printf("%%\n");
    /* Output: % */

    _printf("%d\n", num);
    /* Output: 8 */

    _printf("%u\n", num);
    /* Output: 8 */

    _printf("%o\n", num);
    /* Output: 10 */

    _printf("%x\n", num);
    /* Output: 8 */

    _printf("%X\n", num);
    /* Output: 8 */

    _printf("%b\n", num);
    /* Output: 1000 */

    _printf("%S\n", "Holberton\tSchool");
    /* Output: Holberton\x09School */

    _printf("%r\n", str);
    /* Output: !dlrow ,

Authors
Kelvin Atandi
Masilela Zile



