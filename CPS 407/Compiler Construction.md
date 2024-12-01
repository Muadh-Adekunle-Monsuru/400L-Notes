## Compiler and Interpreter 


| Compiler                                                                                   | Interpreter                                                        |
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------ |
| Compiler translates high level language to machine language equivalent for later execution | Translates and executes the program statements by statement        |
| Compiler process the physical statement in their physical input sequence                   | Follows the logical flow of control through the program.           |
| Object-code produced for subsequent execution with compilation                             | No code is produced and the tranlation is required.                |
| The whole program must be error free  before it can be executed to obtain any result.      | They are useful for debugging purposes.                            |
| Requires but source program and object program  be stored                                  | Does not need object program to be stored, just the source program |
Assembly Language:
Only translates programs written in assembly language to machine language.
This is the oldest programming language, it bares the closes resemblace to native machine language. It provides direct access to computer hardware, requiring much understanding of computer architecture and operating system. 
An assembler is a utility program that converts source program from assembly language to machine language which is a numeric language specifically understood by computer processing (CPU). Mnemonics like ADD, SUB, MOV, CALL. 
Each assembly language corresponds to a single machine language instruction. 

An important distinction between high level language, most high level languages are portable, however assembly language is designed for a specific processor family, e.g. Motorolla, 68x00, Intel IA-32, Sun Sparc


| Application                   | High-level language                                                                                                 | Assembly Language                                                                                     |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| Business Application Software | formal structures make it easy to organize and maintain large section of code.                                      | Minimal formal structure, so one must be imposed by programmers who have varying levels of experience |
| Hardware device driver        | Language may not provide direct hardware access.                                                                    | Hardware access is straight forward and simple.                                                       |
| Business application platorm  | They are usually portable, the source code can be recompiled and each target operating system with minimal changes. | It must be recorded separately for each platform using an assembler with different syntax.            |
|                               |                                                                                                                     |                                                                                                       |
|                               |                                                                                                                     |                                                                                                       |
