> # 3. Syntax Analysis (parse tree)


The correct example: ✅
```C++
double number  = 1.5;
```
```bash
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
```bash
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
2. Parse Trees:  
use techniques like Top-to-bottom parsing(eg. Java) or Bottom-to-up parsing(eg. CSS).
3. Error Handling:  
Syntax analysis can detect structural errors (like missing semicolons) and can also highlight semantic errors (like type mismatches).