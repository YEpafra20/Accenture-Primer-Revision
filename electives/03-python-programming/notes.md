# Programming using Python — Revision Notes

**Category:** Electives · **Focus Area:** Python Programming · **Level:** Beginner

---

## Table of Contents

1. [Introduction to Python](#1-introduction-to-python)
2. [Control Structures](#2-control-structures)
3. [Collection Frameworks](#3-collection-frameworks)
4. [Functions and Modules](#4-functions-and-modules)
5. [File Handling](#5-file-handling)
6. [Code Analysis and Debugging](#6-code-analysis-and-debugging)

---

## 1. Introduction to Python

### 1.1 Why Python?

**General Characteristics:** High-level language, Readable, General Purpose, Widely used

**For Developers:** Intuitive Syntax, Free and Open Sourced, Community Support, Strong Guidelines, Strong Standards

**Applications:** Data Science, Data Engineering, Web Development, Big Data, Analytics, Web Testing, Artificial Intelligence, Smart Device Programming

### 1.2 Applications of Python

| Category | Details |
|---|---|
| **Web Development** | Django, Tornado, Flask |
| **General** | Scientific Analysis, Testing Applications |
| **Data Science** | Machine Learning, Web Scraping, Exploratory Data Analysis, Deep Learning, Artificial Intelligence, Unstructured Data Analysis |

### 1.3 Tokens

**Keywords** — reserved words with special meaning for the Python interpreter:

```
and, del, from, not, while, as, elif, global, or, with,
assert, else, if, pass, yield, break, except, import, print,
class, exec, in, raise, continue, finally, is, return, def, for, lambda, try
```

**Identifiers (names)** — names given to different parts of a program (variables, objects, classes, functions, etc.)

**Rules for identifiers:**
- The first character must be a letter or underscore
- Upper and lower case are different (case-sensitive)
- Must not be a keyword
- No special characters allowed other than underscore
- Spaces are not allowed

**Operations** — covered under [Types of Operators](#17-types-of-operators)

**Literals/Values** — data items that have a fixed value:

| Literal Type | Examples |
|---|---|
| String Literals | `"python"`, `"12345"` |
| Numeric Literals | `12345`, `123.45` |
| Boolean Literals | `True`, `False` |
| Special Literals | `None` |
| Literal Collections | Lists, Tuples, Sets, Dictionaries |

### 1.4 Comments

| Type | Example |
|---|---|
| **Single-line comment** | `# This is a program for calculating the area of a circle` |
| **Inline comment** | `area = length * breadth  # calculating area of rectangle` |
| **Multi-line comment** | `"""` <br> `Program name: rectangle area calculation` <br> `Owner: xyz` <br> `Language: Python` <br> `"""` |

### 1.5 Data Types

**Variable Declaration:** Declaring a variable in Python is straightforward. Python destroys unused variable storage automatically; you can add variables during runtime.

| Data Type | Description | Example |
|---|---|---|
| **Numbers** (Integer, Float) | — | `TotalPrice = 100.78`, `Complex_value = 2 + 3j` |
| **Boolean** (True/False) | — | `if (Age >= 18): eligible_to_vote = True else: eligible_to_vote = False` |
| **Strings** | Sequence of Unicode characters | `Message = "Welcome to python"` or `Message = 'Welcome'` |
| **Bytes and ByteArray** | Immutable and mutable sequences | `x = b"Welcome"` (byte object), `x = bytearray(b"Python Bytes")` (byte array) |
| **Lists** | Ordered, mutable sequence of values | `Value = [1, 2.2, "Python"]` |
| **Tuples** | Ordered, immutable sequence of values | `Value = (2, "Tuple", "95")` |
| **Sets** | Unordered collection of values | `week = {'Mon', 'Tue', 'Wed'}` |
| **Dictionaries** | Unordered collection of key-value pairs | `Value = {'key': 1, 'value': 'apple'}` |

**Integers:** All positive and negative whole numbers are considered INTEGERS in Python.

**Float:** Numbers with a fractional part (decimal points) are considered FLOAT.

**Strings:** A sequence of literal characters enclosed in a matching pair of quotation marks — single (`'`), double (`"`), or triple (`"""` or `'''`) quotes.

**Boolean:** Holds a value of either `True` or `False`. Boolean values can be derived from numbers or strings.

### 1.6 Type Conversion

`int()` — rounds off a float number and converts it to an integer. If the floating variable contains null or infinity, the conversion throws an error.

Integers can easily be converted to float. Strings containing only numbers inside quotes can also be converted to float or integer, depending on the number type inside the string.

```python
X1 = 10.5
X2 = int(X1)
X2, type(X2)
# Output: (10, <class 'int'>)
```

**None:** A special type denoting a "null object" — useful when a variable is available, but its value is considered undefined.

### 1.7 Integer vs Float Division

By default, Python 3 does float division — even if two integers are divided, the result is a float. To get an integer result, use the double forward slash `//` (floor division); the fractional part is discarded.

```python
10 / 5    # Output: 2.0
10 // 3   # Output: 3
```

### 1.8 Input Statements

`input()` — takes input from the user. The value returned by `input()` is always of **string** type.

**Syntax:** `variable = input(<message to display>)`

> Note: Even if you enter `100`, it will be treated as a string and will not allow arithmetic operations.

**Reading numbers as input:**
Convert the value from `input()` to a numeric type using `int()` or `float()`.

### 1.9 Output/Print Statements

Python allows displaying output using `print()`.

```python
# Printing in the same line
print("Python Programming", end="")
print("Developed by Guido Van Rossum")
# Output: Python Programming Developed by Guido Van Rossum
```

### 1.10 Types of Operators

| Operator Type | Operators |
|---|---|
| **Unary Operators** | `+` (unary plus), `-` (unary minus), `~` (bitwise complement), `not` (logical negation) |
| **Arithmetic Operators** | `+`, `-`, `*`, `/`, `%`, `**`, `//` |
| **Identity Operators** | `is`, `is not` |
| **Relational Operators** | `<`, `>`, `<=`, `>=`, `==`, `!=` |
| **Logical Operators** | `and`, `or`, `not` |
| **Assignment Operators** | `=`, `/=` (assign quotient), `+=` (assign sum), `-=` (assign difference), `*=` (assign product), `**=` (assign exponent), `//=` (assign floor division) |
| **Membership Operators** | `in`, `not in` |

---

## 2. Control Structures

### 2.1 Conditional Statements

- Used to test assumptions or compare values
- Must be indented properly
- Nested conditional statements are possible
- A simple conditional statement can have just the `if` part alone

```python
x = 1
y = 2
if x == y:
    print('x and y are equal')
else:
    print('x and y are not equal')
# Output: x and y are not equal
```

### 2.2 Single-Line and ELIF Statements

**Single-line conditional:**

```python
print('x and y are equal' if x == y else 'x and y are not equal')
# Output: x and y are not equal
```

**ELIF:**

```python
x = 1
y = 2
if x > y:
    print('x is greater than y')
elif x < y:
    print('x is less than y')
else:
    print('x is equal to y')
# Output: x is less than y
```

### 2.3 Nested Conditional Statements

- Can be nested to any depth
- It is not mandatory that every `if` in nesting must have an `else` coupled with it

```python
age = int(input("Please Enter Your Age Here: "))
if age < 18:
    print("You are Minor")
    print("You are not Eligible to work")
else:
    if age >= 18 and age <= 60:
        print("You are Eligible to work")
        print("Please fill in your details and apply")
    else:
        print("You are too old to work as per the Government rules")
        print("Please Collect your pension!")

# Sample run:
# Please Enter Your Age Here: 7
# You are Minor
# You are not Eligible to work
```

### 2.4 AND / OR Operators in Conditional Statements

```python
if (x > 5) and (y > 5):
    print('Both x and y are greater than 5')
# Statement executes only if condition 1 AND condition 2 are True
```

### 2.5 Iterative Statements — FOR Loop

**Syntax:**
```python
for variableName in groupOfValues:
    statements
```

- Indent the repeated statements with 4 white spaces
- `variableName` names each value so you can refer to it in the statements
- `groupOfValues` can be a range of integers, specified with the `range` function

**Range in Loops:**

```
range(start, stop)
range(start, stop, step)
```

```python
for x in range(5, 0, -1):  # (Start, Stop, Step)
    print(x)
print("Blastoff!")
# Output: 5, 4, 3, 2, 1, Blastoff!
```

### 2.6 Cumulative Loops

Some loops incrementally compute a value that is initialized outside the loop — this is called a **cumulative sum**.

### 2.7 WHILE Loop

**Syntax:**
```python
while condition:
    statements
```

- Executes a group of statements as long as a condition is `True`
- Good for **indefinite loops** (repeats an unknown number of times)

### 2.8 ELSE Statement in Loops

- If `else` is used with a **for** loop, it executes when the loop has exhausted iterating the list
- If `else` is used with a **while** loop, it executes when the condition becomes false

### 2.9 Nested Loops

A nested loop is a loop that occurs within another loop.

```python
# Program to print a number pattern
for i in range(1, 6):
    for j in range(i):
        print(i, end=' ')
    print()
```

### 2.10 Control Statements in Loops

Loop control statements change execution from its normal sequence.

| Statement | Description |
|---|---|
| **break** | Terminates the loop statement and transfers execution to the statement immediately after the loop |
| **continue** | Causes the loop to skip the remainder of its body and immediately retest its condition prior to the next iteration |
| **pass** | Used when a statement is required syntactically, but no command or code should execute |

**BREAK example:**

```python
for n in range(0, 11):
    if n == 5:
        break
    print(n)
print("End of the loop")
# Output: 0, 1, 2, 3, 4, End of the loop
```

**CONTINUE example:**

```python
print("Odd Numbers are: ")
for n in range(1, 11):
    if n % 2 == 0:
        continue
    print(n)
# Output: Odd Numbers are: 1, 3, 5, 7, 9
```

---

## 3. Collection Frameworks

### 3.1 List

- A data structure containing an **ordered collection** of elements
- Can contain numbers, strings, and any other data structures in an arbitrarily nested, heterogeneous fashion
- Surrounded by square brackets `[]`, items separated by commas
- Retains the order in which items are created (unlike a set)
- Elements are completely **mutable** — can be changed at any point in time
- List and string indexing work in the same fashion

```python
marks = [95, 23, 50, 76, 65]
type(marks)   # Output: list
len(marks)    # Output: 5
```

**Adding elements (use `append()` to add to the end):**

```python
names.append('F')
print(names)
# Output: ['A', 'B', 'C', 'D', 'E', 'F']
```

**Deleting elements (use `del` to remove by index):**

```python
del names[0]
print(names)
# Output: ['B', 'C', 'D', 'E']
```

**List Sorting:**

```python
marks.sort()
marks
# Output: [23, 50, 65, 76, 95]
```

- `sort()` alters the original list directly and returns `None`
- `marks.sort(reverse=True)` sorts descending
- `sorted()` avoids in-place sorting — the result is stored in a new variable, leaving the original list unchanged

```python
marks = [95, 23, 50, 76, 65]
marks_sorted = sorted(marks, reverse=True)
print('Original marks:', marks)
print('Sorted marks:', marks_sorted)
# Output:
# Original marks: [95, 23, 50, 76, 65]
# Sorted marks: [95, 76, 65, 50, 23]
```

### 3.2 Tuples

- Similar to a list, but **immutable** (elements cannot be modified)
- Syntax uses parentheses `()` instead of square brackets
- Can also be created without parentheses — useful when returning multiple results from a function

```python
names_tuples = ('A', 'B', 'C', 'D', 'E')
type(names_tuples)
# Output: tuple
```

**Cumulative sum example (using `+=`):**

```python
total_marks = 0
for mark in marks:
    total_marks += mark
total_marks
```

### 3.3 Set

- An **unordered** collection of items
- Every element is **unique** (no duplicates) and **immutable** (individual elements cannot be changed)
- However, the set itself is **mutable** — items can be added or removed from it
- A `for` loop can access individual elements, but order is not maintained

```python
x = {1, 2, 4, 5}
y = {1, 2, 3, 5, 5, 1, 2}
print(x)
print(type(x))
print(y)
# Output:
# {1, 2, 4, 5}
# <class 'set'>
# {1, 2, 3, 5}
```

Even if the values passed contain duplicates, `set` removes them and stores only unique values.

### 3.4 Dictionary

An **associative array** — a value in the dictionary has a name (or key).

```python
employee = {'age': 22, 'total_experience': 2.5, 'Married': False}
type(employee)
# Output: dict
```

---

## 4. Functions and Modules

### 4.1 Functions

- A **named sequence of statements** that performs a computation
- The core of any programming language is the notion of functions
- Functions allow code to be encapsulated into individual units, which can be re-used rather than duplicated
- Define a function with a name and a sequence of statements; call the function by name whenever needed
- Functions generally take arguments and return a result — there can be more than one argument and more than one return value
- Arguments and results can be of any type: number, string, Boolean, list, dictionary, etc.

### 4.2 Doc Strings

- Enclosed with triple quotes
- Used to document functions
- Should follow immediately after defining a function
- Use the `help()` function to view the documentation of any function
- It is advisable to provide documentation to any function that needs to be created

### 4.3 Scope of Variables

- Not all variables are accessible from all parts of the program, and not all variables exist for the same amount of time
- Where a variable is accessible is its **scope**; how long it exists is its **lifetime**
- Two types: **local** vs **global** variables

| Type | Description |
|---|---|
| **Local variable** | A variable inside a function; cannot be accessed outside the function |
| **Global variable** | Can be accessed across functions |

**Example — Local variable:**

```python
def square_number(x):
    x_squared = x * x
    return x_squared

print(square_number(3))
print(x_squared)
# Output: 9
# NameError: name 'x_squared' is not defined
```

**Example — Global variable:**

```python
x = 3
def square_number():
    x_squared = x * x
    return x_squared

print(square_number())
print(x)
# Output: 9, 3
```

**Example — Global & Local variable with the same name:**

```python
x = 3  # Global Variable
def square_number():
    x = 5  # Local Variable
    x_squared = x * x
    return x_squared

print(square_number())
print(x)
# Output: 25, 3
```

### 4.4 Lambda Functions

- Single-line functions
- Can be anonymous (without a name)
- Followed by the `lambda` keyword, then a list of arguments separated by commas
- The entire body is a single expression used to return a value — no explicit `return` keyword required

```python
reverse_dict = lambda x, y: y
reverse_dict(y=10, x=5)
# Output: 10
```

```python
reverse_dict = lambda x, y: print(y)
rev_dict = reverse_dict(y=10, x=5)
print(rev_dict)
# Output: 10, None
```

### 4.5 Python Modules & Packages

- A **module** is a file containing Python definitions (functions) and statements. The file name is the module name, saved with the extension `.py`
- **Packages** structure one or more modules together
- The Python Package Index (PyPI) is a repository of software for Python — it currently contains **118,274 packages**
- To install a package: `pip install <package_name>` from the command prompt

**Common packages:**

| Package | Use |
|---|---|
| `numpy` | Array manipulations |
| `os` | Operating system dependent functionality |
| `pandas` | Data analysis and transformations |
| `matplotlib` | Plotting and visualization |

### 4.6 Modules — Import

Modules/packages are imported using the `import` keyword, followed by the module's name.

```python
from os import *
getcwd()
# Output: 'E:\\Projects\\teknoturf\\python_codebase'
```

```python
from os import getcwd, chdir, listdir
print(getcwd())
# Output: E:\Projects\teknoturf\python_codebase
```

> Note: Importing all definitions using the `*` operator is not recommended.

### 4.7 Standard Libraries

**`os` module** — use the dot operator to call a routine within a module:

```python
import os
os.getcwd()
# Output: 'E:\\Projects\\teknoturf\\python_codebase'

os.chdir('E://Projects/teknoturf/python_codebase//data')
os.getcwd()
# Output: 'E:\\Projects\\teknoturf\\python_codebase\\data'

os.listdir()
# Output: ['odi-batting.csv', 'parliament.csv']
```

**`sys` module:**

| Function/Attribute | Description |
|---|---|
| `sys.argv` | Arguments passed to the program |
| `sys.exit()` | Exits the Python interpreter back to the OS console/terminal |
| `sys.float_info` | A structure containing internal max/min value representation of the float data type |
| `sys.version` | Displays the version of the Python interpreter currently in use |

**`datetime` module:**

| Function | Description |
|---|---|
| `print(dir(datetime))` | Prints all members of the datetime module |
| `print(dir(datetime.datetime))` | Prints the list of methods within this class |
| `now()` | Prints the current local date and time (same as `today()`) |
| `utcnow()` | Prints the UTC date and time |
| `time.strptime()` | A string parser — converts a string format to datetime |
| `datetime.strftime()` | A string formatter — formats a datetime object to string format |

**`math` module:**

```python
import math

math.ceil(x)      # Raises the value to the nearest ceiling integer, e.g. math.ceil(1.0001) = 2.0
math.floor(x)      # Floors the value to the lower integer, e.g. math.floor(1.99999) = 1.0
math.fabs()        # Returns the absolute value of the number
math.factorial()   # Returns the factorial of the number
round(x, [n])      # Rounds the number to a certain precision
                   # e.g. round(1.9991, 3) = 1.999, round(1.9999, 3) = 2.0
```

> Note: `math.floor(1.99999)` returns `1.0` (float), whereas `int(1.99)` returns `1` (integer).

**`shutil` module:**

```python
import shutil

shutil.copy(src, dst, *, follow_symlinks=True)   # Copies source file to destination (both must be strings)
shutil.move(src, dst, copy_function=copy2)        # Moves a file
```

**Other modules:**

| Module | Description |
|---|---|
| `filecmp` | Helps compare files in a directory or across different directories |
| `glob` | Finds all files matching a pattern set by Unix rules |
| `pickle` | Pickling (serialization/marshalling/flattening) — a way to convert a Python object (list, dictionary, etc.) into a storable/transmittable format |

**`pickle` — dumps() and loads():**

| Function | Description |
|---|---|
| `pickle.dumps(obj, protocol=None, *, fix_imports=True, buffer_callback=None)` | Returns the pickled representation of the object as a bytes object, instead of writing to a file |
| `pickle.loads(data, /, *, fix_imports=True, encoding="ASCII", errors="strict", buffers=None)` | Returns the reconstituted Python object from the pickled representation data |

### 4.8 NumPy Package

- **NumPy** — short for Numerical Python
- Helps developers analyze data and perform numerical calculations
- The NumPy array is an N-Dimensional array object
- Useful when working with matrices; has an efficient data structure

```python
import numpy as np
```

**Basic Array Characteristics:**

```python
# Creating an array object
import numpy as np
arr = np.array([1, 2, 3, 4, 5])
print(arr)
# Output: [1 2 3 4 5]

# Printing type of array object
print("array is of type: ", type(arr))
# Output: array is of type: <class 'numpy.ndarray'>

# Printing array dimensions (axes)
print("No. of dimensions: ", arr.ndim)
# Output: No. of dimensions: 1
```

**Using `dtype`:** if `dtype=bool`, the array is treated as Boolean elements:

```python
dlist = np.array([4, 5, 6, 0, 7, 0], dtype=bool)
print(dlist)
# Output: [True True True False True False]
```

**Array Dimensions:**

```python
# One-D array printed as a row
x = np.arange(4)
print(x)
# Output: [0 1 2 3]

# Bi-dimensional as a matrix (rows and columns)
x = np.arange(12)
arr = x.reshape(4, 3)
print(arr)
# Output:
# [[0 1 2]
#  [3 4 5]
#  [6 7 8]
#  [9 10 11]]
```

---

## 5. File Handling

### 5.1 Working with Files — Reading Flat Files

Read the first line of a file using `readline()`:

```python
with open('errors.txt', 'r') as f:
    read_line = f.readline()
print(read_line)
# Output: Errors can be handled using "try" and "except" statements
```

### 5.2 Sample Program — Calculate Total Sales Across Cities

```python
file = 'sales.csv'
reader = csv.DictReader(open(file, 'r'))
total_sales = 0
for row_no, line in enumerate(reader):
    total_sales += float(line['sales'])
print('Total sales across cities is: ', total_sales)
# Output: Total sales across cities is: 374.0
```

### 5.3 JSON and XML Files

**JSON (JavaScript Object Notation):**
- A file format that stores data as key-value pairs
- Enables communication with servers during deployment
- JSON data is stored in a file with the extension `.json`

**JSON in Python:**

| Function | Description |
|---|---|
| `json.load(fileObject)` | Deserializes file content into a Python dictionary |
| `json.loads(string)` | Converts a string object into a Python dictionary |
| `json.dump(dictionary, fileObject)` | Writes contents into a file object as JSON objects (serialization) |

### 5.4 XML File

**XML (Extensible Markup Language):**

| Term | Description |
|---|---|
| **Elements** | Sections in XML documents, defined by a beginning and an ending tag |
| **Root** | The largest, top-level element that contains all other elements |
| **Attributes** | Name-value pairs that exist within a start-tag or empty-element tag |

**Parsing XML using ElementTree:**

- ElementTree is a Python API for manipulating XML
- Has functions to process XML files

```python
import xml.etree.ElementTree as ET
```

**Reading XML using ElementTree:**

| Method | Description |
|---|---|
| `Element.findall()` | Finds the direct children of the current element |
| `Element.find()` | Finds the first child with a particular tag |
| `Element.text` | Accesses the element's text content |
| `Element.get()` | Accesses the element's attributes |

**Modifying an XML File:**

| Method | Description |
|---|---|
| `ElementTree.write()` | Writes XML documents to a file |
| `Element.text` | Changes field values |
| `Element.set()` | Adds and modifies attributes |
| `Element.append()` | Adds new elements |

**Removing an Element from an XML File:**

| Method | Description |
|---|---|
| `Element.remove()` | Removes elements from an XML tree |

---

## 6. Code Analysis and Debugging

> Placeholder — the source notepad covered Introduction, Control Structures, Collection Frameworks, Functions & Modules, and File Handling in depth, but did not include dedicated content for code analysis or debugging (e.g., `try`/`except` error handling, the `pdb` debugger, linting tools like `pylint`/`flake8`, or common debugging workflows). Add this content here once available — note that the File Handling section already references `try`/`except` for error handling in passing, which may be a useful starting point.

---

## Quick Revision Checklist

- [ ] Can list Python's general characteristics and developer-facing advantages
- [ ] Can list all Python keywords and the 4 rules for valid identifiers
- [ ] Can list all 4 literal types
- [ ] Can list all 8 core Python data types with an example each
- [ ] Can explain the difference between `/` and `//` division
- [ ] Can explain why `input()` always returns a string
- [ ] Can list all 7 operator categories
- [ ] Can write an if/elif/else block and a single-line conditional
- [ ] Can write a for loop using `range(start, stop, step)`
- [ ] Can differentiate `break`, `continue`, and `pass`
- [ ] Can differentiate List, Tuple, Set, and Dictionary by mutability and order
- [ ] Can explain `sort()` vs `sorted()`
- [ ] Can differentiate local vs global variable scope, including shadowing
- [ ] Can write a basic lambda function
- [ ] Can name at least 5 standard library modules and what each is used for
- [ ] Can create a NumPy array and check its type and dimensions
- [ ] Can differentiate `json.load()`, `json.loads()`, and `json.dump()`
- [ ] Can list the 3 core XML concepts (Elements, Root, Attributes)
- [ ] Can list the ElementTree methods for reading, modifying, and removing XML elements