# Chapter 2: Python Primer

In this chapter, we aim to provide a quick primer on Python programming to help you get started with test automation. Python is a versatile, high-level programming language known for its readability and simplicity. Its straightforward syntax, extensive library ecosystem, and strong community support make Python an excellent choice for various tasks, including test automation.

This chapter serves as a brief refresher for those already familiar with Python, and a starting point for those new to the language. We will cover core concepts like variables, operators, conditionals, loops, functions, classes, and unit testing frameworks with concise examples. Additionally, we will include references to resources where you can learn more in-depth information about Python.

By the end of this chapter, you will have a solid understanding of Python's fundamental concepts, enabling you to tackle test automation tasks and projects confidently.

## 2.1 Python Programming Syntax

Python's syntax is designed to be simple and easy to read, making it an excellent choice for beginners and experienced programmers alike. In this section, we'll cover some basic syntax rules that you should be familiar with when writing Python code.

1. **Indentation**: Python uses indentation to define blocks of code, such as those within loops, conditionals, and functions. Indentation is typically done with four spaces, but you can also use tabs. Consistent indentation is crucial for proper code execution and readability.
Example:

``` python
if x > 0:
    print("x is positive")
else:
    print("x is not positive")
```

1. **Comments**: Comments are an essential part of any programming language, as they allow you to add explanations and notes to your code. In Python, you can use the hash symbol (#) to write single-line comments. For multi-line comments, you can use triple quotes (''' or """).

Example:

``` python
# This is a single-line comment

'''
This is a
multi-line
comment
'''

```

By understanding these basic syntax rules, you'll be able to write clean and readable Python code, setting a strong foundation for your test automation projects.

## 2.2 Variables, Data Types, and Operators

In this section, we will cover variables, common data types, and operators in Python. These fundamental concepts are essential for writing Python code and understanding how data is stored and manipulated.

### 1. **Variables and Naming Conventions**: 

Variables are used to store data in Python. Variable names should be descriptive and follow the standard naming conventions (lowercase words separated by underscores). Avoid using reserved Python keywords as variable names.

Example:

``` python

age = 25
first_name = "Alice"

```

### 2. **Common Data Types**

Python has several built-in data types, including:

   - `int`: Integer numbers (e.g., 42)
   - `float`: Floating-point numbers (e.g., 3.14)
   - `str`: Strings (e.g., "Hello, World!")
   - `list`: Ordered, mutable collections (e.g., [1, 2, 3])
   - `tuple`: Ordered, immutable collections (e.g., (1, 2, 3))
   - `dict`: Key-value pairs (e.g., {"apple": 3, "banana": 5})

Example:

``` python
integer_value = 42
floating_point_value = 3.14
string_value = "Hello, World!"
list_value = [1, 2, 3]
tuple_value = (1, 2, 3)
dictionary_value = {"apple": 3, "banana": 5}
```

### 3. **Operators**: 

Python provides various operators to perform operations on data, such as:

- *Arithmetic operators*: 
    - `+`  : Addition Operator
    - `-`  : Subtraction Operator
    - `*`  : Multiplication Operator
    - `/`  : Division Operator
    - `//` : Floor Division (Example `5//2 = 2`)
    - `%`  : Modulo (reminder) Operator (Example `5%2 = 1`)
    - `**` : Exponent Operator (Example `2**3 = 8`)

- *Comparison operators*: 
    - `==` : Equality check
    - `!=` : Not equal check
    - `<`  : Less than check
    - `>`  : Greater than check
    - `<=` : Less than or equal to check
    - `>=` : Greater than or equal to check

- *Logical operators*: 
    - `and`: Logical AND (Example `True and True = True`)
    - `or` : Logical OR (Example `True or False = True`)
    - `not` : Logical NOT (Example `not True = False`)

- *Membership operators*: 
    - `in` : Check if a value is in a collection. (Example `5 in [1, 2, 3, 4, 5] = True`)
    - `not in`: Check if a value is not in a collection. (Example `6 not in [1, 2, 3, 4, 5] = True`)

- *Identity operators*: 
    - `is` : Check if two variables are the same object
    - `is not`: Check if two variables are not the same object

Some examples:

``` python

x = 10
y = 5

sum = x + y
difference = x - y
product = x * y
quotient = x / y

is_equal = x == y
is_greater = x > y

result = x > 0 and y > 0

found = y in [1, 2, 3, 4, 5]

is_same_object = x is not y

```

By understanding variables, data types, and operators in Python, you'll be able to work with data effectively and write efficient test automation code.

## 2.3 Conditional Statements

Conditional statements are a fundamental concept in Python programming. They allow you to make decisions and execute different blocks of code based on specific conditions. In this section, we'll cover the `if`, `if`-`else`, and `if`-`elif`-`else` statements.

1. `if` statement: The `if` statement is used to execute a block of code when a specific condition is true.

Example:

``` python
temperature = 35

if temperature > 30:
    print("It's hot outside.")
```

2. `if`-`else` statement: The `if`-`else` statement is used to execute one block of code if a condition is true, and another block if the condition is false.

Example:

``` python
temperature = 25

if temperature > 30:
    print("It's hot outside.")
else:
    print("It's not hot outside.")

```


3. `if`-`elif`-`else` statement: The `if`-`elif`-`else` statement is used to test multiple conditions and execute the corresponding block of code. If none of the conditions are true, the code within the else block is executed.

Example:

``` python
temperature = 20

if temperature > 30:
    print("It's hot outside.")
elif temperature < 10:
    print("It's cold outside.")
else:
    print("The temperature is moderate.")
```

By mastering conditional statements in Python, you can create complex and flexible test automation scripts that can adapt to various situations and conditions.

## 2.4 Loops

Loops are another essential concept in Python programming. They allow you to execute a block of code repeatedly until a specific condition is met. In this section, we will cover the `for` loop, `while` loop, and `list` comprehensions.

### `for` loop: 
The `for` loop iterates over a sequence (such as a list, tuple, or string) and executes a block of code for each element in the sequence.

Example:

``` python
fruits = ["apple", "banana", "cherry"]

for fruit in fruits:
    print(fruit)
```

Output:
```
apple
banana
cherry
```


### `while` loop: 
The `while` loop repeatedly executes a block of code as long as a specific condition remains true.

Example:

``` python
count = 0

while count < 5:
    print(count)
    count += 1
```

Output:
```
0
1
2
3
4
```


### `list` comprehensions: 
`list` comprehensions are a concise way to create a new list by applying an expression to each element in an existing list or other iterable object.

Example:

``` python
numbers = [1, 2, 3, 4, 5]
squares = [x ** 2 for x in numbers]

print(squares)
```

Output:
```
[1, 4, 9, 16, 25]
```

Understanding loops in Python will enable you to write more efficient and effective test automation scripts by repeating tasks and processing large amounts of data with ease.

### `break` and `continue`: 
The `break` and `continue` statements can be used to control the flow of a loop.

For example: 

``` python
for x in range(10):
    if x == 5:
        break
    print(x)
```

The above code will print the numbers from 0 to 4 and then exit the loop.

Output:
``` bash
0
1
2
3
4
```

``` python
for x in range(10):
    if x == 5:
        continue
    print(x)
```

The above code will print the numbers from 0 to 9, except 5.

```bash
0
1
2
3
4
6
7
8
9
```

### `range()` function

`range()` is a built-in function that generates a sequence of numbers, which can be used with a `for` loop to iterate a specific number of times.

Example:

``` python
for i in range(5):
    print(i)
```

Output:
``` bash
0
1
2
3
4
5
```


### Nested Loops


You can also have nested loops, where one loop is placed inside another loop. This is useful when you need to iterate over multiple dimensions, such as a matrix or a nested list.

Example:

``` python

matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

for row in matrix:
    for element in row:
        print(element, end=" ")
    print()  # Print a newline after each row

```

Output:
``` bash
1 2 3
4 5 6
7 8 9
```


### `for` loop with `enumerate()`


`enumerate()` is a built-in function that can be used with a `for` loop to iterate over a sequence while keeping track of the index of the current element.

Example:

``` python

fruits = ["apple", "banana", "cherry"]

for index, fruit in enumerate(fruits):
    print(index, fruit)

```

Output:
``` bash
0 apple
1 banana
2 cherry
```

### `for` loop with `zip()`

`zip()` is a built-in function that can be used with a `for` loop to iterate over multiple sequences at the same time.

Example:

``` python

names = ["John", "Jane", "Bob"]
ages = [24, 25, 26]

for name, age in zip(names, ages):
    print(name, age)

```

Output:
``` bash
John 24
Jane 25
Bob 26
```

### `for` loop with `reversed()`

`reversed()` is a built-in function that can be used with a `for` loop to iterate over a sequence in reverse order.

Example:

``` python
for i in reversed(range(5)):
    print(i)
```

Output:
``` bash
4
3
2
1
0
```

### `for` loop with `sorted()`

`sorted()` is a built-in function that can be used with a `for` loop to iterate over a sequence in sorted order.
    
Example:

``` python
fruits = ["apple", "banana", "cherry"]

for fruit in sorted(fruits):
    print(fruit)
```

Output:
``` bash
apple
banana
cherry
```

### `for` loop with `dict.items()`

`dict.items()` is a built-in function that can be used with a `for` loop to iterate over a dictionary and access its keys and values.

Example:

``` python
person = {
    "name": "John",
    "age": 24,
    "country": "Norway"
}

for key, value in person.items():
    print(key, value)
```

Output:
``` bash
name John
age 24
country Norway
```

### `while` loop with `else`

The `else` clause can be used with the `while` loop to execute a block of code once when the condition no longer holds true. This can be helpful for handling scenarios that occur after the loop has finished iterating.

Example:

``` python

count = 0

while count < 5:
    print(count)
    count += 1
else:
    print("Loop finished")

```

Output:
``` bash
0
1
2
3
4
Loop finished
```

These examples showcase the versatility of loops in Python and their importance in creating efficient test automation scripts.


## 2.5 Functions and Modules

Functions and modules are crucial components of Python programming that allow you to organize and reuse code efficiently. In this section, we will cover defining and calling functions, function parameters and arguments, the return statement, and importing modules.

### Defining and Calling Functions
Functions are defined using the def keyword, followed by the function name and a pair of parentheses containing the function's parameters. The function's code block is then indented. Functions are called by their name, followed by parentheses containing the arguments.

Example:
```
def greet(name):
    print(f"Hello, {name}!")

greet("Alice")  # Will output "Hello, Alice!"
```

We've been using functions all this while. For example, the `print()` function prints the specified message to the console. The `range()` function returns a sequence of numbers, starting from 0 by default, and increments by 1 (by default), and stops before a specified number. These functions are in-built functions that come with Python.

### Function Parameters and Arguments:

Parameters are the variables listed in the function definition, while arguments are the values passed to the function when it is called. You can pass multiple arguments to a function by separating them with commas.

Example:

``` python
def add(a, b):
    result = a + b
    print(f"The sum of {a} and {b} is {result}")

add(5, 3)

```

### The `return` statement:

The `return` statement is used to exit a function and return a value. The `return` statement can be used without any arguments to exit a function. 

Example:

``` python
def multiply(a, b):
    return a * b

product = multiply(4, 3)
print(f"The product of 4 and 3 is {product}")
```

Functions without a `return` statement return `None`.

### Modules and Importing:

Modules are Python files containing functions, classes, and variables that can be imported into other Python scripts. To use a module, you need to import it using the import keyword. You can also use the from keyword to import specific functions or classes from a module.

Example:


``` python
# Import the entire math module
import math
print(math.sqrt(16))

# Import only the sqrt function from the math module
from math import sqrt
print(sqrt(16))

# Import the sqrt function with an alias (nickname)
from math import sqrt as square_root
print(square_root(16))
```

Understanding functions and modules in Python will help you write modular and reusable test automation code, making your scripts more maintainable and efficient.


### Default Parameter Values:
Below are a few more advanced concepts that we are listing here for reference. 

You can assign default values to function parameters. This way, if the caller doesn't provide a value for a parameter, the default value will be used.

Example:

``` python
def greet(name, greeting="Hello"):
    print(f"{greeting}, {name}!")

greet("Alice")  # Uses the default greeting
greet("Bob", "Hi")  # Uses a custom greeting
```

### Keyword Arguments:

When calling a function, you can use keyword arguments to specify the values for specific parameters. This can make your function calls more readable and flexible.

Example:

``` python
def display_info(name, age, city):
    print(f"{name} is {age} years old and lives in {city}.")

display_info("Alice", 25, "New York")
display_info(age=30, city="London", name="Bob")

```

### Variable-length Arguments:


You can use the `*args` and `**kwargs` syntax to accept a variable number of arguments in your functions. This is useful when you don't know how many arguments will be passed to a function.

``` python
def sum_numbers(*args):
    total = 0
    for number in args:
        total += number
    return total

print(sum_numbers(1, 2, 3))  # Output: 6
print(sum_numbers(4, 5))  # Output: 9
```

### Lambda Functions:

Lambda functions are small, anonymous functions defined using the lambda keyword. They can have any number of arguments but can only contain a single expression.

Example:

```
square = lambda x: x ** 2
print(square(4))  # Output: 16
```

### Organizing Modules in Packages:

Packages are a way to organize related modules in a directory hierarchy. To create a package, create a directory and include an `__init__.py` file in it. You can then import modules from the package using the dot notation.

Example:

```
my_package/
    __init__.py
    module1.py
    module2.py
```

``` python
from my_package import module1
from my_package.module2 import some_function
```

These additional concepts related to functions and modules will further enhance your ability to create modular, reusable, and efficient test automation code in Python.


## 2.6 Classes and Objects

Classes and object-oriented programming (OOP) are essential concepts in Python that help you create organized and reusable code. In this section, we will cover classes, objects, methods, inheritance, and polymorphism.


### Classes and Objects:
A class is a blueprint for creating objects (instances) with specific properties (attributes) and behaviors (methods). Objects are instances of classes.

Example:

``` python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model

    def honk(self):
        print(f"The {self.make} {self.model} honks!")

my_car = Car("Toyota", "Corolla")
my_car.honk()  # Output: The Toyota Corolla honks!
```

### Methods:

Methods are functions that belong to a class and act on the object's attributes. They are defined within a class and are called on instances of the class.

Example:

``` python

class Circle:
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * (self.radius ** 2)

my_circle = Circle(5)
print(my_circle.area())  # Output: 78.5

```


### Inheritance:

Inheritance allows you to create a new class that inherits attributes and methods from an existing class. The new class is called the subclass, and the existing class is the superclass.

Example:

```python
class Vehicle:
    def __init__(self, make, model):
        self.make = make
        self.model = model

class Car(Vehicle):
    def honk(self):
        print(f"The {self.make} {self.model} honks!")

my_car = Car("Toyota", "Corolla")
my_car.honk()  # Output: The Toyota Corolla honks!
```



### Polymorphism:

Polymorphism enables you to use a single interface for different data types or classes, allowing you to write more flexible and reusable code. Polymorphism is often used in conjunction with inheritance.

For beginner programmers - inheritance and polymorphism might not be of much use in the beginning. But as you progress in your career, you will find that these concepts are very useful in writing efficient and reusable code.

Example:

``` python
class Dog:
    def speak(self):
        return "Woof!"

class Cat:
    def speak(self):
        return "Meow!"

def make_sound(animal):
    print(animal.speak())

dog = Dog()
cat = Cat()

make_sound(dog)  # Output: Woof!
make_sound(cat)  # Output: Meow!

```

Understanding classes and object-oriented programming in Python is vital for creating modular, reusable, and maintainable test automation code, as it helps you model real-world entities and their relationships.


### Advanced concepts

Below are a few more concepts related to classes and object-oriented programming that are worth highlighting:

- **Class Attributes**
Class attributes are variables shared by all instances of a class. They are defined at the class level, outside any method.

Example:

``` python
class Car:
    wheels = 4  # Class attribute

    def __init__(self, make, model):
        self.make = make  # Instance attribute
        self.model = model  # Instance attribute

my_car = Car("Toyota", "Corolla")
print(my_car.wheels)  # Output: 4
```

- **Instance Methods, Class Methods, and Static Methods**

In addition to instance methods, classes can have class methods and static methods. Class methods are bound to the class and not the instance, while static methods don't depend on the class or instance and are used like regular functions.

Example:

``` python
class MyClass:
    @classmethod
    def class_method(cls):
        print("Called class method.")

    @staticmethod
    def static_method():
        print("Called static method.")

    def instance_method(self):
        print("Called instance method.")

obj = MyClass()
obj.instance_method()
MyClass.class_method()
MyClass.static_method()
```

- **Property Decorator**

The property decorator allows you to create getter and setter methods for class attributes. This can be useful for encapsulating internal state and validating attribute values.

Example:

``` python

class Person:
    def __init__(self, first_name, last_name):
        self.first_name = first_name
        self.last_name = last_name

    @property
    def full_name(self):
        return f"{self.first_name} {self.last_name}"

    @full_name.setter
    def full_name(self, name):
        first_name, last_name = name.split(" ")
        self.first_name = first_name
        self.last_name = last_name

```

These additional concepts related to classes and object-oriented programming may not be necessary for beginner programmers, but they are worth knowing as you progress in your career.


## 2.7 Unit Testing with PyTest

Unit testing is a critical part of the software development process that helps ensure the correctness and reliability of your code. Python offers several testing frameworks to write and execute unit tests, with PyTest being one of the most popular.

In this section, we will provide a brief introduction to PyTest, explaining how to install it, write simple tests, and run them.

### Installing PyTest:

To install PyTest, you can use pip, the Python package manager. Open a terminal or command prompt and run the following command:

``` bash
pip install pytest
```

### Writing Tests:

PyTest uses the `assert` keyword to verify that the expected result matches the actual result. If the assertion fails, the test fails.

Example:

``` python
# test_example.py
def add(a, b):
    return a + b

def test_add():
    result = add(3, 4)
    assert result == 7
```

### Running Tests:

To run the tests, open a terminal or command prompt in the directory containing your test file and run the pytest command. PyTest will automatically discover and run tests in your project.

``` bash
pytest
```

PyTest will display the results of your tests, indicating whether they passed or failed.


### Assertions and Test Fixtures:

In PyTest, you use the assert statement to verify that your code behaves as expected. PyTest also supports test fixtures, which are reusable pieces of code for setting up and tearing down test environments.

Example:

``` python
import pytest

@pytest.fixture
def sample_data():
    return [1, 2, 3, 4, 5]

def test_sum(sample_data):
    result = sum(sample_data)
    assert result == 15

def test_len(sample_data):
    assert len(sample_data) == 5

```

This brief introduction to PyTest should help you get started with writing and running unit tests in Python. As you progress through the book, you will learn more advanced testing techniques and apply them to your test automation projects.


## 2.8 Summary

In Chapter 2, we provided a quick primer on Python to help you get familiar with the core concepts necessary for test automation. Here's a summary of the key topics we covered:

- **Python programming syntax**: We discussed the basic structure and syntax of Python programs, including comments, indentation, and import statements.

- **Variables, data types, and operators**: We introduced variables and basic data types in Python (integers, floats, strings, and booleans), as well as common operators for performing arithmetic, comparison, and logical operations.

- **Conditional statements (if/else)**: We explained how to use `if`, `elif`, and `else` statements to control the flow of a program based on conditions.

- **Loops (for and while)**: We covered `for` and `while` loops, which allow you to execute a block of code repeatedly based on a condition or a sequence.

- **Functions and modules**: We demonstrated how to define and call functions, as well as how to organize your code into modules and import them.

- **Classes and object-oriented programming**: We explored classes, objects, methods, inheritance, and polymorphism, which are fundamental concepts in Python's object-oriented programming model.

- **Introduction to Python unit testing frameworks (PyTest)**: We provided a brief overview of PyTest, a popular Python testing framework, and showed you how to install it, write simple tests, and run them.

This chapter aimed to equip you with a solid understanding of Python's core concepts, laying the foundation for the more advanced topics and test automation techniques we'll cover in the upcoming chapters. Remember that practice is crucial for mastering Python, so don't hesitate to experiment with the examples and write your own code as you progress through the book.

For those interested in diving deeper into Python, here is a list of excellent resources to learn more:

- **[Python.org](https://www.python.org/about/gettingstarted/)**: Python.org offers beginner's guides, advanced guides, and various other resources for learning Python, directly from the organization that maintains the language. 

- **[Real Python](https://realpython.com/)**: Real Python offers high-quality tutorials, articles, and other resources for learning Python, covering a wide range of topics and skill levels. 

- **[Codecademy](https://www.codecademy.com/learn/learn-python-3)**: Codecademy provides an interactive Python course that covers essential concepts with hands-on exercises and projects. 

- **[Coursera](https://www.coursera.org/specializations/python)**: Coursera offers numerous Python courses, including the popular "Python for Everybody" specialization by the University of Michigan. 

- **[edX](https://www.edx.org/course/introduction-to-computer-science-and-programming-7)**: edX also provides various Python courses, such as the "Introduction to Computer Science and Programming Using Python" course by MIT. 

- **[Automate the Boring Stuff with Python](https://automatetheboringstuff.com/)**: This book by Al Sweigart focuses on practical Python programming and automation of everyday tasks, making it an excellent resource for those who want to apply Python to real-world problems. 

- **[Corey Schafer's YouTube Channel](https://www.youtube.com/user/schafer5)**: Corey Schafer's YouTube channel offers an extensive collection of Python tutorials, covering basics, intermediate, and advanced topics. 

- **[SoloLearn](https://www.sololearn.com/Course/Python/)**: SoloLearn offers a mobile app and website for learning Python and other programming languages with interactive exercises and a supportive community. 

- **[Python Crash Course](https://nostarch.com/pythoncrashcourse2e)**: This book by Eric Matthes provides a fast-paced and thorough introduction to Python, aimed at beginners who want to quickly learn the language and start working on real-world projects. 

These resources cater to various learning styles and proficiency levels, so feel free to explore and find the ones that suit you best. As you learn more about Python, remember to practice regularly, experiment with the concepts you learn, and apply them to your test automation projects.

