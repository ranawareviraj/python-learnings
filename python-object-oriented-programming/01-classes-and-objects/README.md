## Classes and Objects

*Defining a class*

```python
class ClassName:
    pass
```
**Naming rules:**

The following rules must be adhered to when naming classes:
 - Must start with a letter or underscore
 - Should only be comprised of numbers, letters, or underscores
 - Cannot be a reserved word

*Creating an object* 

```python
class MyClass:
    pass

obj = MyClass()  # creating a MyClass Object
print(obj)
```

**Implementing Properties in a Class**

Initializing the values of properties inside the class is necessary. If we do not initialize the properties of a class, the Python code will not compile.
- With default values
 ```python
# this code will compile
class Employee:
    # defining the properties and assigning them none
    ID = None
    salary = None
    department = None
 ```

- Without default values
 ```python
# this code will give a compilation error
class Employee:
    # defining the properties and not assigning them none
    ID
    salary
    department
 ```
**Accessing properties and assigning values**
    
```python
class Employee:
    # defining the properties and assigning values to them
    ID = 3789
    salary = 2500
    department = "Human Resources"


# cerating an object of the Employee class
Steve = Employee()

# printing properties of Steve - an object of the Employee class
print("ID =", Steve.ID)
print("Salary", Steve.salary)
print("Department:", Steve.department)
```

**Creating properties outside a class**

- In python, we can create properties outside a class. This is done by using the object name and the dot operator, followed by the property name.
- The property added outside the class will only be added to the particular object and all other future objects will only have the properties which are declared in the class.

```python
class Employee:
    # defining the properties and assigning them None
    ID = None
    salary = None
    department = None


# cerating an object of the Employee class
Steve = Employee()

# assigning values to properties of Steve - an object of the Employee class
Steve.ID = 3789
Steve.salary = 2500
Steve.department = "Human Resources"
# creating a new attribute for Steve
Steve.title = "Manager"

# Printing properties of Steve
print("ID =", Steve.ID)
print("Salary", Steve.salary)
print("Department:", Steve.department)
print("Title:", Steve.title)
```
**Note:** The property, title, will only be added to Steve and all other future objects will only have the properties which are declared in the Employee class i.e. ID, salary, and department.