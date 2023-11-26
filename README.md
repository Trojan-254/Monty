# Monty Interpreter

[Monty 0.98](http://montyscoconut.github.io/) is a scripting language that is first compiled into Monty byte codes (Just like Python). It relies on a unique stack, with specific instructions to manipulate it. The goal of this project is to create an interpreter for Monty ByteCodes files. Monty aims to close the gap between scripting and programming languages.

# The monty program

* Usage: monty file
        where file is the path to the file containing Monty byte code
* If the user does not give any file or more than one argument to your program, print the error message USAGE: monty file, followed by a new line, and exit with the status EXIT_FAILURE
* If, for any reason, it’s not possible to open the file, print the error message Error: Can't open file <file>, followed by a new line, and exit with the status EXIT_FAILURE
where <file> is the name of the file
* If the file contains an invalid instruction, print the error message L<line_number>: unknown instruction <opcode>, followed by a new line, and exit with the status EXIT_FAILURE
where is the line number where the instruction appears.
Line numbers always start at 1
* The monty program runs the bytecodes line by line and stop if either:
it executed properly every line of the file
it finds an error in the file
an error occured

## Compilation

To compile this project, you can use the following command:

```
$ gcc -Wall -Werror -Wextra -pedantic -std=c89 *.c -o monty
```

## Allowable opcodes and what they do


|opcode  |  functionality|
| --- | --- |
| push | add element to the 'top' of stack and 'end' of queue  |
| pop  | remove element from 'top' of stack and 'end' of queue |
|pall  |print every member of the structure|
| pint | prints the member value at the top of stack |
| swap | swaps the order  of the 1st and 2nd elements in stack |
| add | add top two member values |
| sub | subtract the top element from the 2nd top element |
| div | divide the 2nd element by the top element |
| mul | multiply the top two elements of the stack |
| mod | the remainder when the 2nd element is divided by the top element |
| comment | there is the ability to parse comments found in bytecode ->'#'|
| pchar | print character at the top of the stack |
| pstr | print the character at the top of the stack|
| rotl | moves element at the top to the bottom of the stack |
| rotr | the bottom of the stack becomes the top |
| queue, stack | toggles the doubly link list implementation style |
| nop | opcode should do nothing |




Examples:
`$ cat opcodetestfile.m`

`push 1`

`push 2`

`push 3`

`pall`

`$ ./montyfile opcodetestfile.m`

`3`

`2`

`1`

`$`

---

`$ cat opcodetestfile.m`

`push 1`

`push 2`

`push 3`

`pall`

`rotl`

`pall`

`$ ./montyfile opcodetestfile.m`

`3`

`2`

`1`

`2`

`1`

`3`

## Exit Status
Exits with status `EXIT_FAILURE`


## Compilation
All files were compiled on Ubuntu 14.04 LTS.

All programs and functions were compiled with `gcc 4.8.4` using flags `-Wall -Werror -Wextra and -pedantic`.

## Styling
All files have been written in the Betty Style.

## Importance of the Monty ByteCode Interpreter
The Monty ByteCode interpreter project holds significance as it bridges the gap between scripting and programming languages, aiming to provide a versatile tool for executing Monty ByteCode files. By creating this interpreter, a fundamental understanding of language parsing, bytecode execution, and data structure manipulation is achieved.

## Importance in Language Interpretation
Interpreters serve as critical components in understanding and executing code written in specific languages. This Monty interpreter facilitates the execution of Monty ByteCode files, allowing developers and enthusiasts to experiment and explore this unique language's functionalities in a controlled environment.

## Skills Acquired
Building the Monty ByteCode interpreter was an enriching experience that provided opportunities to develop various technical skills, including:

* Language Design Understanding:
 Grasping the syntax and semantics of Monty ByteCode and implementing corresponding functionality.

* Parser Development: 
Creating a parser to read and interpret the bytecode instructions, handling edge cases and unknown instructions gracefully.

* Data Structure Handling: 
Implementing stack and queue data structures, pivotal in executing stack and queue-related operations defined by Monty opcodes.

* Error Handling and Reporting: 
Devising error handling mechanisms to report issues such as unknown instructions, file opening failures, or invalid bytecode structures.

* Programming Logic: 
Designing algorithms to execute Monty instructions efficiently and accurately, considering the specifics of each opcode's functionality.

* Debugging and Troubleshooting: 
Identifying and resolving issues within the interpreter, refining the code for enhanced reliability.

## Learning Outcomes
The process of creating this Monty ByteCode interpreter not only allowed for a deeper understanding of language interpretation but also honed problem-solving abilities, coding practices, and familiarity with low-level programming concepts

## Author

**Trojan-254** 