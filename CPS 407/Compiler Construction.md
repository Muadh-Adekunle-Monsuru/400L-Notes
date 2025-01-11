
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

### Lexical Analysis

**Lexical Analyzer or Scanner**:  
A lexical analyzer is a program that scans through the characters of a source program from left to right and generates tokens (the smallest units of any language) for the program.  

This is the first step in the compilation process. At the lexical analysis stage, a program called a lexical analyzer or scanner scans the characters of a source program from left to right and builds up the tokens of the program. The procedure is as follows:

1. When a source program is read by the lexical analyzer (LA), the first character scanned enables a token category to be identified:  
   - Scanning a digit first indicates a token category like **"literal (LT)"**.  
   - Scanning an alphabet first indicates a token category like **"identifier (ID)"**.  
   The lexical analyzer continues scanning and concatenating character by character.  

**Token Categories in Most Programming Languages**:  
1. **Identifiers**: Variable names used by the programmer.  
2. **Keywords**: Predefined words like `DO`, `SELECT`.  
3. **Special Operators**: Symbols like `<`, `>`, `=`.  
4. **Delimiters**: Characters like `,`, `;`.  
5. **Literals**: Numeric constants, strings, etc.  
6. **Separators**: Blank characters, arithmetic operators, delimiters, etc.  

**Token Generation**:  
Token generation is done by specifying the rules governing how language alphabet symbols can be combined to form valid tokens such as identifiers, operators, and keywords.  

**Example Token Generation**:
For the statement:  
``` 
10 LET B = 5.3 x 3.2 + A  
```

| **Step** | **Token Category**        | **Value** |
|----------|----------------------------|-----------|
| 1        | LT (Literal)               | 10        |
| 2        | KD (Keyword)               | LET       |
| 3        | ID (Identifier)            | B         |
| 4        | OP (Operator)              | =         |
| 5        | LT (Literal)               | 5.3       |
| 6        | OP (Operator)              | x         |
| 7        | LT (Literal)               | 3.2       |
| 8        | OP (Operator)              | +         |
| 9        | ID (Identifier)            | A         |

---

### Syntax Analysis (Parser)

**Purpose**:  
The syntax analysis phase ensures the tokens generated during lexical analysis are grouped according to the syntactic rules of the programming language.  

- If the tokens are grouped correctly, the string of tokens is accepted as a valid construct.  
- If not, an error handler is invoked.  

**Key Design Considerations for Syntax Analysis**:  
1. All valid constructs of the language must be specified to form valid programs.  
2. A recognizer should be designed to verify if the string of tokens generated by the lexical analyzer forms a valid construct.  

**Examples of Syntactic Constructs**:  
1. **Expressions**: Arithmetic, relational, logical (e.g., `2 + 3`).  
2. **Assignment Statements**: (e.g., `LET A = 4`).  
3. **Declarative Statements**.  
4. **Loops**: Iterative constructs.  

---

**Formation of Syntactic Entities Using BNF (Backus-Naur Form)**:  
BNF is a notation used to describe the formation of syntactic entities in a context-free grammar.  

**Key Symbols in BNF**:  
1. `< >`: Denotes syntactic entities or non-terminal symbols (can be further divided).  
2. `::= or ->`: Indicates "may be replaced by" or "may be defined by".  
3. `|`: Represents "or".  
4. `[]`: Encloses optional text.  
5. `()`: Groups terms.  

**Example Grammar**:  

```  
<calculation> ::= <expression>  
<expression> ::= <value> <operator> <expression>  
<value> ::= <signed> <unsigned>  
<unsigned> ::= <digit> <unsigned>  
<digit> ::= 0 | 1 | 2 | 3 | 4 | ...  
<signed> ::= + | -  
<operator> ::= + | - | * | =  
```  

**BNF for PRINT Statement**:  
```  
<PRINT> ::= <expression>  
```  


---
## Symbol Table
It is a data structure used in programming languages. It is used to store information about identifiers. Identifiers could be a variable, functions, classes and object names the aim is to act as a central repository for information about the symbols in the program. The information collected in a symbol table is used in semantic analysis.

