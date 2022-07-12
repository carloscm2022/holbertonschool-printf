<h1 align ="center"> <img src="https://assets.website-files.com/6105315644a26f77912a1ada/610540e8b4cd6969794fe673_Holberton_School_logo-04-04.svg" height="60%" width="50%"> </h1>

# C – PRINTF

In this project we will create our own _printf() function, that replicates the standard printf() function. This project was to be done in a group of two (pair programming).
**Function prototype:**
>int _printf(const char *format, ...);

**Compilation and testing**
>$ gcc -Wall -Werror -Wextra -pedantic *.c


## FILES

|                FILES                       |DESCRIPTION               |         
|----------------------------------------|---------------------------|
|main.h                                  |`File where the structures and prototypes are found.`          |  
|_printf.c                                 |`Program that gives an output according to the format.`         |               
|_vsprintf.c                              |`Receives the main string and all the necessary parameters to print a formatted string.`  |                  
|decimal_specifier.c                                  |`function that returns an int to signed decimal`  |          
|main.c                                |`File with which it will be tested if the "_printf" works correctly.`           |             
|string_specifier.c  |     `Print a string.`                   |            
|percent_specifier.c                               |`Print a percent symbol`                        
|_putchar.c                              |`Writes the character c to stdout`

### Format tags
Format tags implemented in _printf

| **specifier** | **output**                            |
|---------------|---------------------------------------|
| c             | characters                            |
| s             | string of characters                  |
| d or i        | int to signed decimal                 |

.EXAMPLE

````
#include <limits.h>
#include <stdio.h>
#include "main.h"

/**
 * main - Entry point
 *
 * Return: Always 0
 */
int main(void)
{
    int len;
    int len2;
    unsigned int ui;
    void *addr;

    len = _printf("Let's try to printf a simple sentence.\n");
    len2 = printf("Let's try to printf a simple sentence.\n");
    ui = (unsigned int)INT_MAX + 1024;
    addr = (void *)0x7ffe637541f0;
    _printf("Length:[%d, %i]\n", len, len);
    printf("Length:[%d, %i]\n", len2, len2);
    _printf("Negative:[%d]\n", -762534);
    printf("Negative:[%d]\n", -762534);
    _printf("Unsigned:[%u]\n", ui);
    printf("Unsigned:[%u]\n", ui);
    _printf("Unsigned octal:[%o]\n", ui);
    printf("Unsigned octal:[%o]\n", ui);
    _printf("Unsigned hexadecimal:[%x, %X]\n", ui, ui);
    printf("Unsigned hexadecimal:[%x, %X]\n", ui, ui);
    _printf("Character:[%c]\n", 'H');
    printf("Character:[%c]\n", 'H');
    _printf("String:[%s]\n", "I am a string !");
    printf("String:[%s]\n", "I am a string !");
    _printf("Address:[%p]\n", addr);
    printf("Address:[%p]\n", addr);
    len = _printf("Percent:[%%]\n");
    len2 = printf("Percent:[%%]\n");
    _printf("Len:[%d]\n", len);
    printf("Len:[%d]\n", len2);
    _printf("Unknown:[%r]\n");
    printf("Unknown:[%r]\n");
    return (0);
}

Let's try to printf a simple sentence.
Let's try to printf a simple sentence.
Length:[39, 39]
Length:[39, 39]
Negative:[-762534]
Negative:[-762534]
Unsigned:[2147484671]
Unsigned:[2147484671]
Unsigned octal:[20000001777]
Unsigned octal:[20000001777]
Unsigned hexadecimal:[800003ff, 800003FF]
Unsigned hexadecimal:[800003ff, 800003FF]
Character:[H]
Character:[H]
String:[I am a string !]
String:[I am a string !]
Address:[0x7ffe637541f0]
Address:[0x7ffe637541f0]
Percent:[%]
Percent:[%]
Len:[12]
Len:[12]
Unknown:[%r]
Unknown:[%r]
````

# Authors

- Julieth Alvarado Calvo. (america02anarosa@gmail.com)
- Carlos Cantoral Milián. (carloscr7cmreal@gmail.com)
