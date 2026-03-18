# Exp.No:25  
## Hierarchical Inheritance

---

### AIM  
To write a Python program to get the employee and doctor details and display them using hierarchical inheritance. Create a parent (base) class named `Details` and two child (derived) classes named `Employee` and `Doctor`.

---

### ALGORITHM

1. **Begin the program.**
2. **Create a class Details** with an `__init__` method to initialize three attributes: `id`, `name`, and `gender`.
3. **Define a method display_details()** to print the values of `id`, `name`, and `gender`.
4. **Create a class Employee** that inherits from the `Details` class. 
   - Add two additional attributes: `company` and `department`.
   - Override the `display_details()` method to print the employee-specific attributes (`company` and `department`) along with the inherited details.
5. **Create a class Doctor** that also inherits from the `Details` class. 
   - Add two additional attributes: `hospital` and `department`.
   - Override the `display_details()` method to print the doctor-specific attributes (`hospital` and `department`) along with the inherited details.
6. **Accept input** for employee and doctor details.
7. **Create objects of Employee and Doctor** using the input.
8. **Call the `display_details()` method** for both objects to print the details.
9. **Terminate the program.**

---

### PROGRAM
```
class Details:
    def __init__(self, emp_id, name, gender):
        self.emp_id = emp_id
        self.name = name
        self.gender = gender

class Employee(Details):
    def __init__(self, emp_id, name, gender, company, department):
        super().__init__(emp_id, name, gender)  
        self.company = company
        self.department = department

    def display_employee(self):
        return (f"Employee Object\n"
                f"Id:  {self.emp_id}\n"
                f"Name:  {self.name}\n"
                f"Gender:  {self.gender}\n"
                f"Company:  {self.company}\n"
                f"Department:  {self.department}")

class Doctor(Details):
    def __init__(self, emp_id, name, gender, hospital, department):
        super().__init__(emp_id, name, gender)
        self.hospital = hospital
        self.department = department

    def display_doctor(self):
        return (f"Doctor Object\n"
                f"Id:  {self.emp_id}\n"
                f"Name:  {self.name}\n"
                f"Gender:  {self.gender}\n"
                f"Hospital:  {self.hospital}\n"
                f"Department:  {self.department}")

if __name__ == "__main__":
    # Input for Employee
    emp_id = int(input())
    emp_name = input()
    emp_gender = input()
    emp_company = input()
    emp_department = input()

    employee = Employee(emp_id, emp_name, emp_gender, emp_company, emp_department)

    doc_id = int(input())
    doc_name = input()
    doc_gender = input()
    doc_hospital = input()
    doc_department = input()

    doctor = Doctor(doc_id, doc_name, doc_gender, doc_hospital, doc_department)

    print(employee.display_employee())
    print()
    print(doctor.display_doctor())



```

## OUTPUT  
<img width="1015" height="437" alt="Screenshot 2025-11-20 093122" src="https://github.com/user-attachments/assets/bcc09e67-cb50-4b8d-bd07-8e99fc8ceca5" />

## RESULT
Thus, the Python program to demonstrate hierarchical inheritance using Details, Employee, and Doctor classes has been implemented and executed successfully.
