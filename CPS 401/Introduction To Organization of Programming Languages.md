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
## Syntatic Elements of Programming Langauges










Is a set OF RULES THAT DETERMINES WHAT SYMBOLS ARE CONSIDERED TO BE VALID EXPRESSION (PROGRAM) IN THE LANGUAGE. The general syntactic style of the langugue is set by the choice of the various syntactic elements. The different synthetic elements are:

- **Character set:** The choice of character set are one of the first choices to be made in designing language syntax the character set is nothing but group of characters which are allowed in programming language, including special characters such as "\o", each language may have its own character set or many language may share the same character set. Many different character sets,e.g. ASCII, each containing different sets of special characters in addition to the basic letters and digits. C character set is available on most input/output equipment, however APL character set cannot be used directly on most input output device. Today the computer industry is getting more international. different countries has their own speical character in the set such as spanish tidle(~)
- **Identifiers:** It is a string of letters and digits beginning with letters these are names that are given to various programs elements, such as variables, functions, 
- operator symbols: Most language use the special character + and - to represent the two basic arithmetic operations. Primitive operations may be represented entirely by special characters like APL. Some langauges adopt some combination of some special characters for some operators (&) and identifiers. EQ for equality and  ** for exponential 
-  **Keywords and reserved words**: A keyword is an identifier used as a fixed part of the syntax of a statement. E.g. "IF": begins a C conditional statement, "for" begins an iterative statement. A keyword is a reserved word if it is not used as a programmer chosen identifier. Syntatic analysis during translation is made easy by using reserve words. C uses the reserve words heavily while fortran makes syntactic analysis difficult. In this, "DO" and "IF" statements are not reserved words used for iterative and condition checking, they can be used as programmer defined identifiers. 
- **Noise Words**: These are optional words that are inserted in statements to improve readability. E.g in COBOL the "GO TO" statement transfer control within the program. It is written as "GO TO LABEL" where GO is required and TO is optional ,it carries no information and is only used to improve readability. 
- Comments: Inclusion of comments in a program is an important part of its documentation, a language will allow comments in several ways basic programming takes REM Statement as a separate comment line in a program. Delimited by special marker such as 'C', '/*', '&', */* the disadvantage is a missing termination delimited on comments will turn the following statements into comments and there will not be translated and executed.
- Blank Space: This rules on the use of blanks varies wide across languages. In C blanks are used with characters and string data and separators between elements or statements. 

