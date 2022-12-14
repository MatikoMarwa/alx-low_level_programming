## Nested Loops

In C programming, a nested loop is a loop that is inside another loop. Nested loops are commonly used to perform a certain action on every element in a two-dimensional array, or to perform a certain action on every pair of elements in a one-dimensional array.

Example of a loop
```
int i, j;

for (i = 0; i < 10; i++) {
    for (j = 0; j < 10; j++) {
        printf("%d, %d\n", i, j);
    }
}
```
In this example, the outer loop is the `for` loop that uses the variable `i`, and the inner loop is the `for` loop that uses the variable `j`. The inner loop will run 10 times for each iteration of the outer loop, so a total of 100 iterations of the inner loop will occur. This can be useful for processing a two-dimensional array of size 10x10, for example.

## What is a function and how to use

In programming, a function is a piece of code that performs a specific task. It is often used to perform a repetitive task, or to perform a task that is triggered by a certain event. Functions are an important part of most programming languages, and they can be used to make your code more organized and easier to understand.
To use a function, you first need to define it. This usually involves specifying the name of the function, along with the input that the function will take (known as arguments or parameters) and the code that the function will execute.
In general, using functions can make your code more modular and easier to understand. It also allows you to reuse the same code in multiple places, which can save you time and reduce the likelihood of errors.

## Declaration of a function

In the C programming language, a function is declared with the following syntax:
```
return_type function_name(parameter1, parameter2, ...) {
  // function body
}
```
Here, `return_type` is the data type of the value that the function will return, `function_name` is the name of the function, and `parameter1`, `parameter2`, etc. are the parameters (also known as arguments) that the function can accept. The function body is the code that will be executed when the function is called.

For example, the following code defines a function called `max` that accepts two integer parameters and returns the maximum value:
```
int max(int x, int y) {
  if (x > y) {
    return x;
  } else {
    return y;
  }
}
```
To call this function, you would use the following syntax:
`int result = max(5, 10); // result = 10`

Note that the function declaration specifies a return type of `int`, so the function must return an integer value. You can use the return keyword in the function body to return a value.

It's also possible to define a function in C that does not accept any parameters or return a value. In this case, you would use the keyword `void` for the return type and leave the parameter list empty. For example:
```
void printMessage() {
  printf("Hello, world!\n");
}
```
Here, the `printMessage` function does not accept any parameters and does not return a value. You can call this function like this:
`printMessage(); // Output: "Hello, world!"`
The exact syntax for declaring a function in C may vary depending on the specific context in which it is used. Consult the C language documentation for more information.

## Definition of a function

In C, a function is a block of code that performs a specific task. To define a function in C, you need to specify the name of the function, the return type of the function, and the input parameters that the function takes. Here is an example of defining a simple function called "add" in C that takes two integer parameters and returns their sum:

```int add(int x, int y)
{
    return x + y;
}
```

## Function Prototype

A function prototype is a declaration of a function that specifies the function's name, return type, and the types of its parameters. The purpose of a function prototype is to inform the compiler about the function's signature, so that the compiler can check the correctness of function calls and generate the appropriate machine code for invoking the function.
The function prototype tells the compiler the name of the function, the type of data that the function expects as input (in this case, two `int` values), and the type of data that the function will return (in this case, an `int` value).
In C and C++, a function prototype typically takes the following form:
`return_type function_name(parameter_type1 parameter1, parameter_type2 parameter2, ...);`

For example, the prototype for a function that takes two `int` arguments and returns an `int` might be:
`int add(int x, int y);`
Function prototypes are usually placed in header files, which are included in the source files that use the functions declared in the header. This allows the compiler to check the correct use of the functions throughout the program.

In some programming languages, function prototypes are not required and the compiler is able to infer the function signature from the function definition. However, in C and C++, it is good practice to always include function prototypes to avoid potential compile-time errors.

## Scope of variables

The scope of a variable refers to the parts of a program where the variable is visible and can be accessed. In other words, it determines the region of the program where the variable is defined and can be used.

There are two main types of variable scope: local and global. A local variable is only visible and accessible within the block of code where it is declared. A global variable, on the other hand, is visible and accessible throughout the entire program.
A local variable is a variable that is declared inside a function and can only be accessed within that function. It is only available for use within the block of code in which it is defined, and it is destroyed when the function ends.
In some programming languages, the scope of a variable may also be restricted to a specific function or object, in which case the variable is known as a local or class variable. This can be useful for preventing naming conflicts and ensuring that variables are used correctly within the correct context.

A global variable is a variable that is declared outside of all functions, and it is available for use by any part of the program. Because global variables can be accessed by any function, they can make it difficult to understand and maintain the code. In general, it is considered better practice to use local variables whenever possible.

The scope of a variable can also be affected by other factors, such as the location of the variable declaration and the use of certain keywords or statements, such as `static`, `extern`, or `const`.

## What are the gcc flags -Wall -Werror -pedantic -Wextra -std=gnu89

The `-Wall` flag enables all warnings, `-Werror` makes all warnings into errors, `-pedantic` enables additional language-specific warnings, `-Wextra` enables extra warning checks that are not enabled by `-Wall`, and `-std=gnu89` specifies that the code should be compiled in compliance with the version of the C standard published in 1989 (including the amendments made by ISO/IEC 9899:1990 Technical Corrigendum 1).

## What are header files and how to to use them with #include

In the C and C++ programming languages, a header file is a file that is included at the top of a program source file. Header files typically contain declarations for functions, variables, and other constructs that are used in the main body of the program.

To use a header file in a C or C++ program, you must include it using the `#include` preprocessor directive. This directive tells the compiler to include the contents of the specified header file in the program source code.

For example, if you have a header file called `myheader.h`, you could include it in your program like this:

`#include "myheader.h"`

This would include the contents of the `myheader.h` file in your program source code. You can then use any declarations or definitions from the header file in the main body of your program.

It's worth noting that the angle brackets (`<` and `>`) are used to include system header files, while quotation marks (`"` and `"`) are used to include header files that are part of your program. For example:

```
#include <stdio.h>  // include a system header file
#include "myheader.h"  // include a header file from your program

```
In general, header files are a convenient way to organize declarations and definitions in your program, and to reuse code in multiple source files. They help to make your code more modular and easier to maintain.
