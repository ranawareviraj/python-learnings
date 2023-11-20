# Python Learnings
### Author: Viraj Ranaware

## Naming Convention
- The name can start with an upper or lower case alphabet.
```
For example, you can define your income variable as Income or income, both are valid.
```

- All the names are case sensitive.
```
Income and income are two different variables and not one.
```

- A number can appear in the name, but not at the beginning.
```
12income is not a valid name but income12 or in12come are valid.
```

- The _ character can appear anywhere in the name.
```
_income or income_ are valid names.
```

- Spaces are not allowed. Instead, we must use snake_case to make variable names readable.
```
- monthly_income is a valid name.
```

- The name of the variable should be something meaningful that describes the value it holds, instead of being random characters.
```
inc or even income would not give any useful information but names like weekly_income, monthly_income, or annual_income explain 
the purpose of our defined variable
```

## Data Types
Python does not place a strong emphasis on defining the data type of an object.

Python has three main data types:
- Numbers
- Strings
- Booleans


### Numbers

<img width="572" alt="image" src="https://user-images.githubusercontent.com/112779376/228924758-53c3a1a5-8563-4f75-989f-fccaeeb0de58.png">

**Integers**
- All the positive and negative whole numbers.
- The amount of memory an integer occupies depends on its value. 
  For example, 0 will take up 24 bytes whereas 1 would occupy 28 bytes.
 - In Python, all negative numbers start with the - symbol.
```python 
  print(10)  # A positive integer
  print(-3000)  # A negative integer

  num = 123456789  # Assigning an integer to a variable
  print(num)
  num = -16000  # Assigning a new integer
  print(num)
```
 
 **Floating Point Numbers**
- Refer to positive and negative decimal numbers.
- Python allows us to create decimals up to a very high decimal place. This ensures accurate computations for precise values.
- A float occupies 24 bytes of memory.
- In Python, 5 is considered to be an integer while 5.0 is a float.
```python
  print(1.00000000005)  # A positive float
  print(-85.6701)  # A negative float

  flt_pt = 1.23456789
  print(flt_pt)
```

**Complex Numbers**
- Python also supports complex numbers, or numbers made up of a real and an imaginary part.
- Complex numbers are useful for modelling physics and electrical engineering models in Python. 
- A complex number usually takes up 32 bytes of memory.
- Just like the print() statement is used to print values, complex() is used to create complex numbers.
- It requires two values.  
  -> The first one will be the real part of the complex number,  
  -> the second value will be the imaginary part.
```python
  print(complex(10, 20))  # Represents the complex number (10 + 20j)
  print(complex(2.5, -18.2))  # Represents the complex number (2.5 - 18.2j)

  complex_1 = complex(0, 2)
  complex_2 = complex(2, 0)
  print(complex_1)
  print(complex_2)
```
  
**Note:** In normal mathematics, the imaginary part of a complex number is denoted by i. However, in the code above, it is denoted by j. This is because Python follows the electrical engineering convention which uses j instead of i.

### Booleans
- The Boolean (also known as bool) data type allows us to choose between two values: true and false
- In Python, we can simply use True or False to represent a bool.
```python
  print(True)

  f_bool = False
  print(f_bool)
```
**Note:** The first letter of a bool needs to be capitalized in Python.

### Strings
- A string is a collection of characters closed within single, double or triple quotation marks.
- A string can also contain a single character or be entirely empty.
- A blank space inside the string quotation marks is also considered to be a character.
- To add a multi-line string we can use triple quotes.

```python
  print("Harry Potter!")  # Double quotation marks

  got = 'Game of Thrones...'  # Single quotation marks
  print(got)
  print("$")  # Single character

  empty = ""
  print(empty)  # Just prints an empty line

  multiple_lines = '''Triple quotes allows
  multi-line string.'''
  print(multiple_lines)
```
**The Length of a String**
- The length of a string can be found using the len() built-in function.
- This length indicates the number of characters in the string:
```python
  random_string = "I am Batman"  # 11 characters
  print(len(random_string))
```
**Indexing**
- In a string, every character is given a numerical index based on its position.
- A string in Python is indexed from 0 to n-1 where n is its length.

<img width="572" alt="image" src="https://user-images.githubusercontent.com/112779376/228928294-774f6155-a930-418e-95bf-a0f47aef1223.png">

**Accessing Characters**
- Each character in a string can be accessed using its index.
-  The index must be closed within square brackets, [], and appended to the string.
```python
  batman = "Bruce Wayne"

  first = batman[0]  # Accessing the first character
  print(first)

  space = batman[5]  # Accessing the empty space in the string
  print(space)

  last = batman[len(batman) - 1]
  print(last)
  # The following will produce an error "IndexError: string index out of range". Since, the index is out of bounds
  # err = batman[len(batman)]
```
**Reverse Indexing**
- We can also change our indexing convention by using negative indices.
- Negative indices start from the opposite end of the string.
- Hence, the -1 index corresponds to the last character:
```python
  batman = "Bruce Wayne"
  print(batman[-1])  # Corresponds to batman[10]
  print(batman[-5])  # Corresponds to batman[6]
```
**String Immutability**
- Once we assign a value to a string, we can’t update it later.
```python
  string = "Immutability"
  string[0] = 'O' # Will give error
```
- When we assign a new value to str1 (at line 4 below) its identity(reference) changes not the value.
```python
  str1 = "hello"
  print(id(str1))

  str1 = "bye"
  print(id(str1))
```
## More About Strings
### String Operations
The string data type has numerous utilities that make string computations much easier. 

