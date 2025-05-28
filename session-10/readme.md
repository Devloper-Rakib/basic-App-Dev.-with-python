# Modules and Packages in Python

## Table of Contents
1. [Introduction to Modules in Python](#1-introduction-to-modules-in-python)
2. [Selected Python Modules](#2-selected-python-modules)
3. [Modules and Packages](#3-modules-and-packages)
4. [Python Package Installer (PIP)](#4-python-package-installer-pip)

## 1. Introduction to Modules in Python
Modules in Python are files that contain Python code (functions, variables, classes) that you can reuse across different parts of your project or even in other projects. Instead of writing everything in a single script, you can create a module, import it, and access its contents.

### Key Points:
- A module is any Python file ending with `.py`.
- Use the `import` statement to include a module.
- Modules promote code reuse and help maintain organization.

### Example:
```python
# sample_module.py
def greet(name):
    return f"Hello, {name}!"

# main.py
import sample_module

print(sample_module.greet("Alice"))  # Output: Hello, Alice!
```

## 2. Selected Python Modules
Python comes with a large standard library that includes modules for various functionalities. Here are some commonly used modules:

- **`math`**: Provides mathematical functions.
- **`datetime`**: Deals with date and time.
- **`os`**: Provides functions for interacting with the operating system.
- **`sys`**: Used for system-specific parameters and functions.
- **`json`**: Works with JSON data.

### Example Usage:
Here are some example usages for the `math`, `datetime`, `os`, `sys`, and `json` modules in Python.

---

### 1. `math` Module
The `math` module provides mathematical functions, constants, and tools to work with numbers.

#### Example Usage:
```python
import math

# Find the square root of a number
print(math.sqrt(16))  # Output: 4.0

# Calculate the cosine of 0 radians
print(math.cos(0))  # Output: 1.0

# Calculate factorial of a number
print(math.factorial(5))  # Output: 120

# Using the constant pi
print(math.pi)  # Output: 3.141592653589793
```

---

### 2. `datetime` Module
The `datetime` module is used for working with dates and times, providing functions to get the current date and time, format dates, and perform date arithmetic.

#### Example Usage:
```python
from datetime import datetime, timedelta

# Get the current date and time
now = datetime.now()
print(now)  # Output: 2024-11-03 14:22:12.345678 (example)

# Format date and time
formatted_date = now.strftime("%Y-%m-%d %H:%M:%S")
print(formatted_date)  # Output: 2024-11-03 14:22:12

# Calculate a date 7 days from now
next_week = now + timedelta(days=7)
print(next_week)  # Output: 2024-11-10 14:22:12.345678

# Get the current year, month, and day
print(now.year, now.month, now.day)  # Output: 2024 11 3
```

---

### 3. `os` Module
The `os` module provides a way to interact with the operating system, such as accessing file paths, creating directories, and getting environment variables.

#### Example Usage:
```python
import os

# Get the current working directory
current_directory = os.getcwd()
print(current_directory)  # Output: /Users/yourusername/project

# List all files and directories in the current directory
print(os.listdir(current_directory))

# Create a new directory (if it doesn't exist)
new_dir = "example_dir"
if not os.path.exists(new_dir):
    os.mkdir(new_dir)
    print(f"Directory '{new_dir}' created")

# Get an environment variable (e.g., PATH)
path = os.getenv("PATH")
print(path)
```

---

### 4. `sys` Module
The `sys` module provides access to variables and functions that interact closely with the Python interpreter, such as handling command-line arguments, exiting programs, and getting Python version information.

#### Example Usage:
```python
import sys

# Get the version of Python
print(sys.version)  # Output: Python 3.9.1 (or your version)

# Get command-line arguments (first argument is the script name)
print(sys.argv)  # Output: ['script_name.py', 'arg1', 'arg2', ...]

# Exit a program with a specific status code
sys.exit(0)  # Status code 0 indicates success

# Set the maximum recursion limit (use with caution)
sys.setrecursionlimit(1500)
print("Recursion limit set to:", sys.getrecursionlimit())
```

---

### 5. `json` Module
The `json` module is used to work with JSON data in Python. It can parse JSON strings into Python objects and convert Python objects back to JSON strings.

#### Example Usage:
```python
import json

# Convert a Python dictionary to a JSON string
data = {
    "name": "Alice",
    "age": 30,
    "city": "Wonderland"
}
json_string = json.dumps(data)
print(json_string)  # Output: {"name": "Alice", "age": 30, "city": "Wonderland"}

# Write JSON data to a file
with open("data.json", "w") as file:
    json.dump(data, file)

# Read JSON data from a file
with open("data.json", "r") as file:
    loaded_data = json.load(file)
    print(loaded_data)  # Output: {'name': 'Alice', 'age': 30, 'city': 'Wonderland'}

# Convert JSON string back to a Python dictionary
parsed_data = json.loads(json_string)
print(parsed_data)  # Output: {'name': 'Alice', 'age': 30, 'city': 'Wonderland'}
```

## 3. Modules and Packages
While a module is a single file, a package is a collection of modules in a directory with a special `__init__.py` file. Packages are used to organize related modules together. For example, a package for data science might contain modules for data cleaning, visualization, and modeling.

### Creating a Package:
1. Create a directory with the desired package name.
2. Add an `__init__.py` file inside the directory.
3. Add your module files.

### Example Structure:
```
data_science_package/
├── __init__.py
├── cleaning.py
├── visualization.py
```

### Importing from a Package:
```python
from data_science_package import cleaning
from data_science_package.visualization import plot_graph
```

## 4. Python Package Installer (PIP)
PIP is the standard package manager for Python, used to install and manage additional libraries that are not included in Python’s standard library. With PIP, you can install packages from the Python Package Index (PyPI) and make use of libraries created by others.

### Basic Commands:
- **Install a package**: `pip install package_name`
- **Upgrade a package**: `pip install --upgrade package_name`
- **Uninstall a package**: `pip uninstall package_name`

### Example:
```bash
pip install requests
```

The `requests` module is widely used for making HTTP requests in Python. Here's an example of how to use it with a mock API, such as [JSONPlaceholder](https://jsonplaceholder.typicode.com/), which provides fake online REST APIs for testing and prototyping.

### Example Usage of `requests` Module with JSONPlaceholder Mock API

Install the `requests` module if you haven't already:
```bash
pip install requests
```

### 1. Basic GET Request
Let's fetch a list of users from JSONPlaceholder's `/users` endpoint.

```python
import requests

# GET request to fetch user data
response = requests.get("https://jsonplaceholder.typicode.com/users")

# Check if request was successful
if response.status_code == 200:
    users = response.json()  # Convert response to JSON
    for user in users:
        print(f"Name: {user['name']}, Email: {user['email']}")
else:
    print("Failed to retrieve data:", response.status_code)
```

### 2. GET Request with Query Parameters
Fetching posts by a specific user ID using query parameters.

```python
# Fetch posts by user with ID 1
response = requests.get("https://jsonplaceholder.typicode.com/posts", params={"userId": 1})

if response.status_code == 200:
    posts = response.json()
    for post in posts:
        print(f"Title: {post['title']}\nBody: {post['body']}\n")
else:
    print("Failed to retrieve posts:", response.status_code)
```

### 3. POST Request to Create a New Post
You can also simulate creating a new resource, like a blog post, using a POST request.

```python
# Define data for the new post
new_post = {
    "userId": 1,
    "title": "Mock Post Title",
    "body": "This is a mock post body content."
}

# Make a POST request
response = requests.post("https://jsonplaceholder.typicode.com/posts", json=new_post)

if response.status_code == 201:  # 201 Created
    created_post = response.json()
    print("New post created:", created_post)
else:
    print("Failed to create post:", response.status_code)
```

### 4. PUT Request to Update an Existing Post
Updating a resource, like modifying an existing post.

```python
# Update post with ID 1
updated_post = {
    "userId": 1,
    "title": "Updated Title",
    "body": "This is the updated content of the post."
}

response = requests.put("https://jsonplaceholder.typicode.com/posts/1", json=updated_post)

if response.status_code == 200:
    print("Post updated:", response.json())
else:
    print("Failed to update post:", response.status_code)
```

### 5. DELETE Request to Delete a Post
Deleting a resource, such as removing a post.

```python
# Delete post with ID 1
response = requests.delete("https://jsonplaceholder.typicode.com/posts/1")

if response.status_code == 200:
    print("Post deleted successfully.")
else:
    print("Failed to delete post:", response.status_code)
```

### _Happy learning!_
