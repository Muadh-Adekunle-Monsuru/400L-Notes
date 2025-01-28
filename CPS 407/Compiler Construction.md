
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
### Symbol Table

A **symbol table** is a data structure used in programming languages to store information about identifiers such as variables, functions, classes, and object names. Its primary purpose is to serve as a central repository for information about the symbols in a program. This information is critical during semantic analysis in the compilation process.

---

#### Approaches to Symbol Table Organization

1. **Linear List**  
   - A simple and straightforward implementation of a symbol table.  
   - **Procedure**:  
     - New identifiers are added sequentially in the order they arrive.  
     - Before adding a new identifier, the table is searched linearly to check for duplicates.  
     - If not found, a new record for the identifier is created and appended to the list.  
   - **Example**:  
     Consider identifiers `x, y, z`. A search for `z` will require scanning through `x` and `y` sequentially.

2. **Search Tree**  
   - Implements a binary search tree where each node contains an identifier.  
   - **Characteristics**:  
     - Each node has two links: left and right.  
     - Identifiers are arranged alphabetically.  
     - Identifiers preceding the current node alphabetically are accessible via the left link, while succeeding identifiers are via the right link.  
   - **Example**:  
     For identifiers `d, b, f, a`, the search tree structure is:  
     ```
            d
          /   \
         b     f
        /
       a
     ```

3. **Hash Table**  
   - A highly efficient method for symbol table organization using a hash function.  
   - **Process**:  
     - A hash function converts an identifier into a numerical value (hash code).  
     - The hash code determines the index where the identifier is stored in the table.  
   - **Example**:  
     If `hash("x") = 2`, identifier `x` is stored at index 2 in the table.

---

### Parsing

**Definition**: Parsing is a stage in program compilation where the program's linear text is analyzed to construct a tree structure, mapping symbols to rules of formal grammar.

---

#### Parsing Methods

1. **Top-Down Parsing**  
   - Starts with the start symbol of a grammar and expands it into terminal symbols using production rules.  
   - **Example** (Top-Down Parsing for Grammar):  
     ```
     S → aAb
     A → cd | c
     ```
     Input String: `w = acb`  
     **Steps**:  
     - Start with `S → aAb`.  
     - Expand `A` using `A → c`. Now, `S = acb`.  
     - Match input with the parse tree.  

2. **Bottom-Up Parsing**  
   - Starts with terminal symbols (input tokens) and works upwards to construct the parse tree.  
   - **Example** (Bottom-Up Parsing for Grammar):  
     ```
     S → aABe
     A → Abc | b
     B → d
     ```
     Input String: `abbcde`  
     **Steps**:  
     - Reduce `b` to `A`.  
     - Expand `A` to `Abc`.  
     - Reduce `B` to `d`.  
     - Reduce to `S → aABe`.

---

| **Aspect**         | **Top-Down Parsing**                             | **Bottom-Up Parsing**                                       |
| ------------------ | ------------------------------------------------ | ----------------------------------------------------------- |
| **Direction**      | From start symbol to input token                 | From input token (terminal symbol) back to the start symbol |
| **Construction**   | Starts from the root of the parse tree           | Starts from the leaf nodes of the parse tree                |
| **Input Handling** | Matches production rules left-to-right           | Reduces input symbols to non-terminals using grammar rules  |
| **Error Handling** | Easier to implement error reporting and recovery | More complex error handling                                 |

---

### Semantic Analysis

**Definition**:  
Semantic analysis is a phase in compiler design where the syntax tree or intermediate representation of a program is analyzed to check its meaning and consistency according to the rules of the programming language.

---

#### Parse Tree / Syntax Tree  
A **parse tree** represents the syntactic structure of a statement. It is also referred to as a **syntax tree** or **binary tree**.

**Rules for Construction**:  
1. Variables are terminal nodes.  
2. Operators form binary trees with their operands as branches.  

**Examples**:  
- Arithmetic Statement: `A = B + C`  
  ```
      =
     / \
    A   +
       / \
      B   C
  ```
- Logical Statement: `IF E THEN S1 ELSE S2`  
  ```
       IF
      /  \
     E    THEN
         /   \
       S1    ELSE
             /   \
           S2
  ```

---

#### Polish Notation  
**Definition**:  
A notation used to represent arithmetic or logical expressions, where operators are placed after their operands. Also called **postfix notation**.  

**Example**:  
Expression: `w = x * y + z`  
- In Polish Notation: `w = xy*z+`  

---

#### Unary Operator  
Unary operators operate on a single operand. They can be handled as binary operators with specific rules.  

**Example**:  
Expression: `Z + (-W + Y * X)`  
1. Convert unary operator `-` to binary format:  
   ```
   Z + (0 - W + Y * X)
   ```
2. Polish Notation Conversion:  
   ```
   Z 0 W - Y X * + +
   ```  