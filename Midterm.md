2 Parts:
  1. Multiple Choice (4 marks, 4 questions)
  2. Programming (13 marks, 4 questions)

Part 1
(1) Makefile 
- Compiling and Linking Programs: makefile is a text file of compile commands and dependencies.
- Example:
  - make foo:
    
    foo: foo.o foo2.o // all object files
        g++ -o foo foo.o foo2.o
    foo.o: foo.cc
        g++ -c foo.cc
    foo2.o: foo2.cc
        g++ -c foo2.cc
    
(2) Memory Areas
- Stack: Static memory for local variables, function parameters, and data.
- Heap: Dynamically allocated memory (e.g., using new and delete).
- Data Segment: Global and static variables.
- Code or Text Segment: Contains the executable instructions.
