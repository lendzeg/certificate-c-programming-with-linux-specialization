# Course 3 - Modular Programming and Memory Management

![certificate](./certificate-course-3-modular-programming-memory-management.jpg)

---


## Week 1 - Functions and Recursion

- All C programs must have the **main function**. It tells C where to start executing the code.
- The `void` argument in a function means there is **no input** to the function.
- Functions can be **defined** between the `#include` headers and the main function `int main(void)`.
- **Arguments** are used to pass values. **Parameters** are used to receive values.

```c
#include <stdio.h>

int sum(int x, int y){ 
    return x+y;
}

int main(void){
    int a, b;
    scanf("%d%d", &a, &b);
    printf("%d", sum(a,b));
    return 0;
}
```

- **Arguments** are used to pass values (in the calling)
- **Parameters** are used to receive values (in the prototyping and definition)
- When **calling a function**, the arguments values are **copied** to the function parameters.
- In the **definition** you need to specify the **type** of parameters `int sum(int x, int y)`
- In the **calling** you don't need to specify the **type** of arguments `result=sum(a,b)`; they have already specified at the beginning `int a, b, result;`

```c
#include <stdio.h>

// function definition
int sum(int x, int y){ // parameters
    return x+y;
}

int main(void){
    int a, b, result;
    scanf("%d%d", &a, &b);
    // function calling
    result = sum(a,b); // arguments
    printf("%d", result);
    return 0;
}
```

- **Function prototype** only tells C the **type** of the value returned by the function and the **type** of the function parameters.
- It's a **safer practice** to always write all your function definitions **below the main function** and all your function prototypes **right at the top**.
- Prototypes must be **above the main function**, to avoid **compilator warnings**.
- During a **prototype calling**, the compiler checks that all the types of the prototype **parameters** match all the types of the **arguments** in the **function calling**.
- **Definitions** are generally written below the main function, to avoid confusion on the **correct order of function callings** based on where those functions were defined.

```c
#include <stdio.h>

// function prototype
int sum(int, int); // parameters: types

int main(void){
    int a, b, result;
    scanf("%d%d", &a, &b);
    result = sum(a,b); // function calling, arguments
    printf("%d", result);
    return 0;
}

// function definition
int sum(int x, int y){ // parameters: types + names
    return x+y;
}
```

- You can prototype by optionally specifying the **name of parameters**. In addition, they don't have to match with names in the definition.

```c
// function prototype
int sum(int k, int l); // parameters: types + names

// function definition
int sum(int x, int y){ // parameters: types + names
    return x+y;
}
```

- **Recursion** is when one function calls itself.
- Is recursion replacing in some way a for loop?
- All **recursive functions** must have a **stop condition**, or you will get an infinite loop, and **recursion condition**, to continue calling the function.  

![alt text](./recursive%20functions%20parts.png)