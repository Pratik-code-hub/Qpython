# 📘 Python Functions – Complete Notes

---

## 🔹 1. What is a Function?

A function is a reusable block of code that performs a specific task.

Instead of writing the same code multiple times, we define a function once and call it whenever needed.

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

#### ✅ Definition

Built-in functions are predefined functions provided by Python that can be used directly.

#### ✅ Examples

```python
print("Hello")

length = len("Python")
print(length)

maximum = max(3, 7, 2)
print(maximum)
✅ Common Built-in Functions
print() → display output
len() → length of object
max() → largest value
min() → smallest value
sum() → total sum
type() → data type
🔸 3.2 User-defined Functions
✅ Definition

Functions created by the programmer using the def keyword are called user-defined functions.

🔹 4. Syntax of a Function
def function_name(parameters):
    # function body
    return value
✅ Explanation
def → keyword to define function
function_name → name given by user
parameters → inputs (optional)
return → sends result back (optional)
🔹 5. Steps of Working of a Function
Define the function
Call the function
Pass arguments (if required)
Execute function body
Return result (if any)
🔹 6. Types of User-defined Functions
🔸 Type 1: No Parameters, No Return
✅ Theory
No input is taken
No value is returned
Performs task using print()
✅ Example
def greet():
    print("Hello, World!")

greet()
🔸 Type 2: Parameters, No Return
✅ Theory
Takes input
Does not return value
Uses print()
✅ Example
def greet(name):
    print("Hello", name)

greet("Aman")
🔸 Type 3: Parameters with Return ⭐
✅ Theory
Takes input
Returns value using return
Output can be reused
✅ Example
def add(a, b):
    return a + b

result = add(4, 6)
print(result)
🔸 Type 4: No Parameters but Return
✅ Theory
No input
Returns value
✅ Example
def get_number():
    return 10

print(get_number())
🔹 7. Parameters vs Arguments
Term	Meaning
Parameter	Variable in function definition
Argument	Value passed during function call
🔹 8. Types of Arguments
1. Positional Arguments
def add(a, b):
    return a + b

print(add(2, 3))
2. Keyword Arguments
print(add(b=3, a=2))
3. Default Arguments
def greet(name="User"):
    print("Hello", name)

greet()
greet("Aman")
4. Variable-Length Arguments
*args (multiple values)
def total(*numbers):
    return sum(numbers)

print(total(1, 2, 3, 4))
**kwargs (key-value pairs)
def info(**data):
    print(data)

info(name="Aman", age=20)
🔹 9. print() vs return
Feature	print()	return
Purpose	Display output	Send value back
Reuse	❌ No	✅ Yes
Store value	❌ No	✅ Yes
🔹 10. Lambda Functions (Anonymous Functions)
✅ Definition

Small one-line functions without name.

✅ Example
square = lambda x: x * x
print(square(5))
🔹 11. Recursion
✅ Definition

A function calling itself.

✅ Example
def factorial(n):
    if n == 1:
        return 1
    return n * factorial(n-1)

print(factorial(5))
🔹 12. Scope of Variables
Local Scope
def func():
    x = 10
Global Scope
x = 10

def func():
    print(x)
🔹 13. Important Points
Function stops execution after return
Indentation is important
Function must be defined before calling
Can return multiple values
Functions improve modularity
🔹 14. Summary
Functions are reusable blocks of code
Types:
Built-in functions
User-defined functions
User-defined types:
No input, no return
Input, no return
Input with return
No input but return
🔹 15. Conclusion

Functions are a core concept in Python that:

Simplify code
Improve structure
Enable reuse
Help in writing efficient programs