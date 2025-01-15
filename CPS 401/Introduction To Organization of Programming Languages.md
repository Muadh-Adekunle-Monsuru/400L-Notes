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
### **8. Free & Fixed field format**
A language syntax is free field if program statement can be written anywhere on an input line without regard for positioning on the lines or breaks between them. While a fixed field syntax uses the positioning on an input line 

### **9. Expressions**
These are functions that access data objects in a program and return some value. Expressions are the basic syntactic building blocks from which statements are built.

### **10. Statements**
Statements are the most prominent syntactic components in imperative languages their syntax has a critical effect on the overall regularity, readability and writability of the language.

Types of statements:
1. Simple Statements
2. Structured/Nested Statements

---
## **Programming Paradigms**
- **Imperative or Procedural**: Procedural, state-modifying languages (e.g., C, Java) They are command driven or statement oriented languages where a program consists of a sequence of statements and the execution of each statement causes the computer change the value of one or more location in the memory at any point in time.
- **Functional or Applicative**: Stateless computation using recursion and function application (e.g., Haskell, O-Caml) More emphasis are given to the function than the program it represents rather than just the state changes, as the program executes, statement by statement till execution, instead of looking at a sequence of state that the machine must pass through in achieving an answer we look at the function that must be applied to the initial machine state by accessing the initial set of variables and combine them in a way that list to the problem solution.
- **Logic-Based or Rule-Based**: Uses rules and logical inference for computation (e.g., Prolog). Checks for the presence of certain enabling conditions and when found present it executes appropriate actions. We can define rule-based languages as a set of filters which we apply to data storage and enabling conditions to determine the order of execution
- **Dynamic/Scripting**: Quick prototyping and ease of use (e.g., Python, Ruby).
- **Object-Oriented:** This is an approach that provides a way of modularizing programs by creating partitioned memory layer for both data and functions that can be used as templates for creating copies of such modules on demand. This allows the composition of a problem into a number of entities called objects and then builds data and functions around these objects
- **Concurrent:** The fundamental concepts of  concurrent programming is the notion of a process. The process corresponds to a sequential computation with its own thread of control. Sequential processes are used to study concurrency


Features of OOP:
1. **Encapsulation**: Also known as information hiding is simply packing things together in a well defined programming unit. When information is encapsulated in an abstraction it means that the users of the abstraction do not need to know the hidden information to use this abstraction. And they are not permitted to directly us or manipulate hidden information even if they desire. The process of encapsulation is accomplished by hiding of the internal state of an objects and methods from external access. Encapsulation can also refer to the isolation of the operational details of a procedure from the environment where it is used. Encapsulation is an essential criteria for abstraction and it permits necessary details of implementation to be encapsulated within an object. 
2. **Data Abstraction:** An abstract data type is defined as collection of data strucutres abstracted into a simple datatype. It can also be defined as a set of data object ordinarily using on or more type definitions. Among the forms of abstractions are data types, procedures, modules and objects. For example a stack as user data-type defined can be represented in an array with the top index as a linked list
3. **Inheritance**: To inherit a class of object you are simply to incorperate the definition of one class into another class by using some specific keywords and rerserver words. When a class implements an interface that inherits another interface, it must provide full implementation for all the methods defined within the interface-inheritance chain
4. **Polymorphism**: In connection with polymorphism when an object receives a message, it will search its structure class to see if there is a method associated with the received message. If not the super class of the object is required and so on until the either a method is found for the message or a class is reached that has no super class. 
	1.  **Pure polymorphism**:  There is one function and a number of interpretations also the program uses polymorphism whenever functions in different classes have the same structure but different in the interpretation of the function body 
	2. **Ad-hoc polymorphism:** also called **overloading**   occurs when there is a number of different functions all denoted by the same name and function. It allows the operator to specify its actions without knowing the type of object
5. **Extensibility:** The policy of being designed in a way to allow the addition of new capabilities of functionality at any point in time during the process of software development

Basic Concepts of OOP:
1. Emphasis are on data rather than procedure
2. Programs are divided into what are known as object
3. Data structure are designed such that they charactirize the objects
4. Functions that operate on the data of object are tied together in the data structure
5. Data are hidden and cannot be accessed by external functions
6. Object may communicate with each other through functions
7. New data and functions can be easily added whenever necessary
8. Follows bottom up approach

Why all those programming languages:
- Not every language is perfect for every task
- advance in hardware