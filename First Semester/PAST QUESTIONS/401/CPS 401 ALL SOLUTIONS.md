![[401 test.jpeg]]
### 1. Why do we need to study programming languages?
- To understand how computers execute instructions.
- To develop efficient and maintainable software.
- To improve problem-solving skills and logical thinking.
- To choose the most appropriate language for a specific application.

### 2. Briefly explain linear data structures and non-linear data structures with appropriate examples.

**Linear Data Structures:**
- Elements are arranged sequentially.
- Examples: 
  - **Array**: A list of integers `[1, 2, 3]`.
  - **Linked List**: Nodes connected in a chain.
  - **Queue**: First In, First Out (e.g., ticket booking queue).
  - **Stack**: Last In, First Out (e.g., undo operations in text editors).

**Non-Linear Data Structures:**
- Elements are not arranged sequentially.
- Examples:
  - **Tree**: Hierarchical structure (e.g., file system).
  - **Graph**: Nodes connected by edges (e.g., social networks).


### 3. Define Data Types and give the basic data types that you know with examples.

**Definition:**
- Data types specify the type of data a variable can hold.

**Basic Data Types:**
1. **Integer (int):** Holds whole numbers. Example: `5`
2. **Float:** Holds decimal numbers. Example: `3.14`
3. **Character (char):** Holds a single character. Example: `'A'`
4. **String:** Holds sequences of characters. Example: `"Hello"`
5. **Boolean:** Holds true/false values. Example: `True`

### 4. What is the relationship between data type and variable?
- A variable is a container that holds data.
- The data type defines the type of data the variable can store.
  - Example: `int x = 10;` Here, `x` is a variable of type `int`.

### 5. Define a subprogram.
- A subprogram is a self-contained block of code designed to perform a specific task within a program.
- Examples: Functions, Procedures.

### 6. What are the characteristics of a subprogram in a program?
- **Reusable:** Can be called multiple times.
- **Encapsulated:** Has its own local variables and scope.
- **Modular:** Makes the program more organized and readable.
- **Takes Inputs and Returns Outputs:** Can process data using parameters and return results.

### 7. In most languages, keywords like `begin` and `while` are reserved and may not be used as identifiers. Other languages do not have reserved keywords. What are the advantages and disadvantages of reserved words?

**Advantages:**
- Avoids ambiguity in the program.
- Makes the language syntax consistent and clear.

**Disadvantages:**
- Reduces flexibility in naming variables or identifiers.

### 8. Explain the term Garbage Collection and two (2) common approaches to garbage collection.

**Definition:**
- Garbage Collection is the process of automatically reclaiming memory that is no longer in use to free up resources for other tasks.

**Approaches:**
1. **Reference Counting:**
   - Keeps a count of references to an object.
   - Object is deleted when the reference count drops to zero.
   - Example: Python uses this approach.

2. **Mark-and-Sweep:**
   - Identifies reachable objects starting from root nodes.
   - Unreachable objects are collected as garbage.

---

![[401_1 2023.jpeg]]

### **Question One**
**(a) Write briefly on "APPLETS."**
- Applets are small Java programs that can run in a web browser or applet viewer.
- Typically embedded in HTML pages.
- Often used for interactive features, animations, or small applications on websites.

**(b) Write briefly on Assembly Language.**
- Assembly language is a low-level programming language that provides symbolic representations of machine code instructions.
- It is hardware-specific and allows direct manipulation of hardware resources.

**(c) Highlight three (3) merits of Assembly Language.**
- Efficient in memory space used and processing time
- Generation of error messages that are useful in debugging 
- Support for modular programming


**(d) Highlight three (3) demerits of Assembly Language.**
1. Difficult to learn and debug.
2. Lack of portability between different hardware architectures.
3. Requires more development time compared to high-level languages.

**(e) Explain how syntax affects the overall regularity, readability, and writability of a language.**
- **Regularity:** A consistent syntax ensures that the rules are predictable, reducing complexity.
- **Readability:** Intuitive syntax makes code easier for programmers to understand.
- **Writability:** Clear and consistent syntax allows developers to write code faster and with fewer errors.

### **Question Two**
**(a) Explain computer program and state its basic components.**
- A computer program is a sequence of instructions written in a programming language that tells a computer what to do.
- **Basic Components:**
	1. Operation Code
	2. Operand

**(b) Highlight two (2) merits of Machine Language.**
- Most efficient in terms of storage area usage and execution speed
- Machine language allows programmers to fully utilize the computers potential for processing data.

**(c) Highlight four (4) demerits of Machine Language.**
- It is extremely tedious and time consuming 
- Instructions are difficult to remember and use because they are in 0s and 1s
- It is completely machine dependent, and programs written in machine language will execute only on the specific machine for which its written.
- Machine language is totally unstandardized unlike high-level languages.

**(d) Describe an abnormal condition that arises in a code sequence at runtime.**
- **Runtime Error:** Occurs when a program executes an illegal operation, such as division by zero, accessing invalid memory, or type mismatch.
### **Question Three**
**(a) What makes a good programming language acceptable?**
- Clarity, simplicity and unity
- Orthogonality 
- Naturalness of the application
- Support for abstraction
- Ease of program verification
- Program environment
- Portability of the program
- Cost

**(b) Differentiate between constant and variable.**
- **Constant:** A fixed value that does not change during program execution. Example: `PI = 3.14`.
- **Variable:** A memory location whose value can change during program execution. Example: `x = 5`.

### **Question Four**
**(a) Write briefly on Object-Oriented Programming (OOP).**
- OOP is a programming paradigm based on objects that contain both data and methods.
- Promotes modularity, code reusability, and abstraction.

