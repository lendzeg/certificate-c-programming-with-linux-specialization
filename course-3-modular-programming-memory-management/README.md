# Course 3 - Modular Programming and Memory Management

## Week 1 - Functions and Recursion

- All C programs must have the **main function**. It tells C where to start executing the code.
- **Arguments** are used to pass values. **Parameters** are used to receive values.
- When **calling a function**, the arguments values are **copied to** the function parameters.
- **Prototype** only tells C the type of the value returned by the function and the type of the function parameters.
- It's a **safer practice** to always write all your definitions **below the main function** and all your prototypes **right at the top**.
- Prototypes must be **above the main function**, to avoid **compilator warnings**.
- During a **prototype calling**, the compiler checks that all the types of a prototype match all the types of the variables of the main function.
- **Definitions** are generally written below the main function, to avoid confusion on the correct order of function callings based on where those functions were defined.

```c
#include <stdio.h>
int sum(int, int); //function PROTOTYPE
int main(void) {
    int a, b;
    int result;
    printf("Please enter two integers: ");
    scanf("%d%d", &a, &b);
    printf("You entered %d and %d.\n", a, b);
    result = sum(a, b); //copies of the VALUES of the ARGUMENTS a and b
    printf("Result of the sum = %d.\n", result);
    return 0;
}
// Function DEFINITION
int sum(int x, int y){ //values are copied into PARAMETERS x and y
    int compute;
    printf("Starting the computation!\n");
    compute = x + y;
    printf("Finished the computation successfully!\n");
    return compute;
}
```

- **Recursion** is when one function calls itself.
- Is recursion replacing in some way a for loop?
- All **recursive functions** must have a **stop condition**, or you will get an infinite loop, and **recursion condition**, to continue calling the function.  

![alt text](./recursive%20functions%20parts.png)