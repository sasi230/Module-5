# Exp.No:23  
## Multiple Inheritance

---

### AIM  
To write a Python program to get the name, attendance, and ID of a student and check if they are eligible for the next module using multiple inheritance. If attendance > 80, the student is eligible; otherwise, not eligible.

---

### ALGORITHM

1. Define the `Student` class.
2. Inside the `Student` class, define the `__init__` method (constructor). The `__init__` method accepts two parameters: `name` and `student_id`.
    - Inside the `__init__` method: Assign the value of `name` to `self.name` and `student_id` to `self.student_id`.
3. Define the `get_student_info` method inside the `Student` class:
    - This method should return a string formatted with `self.name` and `self.student_id`.
4. Define the `Attendance` class, which inherits from the `Student` class.
5. Inside the `Attendance` class, define the `__init__` method (constructor).
    - The `__init__` method accepts three parameters: `name`, `student_id`, and `attendance`.
    - Inside the `__init__` method: Call the parent class constructor `super().__init__(name, student_id)` to initialize `name` and `student_id`. Assign the value of `attendance` to `self.attendance`.
6. Define the `check_eligibility` method inside the `Attendance` class:
    - If `self.attendance` is greater than 80, return a formatted string indicating the student is eligible for the module exam.
    - Otherwise, return a formatted string indicating the student is not eligible for the module exam.
7. Prompt the user to enter the `name` (as a string), `student_id` (as an integer), and `attendance` (as an integer).
8. Create an instance `student` of the `Attendance` class, passing the entered `name`, `student_id`, and `attendance` to the constructor.
9. Call the `check_eligibility` method on the `student` object and print the result.
10. Terminate the program.

---

### PROGRAM

```
class Addition:
    def add(self, a, b):
        return a + b

class Multiplication:
    def multiply(self, a, b):
        return a * b

class Division:
    def divide(self, a, b):
        if b != 0:
            return a / b
        else:
            return "Division by zero is not allowed."

class Calculator(Addition, Multiplication, Division):
    def calculate(self, a, b):
        addition = self.add(a, b)
        multiplication = self.multiply(a, b)
        division = self.divide(a, b)
        return addition, multiplication, division

if __name__ == "__main__":
    num1 = int(input())
    num2 = int(input())
    calc = Calculator()
    add_result, mul_result, div_result = calc.calculate(num1, num2)
    print(f"{add_result}")
    print(f"{mul_result}")
    print(f"{div_result}")


```

### OUTPUT
<img width="832" height="245" alt="image" src="https://github.com/user-attachments/assets/faf64388-8232-4588-97be-d6e7ecc4da7b" />


### RESULT
Thus, the Python program to perform addition, multiplication, and division using multiple inheritance has been implemented and executed successfully.
