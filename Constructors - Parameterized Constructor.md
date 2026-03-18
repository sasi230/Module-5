# Exp.No:21  
## Constructors - Parameterized Constructor

---

### AIM  
To write a Python code to create a class for a person with a parameterized constructor, which will take the `name` and `userid` of the person as parameters and print the `userid` of the person.

---

### ALGORITHM

1. Begin the program.  
2. Define a `person` class.  
3. The `person` class should have a parameterized `__init__` method that accepts two parameters: `name` and `userid`.  
4. Inside the `__init__` method, assign the `name` to `self.name` and the `userid` to `self.userid`.  
5. Print the `self.userid`.  
6. Prompt the user to enter their `name` (string) and `userid`.  
7. Create an instance `s1` of the `person` class by passing the entered `name` and `userid` to the constructor.  
8. Terminate the program.

---

### PROGRAM

```
class Name:
    def __init__(self,name):
        self.name = name
        
    def display(self):
        print("Hello "+ self.name)

name = input()
s = Name(name)
print("This is non parametrized constructor")
s.display()

```

### OUTPUT
<img width="1165" height="280" alt="image" src="https://github.com/user-attachments/assets/2711510d-f442-49dd-b8f4-f3e856b90875" />


### RESULT
Thus, the Python program to create a class with a parameterized constructor that accepts a name and displays a greeting using a class method has been implemented and executed successfully.
