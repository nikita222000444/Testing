# calculator-kuznetsov-nd
A program written in C. It reads an arithmetic expression from standard input, parses it, and prints the result. The program supports the following operators on integers: `+` , `-` , `*` , `/` , `(` , and `)` . Any whitespace characters are allowed in input. 
## Building the Program
To build the program, you need a C compiler such as `gcc` or `clang`. Follow these steps:
1. Open a terminal.
2. Navigate to the directory containing the source code(`main.c`).
3. Run the following command to compile the program.
```
gcc main.c -o calculator.exe
```
This will create an executable file named calculator.exe.
## Running the Program
To run the program in integer mode, use the following command:
```
./calculator.exe
```
Use following command to run program in __real__ numbers mode
```
./calculator.exe --float
```
The program will prompt you to enter an arithmetic expression. After entering the expression, press `Enter` to see the result.

##Important remarks
- Input passed through `stdin`
- Output passed through `stdout`
- Less than 1KiB of input data (else `UB`)
- Only allowed charset `[0-9()*+\/\s\.-]` (else code not equal to 0 returns)
  - `0-9` matches a single character in the range between 0 and 9 
  - `()*+` matches a single character in the list `()*+`
  - `\/` matches the character `/` 
  - `\s` matches any whitespace character (equivalent to [\r\n\t\f\v ] )
  - `\-` matches the character `-`
- Only correct arithmetic expression are allowed (else code not equal to 0 returns)
- All numbers in a given expression are integers from a range $[0 \dots 2 \times 10^9$ (else `UB`)
- All intermediate results (for any allowed order of evaluation) are fit into range $[-2 \times 10^9 \dots + 2\times 10^9]$
- Supports flag `--float` that switch app calculations into __real__ numbers mode
- In integer mode:
  - `/` return an integer part of an division (rounds towards $-\infty$)
  - Answer must be given on a single line as an integer number (with `-` sign if negative)
- In __real__ numbers mode:
  - `/` return a fraction number
  - Answer must be given on a single line as a real number (decimal notation) with an absolute accuracy $\pm 10^{-4}$
In any mode division on a number less than $10^{-4}$ are forbidden (else UB)
