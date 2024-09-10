> # 3. Syntax Analysis (parse tree)


The correct example: ✅
```C++
double number  = 1.5;
```
```arduino
Assignment
  /        \
Type   Initialization
  |          /      \
double  Identifier   Value
           |           |
       number         1.5
```
The incorrect example: ❌
```C++
int number  = 1.5;
```
```arduino
Assignment
  /        \
Type   Initialization
  |          /      \
int    Identifier   Value
           |           |
       number         1.5
```

**inside Syntax Analysis these are key points.**
1. Grammer validation:  
it checks if the structure of the statement is correct.
2. Type Checking:  
it crossverify if the assigned value & it datatypes matches or not.
3. Parse Trees:  
use techniques like Top-to-bottom parsing or Bottom-to-up parsing.
4. Error Handling:  
Syntax analysis can detect structural errors (like missing semicolons) and can also highlight semantic errors (like type mismatches).