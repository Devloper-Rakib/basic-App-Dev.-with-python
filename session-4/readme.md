# Program Control Flow - 1


## Table of Contents

1. [Relational Operators](#1-relational-operators)
2. [Conditional Execution](#2-conditional-execution)
3. [Programming Task](#3-programming-task)

---

## 1. Relational Operators

**Relational operators** are used to compare two values. The result of a relational operation is always a boolean value (`True` or `False`). These operators are essential in making decisions within a program.

### Relational Operators:
- `==` : Equal to
- `!=` : Not equal to
- `>`  : Greater than
- `<`  : Less than
- `>=` : Greater than or equal to
- `<=` : Less than or equal to

### Code Example:

```python
# Using relational operators to compare values
a = 10
b = 20

print(a == b)  # False
print(a != b)  # True
print(a > b)   # False
print(a < b)   # True
print(a >= 10) # True
print(b <= 15) # False
```

### Task: Comparing Numbers
Write a program that asks the user for two numbers and compares them using relational operators. Display whether the first number is greater than, less than, or equal to the second number.


## 2. Conditional Execution
Conditional execution allows a program to execute certain blocks of code only if a specific condition is met. In Python, this is achieved using if, elif, and else statements.

### `if`, elif`, and `else`:
- `if`: Executes a block of code if a specified condition is True.
- `elif`: Checks another condition if the previous if condition was False.
- `else`: Executes a block of code if all preceding conditions were False.
### Code Example:

```python
# Conditional execution example
age = int(input("Enter your age: "))

if age < 18:
    print("You are a minor.")
elif age >= 18 and age <= 65:
    print("You are an adult.")
else:
    print("You are a senior.")
```
### Task: Number Classification
Write a Python program that asks the user for a number and determines whether the number is:

- Positive
- Negative
- Zero
Use `if`, `elif`, and `else` to implement this logic.

### Task: Basic Grade Calculator
Write a Python program that:

1. Asks the user for a score between 0 and 100.
2. Classifies the score into the following categories:
   - A (90–100)
   - B (80–89)
   - C (70–79)
   - D (60–69)
   - F (0–59)
3. Display the letter grade based on the user's input.

### Example Output:
```
Enter your score: 85
Your grade is B.
```

### _Happy learning!_