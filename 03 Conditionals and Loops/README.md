# Python Learnings
### Author: Viraj Ranaware

This sections describes Conditionals and Loops in Python

## Conditionals
To handle conditional statements, Python follows a particular convention:
```python
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
```python
num = 6

if (num == 5):  # The condition is true
    print("The number is equal to 5")  # The code is executed

if num > 5:  # The condtion is false
    print("The number is greater than 5")  # The code is not executed
```

**Conditions with Logical Operators**
```python
num = 12

if num % 2 == 0 and num % 3 == 0 and num % 4 == 0:
    # Only works when num is a multiple of 2, 3, and 4
    print("The number is a multiple of 2, 3, and 4")

if (num % 5 == 0 or num % 6 == 0):
    # Only works when num is either a multiple of 5 or 6
    print("The number is a multiple of 5 and/or 6")
```

**Nested if Statements**
```python
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
```python
num = 60

if num <= 50:
    print("The number is less than or equal to 50")
else:
    print("The number is greater than 50")
```

**Sample if-else Statement**
```python
num = 60

if num <= 50:
    print("The number is less than or equal to 50")
else:
    print("The number is greater than 50")
```

**Conditional Expression**
```python
num = 60

output = "The number is less than or equal to 50" \
    if num <= 50 else "The number is greater than 50"

print(output)
```
- Note: The backslash \ in the above code is only a line continuation character that can be used to split a single line into multiple lines.

### if-elif-else
- It is the most comprehensive conditional statement because it allows us to create multiple conditions easily.
```python
light = "Red"

if light == "Green":
    print("Go")
elif light == "Yellow":
    print("Caution")
elif light == "Red":
    print("Stop")
else:
    print("Incorrect light signal")
```
- **Note:** An if-elif statement can exist on its own without an else block at the end. However, an elif cannot exist without an if statement preceding it (which naturally makes sense).

## Loops in Python
There are two types of loops that we can use in Python:
- The **for** loop
- The **while** loop

- In a **for** loop, we need to define three main things:  
    - The name of the iterator
    - The sequence to be traversed
    - The set of operations to perform

**Looping Through a Range - syntax**
```python
range(start, end, step)
```
- Note: The end value is not included in the list.
- The step decides the number of steps the iterator jumps ahead after each iteration. (Optional, default is 1).
**Looping Through a Range - example**
```python
for i in range(1, 11):  # A sequence from 1 to 10
    if i % 2 == 0:
        print(i, " is even")
    else:
        print(i, " is odd")
```
- A list or string can be iterated through its indices.

**Looping Through a List/String - using range**
```python
float_list = [2.5, 16.42, 10.77, 8.3, 34.21]
print(float_list)

for i in range(0, len(float_list)):  # Iterator traverses to the last index of the list
    float_list[i] = float_list[i] * 2

print(float_list)
```
- We could also traverse the elements of a list/string directly through the iterator.

**Looping Through a List/String - using iterator**
```python
float_list = [2.5, 16.42, 10.77, 8.3, 34.21]
count_greater = 0

for num in float_list:  # Iterator traverses to the last index of the list
    if num > 10:
        count_greater += 1

print(count_greater)
```
- Note: In the case above (using iterator), altering num will not alter the actual value in the list


**While Loop:**
- In a **while** loop, the number of iterations is based solely on the condition associated with it.
```python
n = 2  # Could be any number
power = 0
val = n
while val < 1000:
    power += 1
    val *= n
print(power)
```

The **break** Keyword:
- It can break the loop whenever we want. We can make our loop to break when specific condition is met.
```python
n = 50
num_list = [10, 25, 4, 23, 6, 18, 27, 47]
found = False  # This bool will become true once a pair is found

for n1 in num_list:
    for n2 in num_list:
        if(n1 != n2):
            if(n1 + n2 == n):
                found = True  # Set found to True
                break  # Break inner loop if a pair is found
    if found:
        print(n1, n2) # Print the pair
        break  # Break outer loop if a pair is found
```

The **continue** Keyword:
- When the continue keyword is used, the rest of that particular iteration (only) is skipped.
```python
num_list = list(range(0, 10))

for num in num_list:
    if num == 3 or num == 6:
        continue
    print(num)
```
- On executing the above code, 3 and 6 will not be printed. 

The **pass** Keyword:
- In all practical meaning, the pass statement does nothing to the code execution. 
- It can be used to represent an area of code that needs to be written. 
- It is simply there to assist you when you haven’t written a piece of code but still need your entire program to execute. (Similar to **//TODO** in Java)
