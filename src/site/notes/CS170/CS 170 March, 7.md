---
{"dg-publish":true,"permalink":"/cs-170/cs-170-march-7/"}
---

***LAB CONTENTS***

- [[Linked files/Virtual Destructor\|Virtual Destructor]] 

- ***GCC Compilation process***
![Pasted image 20250307113233.png](/img/user/Pasted%20image%2020250307113233.png)

- [GNU compilation options](https://gcc.gnu.org/onlinedocs/gcc-3.2.2/gcc/Overall-Options.html#Overall%20Options)

| `-x none` | Turn off any specification of a language, so that subsequent files are handled according to their file name suffixes (as they are if -x has not been used at all).<br><br>If you only want some of the stages of compilation, you can use -x (or filename suffixes) to tell `gcc` where to start, and one of the options -c, -S, or -E to say where `gcc` is to stop. Note that some combinations (for example, ‘-x cpp-output -E’) instruct `gcc` to do nothing at all. |
| --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `-c`      | Compile or assemble the source files, but do not link. The linking stage simply is not done. The ultimate output is in the form of an object file for each source file.<br><br>By default, the object file name for a source file is made by replacing the suffix ‘.c’, ‘.i’, ‘.s’, etc., with ‘.o’.<br><br>Unrecognized input files, not requiring compilation or assembly, are ignored.                                                                                |
| `-S`<br>  | Stop after the stage of compilation proper; do not assemble. The output is in the form of an assembler code file for each non-assembler input file specified.<br><br>By default, the assembler file name for a source file is made by replacing the suffix ‘.c’, ‘.i’, etc., with ‘.s’.<br><br>Input files that don’t require compilation are ignored.<br>                                                                                                               |
| `-E`      | <br>Stop after the preprocessing stage; do not run the compiler proper. The output is in the form of preprocessed source code, which is sent to the standard output.<br><br>Input files that don’t require preprocessing are ignored.                                                                                                                                                                                                                                    |





- [[Linked files/GNU compilation options for students\|GNU compilation options for students]] 

- ***Function declarations and function prototypes*** 
The function declaration makes known to the compiler the name and type of the function along with the number and type of parameters received by the function. This allows the compiler to determine if the function is being referenced correctly in the subsequent text in the source file

- ***Difference between implementation and declaration of functions*** 
*see more : https://learn.microsoft.com/en-us/cpp/c-language/c-function-definitions?view=msvc-170*

| Definition                       (Declaration+implementation) | memory will be reserved for the instructions of that function.                                                                                |
| ------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| **Declaration**                                               | **Only the name and parameters are known and used to confirm the correct usage of the function. A reference to a function DEFINED elsewhere** |
How to build to Exe:
gcc main.o greetings.o -o output.exe

- Reasons to use Header files
1. Removes errors that are created by copy pasting declarations across multiple files
2. localizes related files -> easy for making changes
3. Robust and well-designed libraries can be implemented by separating _**implementation details**_ in a source file from the _**interface**_ 


