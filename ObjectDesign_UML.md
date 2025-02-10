#### Overview
*Lecture (Mon: Feb 3) and (Wed: Feb 5)*
- Covers lecture slides 8 and 9.
- Overview: object design categories, collection classes, UML Class Diagrams

#### Reminder Notes:
- Assignment 2 is out, try as early as possible. 
- See if you can do this assignment (Panel), if you can't do what the specification says, do it in a way that you are 'halfway' of accomplishing the assignment.
- Prof is more concerned about the C++ coding and memory management.
- SEE Code implementation 08:O-0Design Categories; the application logic is kind of like the same. 
- If you finished coding your assignment 2 early, give feedback to prof. 

## About
1. Object Design Categories, Collection Classes (Class' Design Focus)
2. UML Class Diagram

### Modular Design
- classes should have **single** responsibility or use. 
- Modular code := encapsulation, abstraction, Principle of Least  Privilege

# 1. Types of Object Categories
As we start to make modular code, we need to think about the object categories.

**a. Entity Object** 
- Information about real-world objects tracked by the program.
    - simplest form of object and have persistent information.
- E.g., University, Student, Instructor classes

**b. Control Object** 
- What code is executing? 
- Takes charge of program flow; often manage high-level interaction between other classes.

**c. Boundary Object**
- manage interaction of the application with **foreign entities**, i.e., other programs, users.
- E.g., API, UI (Make sit easy to wap out a user interface)

**d. Collection Objects**
- storage of multiple entities of the same type along with relevant behaviors.
- Collections may be primitive:
    - creating a class that has an array member variable (the array is the actual collection but remains hidden)
    - our class provides an abstraction layer of common collection functions.
- An excellent example of good OO-Programming 
    - provides encapsulation and an abstraction layer to data access.
- Review example: ![alt text](image.png)

- *Code example 08: Object Design Categories*
_______________________________________________________________________
## 2. UML Class Diagram (& Documentation)
#### Types of Documentations:
1. **Requirements analysis** - figuring out what you are building
2. **Design** - making a plan
3. **Implementation** - implementing the plan
4. **Testing** - did this all work?

Note: code should be self-documenting whenever possible, even though you have documentations and comments.

### Unified Modelling Language (UML)
- Used during the design-phase of building to help document OO design.
#### Types of UMLs:
1. **UML Class Diagram** - attributes and operators, class associations.
2. **UML Activity Diagram** - looks into the program behavior and interactions between classes. Similar to flow chart.
3. **UML State Machine Diagrams** 

... See slides page 16 onwards for UML Class Diagram Specification
