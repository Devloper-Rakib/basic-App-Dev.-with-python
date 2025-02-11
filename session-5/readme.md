# Program Control Flow - 2

## Table of Contents

1. [Loops](#1-loops)
2. [Logical Operators](#2-logical-operators)

---

## 1.Loops

Loops are used to repeat a block of code multiple times. In Python, there are two main types of loops: `for` and `while`.

### For Loop:
A `for` loop is used to iterate over a sequence (like a list, tuple, or string) or a range of numbers.

**Syntax**:
```python
for item in sequence:
    # Do something
```
**Code Example:**
```python
for i in range(5):
    print(i)
    
# Output 
0
1
2
3
4
```
### While Loop:
A `while` loop repeats as long as a specified condition is `True`.
**Syntax**:
```python
while condition:
    # Do something
```
**Code Example:**
```python
count = 0
while count < 5:
    print(count)
    count += 1

    
# Output 
0
1
2
3
4
```
### Nested Loops:
You can use loops inside other loops. These are called nested loops.

**Code Example:**
```python
for i in range(3):
    for j in range(2):
        print(f"i = {i}, j = {j}")

    
# Output 
i = 0, j = 0
i = 0, j = 1
i = 1, j = 0
i = 1, j = 1
i = 2, j = 0
i = 2, j = 1
```

## 2. Logical Operators
Logical operators in Python are used to combine conditional statements. The most common logical operators are:

### `and`, `or`, and `not`:
- `and` : Returns `True` if both statements are true
- `or` : Returns `True` if one of the statements is true
- `not` : Reverses the result of a condition

### Code Example:

```python
x = 10
y = 5

# Using 'and'
if x > 5 and y < 10:
    print("Both conditions are true")

# Using 'or'
if x > 5 or y > 10:
    print("At least one condition is true")

# Using 'not'
if not(x < 5):
    print("x is not less than 5")

```
### Task: Print Numbers from 1 to N
Write a Python function that takes an integer N as input and prints all numbers from 1 to `N` using a `for` loop.

#### Example:
```python
# Input: N = 5
# Output: 1,2,3,4,5
```


### Task: Pattern 
Write a program that prints the following pattern:
### Example Output:
```python
1
12
123
1234
12345
```
### Task: Fibonacci Sequence 
Write a program to generate the first `n` Fibonacci numbers:.
### Example Output:
```python
# input : n = 10
# output : 0 1 1 2 3 5 8 13 21 34
```

### _Happy learning!_
