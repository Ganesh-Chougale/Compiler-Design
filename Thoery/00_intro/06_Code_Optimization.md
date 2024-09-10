> # 6. Code Optimization

Code optimization is achieved by transforming the intermediate code to make better use of computational resources and reduce unnecessary operations.

1. **Data Flow Analysis-Based Optimizations**:

- - Constant Propagation:
Replacing variables with their constant values.
Example
```C++
int a = 10;
int b = a + 5;
int c = b * 2;
```
In this code, a is a constant with the value 10. We can propagate this constant through the program:  
> **b** becomes **10 + 5** which simplifies to **15**.
> **c** becomes **15 * 2** which simplifies to **30**.
```C++
int c = 30;
```
- B. Dead Code Elimination:
Removing code that has no effect on the program's output.
- - Common Subexpression Elimination:
Identifying and eliminating redundant computations.

2. **Loop Optimizations**:

Loop Invariant Code Motion:
Moving code that is invariant within a loop outside of it.
Loop Unrolling:
Replicating the body of a loop multiple times to reduce loop overhead.
Strength Reduction:
Replacing expensive operations with cheaper ones (e.g., replacing multiplication by repeated addition).

3. **Register Allocation**:

- - Graph Coloring:
Assigning variables to registers to minimize memory accesses.