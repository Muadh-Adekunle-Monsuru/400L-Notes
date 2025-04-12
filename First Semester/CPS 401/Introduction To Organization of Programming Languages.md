Languages are classified into:
- **Natural Languages**: languages through which human being communicate with each other, eg Hausa Yoruba, English
- Machine Language: These are languages through which human being communicate with the computer. e.g. Java, Python, C++ e.tc.

 **Reasons why natural languages are complex for computers to understand:**
 1. Complexity
 2. Irregularity
 3. Uneconomical
 4. Limited means of abstraction
 5. Ambiguity


Categories of Programming Languages:
- **Machine Language:** This is the only language a computer understands, because information and data are represented using binary i.e. 0s and 1s
- **Assembly Language:** Information and data are represented using symbols and mnemonics
- **High level Language:** Computer language close to regular English language expression.

##### Translators:

These are programs that converts from other categories of programming languages to its machine language equivalent

Types of Translators:
- **Assembler**: A type of translator that would translate from assembly language to its machine language equivalent.
- **Complier**: A type of translator that would translate high-level language to its machine language equivalent  
	- **Interpreter**: An alternative to a complier.

**Stages involved in solving a programming problem:**
1. Problem definition
2. Devising a suitable method
3. Program coding using suitable programming language. 
4. Compilation and program execution
5. Debugging and testing
6. Documentation
7. Maintenance 

---
Data are raw facts  that can be inform of:
1. **Variable**: Data that changes over time due to calculations during program's execution.
	1. Numeric Variables: variable that are made up of numbers alone. e.g. phone number
	2. Alphanumeric Variable: variable that are made up of combinations of numbers and alphabets. eg matric-no
2. Constants: These are data that are fixed and their value can not change during the execution of the program. E.g. PI: 22/7
	1. Numeric Constants
	2. Alphanumeric Constants


---
21/10/24

**Programs**
Program is a series of instructions meant to direct the computer to perform a given task. A computer program has two basic parts, operation code and the operand.

**Advantages of Machine Language:**
- Most efficient in terms of storage area usage and execution speed
- Machine language allows programmers to fully utilize the computers potential for processing data. 

**Disadvantages of machine language:**
- It is extremely tedious and time consuming 
- Instructions are difficult to remember and use because they are in 0s and 1s
- It is completely machine dependent, and programs written in machine language will execute only on the specific machine for which its written.
- Machine language is totally unstandardized unlike high-level languages.

**Advantages of Assembly Language**:
- Efficient in memory space used and processing time
- Generation of error messages that are useful in debugging 
- Support for modular programming

**Disadvantages of Assembly Language**:
- Cumbersome in usage
- Has a one-one relationship with machine language instructions and the assembly language instructions is translated to one machine language instruction which leads to long program preparation time
- It is machine dependent, leading to a substantial reprogramming when they are changes in the machine.

**Characteristics of a good programming language:**
- Clarity, simplicity and unity
- **Orthogonality**: It refers to the design principle where different operations or components can function independently without affecting each other. It means that changes or actions in one part of a system do not impact other parts. 
- Naturalness of the application
- Support for abstraction
- Ease of program verification
- Program environment
- Portability of the program
- Cost

**Simulators:** these are specialist aides that translates programs to make their coding compatible between different makes of machines. It saves the time for recording procedures.

**Emulator:** When a hardware device is used to hold the simulation program, it is known as the emulator. 

---

## **Syntactic Elements of Programming Languages**

Syntactic elements refer to the set of rules that determine what symbols are considered valid expressions (programs) in a programming language. The general syntactic style of a language is defined by the choice of its various syntactic elements. These elements include:

### 1. **Character Set**
The character set is one of the fundamental choices in designing a language's syntax. It consists of the group of characters allowed in the programming language, including special characters like `\0`. Each language may have its unique character set, or multiple languages may share the same set.

Examples of character sets include:
- **ASCII**: Widely used and includes letters, digits, and special characters.
- **C Character Set**: Compatible with most input/output devices.
- **APL Character Set**: Includes special characters not directly usable on most devices.
  
As the computer industry becomes more global, languages accommodate special characters unique to different countries, such as the Spanish tilde (`~`).

---

### 2. **Identifiers**
Identifiers are strings of letters and digits that must begin with a letter. They are used as names for various program elements such as:
- Variables
- Functions

