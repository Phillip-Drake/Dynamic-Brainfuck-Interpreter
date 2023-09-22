# Dynamic-Brainfuck-Interpreter
Interpreter for the esoteric language "Brainfuck" written in javascript, with a boilerplate web interface attached for demonstration purposes.


## What is Brainfuck?

Brainfuck is an esoteric language developed by Urban Müller in 1993, with the intention of creating as minimally featured, but fully turing complete, language as possible.

Brainfuck gives the user access to 8 commands, which are used to affect values in the registry : 
">" - Move the data pointer to the right by 1 unit
"<" - Move the data pointer to the left by 1 unit
"+" - Increment the registry value at the data pointer by 1
"-" - Decrement the registry value at the data pointer by 1
"." - Output the byte at the data pointer
"," - Accept one byte for input from the user
"[" and "]" - opening and closing a loop, which terminates when the "]" character is reached at a registry value of 0

With this limited assortment of commands, a dedicated developer could theoretically create any arbitrary program.

## Why is this interpreter different?

The majority of Brainfuck interpreters execute code whenever some "run" button is pressed. This is effective for development, but doesn't allow you to see the real-time effect of the code you create.
This is unproblematic for the vast majority of programming languages, but the incredibly minamalist nature allows for the possibility of dynamic compilation. 

## How does it work?
Dynamic programming is used to verify that the entire program does not need to be re-executed at the addition of each operation, allowing for much faster viewing of the program's live status

## What are the drawbacks?
The creation of an infinite loop by the user will result in the webpage crashing. This is mitigated through usage of some arbitrary _maxOperations_, but this value needs to be adjusted 
as the program the user makes becomes larger and larger. 

There is unfortunately no solution to this problem, as to detect an infinite loop by the user would be to solve the _halting problem_.

# Have fun with this interpreter!
