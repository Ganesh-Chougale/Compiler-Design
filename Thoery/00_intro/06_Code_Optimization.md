> # 6. Code Optimization

Code optimization is achieved by transforming the intermediate code to make better use of computational resources and reduce unnecessary operations.

## 1. **Data Flow Analysis-Based Optimizations**:

- A. Constant Propagation:
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
Example
```C++
#include <iostream>
using namespace std;

int main(){
int x = 5;
int y = x + 10;
int z = y * 2;
return 0; // return 0 ends the function.
// in this example after ending function z is never used in any manner. the reference end with function.
}
```
```C++
return 0; // Removed the dead code involving z.
```

- C. Common Subexpression Elimination:
Identifying and eliminating redundant computations.
Example:
```C++
int a = x * x;
int b = y + x * x;
int c = z - x * x;
// Here, x * x is computed three times. We can compute it once and reuse it.
```
```C++
int reUse = x * x;
int a = reUse;
int b = y + reUse;
int c = z - reUse;
```
This optimization reduces redundant computations.


## 2. **Loop Optimizations**:

- A. Loop Invariant Code Motion:
Moving code that is invariant within a loop outside of it.
Example:
```C++
for (int i = 0; i < n; i++) {
    int temp = 5; // Since temp does not change within the loop, it can be moved outside the loop.
    array[i] = array[i] + temp;
}
```
```C++
for (int i = 0; i < n; i++) {
    array[i] = array[i] + temp; // optimized by moving temp declaration + initialization outside of the loop
}
```
- B. Loop Unrolling:
Replicating the body of a loop multiple times to reduce loop overhead.
Example:
```C++
// Before Unrolling
for (int i = 0; i < 4; i++) {
    array[i] = array[i] + 1;
}

```
```C++
// After Unrolling
for (int i = 0; i < 4; i += 2) {
    array[i] = array[i] + 1;
    array[i + 1] = array[i + 1] + 1; // Here, the loop body is executed twice as much per iteration, reducing the loop overhead.
}
```
- C. Strength Reduction:
Replacing expensive operations with cheaper ones (e.g., replacing multiplication by repeated addition).
Example:
```C++
for (int i = 0; i < n; i++) {
    array[i] = array[i] * 4; // Instead of multiplying by 4, we can replace it with repeated addition.
}
```
```C++
for (int i = 0; i < n; i++) {
    array[i] = array[i] + array[i] + array[i] + array[i]; // This replaces the multiplication by 4 with a series of additions, which can be cheaper depending on the architecture.
}
```

## 3. **Register Allocation**:

- - Graph Coloring:
Assigning variables to registers to minimize memory accesses.