# Course 1 - C Programming: Getting Started

![certificate](certificate-course-1-getting-started.png)


This course introduces the basics of C programming, including working with characters, user input, decimals, division, remainders, and type conversion. Below is a summary of the key topics and examples covered.

## 1. Printing Characters
- Use `char` to declare character variables.
- Use `printf` to print characters.

### Example:
```c
#include <stdio.h>

int main(void){
    char letter1 = 'i';
    char letter2 = 'n';
    char letter3 = 'C';
    printf("Programming %c%c %c\n", letter1, letter2, letter3);
}
```

## 2. Reading Characters from User Input
- Use `scanf` to read characters from the user.
- Format specifiers like `%c` are used to read characters.
- Spaces or commas in the format string allow reading formatted input. 📌

### Examples:
```c
// Reading two characters without spaces
scanf("%c%c", &letter, &letter2);

// Reading two characters separated by a space
scanf("%c %c", &letter, &letter2);

// Reading two characters separated by a comma
scanf("%c,%c", &letter, &letter2);
```

## 3. Working with Decimals
- Use `double` to declare decimal numbers.
- Use `%.2lf` in `printf` to format decimal output.
- Use `%lf` in `scanf` to read decimal input.

### Examples:
```c
// Declaring and printing decimals
double height = 1.99;
printf("I am %.1lf meters tall.", height);

// Reading decimals from user input
scanf("%lf", &height);
```

## 4. Division in C
- Integer division (`/`) returns an integer result.
- Floating-point division (`/`) returns a decimal result.
- Mixing integers and decimals in division results in a decimal.

### Examples:
```c
// Integer division
printf("5/2 equals %d\n", 5/2); // Output: 2

// Floating-point division
printf("5.0/2.0 equals %lf\n", 5.0/2.0); // Output: 2.5
```

## 5. Finding the Remainder
- Use the modulus operator `%` to find the remainder in integer division.

### Example:
```c
int twenties = 166 / 20; // Number of 20-dollar bills
int rest = 166 % 20;     // Remaining amount
printf("I will pay %d dollars with 20-dollar bills.\n", twenties * 20);
printf("I will then pay %d dollars with 1-dollar bills.\n", rest);
```

## 6. Type Conversion
- Convert integers to decimals using `(double)`.
- Convert decimals to integers using `(int)`.

### Examples:
```c
// Integer to double
double dOne = (double) iOne;

// Double to integer
int iOne = (int) dOne;
```

### Calculating Averages:
```c
#include <stdio.h>
int main(void) {
    int numGrades;
    scanf("%d", &numGrades);
    int sum = 0;
    for (int i = 0; i < numGrades; i++) {
        int grade;
        scanf("%d", &grade);
        sum += grade;
    }
    double average = (double) sum / numGrades;
    printf("%.2lf\n", average);
    return 0;
}
```
