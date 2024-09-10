> # 7. Code Generator

Code generation is the final phase of the compilation process where the optimized intermediate code is translated into machine code for the target architecture.

**Key Aspects of Code Generation**:
- Instruction Selection:
Choosing the appropriate machine instructions to represent the intermediate code.
- Register Allocation:
Assigning variables to registers to minimize memory accesses.
- Instruction Scheduling:
Ordering instructions to improve performance.
- Memory Management:
Allocating and managing memory for variables and data structures.  

Example: 
```Bash
t1 = 5
t2 = 2
t3 = t1 + t2
z = t3
```

```Bash
mov eax, 5
mov ebx, 2
add eax, ebx
mov z, eax
```

**Challenges in Code Generation**:
- Target Architecture-Specific Constraints:
Different architectures have varying instruction sets and register limitations.
- Code Quality:
The generated code should be efficient, maintainable, and easy to debug.
- Optimization Trade-offs:
Optimizations can sometimes introduce overhead or make the code less readable.