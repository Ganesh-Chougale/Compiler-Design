> # 4. Symantic Analysis

Symantic Analysis checks & ensures logic & logical errors  

1. Type Checking:  
it crossverify if the assigned value & it datatypes matches or not.
2. Control Flow Analysis:  
it ensures for snippet control flow & looks for un-neccesory loops.
3. Data Flow Control:  
Makes sure that variable flow is correct or else give reference error.

Example: 
```C++
int x = 5;
double y = 2.5;
int z = x + y;
```
- A. Type Check: Ensure that the assignment operators are compatible (e.g., assigning an int to x and a double to y).
- B. Control Flow Analysis: Verify that the code has a valid control flow (e.g., no infinite loops).
- C. Data Flow Analysis: Determine that x and y are live variables before the addition operation.

```bash
value of z: 7
```


The correct example: ✅
```C++
int c = a + b;
```
The incorrect example: ❌
```C++
int 10 = a + b;
// a constant cannot be a variable
```
