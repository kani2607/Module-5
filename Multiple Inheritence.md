# Arithmetic Operations Using Multiple Inheritance in Python

This Python program demonstrates **multiple inheritance** by performing basic arithmetic operations — Addition, Subtraction, and Division — using three classes.

## 🎯 Aim

To write a Python program to calculate **Add, Sub & Division** using **Multiple Inheritance**.

## 🧠 Algorithm

1. **Define `Calculation1` class**
   - Contains `Summation(a, b)` method to return the sum of two numbers.
2. **Define `Calculation2` class**
   - Contains `Subtraction(a, b)` method to return the difference of two numbers.
3. **Define `Derived` class**
   - Inherits from both `Calculation1` and `Calculation2`.
   - Contains `Division(a, b)` method to return the division result.
4. **Input**
   - Prompt the user to enter two numbers.
5. **Process**
   - Create an object of the `Derived` class.
   - Call `Summation`, `Subtraction`, and `Division` methods.
6. **Output**
   - Display the results of the three operations.

## 💻 Program 
```
# First parent class
class Add:
    def add(self, a, b):
        return a + b


# Second parent class
class Sub:
    def sub(self, a, b):
        return a - b


# Child class (Multiple Inheritance)
class Calc(Add, Sub):
    def div(self, a, b):
        if b != 0:
            return a / b
        else:
            return "Division by zero not possible"


# Input
a = float(input("Enter first number: "))
b = float(input("Enter second number: "))

obj = Calc()

# Output
print("Addition:", obj.add(a, b))
print("Subtraction:", obj.sub(a, b))
print("Division:", obj.div(a, b))

```
## Output Example
<img width="1399" height="657" alt="image" src="https://github.com/user-attachments/assets/98eaa42b-6fd3-4866-b07d-4ba49b9bfa82" />
##Result
the program is executed successfully