For example, `studentName` or `calculateSum` are typical identifiers.

---

### 3. **Operator Symbols**
Operators are special symbols or characters used to perform operations. Common examples include:
- Arithmetic Operators: `+`, `-`
- Logical Operators: `&&` (AND), `||` (OR)
- Special Operators: `**` for exponentiation in some languages.

Some languages use a combination of special characters and identifiers for operators, such as `EQ` for equality or `&` for logical operations.

---

### 4. **Keywords and Reserved Words**
- **Keywords**: Identifiers used as fixed parts of a language's syntax, such as `if`, `for`, or `while` in C.
- **Reserved Words**: Keywords that cannot be used as programmer-defined identifiers, making syntactic analysis easier.  

For example:
- In **C**, reserved words are strictly enforced.
- In **FORTRAN**, some keywords like `DO` and `IF` are not reserved, meaning they can be used as programmer-defined identifiers, complicating syntax analysis.

---

### 5. **Noise Words**
Noise words are optional words included in statements to improve readability.  
- Example: In **COBOL**, the `GO TO` statement transfers control within a program.  
  - Syntax: `GO TO LABEL`  
  - Here, `GO` is required, while `TO` is optional and adds no functional information, serving only to improve readability.

---

### 6. **Comments**
Comments are essential for program documentation. Different languages allow comments in various ways:
- In **Basic**, the `REM` statement is used for comments.
- In **C**, comments are enclosed within delimiters like `/* ... */` or begin with `//`.
  
**Caution:** Missing termination markers for comments can cause subsequent statements to be ignored, leading to errors.

---

### 7. **Blank Space**
Rules for the use of blank spaces vary widely among programming languages:
- In **C**, blanks can be used between elements or as separators within strings.
- In other languages, blanks may have stricter or more flexible roles.

---

## **8. Free & Fixed Field Format**
- **Free Field Syntax**: Allows program statements to be written anywhere on an input line without regard to positioning or line breaks.  
- **Fixed Field Syntax**: Requires program statements to follow specific positioning rules on an input line.

---

## **9. Expressions**
- Functions that access data objects and return values.  
- They are the basic building blocks from which statements are constructed.

---

## **10. Statements**
- Key syntactic components in imperative languages that influence regularity, readability, and writability.  

### **Types of Statements**
1. **Simple Statements**  
2. **Structured/Nested Statements**

---

## **Programming Paradigms**
1. **Imperative/Procedural**:  
   - Command-driven languages (e.g., C, Java).  
   - Programs consist of sequential statements that modify memory states.

2. **Functional/Applicative**:  
   - Stateless computation using recursion and function application (e.g., Haskell, OCaml).  
   - Focuses on functions rather than state changes.

3. **Logic-Based/Rule-Based**:  
   - Uses logical rules for computation (e.g., Prolog).  
   - Executes actions based on enabling conditions and rule filters.

4. **Dynamic/Scripting**:  
   - Designed for quick prototyping and ease of use (e.g., Python, Ruby).

5. **Object-Oriented**:  
   - Modularizes programs into objects containing data and functions.  
   - Promotes encapsulation, inheritance, and polymorphism.

6. **Concurrent**:  
   - Focuses on processes with individual threads of control for concurrency.  

---

## **Features of Object-Oriented Programming (OOP)**  
1. **Encapsulation**:  
   - Hides internal object details, exposing only necessary functionality.  
   - Ensures users cannot directly access hidden data.  

2. **Data Abstraction**:  
   - Simplifies complex data structures into abstract data types (e.g., stacks represented as arrays).  

3. **Inheritance**:  
   - Allows a class to inherit attributes and methods from another class.  

4. **Polymorphism**:  
   - Enables methods to have different implementations based on the object.  
     - **Pure Polymorphism**: One function with multiple interpretations.  
     - **Ad-Hoc Polymorphism (Overloading)**: Multiple functions with the same name but different actions.  

5. **Extensibility**:  
   - Allows the addition of new features or functionalities during development.  

---

## **Basic Concepts of OOP**  
1. Emphasizes data over procedures.  
2. Divides programs into objects.  
3. Objects encapsulate data and associated functions.  
4. Data is hidden from external access.  
5. Objects communicate via functions.  
6. New data and functions can be easily added.  
7. Adopts a bottom-up development approach.  

--- 

Why all those programming languages:
- Not every language is perfect for every task
- advance in hardware