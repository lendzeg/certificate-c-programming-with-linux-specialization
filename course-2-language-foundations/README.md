# Course 2 - C Programming: Language Foundation

![certificate](./certificate-course-2-language-foundations.jpg)

---

This course builds on the basics of C programming, focusing on **conditional statements**, **arrays**, **strings**, **loops**, and **sorting algorithms**. Below is a summary of the key topics and concepts covered in this course.

## Key Topics

### 1. Using the `if` Statement
- The `if` statement evaluates a condition:
  - **FALSE**: `0` or `0.0`.
  - **TRUE**: Any non-zero value (positive or negative).
- Example:
  ```c
  if (condition) {
      // Code to execute if condition is TRUE
  }
  ```

### 2. Arrays and Strings
- **Arrays**:
  - A collection of elements of the same type.
  - Declare and initialize an array:
    ```c
    int numbers[] = {1, 2, 3, 4};
    int size = 4; // Size of the array
    ```
  - Arrays are stored in contiguous memory locations.

- **Strings**:
  - An array of characters ending with a **null terminator** (`\0`).
  - Declare and initialize a string:
    ```c
    char word[] = "Hello";
    ```
  - The null terminator indicates the end of the string.
  - Use `%s` in `scanf` and `printf` to handle strings:
    ```c
    scanf("%s", word); // No ampersand (&) needed for strings
    printf("%s", word);
    ```

### 3. Loops
- **`for` Loop**:
  - Syntax:
    ```c
    for (int i = 0; i < size; i++) {
        // Code to repeat
    }
    ```
  - Used for iterating over arrays or performing repetitive tasks.

- **`while` Loop**:
  - Syntax:
    ```c
    while (condition) {
        // Code to repeat
    }
    ```
  - Used when the number of iterations is not known in advance.

- **Nested Loops**:
  - Loops inside other loops, useful for multi-dimensional arrays or complex iterations.

### 4. String Manipulation
- **Finding the Length of a String**:
  - Iterate through the string until the null terminator (`\0`) is found.
  - Example:
    ```c
    int length = 0;
    while (word[length] != '\0') {
        length++;
    }
    ```

- **Comparing Strings**:
  - Compare characters using their ASCII codes.
  - Example:
    ```c
    if (str1[i] < str2[i]) {
        // str1 comes before str2 alphabetically
    }
    ```

### 5. Sorting and Searching
- **Bubble Sort**:
  - Repeatedly swaps adjacent elements if they are in the wrong order.
  - Example:
    ```c
    for (int i = 0; i < size - 1; i++) {
        for (int j = 0; j < size - i - 1; j++) {
            if (array[j] > array[j + 1]) {
                // Swap elements
                int temp = array[j];
                array[j] = array[j + 1];
                array[j + 1] = temp;
            }
        }
    }
    ```

- **Selection Sort**:
  - Repeatedly finds the minimum element and swaps it with the first unsorted element.
  - Example:
    ```c
    for (int i = 0; i < size - 1; i++) {
        int minIndex = i;
        for (int j = i + 1; j < size; j++) {
            if (array[j] < array[minIndex]) {
                minIndex = j;
            }
        }
        // Swap elements
        int temp = array[i];
        array[i] = array[minIndex];
        array[minIndex] = temp;
    }
    ```

- **Linear Search**:
  - Iterates through the array to find a specific value.
  - Example:
    ```c
    for (int i = 0; i < size; i++) {
        if (array[i] == target) {
            // Target found at index i
        }
    }
    ```

- **Binary Search**:
  - Efficiently searches a sorted array by repeatedly dividing the search interval in half.
  - Example:
    ```c
    int left = 0, right = size - 1;
    while (left <= right) {
        int mid = left + (right - left) / 2;
        if (array[mid] == target) {
            // Target found at index mid
        }
        if (array[mid] < target) {
            left = mid + 1;
        } else {
            right = mid - 1;
        }
    }
    ```

---

## Learning Objectives
By the end of this course, you will be able to:
- Create and manipulate **arrays** to store integers, floating-point numbers, and strings.
- Use the **null terminator** (`\0`) to identify the end of a string.
- Find the length of a string and compare strings alphabetically.
- Use **`for`** and **`while`** loops for repetitive tasks and nested iterations.
- Sort arrays using **bubble sort** and **selection sort**.
- Search for elements in arrays using **linear search** and **binary search**.