#### Various approaches to symbol table organization
1. Linear List: The linear list of record is the easisiest way to implement a symbol table. The new names are added to the table in the order they arrive. Whenever a new name is to be added to the table, the table is first searched linearly or sequentially to check whether the name is present or not then the record for the new name is created and added to the list
2. **Search Tree**: Has two links (left and right) and has the property of alphabetical accessibility, that is all the names that precedes the name 1 in alphabetical order will be accessible from name 1 by following the left link, similarly, all the names that follows name 1 in alphabetical order will be accessible from name 1 by following the right link. It is a more efficient approach to symbol table organization
3. **Hash Table:** Hash function is a formula or algorithm designed to convert input data into a numerical value(has code) the hash code is used to determine the location (index) of the corresponding value in the hash table

#### Parsing
Definition:
	This is a stage in program compilation that maps from the linear strings of the program text into a tree structure. It is the process of analyzing a string of symbols according to production rules or rules of formal **grammar** (a set of rules defining the syntax of a language) 
Parsing Method
Top-down: Method of parsing in which the parser starts from the start symbol of a grammar and tries to construct the past tree by progressively expanding non-terminal symbols down to terminal symbols. Uses the production rule of the grammar to break the input string into smaller components.
Backtracking:

Consider the topdown parsing for the following grammar,
```
S=aAb
A = cd | c
the input string is w = acb
```

describe the parsing tree using topdown parsing

1. Start with the start symbol S from the production rule That is S to ab
2. Expand A according to the grammar, a could be expanded to `A to cd` or `A to c`
3. Match A to c, so S is now acb, now the input string is completely consumed
Note: if the parse fails to match a leaf 

Bottom-Up: It is a parsing technique that construct the past tree for a given input string by starting from the leaf node, (input token) and walking it s way up to the start symbol of the grammar. The approach is also called shift reduced parsing.
& implies empty string

Consider the bottom up parsing for the following grammar:

```
S-> aABe
A-> Abc | b
B-> d
 input string is abbcde
```

Steps:
1. Start from b-> A or A-> b
2. Expand A to abc
3. Expand B to d
4. Expand S to be aABe


|                      | Top down                                               | Bottom Up                                                     |
| -------------------- | ------------------------------------------------------ | ------------------------------------------------------------- |
| Direction of Parsing | Parses from the start symbol towards the input string  | Parses from the input string back to the start symbol         |
| Construction         | It builds the parse tree staring from the root         | Builds the parse three starting from the leafs                |
| Input Handling       | It matches production rules with input from left-right | Reduces input symbols to non-terminal using the grammar rules |
| Error Handling       | Easier to implement error reporting and recovery       | More complex error handling mechanism                         |
|                      |                                                        |                                                               |

---
## Semantic Analysis
It is the phase in the compiler design process that checks the meaning and consistency of a program by analyzing its syntax tree or intermediate representation. It ensure that the programs adheres to the rules and constraints of the programming languages

Parse Tree / Syntax Tree: One intermidate form of an arithmetic statement is the parse tree, also called syntax tree or binary tree. The rules of converting an arithmetic statement into a parse three are:
1. Any variable is a terminal node of the tree
2. For every operator, construct (in the order dictated by the rules of algebra) a binary (two branches) tree whose left branch is the operand and whose right branch is the tree for the second operand

expamples of syntax tree
A = B+C
D = A*D+R
Y= A*B -C/D
IF E THEN S1 ELSE S2


Polish Notation: used to represent arithmetic or logical expressions in a manner which specifies simply and exactly the order in which operators are to be evaluated. In this notation operators come immediately after their operands also postfix notation
example
w = x * y +z
w = xy * z +
wxy * z + =

Unary Operator:
They operate only on one operand, one simple way of handling unary operator like unary - `-2` is to write them as a binary operator

```
-B
O-B
OB-
```

```
Z+(-W+Y*X)
Z+(-W + YX*)
Z+(0-W+YX*)
Z+ (0W-+YX*)
Z+(0W-YX*+)
Z0W-YX*++

```