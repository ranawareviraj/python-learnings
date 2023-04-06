# Python Learnings
### Author: Viraj Ranaware

This sections describes Conditionals and Loops in Python

## Conditionals
To handle conditional statements, Python follows a particular convention:
```
if condtional statement is True:
    # execute expression1
    pass
else:
    # execute expression2
    pass 
```
There are three types of conditional statements in Python:
- if
- if-else
- if-elif-else

### The if Statement
- The : in the illustration below is necessary to specify the beginning of the if statement’s code to be executed. 
- The parentheses, **()**, around the condition are optional.
- The code to be executed is indented at least one tab to the right.
- The convention of our indents must also be consistent throughout a block.

<img width="469" alt="image" src="https://user-images.githubusercontent.com/112779376/230457992-a57ad200-b71c-450a-a487-5062124abe81.png">

**Sample if Statement**
```
num = 6

if (num == 5):  # The condition is true
    print("The number is equal to 5")  # The code is executed

if num > 5:  # The condtion is false
    print("The number is greater than 5")  # The code is not executed
```

**Conditions with Logical Operators**
```
num = 12

if num % 2 == 0 and num % 3 == 0 and num % 4 == 0:
    # Only works when num is a multiple of 2, 3, and 4
    print("The number is a multiple of 2, 3, and 4")

if (num % 5 == 0 or num % 6 == 0):
    # Only works when num is either a multiple of 5 or 6
    print("The number is a multiple of 5 and/or 6")
```

**Nested if Statements**
```
num = 63

if num >= 0 and num <= 100:
    if num >= 50 and num <= 75:
        if num >= 60 and num <= 70:
            print("The number is in the 60-70 range")
```
- Nested if statements should have corresponding nested indent

### if-else statement
- If the condition turns out to be False, the code after the else: keyword is executed.
- The else keyword will be on the same indentation level as the if keyword.
- The body of else block will be indented one tab to the right just like the if statement.
**Sample if-else Statement**
```
num = 60

if num <= 50:
    print("The number is less than or equal to 50")
else:
    print("The number is greater than 50")
```

**Sample if-else Statement**
```
num = 60

if num <= 50:
    print("The number is less than or equal to 50")
else:
    print("The number is greater than 50")
```

**Conditional Expression**
```
num = 60

output = "The number is less than or equal to 50" \
    if num <= 50 else "The number is greater than 50"

print(output)
```
- Note: The backslash \ in the above code is only a line continuation character that can be used to split a single line into multiple lines.
