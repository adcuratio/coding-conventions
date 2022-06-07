# Python

## Pep8

Python code has to conform with pep8 standards

**1. Use 4-space indentation and no tabs**

``` python
def func():
    pass
```

**2. Type Hinting:** Type hinting is a formal solution to statically indicate the type of value within Python code

In the below example, arg1 and arg2 are both string typed arguments. Similary, my_func() is also returning same data
typed value i.e. string.

``` python
def my_func(arg1: str, arg2: str) -> str
    pass
```

**3. Use docstrings:** Documenting every method with proper specification of parameters, return value and their
description. Try to avoid multiple returns from a function, a single generic return is preferred

``` python 
def add(num1: int, num2: int) -> int:
    """
    Add 2 numbers and return the addition
    
    Args:
        num1: Number 1
        num2: Number 2
       
    Returns:
        Returns result of addition operation
    """
    return num1 + num2
```

**4. Naming Conventions:** Use grammatically correct variable names, the class name should start with an uppercase and
must follow PascalCase convention If more than two words are to be used. In the same way, a function name should be
joined with an underscore, and it must be lowercase. In method arguments, always use self as the first argument to
declare an instance variable. In the same way, use ‘cls’ for the first argument for the class method. If the function
name clashes with a reserved argument, use an underscore instead of a wrong spelling. Constants are declared in all
capital letters.

```python
# class name follows camelcase convention
class StudentDetails:
    def __init__(self, first_name, last_name):
        self.first_name = first_name
        self.last_name = last_name
        self.student_grade = None

    # Method name, variable names in lowercase joined with an underscore
    def grade(self, marks_obtained):
        # constants in capital
        GRACE = 2
        marks_obtained = GRACE + marks_obtained

        if marks_obtained > 90:
            self.student_grade = "A"
        elif marks_obtained > 70:
            self.student_grade = "B"
        else:
            self.student_grade = "C"
```

**5. Use spaces around operators and after commas, but not directly inside bracketing constructs**

``` python
a, b = b, a

x = y(1, 2) + z(3, 4) 
```

**6. Use of trailing commas:** This is not mandatory except while making a tuple

``` python
tup = (10,)
```

**7. Use DRY (Don’t Repeat Yourself):** Always use the DRY principle to reuse the code. The best way to do it is to use
functions and classes. The common functions can be put into a separate helper.py file and can be used several times
instead of creating similar functions again and again.

Suppose if you need to read three files, instead of writing code for file read thrice, you can read it as a function and
save your time.

``` python
# function to read the file read
def file_read(filename):
    with open(filename, 'r') as f:
        return f.read() 

qualities = file_read('quality.txt')
description = file_read('description.txt')
summary = file_read('summary.txt')
```

**8. Single Quotes or Double Quotes:** In this case both can be used, make sure you choose any one of them and consistent
with it. We personally used double quotes in our code and recommend using the same.

``` python
s = "This is string"
t = "String with 'quotes'"
```

**9. Auto-Formatting:** There are several auto-formatting tools that can reformat your code, in order to comply 
with PEP 8. Refer to this [document](https://docs.python-guide.org/writing/style/#auto-formatting) for more information.