**(b) Explain the concepts a programming language must support before it can be considered to be object-based.**
1. **Encapsulation:** Combining data and methods within objects.
2. **Abstraction:** Hiding implementation details from users.
3. **Inheritance:** Reusing properties and methods of a parent class in a child class.
4. **Polymorphism:** Using a single interface to represent multiple types.

### **Question Five**
**(a) Write briefly on "Classes" in programming.**
- A class is a blueprint for creating objects in OOP, defining their attributes (data) and behaviors (methods).

**(b) Classes programming can have several different forms of responsibility. Explain each.**
1. **Data Encapsulation:** Organizing related data and methods.
2. **Reusability:** Creating reusable components.
3. **Inheritance:** Facilitating code reuse by extending existing classes.
4. **Polymorphism:** Allowing methods to behave differently based on object types.

**(c) What do you understand by Translator?**
- A translator converts code written in one programming language into another.
- Types: Compiler, Interpreter, Assembler.

### **Question Six**
**(a) Write briefly on "Messages" in programming.**
- Messages are a mechanism in OOP where objects communicate by calling each other’s methods.

**(b) Highlight and discuss each of the three (3) categories of messages in programming.**
1. **Synchronous Messages:** Sender waits for a response.
2. **Asynchronous Messages:** Sender continues without waiting.
3. **Broadcast Messages:** Sent to multiple objects simultaneously.

**(c) Substantiate with reasons why natural languages are complex for computers to understand.**
 1. Complexity
 2. Irregularity
 3. Uneconomical
 4. Limited means of abstraction
 5. Ambiguity

---

![[WhatsApp Image 2025-02-06 at 7.55.01 PM.jpeg]]

### **Question One**
(a) **Describe Imperative Programming Language.**  
Imperative programming is a programming paradigm that uses statements to change a program's state. It focuses on describing how a program operates by specifying sequences of instructions that the computer must execute. Examples include C, Java, and Python.

(b) **What is an Assembly Language?**  
Assembly language is a low-level programming language that is closely related to machine code but uses symbolic instructions (mnemonics) instead of binary. It is specific to a computer architecture and requires an assembler to translate it into machine code.

(e) **Statements are one of the most prominent syntactic components in imperative languages. Explain how their syntax has a critical effect on the overall regularity, readability, and writability of the language.**  
Statements define the structure and flow of an imperative program. Clear and well-structured syntax improves readability by making code easier to understand. Regularity in syntax ensures consistency, making learning and debugging easier. Writability is enhanced when syntax is intuitive and minimal, reducing the effort required to express logic.

---

### **Question Two**
(a) **Describe Applicative Programming Language.**  
An applicative programming language, also known as a functional programming language, is based on the application of functions rather than changing state or mutable data. It relies on mathematical functions and avoids side effects. Examples include Haskell and Lisp.

(c) **What is a Machine Language?**  
Machine language is the lowest-level programming language, consisting of binary instructions (0s and 1s) that a computer’s CPU can directly execute.
### **Question Three**
(a) **What are the Syntactic Elements of a Programming Language?**  
Syntactic elements refer to the set of rules that determine what symbols are considered valid expressions (programs) in a programming language. The general syntactic style of a language is defined by the choice of its various syntactic elements.  They include:  
1. Character set
2. Identifiers
3. Operator Symbols
4. Keywords and Reserved Words
5. Noise Words
6. Comments
7. Blank Space
8. Free & Fixed field Format
9. Expressions
10. Statements
(b) **Differentiate between Constant and Variable.**  
- **Constant:** A fixed value that does not change during program execution (e.g., `PI = 3.1416`).  
- **Variable:** A named storage location whose value can change during execution (e.g., `x = 10; x = x + 5`).

---

### **Question Four**
(a) **Write briefly on Object-Oriented Programming (OOP).**  
Object-Oriented Programming (OOP) is a paradigm based on the concept of objects, which encapsulate data and behavior. It promotes modularity, reusability, and abstraction using principles like encapsulation, inheritance, and polymorphism. Examples include Java, Python, and C++.

(b) **Discuss each of the stages involved in solving a programming problem.**  
1. **Problem Definition** – Understanding the requirements.  
2. Devising a suitable method  
3. **Program Coding** – Creating algorithms and flowcharts.  
4. **Compilation and Program Execution** – Writing code in a programming language.  
5. **Testing & Debugging** – Finding and fixing errors.  
6. **Documentation**   
7. **Maintenance** – Updating and improving over time.

---

### **Question Five**
(a) **Explain each of the features of Object-Oriented Programming.**  
1. **Encapsulation** – Bundling data and methods within objects.  
2. **Inheritance** – Allowing one class to derive properties from another.  
3. **Polymorphism** – Enabling multiple methods to have the same name with different implementations.  
4. **Abstraction** – Hiding implementation details and exposing only necessary functionality.
5. Extensibility

(b) **What do you understand by Translator?**  
A translator is a program that converts code from one language to another. It can be:  
- **Compiler** – Converts entire code to machine language at once.  
- **Interpreter** – Converts and executes line by line.  
- **Assembler** – Converts assembly language to machine code.

---

### **Question Six**
(a) **Describe each of the following programming language paradigms:**  
(i) **Rule-Based Languages:** These languages follow a set of rules to derive conclusions. They are commonly used in AI and expert systems. Examples include Prolog and CLIPS.  

(ii) **Concurrent Languages:** These languages support concurrent execution, allowing multiple tasks to run simultaneously. They are used in parallel computing and real-time systems. Examples include Java (multithreading) and Erlang.

(b) **Explain the reasons why natural languages are complex for computers to understand.**  
1. **Ambiguity** – Words and sentences can have multiple meanings.  
2. **Irregularity** – Meaning changes based on context.  
3. **Uneconomical** – Variability in sentence structures.  
4. Limited means of abstraction  
5. Complexity