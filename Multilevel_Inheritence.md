# Multilevel Inheritance Example in Python

This Python project demonstrates the concept of **Multilevel Inheritance** to collect and display the **name**, **age**, and **location** of a person.

## 🎯 Aim

To write a Python program that uses multilevel inheritance to get and display a person’s name, age, and location.

## 🧠 Algorithm

1. **Parent Class**  
   - `__init__(name)` initializes the `name` attribute.  
   - `getName()` returns the `name`.

2. **Child Class (inherits Parent)**  
   - `__init__(name, age)` initializes `name` using `super()` and adds `age`.  
   - `getAge()` returns the `age`.

3. **Grandchild Class (inherits Child)**  
   - `__init__(name, age, location)` initializes `name` and `age` using `super()` and adds `location`.  
   - `getLocation()` returns the `location`.

4. **Input & Output**  
   - Take user input for name, age, and location.  
   - Create an instance of `Grandchild`.  
   - Print all details using class methods.

## Program

```
# Base class
class Person:
    def __init__(self, name):
        self.name = name

    def display_name(self):
        print("Name:", self.name)


# Intermediate class
class Details(Person):
    def __init__(self, name, age):
        super().__init__(name)
        self.age = age

    def display_age(self):
        print("Age:", self.age)



class Location(Details):
    def __init__(self, name, age, place):
        super().__init__(name, age)
        self.place = place

    def display_location(self):
        print("Location:", self.place)



name = input("Enter name: ")
age = int(input("Enter age: "))
place = input("Enter location: ")

obj = Location(name, age, place)

print("\nPerson Details")
obj.display_name()
obj.display_age()
obj.display_location()

```


## Sample Output

<img width="1314" height="613" alt="image" src="https://github.com/user-attachments/assets/3c9468cc-0bfb-4d22-89e2-312c06c3d6a8" />
