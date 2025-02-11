#  Python Data Structure-Lists

## Table of Contents
1. [Basic Operators in Python](#1-basic-operators-in-python)
2. [Lists](#2-lists)
3. [Operations on Lists](#3-operations-on-lists)
4. [Lists in Advanced Applications](#4-lists-in-advanced-applications)

---

## 1. Basic Operators in Python


### Arithmetic Operators:
- `+` : Addition
- `-` : Subtraction
- `*` : Multiplication
- `/` : Division
- `//` : Floor Division
- `%` : Modulus
- `**` : Exponentiation


**Code Example:**
```python
a = 10
b = 3
print(a + b)  # Output: 13
print(a - b)  # Output: 7
print(a * b)  # Output: 30
print(a / b)  # Output: 3.3333333333333335
print(a // b)  # Output: 3
print(a % b)  # Output: 1
print(a ** b)  # Output: 1000
```
### Comparison Operators:
- `==` : Equal to
- `!=` : Not equal to
- `>`: Greater than
- `<` : Less than
- `>=` : Greater than or equal to
- `<=` : Less than or equal to

**Code Example:**
```python
a = 10
b = 3
print(a == b)  # Output: False
print(a != b)  # Output: True
print(a > b)  # Output: True
print(a < b)  # Output: False
print(a >= b)  # Output: True
print(a <= b)  # Output: False
```
### Logical Operators:

- `and` : Returns `True` if both statements are true
- `or` : Returns `True` if one of the statements is true
- `not` : Reverses the result of a condition

### Code Example:

```python
a = True
b = False
print(a and b)  # Output: False
print(a or b)   # Output: True
print(not a)    # Output: False
```

## 2. Lists

A list in Python is an ordered collection of items that can contain elements of different types. You can access elements by index, where the first element is at index 0.

```python
my_list = [1, 2, 3, "Hello", 5.5]
print(my_list) 

print(my_list[0])  # Output: 1
print(my_list[-1]) # Output: 5.5 (last element)
```

## 3. Operations on Lists

### List Methods
- `append()` : Add an item to the end of the list.
- `insert()` : Add an item at a specified index.
- `remove()` : Remove the first item that matches the value.
- `sort()` : Sort the list in ascending or descending order.
- `reverse()` : Reverse the order of the list.
- `clear()` : Clear list.
- `copy()` : Copy list.
- `count()` : Count element in list.

### Code Example:

```python
numbers = [3, 1, 4, 1, 5]

numbers.append(9)
print(numbers)  # Output: [3, 1, 4, 1, 5, 9]

numbers.insert(2, 2)
print(numbers) # Output: [3, 1, 2, 4, 1, 5, 9]

numbers.remove(2)
print(numbers) # Output: [3, 1, 4, 1, 5, 9]

count_element = numbers.count(1)
print(count_element) # Output: 2

numbers.pop()
print(numbers) # Output: [3, 1, 4, 1, 5]

numbers.reverse()
print(numbers) # Output: [5, 1, 4, 1, 3]

numbers.sort()
print(numbers) # Output: [1, 1, 3, 4, 5]

new_list = numbers.copy()
print(new_list) # Output: [1, 1, 3, 4, 5]

numbers.clear()
print(numbers) # Output: []
```

### Slicing Lists
You can extract a portion of a list using slicing.
```python
my_list = [10, 20, 30, 40, 50]
print(my_list[1:3])  # Output: [20, 30]
print(my_list[:3])   # Output: [10, 20, 30]
print(my_list[2:])   # Output: [30, 40, 50]
print(my_list[:-1])   # Output: [10, 20, 30, 40]
print(my_list[1:-2])   # Output: [20, 30]
```

### List Comprehension
List comprehension provides a concise way to create lists.

```python
squares = [x**2 for x in range(5)]
print(squares)  # Output: [0, 1, 4, 9, 16]
```

## 4. Lists in Advanced Applications

### Multi-dimensional Lists 

```python
matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
print(matrix[1][2])  # Output: 6
```
### Data Analysis
```python
sales = [200, 150, 300, 400]
print(sum(sales))  # Output: 1050
print(max(sales))  # Output: 400
print(min(sales))  # Output: 150
```

### Task: Sum of List Elements
Write a program that takes a list of numbers and returns the sum of its elements (using loop & without loop).

#### Example:
```python
# Input : numbers = [1, 2, 3, 4, 5]
# Output: 15
```

### Task: Remove Duplicates
Write a program that removes duplicates from a list (using loop & without loop) 
### Example Output:
```python
# Input: numbers = [1, 2, 2, 3, 4, 4, 5]
# Output: [1, 2, 3, 4, 5]
```
### Task: Count Occurrences in a List 
Write a program that counts the number of occurrences of an element in a list.

### Example Output:
```python
# Input: 
numbers = [1, 1, 2, 3, 4, 2, 1]
number = 1
# Output: 3
```

### _Happy learning!_
