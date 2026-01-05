# Hierarchical Inheritance in Python

This Python project demonstrates **Hierarchical Inheritance** using a base class `Details` and two derived classes `Employee` and `Patient`. The program collects and displays details for both employees and patients.

## 🎯 Aim

To write a Python program that uses **Hierarchical Inheritance** to input and display **Employee** and **Patient** details.

## 📘 Description

- **Base Class:** `Details`
  - Stores common attributes: `name`, `age`
  - Provides methods: `getName()`, `getAge()`

- **Derived Class 1:** `Employee`
  - Inherits from `Details`
  - Adds: `employee_id`, `department`
  - Method: `getEmployeeDetails()`

- **Derived Class 2:** `Patient`
  - Inherits from `Details`
  - Adds: `patient_id`, `disease`
  - Method: `getPatientDetails()`

## 🧠 Algorithm

1. Create base class `Details` with common attributes.
2. Create `Employee` class extending `Details`, adding employee-specific data.
3. Create `Patient` class extending `Details`, adding patient-specific data.
4. Get user input for employee and patient data.
5. Display collected information using class methods.

## Program
```

class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def display_person(self):
        print("Name:", self.name)
        print("Age:", self.age)



class Employee(Person):
    def __init__(self, name, age, emp_id, salary):
        super().__init__(name, age)
        self.emp_id = emp_id
        self.salary = salary

    def display_employee(self):
        self.display_person()
        print("Employee ID:", self.emp_id)
        print("Salary:", self.salary)



class Patient(Person):
    def __init__(self, name, age, patient_id, disease):
        super().__init__(name, age)
        self.patient_id = patient_id
        self.disease = disease

    def display_patient(self):
        self.display_person()
        print("Patient ID:", self.patient_id)
        print("Disease:", self.disease)



print("Enter Employee Details")
ename = input("Name: ")
eage = int(input("Age: "))
eid = input("Employee ID: ")
salary = float(input("Salary: "))

emp = Employee(ename, eage, eid, salary)
print("\nEmployee Details")
emp.display_employee()


print("\nEnter Patient Details")
pname = input("Name: ")
page = int(input("Age: "))
pid = input("Patient ID: ")
disease = input("Disease: ")

pat = Patient(pname, page, pid, disease)
print("\nPatient Details")
pat.display_patient()


```
## Sample Output
<img width="1617" height="645" alt="image" src="https://github.com/user-attachments/assets/a11d6072-6696-49d8-84f9-8d683c0cc5bb" />

##result
the program is executed successfully


