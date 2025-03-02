#   Function in Python


## Table of Contents
1. [Returning a Result from a Function](#1-returning-a-result-from-a-function)
2. [Scopes in Python](#2-scopes-in-python)
3. [Recursion](#3-recursion)

## 1. Returning a Result from a Function

A **function** in Python can perform computations and return a result using the `return` statement. This allows the function to pass data back to where it was called, enabling more complex programs by reusing function results.

### Example:
```python
def add(a, b):
    return a + b

result = add(5, 3)
print(result)  # Output: 8
```

- **`return` Statement**: Ends the function execution and passes the result to the caller. If no `return` statement is specified, Python returns `None` by default.

### Multiple Return Values:
A function can return multiple values using a tuple.

```python
def get_name_and_age():
    name = "Alice"
    age = 25
    return name, age

name, age = get_name_and_age()
print(name, age)  # Output: Alice 25
```

---

## 2. Scopes in Python

**Scope** defines the visibility of variables. In Python, variables can exist in different scopes, which determines where they can be accessed.

### Types of Scopes:
1. **Local Scope**: Variables defined inside a function are only accessible within that function.
2. **Global Scope**: Variables defined outside of all functions are accessible from any part of the code.
3. **Nonlocal Scope**: Variables in a nested function that are neither local nor global can be accessed with `nonlocal`.

### Example of Local and Global Scope:
```python
x = 10  # Global variable

def my_function():
    x = 5  # Local variable
    print("Inside function:", x)

my_function()               # Output: Inside function: 5
print("Outside function:", x)  # Output: Outside function: 10
```

### Using `global` and `nonlocal` Keywords:
The `global` keyword allows access to a global variable inside a function. 
```python
x = 10  # Global variable

def modify_global():
    global x
    x = 20  # Modifies the global variable `x`

modify_global()
print(x)  # Output: 20
```
The `nonlocal` keyword is used in nested functions to access variables from the outer function’s scope.

```python
def outer_function():
    x = "Hello"
    
    def inner_function():
        nonlocal x
        x = "Hi"
        
    inner_function()
    print(x)  # Output: Hi
```

---

## 3. Recursion

**Recursion** is when a function calls itself in order to solve a problem. Recursion is commonly used in tasks that can be broken down into smaller, similar sub-tasks.

### Basic Structure of a Recursive Function:
1. **Base Case**: A condition where the function stops calling itself to avoid infinite loops.
2. **Recursive Case**: The function calls itself with a modified argument.

### Example: Factorial Calculation
The factorial of a number `n` (denoted as `n!`) is the product of all positive integers up to `n`. This can be computed recursively.

```python
def factorial(n):
    if n == 0:
        return 1  # Base case
    else:
        return n * factorial(n - 1)  # Recursive case

print(factorial(5))  # Output: 120 (5 * 4 * 3 * 2 * 1)
```

### Advantages of Recursion:
- Simplifies code for tasks that involve repetitive sub-tasks.
- Useful for tree-based or nested structures (e.g., file directories, binary trees).

### Disadvantages of Recursion:
- Can lead to high memory usage if the recursion depth is too large.
- May cause stack overflow errors if the base case is not well-defined.

Here are a few tasks to practice recursion in Python, covering different types of problems such as mathematical operations, list processing, and string manipulation.

---

### Task: Factorial of a Number

Calculate the factorial of a number `n`, denoted as `n!`. This is the product of all positive integers up to `n`.

#### Problem:
Write a recursive function `factorial(n)` that returns `n!`.

#### Example:
```python
factorial(5)  # Output: 120 (5 * 4 * 3 * 2 * 1)
```

---

### Task: Fibonacci Sequence

The Fibonacci sequence is a series where each number is the sum of the two preceding ones. Starting from 0 and 1, the sequence goes: `0, 1, 1, 2, 3, 5, 8, ...`.

#### Problem:
Write a recursive function `fibonacci(n)` that returns the `n`-th Fibonacci number.

#### Example:
```python
fibonacci(5)  # Output: 5 (sequence: 0, 1, 1, 2, 3, 5)
```

---

### Task: Sum of a List

Calculate the sum of all elements in a list of integers.

#### Problem:
Write a recursive function `sum_of_list(lst)` that returns the sum of a list `lst`.

#### Example:
```python
sum_of_list([1, 2, 3, 4, 5])  # Output: 15
```


---



### _Happy learning!_
