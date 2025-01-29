#  Fun with Python

## Table of Contents

1. [The “Hello, World!” Program](#1-the-hello-world-program)
2. [Output Operations](#2-output-operations)
3. [Simple Data Types](#3-simple-data-types)
4. [Tasks for Practice](#4-tasks-for-practice)

---

## 1. The “Hello, World!” Program

The "Hello, World!" program is the simplest program you can write in Python. It displays a message to the user.

### Code Example:

```python
print("Hello, World!")
```

### Explanation:
- ``print()`` is a built-in function in Python that outputs a message to the screen.
- ``"Hello, World!"`` is a string (a sequence of characters), and it is displayed when the code is executed.

### Task:
- Write a program that prints ``"Hello, [Your Name]!"``.
- Try changing the message inside the print() function and see what happens.


## 2. Output Operations
In Python, we use the print() function to output data to the console. You can print different types of data such as strings, numbers, and even results of expressions.

### Code Example:

```python
# Printing a string
print("Learning Python is fun!")

# Printing numbers
print(42)

# Printing the result of an expression
print(3 + 5)
```

### Explanation:
- You can pass different data types to the print() function, and it will display them.
- Python evaluates expressions before printing them, so print(3 + 5) will display 8.

### Task:
- Print the result of multiplying two numbers.
- Print the message "The result of 7 * 6 is:" followed by the result of the expression 7 * 6.


## 3. Simple Data Types

Python supports several simple data types that are useful for basic operations.

### Types Covered:
- **Integer**: Whole numbers, e.g., `5`, `42`, `-1`
- **Float**: Numbers with decimals, e.g., `3.14`, `-0.001`
- **String**: A sequence of characters, e.g., `"Python"`, `"123"`
- **Boolean**: True/False values, e.g., `True`, `False`

### Code Example:

```python
# Integer
age = 25
print("Age:", age)

# Float
pi = 3.14159
print("Pi:", pi)

# String
greeting = "Hello, World!"
print(greeting)

# Boolean
is_python_fun = True
print("Is Python fun?", is_python_fun)
```

### Explanation:
- `age`, `pi`, `greeting`, and `is_python_fun` are variables storing values of different data types.
- You can print variables using the `print()` function by passing them as arguments.

### Task:
- Create a variable `x` that stores the number `10` and print its value.
- Create a variable `y` that stores the string `"Python is awesome!"` and print it.
- Create a variable `is_sunny` that stores `False` and print it.

## 4. Tasks for Practice

### Task 1: Personalized Greeting
Write a Python program that asks the user for their name and age, then prints the following message:
```shell
Hello, [name]! You are [age] years old.
```

### Task 2: Simple Calculator

Write a program that takes two numbers from the user and prints:

- Their sum.
- Their difference.
- Their product.
- The result of dividing the first number by the second (handle cases where division by zero might occur).

### Task 3: Temperature Converter
Write a Python program that converts temperature from Celsius to Fahrenheit. The formula to convert is:
```shell
Fahrenheit = (Celsius * 9/5) + 32
```

### _Happy learning!_