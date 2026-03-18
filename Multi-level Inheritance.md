# Exp.No:24  
## Multi-level Inheritance

---

### AIM  
To write a Python program to get the name, age, and ID of a person and display them using multilevel inheritance.

---

### ALGORITHM

1. Define the `Person` class:
   - Inside the `Person` class, define the `__init__` method (constructor) with two parameters: `name` and `age`.
   - Inside the `__init__` method, assign the `name` to `self.name` and `age` to `self.age`.

2. Define the `PersonDetails` class that inherits from the `Person` class:
   - Inside the `PersonDetails` class, define the `__init__` method (constructor) with three parameters: `name`, `age`, and `person_id`.
   - Inside the `__init__` method, call the `__init__` method of the `Person` class using `super()` to initialize `name` and `age`.
   - Assign `person_id` to `self.person_id`.

3. Define the `DisplayDetails` class that inherits from the `PersonDetails` class:
   - Inside the `DisplayDetails` class, define the `__init__` method (constructor) with three parameters: `name`, `age`, and `person_id`.
   - Inside the `__init__` method, call the `__init__` method of the `PersonDetails` class using `super()` to initialize `name`, `age`, and `person_id`.

4. Inside the `DisplayDetails` class, define the `show_details` method:
   - Inside the `show_details` method, return a formatted string with `self.name`, `self.age`, and `self.person_id`.

5. Prompt the user to enter `name` (string), `age` (integer), and `person_id` (integer).

6. Create an instance `person` of the `DisplayDetails` class, passing `name`, `age`, and `person_id` to the constructor.

7. Call the `show_details` method on the `person` object and print the result.

8. Terminate the program.

---

### PROGRAM

```
class Student:
    def __init__(self, name, roll_no):
        self.name = name
        self.roll_no = roll_no

class Marks(Student):
    def __init__(self, name, roll_no, marks1, marks2, marks3):
        super().__init__(name, roll_no)  
        self.marks1 = marks1
        self.marks2 = marks2
        self.marks3 = marks3

class TotalMarks(Marks):
    def __init__(self, name, roll_no, marks1, marks2, marks3):
        super().__init__(name, roll_no, marks1, marks2, marks3)  

    def calculate_total(self):
        return self.marks1 + self.marks2 + self.marks3
    def display_details(self):
        total = self.calculate_total()
        return f"Name:  {self.name} Rollno:  {self.roll_no} Total Marks out of 300:  {total}"


if __name__ == "__main__":
    name = input()
    roll_no = int(input())
    marks1 = int(input())
    marks2 = int(input())
    marks3 = int(input())

    student = TotalMarks(name, roll_no, marks1, marks2, marks3)
    print(student.display_details())



```

### OUTPUT
<img width="1247" height="267" alt="image" src="https://github.com/user-attachments/assets/90de842f-ad0f-4674-b700-c8052f0d4788" />

### RESULT
Thus, the Python program to compute and display the total marks of a student using multilevel inheritance has been implemented and executed successfully.
