#   Function in Python


## Table of Contents
1. [Decomposition](#1-decomposition)
2. [Functions](#2-functions)
3. [How Functions Communicate with Their Environment](#3-how-functions-communicate-with-their-environment)

---

## 1. Decomposition

**Decomposition** is the practice of breaking down a complex problem into smaller, manageable parts. This approach is fundamental to programming as it helps improve readability, simplify debugging, and promote code reuse.

In Python, functions are a primary tool for decomposition, allowing us to group related tasks into a single unit that can be called as needed. Here’s a basic example of decomposition:

### Example:
Suppose you want to calculate the area and circumference of a circle based on its radius. Instead of writing everything in one long piece of code, you can decompose the problem into separate functions.

```python
def calculate_area(radius):
    return 3.14159 * radius ** 2

def calculate_circumference(radius):
    return 2 * 3.14159 * radius

# Main function to output both calculations
def main(radius):
    area = calculate_area(radius)
    circumference = calculate_circumference(radius)
    print(f"Area: {area}, Circumference: {circumference}")

main(5)
```

By decomposing, we make the code modular and more understandable. Each function does one thing and can be reused or tested individually.

---

## 2. Functions

A **function** in Python is a reusable block of code that performs a specific task. Functions are defined using the `def` keyword, followed by the function name, parameters, and a code block.

### Function Syntax
```python
def function_name(parameters):
    """Docstring - optional description of the function."""
    # Code block
    return result  # Optional return value
```

### Defining and Using Functions
1. **Define**: Write the function code, specifying its name, parameters, and logic.
2. **Call**: Execute the function using its name and passing any required arguments.

### Example:
```python
def greet(name):
    """Greets the user by name."""
    print(f"Hello, {name}!")

# Calling the function
greet("Alice")
```

### Function Types
- **Built-in Functions**: Functions provided by Python, like `len()`, `print()`, and `type()`.
- **User-defined Functions**: Functions you define yourself to suit specific needs.
- **Anonymous (Lambda) Functions**: Small, single-expression functions defined with `lambda`.

### Return Statement
A function can return a result using the `return` statement. Without a `return`, a function returns `None`.

```python
def add(a, b):
    return a + b

result = add(3, 4)  # result is 7
```

---

## 3. How Functions Communicate with Their Environment

Functions can **communicate with their environment** in several ways:

### 3.1 Parameters and Arguments
Functions accept input through **parameters** (in the function definition) and **arguments** (when calling the function). Parameters allow functions to perform tasks with varying inputs.

```python
def square(number):
    return number ** 2

print(square(5))  # Output: 25
```

### 3.2 Global and Local Variables
- **Local Variables**: Variables defined inside a function are local and accessible only within that function.
- **Global Variables**: Variables defined outside a function are accessible throughout the program. However, global variables should be used sparingly as they can make debugging difficult.

```python
x = 10  # Global variable

def display_number():
    x = 5  # Local variable
    print("Inside function:", x)

display_number()          # Output: Inside function: 5
print("Outside function:", x)  # Output: Outside function: 10
```

### 3.3 The `return` Statement
Functions can pass data back to the calling code using the `return` statement. This is useful for computations and tasks that generate results.

```python
def multiply(a, b):
    return a * b

product = multiply(4, 5)
print("Product:", product)  # Output: Product: 20
```

### 3.4 Side Effects
Some functions interact with their environment through side effects, like printing output, modifying global variables, or writing to files. While often necessary, side effects should be used carefully to keep functions predictable.

---

## Example Task

### Task: Write a Program that Calculates the Average of a List of Numbers

1. Create a function `calculate_sum` that adds up all numbers in a list.
2. Create a function `calculate_average` that uses `calculate_sum` to find the average.
3. Output the result using a main function.

### _Happy learning!_