**Comparison Operators**
- Strings are compatible with the comparison operators. Each character has a Unicode value.
- This allows strings to be compared on the basis of their Unicode values.
- When two strings have different lengths, the string which comes first in the dictionary is said to have the smaller value.
```python
  print('a' < 'b')  # 'a' has a smaller Unicode value -> True

  house = "Gryffindor"
  house_copy = "Gryffindor"

  print(house == house_copy)    # True

  new_house = "Slytherin"      

  print(house == new_house)     # False

  print(new_house <= house)     # False

  print(new_house >= house)     # True
```
**Concatenation:**
- The + operator can be used to merge two strings together:
```python
  first_half = "Bat"
  second_half = "man"

  full_name = first_half + second_half
  print(full_name)    # Batman
```

- The * operator allows us to multiply a string, resulting in a repeating pattern
```python
  print("ha" * 3)
  print(full_name)    # hahaha
```

**Search:**
- The in keyword can be used to check if a particular substring exists in another string.
- If the substring is found, the operation returns True.
```python
  random_string = "This is a random string"

  print('of' in random_string)  # Check whether 'of' exists in randomString. -> It doesn't -> False
  print('random' in random_string)  # 'random' exists! -> True
```
### String Slicing
- Slicing is the process of obtaining a portion (substring) of a string by using its indices.
- Given a string, we can use the following template to slice it and obtain a substring:
```python
  string[start:end] 
```
- **start** is the index from where we want the substring to start.
- **end** is the index where we want our substring to end.
- The character at the end index in the string, will not be included in the substring obtained through this method.

<img width="625" alt="image" src="https://user-images.githubusercontent.com/112779376/228930727-3a64f1b5-d40b-49c8-9f6e-e1d8f7b99d48.png">

```python
  my_string = "This is MY string!"
  print(my_string[0:4]) # From the start till before the 4th index
  print(my_string[1:7])
  print(my_string[8:len(my_string)]) # From the 8th index till the end
```
**Slicing with a Step:** 
- Python 3 also allows us to slice a string by defining a step through which we can skip characters in the string.
- The default step is 1, so we iterate through the string one character at a time.
- Syntax, Slicing with a Step
```python
  string[start:end:step]
```
- Sample code for slicing with step
```python
  my_string = "This is MY string!"
  print(my_string[0:7])  # A step of 1
  print(my_string[0:7:2])  # A step of 2  -> "Ti s"
  print(my_string[0:7:5])  # A step of 5  -> "Ti"
```
**Partial Slicing:** 
- For String slicing specifying the start and end indices is optional.
- If **start** is not provided, the substring will have all the characters until the **end** index.
- If **end** is not provided, the substring will begin from the start index and go all the way to the **end**.
```python
  my_string = "This is MY string!"
  print(my_string[:8])  # All the characters before 'M' -> This is
  print(my_string[8:])  # All the characters starting from 'M' -> MY string!
  print(my_string[:])  # The whole string -> This is MY string!
  print(my_string[::-1])  # The whole string in reverse (step is -1) -> !gnirts YM si sihT
```

### String Formatting
**String formatting** means substituting values into a string.  
Following are some use cases of string formatting:
- Inserting strings within a string
- Inserting integers within a string
- Inserting floats within a string

**Inserting Strings Within a String**
- The %s is the format specifier, which tells Python to insert the text here
- Python will insert a string if:  
We follow the string with a % and another string or another string type variable.
```python
  string1 = "I like %s" % "Python"
  print(string1) # 'I like Python'

  temp = "Educative"
  string2 = "I like %s" % temp
  print(string2) # 'I like Educative'

  string3 = "I like %s and %s" % ("Python", temp)
  print(string3)  # 'I like Python and Educative'
```
**Inserting Integers Within a String**
- The %i is the format specifier, which tells Python to insert the integers here.
```python
  my_string = "%i + %i = %i" % (1,2,3)
  print(my_string) # '1 + 2 = 3'
```

**Inserting Floats Within a String**
- %f is used to substitute floats within a string. 
- Note, string1 includes extra zeroes. To limit to two decimal places, we can use %.2f.
- If we pass a float that’s greater than two decimal places, then %.2f will round off the number to 2 decimal places.
```python
  string1 = "%f" % (1.11)
  print(string1) # '1.110000'

  string2 = "%.2f" % (1.11)
  print(string2) # '1.11'

  string3 = "%.2f" % (1.117)
  print(string3) # '1.12'
```

## The None Keyword(NoneType)
- Python offers data type called NoneType.
- It only has a single value, **None**.
- We can assign None to any variable, but we can not create other NoneType variables. 
```python
  val = None
  print(val) # prints "None" and returns None
  print (type(val))
```
- None is not a default value for the variable that has not yet been assigned a value.
- None is not the same as False.
- None is not an empty string.
- None is not 0

