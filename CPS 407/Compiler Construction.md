
| **Aspect**               | **Compiler**                                                                                     | **Interpreter**                                                             |
| ------------------------ | ------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------- |
| **Function**             | Translates an entire high-level program into machine code for later execution.                   | Translates and executes program statements line by line during runtime.     |
| **Execution Flow**       | Processes the physical sequence of statements in the source code.                                | Follows the logical flow of control in the program during execution.        |
| **Output**               | Produces an object code (executable) for subsequent execution.                                   | No object code is produced; the source code is translated during execution. |
| **Error Handling**       | The entire program must be error-free before execution; errors are identified after compilation. | Useful for debugging; errors are caught and reported as they occur.         |
| **Storage Requirements** | Both the source code and the compiled object code must be stored.                                | Only the source code needs to be stored.                                    |

---

### **Assembly Language**  

- **Definition:** A low-level programming language closely resembling a computer's machine language. It provides direct access to hardware and requires in-depth knowledge of computer architecture and operating systems.  
- **Key Features:**  
  - Translates assembly instructions (e.g., `ADD`, `SUB`, `MOV`) into machine language using an **assembler**.  
  - Each instruction corresponds to a single machine operation.  
  - Assembly language is **processor-specific**, meaning it must be rewritten for different processor families (e.g., Motorola 68x00, Intel IA-32).  
  - Provides a direct, efficient means to interact with hardware, but lacks portability.  

---

### **Comparison: High-Level Language vs. Assembly Language**  

| **Aspect**                     | **High-Level Language**                                                                                         | **Assembly Language**                                                                                   |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| **Structure**                  | Has formal structures, making it easier to organize and maintain large sections of code.                        | Minimal formal structure; programmers must impose their own structure.                                 |
| **Hardware Access**            | Limited direct hardware access; often requires specialized libraries or APIs.                                  | Direct and straightforward hardware access.                                                            |
| **Portability**                | Portable; source code can be recompiled for different platforms with minimal changes.                          | Not portable; must be rewritten or reassembled for each target platform.                               |
| **Use Cases**                  | Ideal for general-purpose applications, business software, and large-scale projects.                          | Suited for hardware-specific tasks, like device drivers or embedded systems.                           |
| **Ease of Learning**           | Easier to learn and use; abstracts away hardware complexities.                                                 | Requires a deep understanding of the specific processor, architecture, and operating system.           |
| **Examples**                   | Java, Python, C++, and other general-purpose programming languages.                                            | Assembly for Intel IA-32, ARM assembly language, Motorola 68x00 assembly.                              |

---

### Criteria When Determining 
The following are the factors to consider when deciding whether to implement a language as a compiler or interpreter. 

1. Execution efficiency: Compiler is preferable otherwise interpreter
2. Environments: Compiler is more suitable for production environment while interpreter is for training
3. Available main memory: Compiler is for unlimited memory while interpreter for limited memory
4. Debugging and diagnostic support: use compiler If production is critical otherwise use interpreter
5. Detection of all translation errors: Compiler if guarantee of program is of prime concern otherwise use interpreter.

## Compilation Process
1. Lexical analysis
2. Syntactic analysis
3. Semantic analysis
4. Code generation


Questions:
1. Explain why codes in assembly language that runs on machine A will not run on equivalent machine B
2. In terms of speed and execution efficiency what are the necessary factors for consideration when thinking of implementing a language using a compiler, interpreter, and assembler.
3. State clearly the relationship that exist in terms of old translation between compiler to machine language, interpreter to machine language, and assembler to machine language


#### Lexical Analysis
Lexical analyzer or scanner is a program that scans through  the character of a source program from left to right and generate the tokens (smallest unit of any lanugage) for the programs.

This is the first step in the compilation process, at the lexical analysis stage, a program called lexical analyzer or scanner, scans the characters of a source program from left to right and builds up the token of a program, The actual procedure of doing this is as follows
1. When a source program is read by the LA, the first character scanned enable a token category to be identified, e.g. scanning a digit first will indicate a token category "literal, LT", an alphabet first will indicated a token category "identifier, ID", the lexical analyzer keeps scanning and concatenating character by character.

The tokens of most languages falls into these categories:
	1. Identifiers of variable names used by programmer
	2. Keywords, e.g. DO, SELECT
	3. Special operators, <,>,=
	4. Delimiters
	5. Literals: e.g. numeric constants, 
	6. Seperators: e.g. blank character, conventional arithmetic operator, delimiters. e.t.c


Token generation is usually by specifing the rules that governs the way that language alphabet symbol can be combined, so that the result will be a token of that language identifier, operators and keyword. 

Generate a token for the following:
```
	10 LET B = 5.3 x 3.2 + A
```

| Steps | Internal Representation(Token) | Value () |
| ----- | ------------------------------ | -------- |
| 1     | LT (LITERAL)                   | 10       |
| 2     | KD (KEYWORD)                   | LET      |
| 3     | ID (IDENTIFIER)                | B        |
| 4     | OP (OPERATOR)                  | =        |
| 5     | LT (LITERAL)                   | 5.3      |
| 6     | OP (OPERATOR)                  | x        |
| 7     | LT(LITERAL)                    | 3.2      |
| 8     | OP (OPERATOR)                  | +        |
| 9     | ID (IDENTIFIER)                | A        |
|       |                                |          |

### Syntax Analysis/Parser

Checks whether the token generated has been generated based on the rules of that language.
In the syntax analysis phase a compiler verifies whether or not the token generated by the token analyzer are grouped according to the syntatic rules of that language. If the tokens in a string are grouped according to the language rules of syntax then the string of the token generated  by the lexical analyzer is accepted as a valid construct. otherwise an error handler is called.
Two issues are involved when designing the syntax analysis phase of the compilation process:
1. All valid constructs of must be specified, and by using these specification a valid program is formed
2. A suitable recognizer will be designed to recognize whether a string of tokens generated by lexical analyzer is a valid construct or not

Examples of syntatic construct:
1. Expression (arithmetic, relational, logical): 2+3 
2. Assignment statement: Let a = 4
3. Declarative statement 
4. loops 

Formation of syntatic entities can be done through the use of BNF (Backus Naur Form). This is a notation for describing the formation of syntatic entities. for a context-free grammar

1. Items enclosed in an angular brackets <> are called syntactic entities or no-terminal (can be further divided) symbols. This can be further broken down to terminal symbols as shown by the grammar
2. in BNF this symbols ::= or -> is used to denote "may be replaced by"  or " may be defined by" 
3. in BNF this symbol `|` mean or
4. `[]` used to delimiting optional text
5. `()` for grouping terms

<calculation> ::= <expression>
<expression> :: = <value><operator><expression>
<value> ::= <signed><unsigned>
<unsigned>::= <digit><unsigned>
<digit> ::= 0|1|2|3|4....
<signed>::=+|-
<operator>::= +|-|*|=

BNF for PRINT statement:
Consider an example that defines 

<PRINT> ::= <expression>

