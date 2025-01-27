#### Notes:
- Assignment 2 focuses more about Memory Management
- In C++, there is no memory (model) specification, it depends on the Programmer/Developer
- Additional study links:
    - C++ References, Memory Address: [https://www.w3schools.com/cpp/cpp_references.asp, https://www.w3schools.com/cpp/cpp_references_memory.asp]
    - C++ Pointers: [https://www.w3schools.com/cpp/cpp_pointers.asp]

#### Reminder Notes:
- Midterm Practice Test is out (review)
- Assignment 1:
    - Panel notes: if it starts at 0, it ends at 99 not 100 (no overlap)

## Overview
1. Areas of Memory Allocation | Focus: Stack and Heap
2. Pointers
3. Memory Allocation
4. Dynamic Arrays

# 1. Four (4) Areas of Memory Allocation
- *OS allocates 4 areas of memory on program start-up*

    ### 1.1 Function Call Stack (Stack)
    - stores function's local variables and data (meta-data) 
    - stores **statically allocated memory**
    - stack frames (SF):
        - when a function is called: SF is pushed onto the call stack
        - when a function returns: SF is popped off
    - keeps track of functions called and the order in which they are called

    **Stack** is a data structure that follows **LIFO (last-in, first-out)**
        - e.g., pile of dishes
    - pushing (add)
    - popping (remove)

    ### 1.2 Heap
    - stores **dynamically allocated memory**
    - allocation that happens at *runtime* => using *new* keyword
    - is part of the data segment
    - this memory is managed by the programmer
        - whereby, we must *delete* it at some point

 
    ### 1.3 Data Segment
    - global variables
    - static variables
    - literals

    ### 1.4 Code/Text Segment    
    - program instructions and function addresses

    ## Static Memory
    - memory is deleted for us when the context is exited (default deletion)
        - containing object is *deleted*

    ## Dynamic Memory
    - reserved/goes to the **Heap**
    - uses **new** keyword which returns a pointer (memory address from the heap)
    - we must **explicitly delete**
    - static comparison, here, lifespan does NOT depend on the context's lifespan (exited or destroyed)
    ```C++
    int* x = new int;
    Student* stu = new Student;
    ```

# 2. Pointers
- is a variable that stores **memory address** as its value
- example:
    ```C++
    string food = "Pizza"; // A food variable of type string
    cout << food;  // Outputs the value of food (Pizza)
    cout << &food; // Outputs the memory address of food (0x6dfed4)

    string* ptr = &food;    // A pointer variable, with the name ptr, that stores the address of food    
    cout << ptr << "\n"; // Output the memory address of food with the pointer (0x6dfed4)

    ```
- **necessary for dynamic allocation**  => *new* keyword, wehere *new* returns a pointer
### Why use Pointers?
- small fixed size of 8 bytes => easy to pass
- easy way to avoid copy of data
    #### Pointers have:
    - Name, Data Type, Value, Memory location
        
        *Note:*
        ```C++
        char* cptr;         // Valid: 1 name
        char *cptr, c;      // Also valid, 2 names with 1 type char
        // cptr is a pointer, c is not
        ```
- use: it is easier to copy a pointer than to copy a whole Class


### 3 Components of Pointer Declaration
- type of data being pointed to
- the * symbol indicating that it is a pointer
- the  variable name

    #### 3 ways of Declaring a Pointer
    ```C++
    string* mystring; // Preferred
    string *mystring;
    string * mystring;
    ```

### Pointers can recieve a Value of:
- memory address, or
- system call (for new block of memory)

### & => "address-of" operator
- **& returns the memory location** of the operand variable 
    ```C++
    int b;
    int* a = &b;
    int* c = new int
    ```
- other role (not in variable declaration): indicates a **reference**

### * => dereferencing operator
- returns the value stored at the memory address pointed to by the operand
- other role (not in variable declaration): indicates a **pointer**

**null pointer exception** 
- happens when dereferencing a pointer that is set to *nullptr*
- good programming practice to check for nullptr pointers
    - good practice: set garbage pointers to nullptr so that you may **nullptr-check** them


#### Notes:
**Be careful of dangling pointers**
- there is a double pointer (**), even *** and more.
    - focus in ** (double pointers)
    - it can go up to 12 pointers according to the specification

- nullptr and NULL are the same 
    - but *nullptr is safer*

# 3. Memory Allocation
- reserving a specific number of bytes in memory based on data type and size
### Dynamic Memory Allocation
- **new** keyword - heap
- **delete** keyword


# Dynamic Arrays

*Continue 16:13 lecture (Jan 22) then watch Jan 23*
*Current lecture to catch: Jan 27*

For **Primitives** - okay to pass by value.

## Assignment 2/Tutorial 3 Notes
A1: this has to be implemented:
- watch lec 22/25: About decrementing an array (closing the gap but not deleting the last array, just putting some extra so that another can be inserted)
- Heap stuff: dynamic
T3: 
- about **dynamically allocated arrays** 
