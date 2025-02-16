#  Tuples and Dictionaries


## Table of Contents
1. [Sequence Types and Mutability](#1-sequence-types-and-mutability)
2. [Tuples](#2-tuples)
3. [Dictionaries](#3-dictionaries)

---


## 1. Sequence Types and Mutability

In Python, **sequence types** are used to store multiple items in a specific order. Examples include lists, tuples, and strings.

- **Mutable Sequences**: These allow changes after creation. For example, lists are mutable, meaning you can add, remove, or modify elements.
  ```python
  my_list = [1, 2, 3]
  my_list[0] = 10  # [10, 2, 3]
  ```

- **Immutable Sequences**: These do not allow modification after creation. Tuples and strings are examples of immutable sequences.
  ```python
  my_tuple = (1, 2, 3)
  # my_tuple[0] = 10  # This would raise an error as tuples are immutable
  ```

### Key Differences
- **Lists**: Mutable, indexed, allow duplicate elements.
- **Tuples**: Immutable, indexed, allow duplicate elements.
- **Strings**: Immutable, indexed, store characters.

---

## 2. Tuples

A **tuple** is an ordered and immutable sequence of items. Once a tuple is created, its values cannot be modified. Tuples are commonly used to represent fixed collections of items.

### Creating Tuples:
Tuples can be created by placing comma-separated values inside parentheses `()`. 
```python
my_tuple = (1, "hello", 3.14)
```

### Accessing Tuple Elements:
You can access elements in a tuple using **indexing**.
```python
print(my_tuple[0])  # Output: 1
print(my_tuple[1])  # Output: hello
```

### Tuple Operations:
Since tuples are immutable, the only operations allowed are reading and slicing.
```python
# Slicing
sub_tuple = my_tuple[0:2]  # (1, "hello")
```

### Common Uses of Tuples:
- Returning multiple values from a function
- Storing records of fixed, unchanging data
- Using as keys in dictionaries (if elements inside the tuple are also immutable)

---

## 3. Dictionaries

A **dictionary** in Python is an unordered collection of key-value pairs. Each key is unique, and keys must be immutable (e.g., strings, numbers, or tuples). Values can be of any type.

### Creating a Dictionary:
Dictionaries are created using curly braces `{}` with key-value pairs separated by a colon `:`.

```python
my_dict = {
    "name": "Alice",
    "age": 25,
    "city": "New York"
}
```

### Accessing and Modifying Dictionary Elements:
You can access, add, or modify dictionary values by referring to their key.

```python
# Accessing
print(my_dict["name"])  # Output: Alice

# Modifying
my_dict["age"] = 26
```

### Dictionary Operations:
- **Add a New Key-Value Pair**:
  ```python
  my_dict["country"] = "USA"
  ```
- **Delete a Key-Value Pair**:
  ```python
  del my_dict["city"]
  ```

- **Loop Through a Dictionary**:
  ```python
  for key, value in my_dict.items():
      print(key, value)
  ```

---

## Programming Task

### Task: Create a Tuple and a Dictionary and Perform Basic Operations

#### Problem:
1. Create a tuple representing a person’s basic information (name, age, city).
2. Create a dictionary to store multiple people's information, with the name as the key and the tuple as the value.
3. Write a function that prints each person's information in a readable format.

### Expected Output:
```
Name: Alice, Age: 30, City: New York
Name: Bob, Age: 25, City: Los Angeles
Name: Charlie, Age: 35, City: Chicago
```
### _Happy learning!_
