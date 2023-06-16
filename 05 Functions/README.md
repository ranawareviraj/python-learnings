# Python Learnings
### Author: Viraj Ranaware

This sections describes Functions in Python

## Function Creation

<img width="544" alt="image" src="https://github.com/ranawareviraj/python-learnings/assets/112779376/c5995f41-ca26-4223-82d5-7e5b94d2369e">

**Creating a simple function**
```python
    def my_print_function():  # No parameters
        print("This")
        print("is")
        print("A")
        print("function")
    # Function ended
    
    # Calling the function in the program multiple times
    my_print_function()
    my_print_function()
```

**Function Parameters**
```python
    def minimum(n1, n2):
        if (n1 < n2):
            print(n1)
        else:
            print(n2)
    
    num1 = 10
    num2 = -20
    minimum(num1, num2)
```

**Returning a value from a function**
```python
    def minimum(first, second):
        if (first < second):
            return first
        return second
    
    
    num1 = 10
    num2 = 20
    
    result = minimum(num1, num2)  # Storing the value returned by the function
    print(result)
```
