# 📘 Python Functions – Detailed Notes

---

## 🔹 1. Introduction

A function is a reusable block of code that performs a specific task.

Instead of writing the same code multiple times, we define a function once and reuse it.

---

## 🔹 2. Why Use Functions?

- Avoid code repetition (DRY principle)
- Improve readability
- Make debugging easier
- Break large programs into smaller parts
- Reuse code efficiently

---

## 🔹 3. Types of Functions in Python

Python has two main categories of functions:

---

### 🔸 3.1 Built-in Functions (Utility Functions)

#### Definition
Built-in functions are predefined functions provided by Python that can be used directly.

#### Examples

```python
print("Hello")

length = len("Python")
print(length)

maximum = max(3, 7, 2)
print(maximum)


Common Built-in Functions
print()
len()
max()
min()
sum()
type()
Use Case

Used for quick operations without writing custom code.

🔸 3.2 User-defined Functions
Definition

Functions created by the programmer using the def keyword.

🔹 4. Syntax of a Function
def function_name(parameters):
    # function body
    return value
Explanation
def → keyword to define function
function_name → name of function
parameters → inputs (optional)
return → sends result back (optional)
🔹 5. Steps of Function Working
Define the function
Call the function
Pass arguments (if required)
Execute function body
Return result (if any)
🔹 6. Types of User-defined Functions
🔸 Type 1: No Parameters, No Return
Theory
No input is taken
No value is returned
Only performs action using print
Example
def greet():
    print("Hello, World!")

greet()

def show_message():
    print("Welcome to Python")

show_message()
Use Case

Simple display tasks

🔸 Type 2: Parameters, No Return
Theory
Takes input
Does not return value
Uses print()
Example
def greet(name):
    print("Hello", name)

greet("Aman")

def add(a, b):
    print("Sum is:", a + b)

add(3, 5)
Limitation

Output cannot be reused

🔸 Type 3: Parameters with Return ⭐
Theory
Takes input
Returns value using return
Result can be reused
Example
def add(a, b):
    return a + b

result = add(4, 6)
print(result)

def square(n):
    return n * n

print(square(5))
Use Case

Calculations and logic building

🔸 Type 4: No Parameters but Return
Theory
No input
Returns value
Example
def get_number():
    return 10

print(get_number())

def get_message():
    return "Python is easy"

msg = get_message()
print(msg)
Use Case

Fixed or internally generated values

🔹 7. Parameters vs Arguments
Term	Meaning
Parameter	Variable in function definition
Argument	Value passed during function call
Example
def greet(name):   # parameter
    print(name)

greet("Rahul")     # argument
🔹 8. print() vs return
Feature	print()	return
Purpose	Display output	Send value back
Reuse	No	Yes
Store value	No	Yes
Example
def add(a, b):
    print(a + b)
def add(a, b):
    return a + b
🔹 9. Important Points
Function stops execution after return
Indentation is important
Function must be defined before calling
A function can return multiple values
🔹 10. Summary

Functions are reusable blocks of code.

Types:

Built-in functions
User-defined functions

User-defined functions:

No input, no return
Input, no return
Input with return
No input but return
🔹 11. Conclusion

Functions help in:

Organizing code
Improving readability
Reusing logic