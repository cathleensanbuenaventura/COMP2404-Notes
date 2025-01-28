## 2 Parts:
  I. Multiple Choice (4 marks, 4 questions)
  II. Programming (13 marks, 4 questions)
_________________________________
## Part I: Multiple Choice
#### (1) Makefile 
- Compiling and Linking Programs: makefile is a text file of compile commands and dependencies.
- Example:
  - make foo:
    
    foo: foo.o foo2.o // all object files
        g++ -o foo foo.o foo2.o
    foo.o: foo.cc
        g++ -c foo.cc
    foo2.o: foo2.cc
        g++ -c foo2.cc
    
#### (2) Memory Areas
- Stack: Static memory for local variables, function parameters, and data.
- Heap: Dynamically allocated memory (e.g., using new and delete), returned memory from a system call -> allocated at runtime.
- Data Segment: Global, static variables. and literals.
- Code or Text Segment: Contains the executable instructions (i.e., code/program instructions).


#### (3) Where & When Objects are Created in Memory
1. Static Memory (Stack)
2. Dynamic Memory (Heap)

#### (4) Return Parameters
- allows a function to return values to the caller by modifying variables passed it.

1. Return by value: copy of the return value is created and returned to the caller.
    ```C++
    int square(int x) {
        return x * x;   // Returns a copy of the result
    }

    int result = square(5);     // result = 25
    ```
2. Return by reference: returns a reference to an existing variable. 
    - Allows modification of the original variable.
    - Can be used outside of parameter passing.
    ```C++
        // Snippet
        int x = 10; 
        int& y = x; 

        // Sample: Return by Reference
        int& modify(int& x) {
            x += 10;    // Modifies the original variable
            return x;
        }
        
        int num = 5;
        modify(num);    // num = 15
    ```
3. Return by Pointer: function returns the **address** of a variable or dynamically allocated memory.
    ```C++
    int* createArray(int size) {
        return new int[size];   // Returns pointer to dynamic array
        }
    ```
4. Output Parameters (using *void*): pass arguments by reference (to modify their values) without returning anything
    ```C++
    void swap(int& a, int& b) {
        int temp = a;
        a = b;
        b = temp;   // No return => void
    }  
    ```

#### (5) Namespace
- avoids conflicts or collisions especially in large projects that uses multiple libraries.
- The C++ Standard Library is within the std namespace. See to initialize below.
    ```C++
    using namespace std;    // Above part of code 
    ```
- OR use the *scope resolution operator* :: a double-semi colon
1. Declaring a Namespace
    ```C++
    namespace MyNamespace {
        int myFunction(int x) {
            return x * 2;
        }
    }
    ```
2. Accessing a Namespace
- Use the *using* keyword 
- Use the *scope resolution operator* :: a double semi-colon
- Using Declaration
    ```C++
    // :: operator
    int result = MyNamespace::myFunction(5); // result = 10

    // "using" keyword directive
    using namespace MyNamespace;
    int result = myFunction(5); // No need for 'MyNamespace::'

    // using Declaration
    using MyNamespace::myFunction;
    int result = myFunction(5);
    ```
_________________________________
## Part II: Programming
... cont