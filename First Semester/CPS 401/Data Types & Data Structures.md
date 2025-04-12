### Basic Data Types
1. **Primitive Data Types:**
   - **Integer:**  
     Programming languages provide various sizes or ranges for integers. For example:  
     - **C++/Java:**  
       - `short` (2 bytes in Java)  
       - `int` (4 bytes in Java)  
       - `long` (8 bytes in Java)  
     - Java also includes a `byte` type (1 byte).  
     - In C++, `char` is considered an integer type, allowing numerical operations. Many languages use two's complement notation for representing negatives.

   - **Float:**  
     Floating-point numbers come in various sizes and formats. A floating-point number typically consists of:
       - **Sign**
       - **Fraction**
       - **Exponent**  
     - **IEEE Floating-Point Standard:**  
       - In C++/Java:  
         - `float` (4 bytes in Java):  
        - `double` (8 bytes in Java):  
    - Special patterns like `NaN` or `Infinity` are represented using specific bit configurations.

   - **Boolean:**  
     Represents one of two states: `true` or `false`.  
     - **C:** No boolean type. `0` is used as `false` and non-zero as `true`.  
     - **C++:** Supports boolean type.  
     - **Java:** Includes a `boolean` type with no conversion allowed between `int` and `boolean`.  
     - Implementation often uses the smallest accessible memory unit (e.g., 1 byte), even though a single bit could theoretically suffice.

     Example in C++:  
     ```cpp
     bool equal = (x == y); // true if x equals y.
     ```

   - **Char:**  
     Stores a numeric code for characters:
     - **C++:** Uses ASCII encoding.  
     - **Java:** Uses Unicode encoding.  
     - In C++, `char` is considered an integer type, so numerical operations can be performed on it.

2. **Heap Management:**
   - A **heap** is a dynamic memory storage area.
   - **Pointers** access memory locations in the heap.  
   - The heap is divided into equal-sized cells, each with a pointer. These pointers organize the heap as a linked list.

   **Memory Management:**
   - A pointer tracks the "head" of the free list.
   - To allocate space:  
     - Take from the front of the free list.
   - To deallocate:  
     - Add back to the front of the free list.

3. **Complex Data Types:**  
   - Examples include `string`, `enumeration`, `subrange`, and `array`.

4. **Expressions and Assignment:**  
   - Involves the evaluation of values and their assignment to variables.

---

### Pointer Problems
Returning memory to the free list is straightforward, but challenges arise when a reference to the memory persists after deallocation.
dangling reference: memory deallocation, but still have a pointer to it.

**Example in C++:**  
```cpp
int *Foo() {
    int x = 5;
    return &x; // Returns the address of a stack memory location.
}
```
- The `&` operator provides access to stack memory that may already be reclaimed.  
- **Java:** Does not face this issue as it lacks the `&` operator equivalent.

--- 

Garbage reference: Pointer is destroyed by memory has not been deallocated

```C++
void Bar(){
Date today = new Date();
}
```

Two techniques in reclaiming heap memory:
1. Reference count: Along with each heap element stores a reference count
	1. Indicated the number of pointer to the heaps element
	2. When space is allocated its reference count is set to 1
	3. Each time a new pointer is set to it increment the reference count
	4. Each time a pointer is lost decrement the reference count 
	5. reference count provides a simple method for avoiding garbage and dangling reference 
		1. If result of an operation leaves reference count at 0, reclaim memory
		2. It can even doubt check explicit deallocations
2. Garbage collection