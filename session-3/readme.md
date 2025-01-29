# Variables, Expressions, and I/O Operations

Welcome to the **Python Learning Guide**! In this guide, we will cover the basics of Python, including variables, expressions, and input/output operations. We'll also explore key topics like arithmetic operators, how to use comments, and interact with the user in Python.

## Table of Contents

1. [Variables](#1-variables)
2. [Expressions and Arithmetic Operators](#2-expressions-and-arithmetic-operators)
3. [Comments](#3-comments)
4. [Interaction with the User](#4-interaction-with-the-user)
5. [Tasks for Practice](#5-tasks-for-practice)

---

## 1. Variables

A **variable** is a name that refers to a value. In Python, variables are dynamically typed, meaning you don't need to declare their type in advance. 

### Code Example:

```python
# Defining variables
name = "Alice"
age = 25
height = 1.70  # in meters

# Printing variable values
print("Name:", name)
print("Age:", age)
print("Height:", height, "m")
```

### Explanation:
- Variables store data like strings, integers, and floats.
- You can assign values to variables using the `=` operator.
- The `print()` function is used to output the values stored in variables.

### Variable Naming Rules

Here are the basic rules for naming variables in Python:
1. **Variable names must start with a letter or an underscore (`_`)**.
   - Valid: `name`, `_value`, `age1`
   - Invalid: `1age`, `@name`

2. **The rest of the variable name can contain letters, numbers, and underscores**.
   - Valid: `my_variable`, `variable2`
   - Invalid: `my-variable`, `variable@name`

3. **Variable names are case-sensitive**.
   - `age` and `Age` are different variables.

4. **Keywords (reserved words) cannot be used as variable names**.
   - Python has reserved words like `class`, `if`, `for`, `else`, `True`, `False`, etc., which cannot be used as variable names.
   - Example: `if = 5` is invalid because `if` is a Python keyword.

### Best Practices

Here are some best practices to make your variable names more readable and understandable:

1. **Use descriptive names**:
   - Instead of `x`, `y`, or `a`, use names like `length`, `width`, `age`, or `total_cost` to make your code easier to understand.

2. **Use underscores for multi-word variable names** (also known as **snake_case**):
   - Good: `student_name`, `total_price`
   - Bad: `studentName` (though valid, this follows camelCase, which is common in other languages like JavaScript).

3. **Avoid starting variable names with an underscore unless necessary**:
   - Underscores are often used for special purposes (like `_my_variable` for internal or private variables), so avoid them unless you have a specific reason.


### Task: Storing Personal Details
Write a Python program that stores your name, age, and hometown in variables, and then prints them out in the following format:
```shell
Your name is [name], you are [age] years old, and you are from [hometown].
```
## 2. Expressions and Arithmetic Operators

An expression is a combination of values and operators that Python interprets and evaluates to produce a result. Arithmetic operators are used to perform mathematical calculations.

### Arithmetic Operators:
- `+` : Addition
- `-` : Subtraction
- `*` : Multiplication
- `/` : Division
- `%` : Modulus (remainder of division)
- `**` : Exponentiation (power)
- `//` : Floor division (division that rounds down to the nearest whole number)

### Code Example:

```python
# Arithmetic operations
a = 10
b = 3

sum_result = a + b      # Addition
difference = a - b      # Subtraction
product = a * b         # Multiplication
quotient = a / b        # Division
modulus = a % b         # Modulus (remainder)
power = a ** b          # Exponentiation

# Printing results
print("Sum:", sum_result)
print("Difference:", difference)
print("Product:", product)
print("Quotient:", quotient)
print("Remainder (Modulus):", modulus)
print("Exponentiation (a^b):", power)
```

### Explanation:
- Arithmetic operators allow you to perform calculations with variables.
- Expressions like `a + b` are evaluated, and the result is stored in new variables like `sum_result`.

### Task : Basic Calculator

Write a program that takes two numbers from the user and prints:

- Their sum.
- Their difference.
- Their product.
- The result of dividing the first number by the second (handle cases where division by zero might occur).

## 3. Comments
Comments in Python are used to explain your code. Comments make the code more readable and are ignored by Python during execution.

### Code Example:
```python
# This is a single-line comment

"""
This is a multi-line comment.
You can write multiple lines of explanation here.
"""

# Defining a variable
greeting = "Hello, World!"  # Inline comment to explain the line
print(greeting)
```
### Task: Commenting the Code
Write a Python program that performs a few arithmetic operations (addition, subtraction, multiplication, and division) and adds comments to explain each operation. Your comments should include:

- A description of what each section of the code is doing.
- An explanation of the expected output.

## 4. Interaction with the User

In Python, you can interact with the user by using the input() function. The input() function takes user input and returns it as a string.

### Code Example:
```python
# Asking the user for their name and age
name = input("Enter your name: ")
age = int(input("Enter your age: "))  # Convert input to an integer

# Outputting a message using the user's input
print("Hello,", name + "!")
print("You are", age, "years old.")
```
### Task: Interactive Age Calculator

Write a Python program that asks the user for their birth year, and then calculates and prints their current age. The output should be in the following format:
```shell
You are [age] years old.
```

## 5. Additional Practice Tasks

### Task 1: Storing Personal Details
Write a Python program that stores your favorite food, your favorite color, and the number of hours you sleep every night. Print each value on a new line in a formatted string.

### Task 2: Rectangle Area and Perimeter
Write a Python program that asks the user for the length and width of a rectangle, and then calculates and prints the area and perimeter. Use the formula:
```shell 
Area = Length×Width
Perimeter = 2×(Length+Width)
```

### Task 3: BMI Calculator
Write a Python program that asks the user for their weight (in kilograms) and height (in meters), and then calculates their Body Mass Index (BMI). Use the formula:
```shell
BMI = weight / (height ** 2)
```

### _Happy learning!_


