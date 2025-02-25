# calculator-kuznetsov-nd
A program written in C. It reads an arithmetic expression from standard input, parses it, and prints the result. The program supports the following operators on integers: `+` , `-` , `*` , `/` , `(` , and `)` . Any whitespace characters are allowed in input. 

Program does not provide any prompt to user — just reading input until `EOF`.
 
The input is shorter that 1KiB, all numbers are non negative integers fit into `int` type at any stage of evaluation.
 
Program outputs only a number. The whole program fits single `main.c` file. No any external dependencies are used except `libc`. 
## Building the Program
To build the program, you need a C compiler such as `gcc` or `clang`. Follow these steps:
1. Open a terminal.
2. Navigate to the directory containing the source code(`main.c`).
3. Run the following command to compile the program.
``
gcc main.c -o calculator.exe
``
This will create an executable file named calculator.exe.
