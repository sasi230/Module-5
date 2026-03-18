# Exp.No:22  
## Destructor

---

### AIM  
To create a Python class `Student` with a destructor.

---

### ALGORITHM

1. Begin the program.  
2. Define the `student` class.  
3. Inside the `student` class, define the `__init__` method (constructor) and the `__del__` method (destructor).  
4. Create an object `s2` of the `student` class. When the object `s2` is created, the `__init__` method is called, and its print statements are executed.  
5. Use the `del` statement to delete the object `s2`. This triggers the `__del__` method (destructor), and the respective print statements are executed.  
6. Terminate the program.

---

### PROGRAM

```
class Person:
    def __init__(self,name,age):
        print("Person Created")
        self.name = name
        self.age = age
    def printInfo(self):
        print(self.name,self.age)
    def __del__(self):
        print(self.name,"Object Destroyed")

name=input()
age=int(input())
P1=Person(name,age)
#P2=Person("Joe",34)
P1.printInfo()
#P2.printInfo()
del P1

```

### OUTPUT

<img width="827" height="327" alt="image" src="https://github.com/user-attachments/assets/7ccba782-753a-4722-93b6-311576f7c6c6" />

### RESULT
Thus, the Python program to demonstrate the use of a constructor, method, and destructor in a class has been implemented and executed successfully.
