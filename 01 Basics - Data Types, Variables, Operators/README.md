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
``` 
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
```
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
```
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
```
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

```
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
```
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
```
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
```
  batman = "Bruce Wayne"
  print(batman[-1])  # Corresponds to batman[10]
  print(batman[-5])  # Corresponds to batman[6]
```
**String Immutability**
- Once we assign a value to a string, we can’t update it later.
```
  string = "Immutability"
  string[0] = 'O' # Will give error
```
- When we assign a new value to str1 (at line 4 below) its identity(reference) changes not the value.
```
  str1 = "hello"
  print(id(str1))

  str1 = "bye"
  print(id(str1))
```
## More About Strings
### String Slicing
- Slicing is the process of obtaining a portion (substring) of a string by using its indices.
- Given a string, we can use the following template to slice it and obtain a substring:
```
  string[start:end] 
```
- **start** is the index from where we want the substring to start.
- **end** is the index where we want our substring to end.
- The character at the end index in the string, will not be included in the substring obtained through this method.

<img width="625" alt="image" src="https://user-images.githubusercontent.com/112779376/228930727-3a64f1b5-d40b-49c8-9f6e-e1d8f7b99d48.png">
```
  my_string = "This is MY string!"
  print(my_string[0:4]) # From the start till before the 4th index
  print(my_string[1:7])
  print(my_string[8:len(my_string)]) # From the 8th index till the end
```
**Slicing with a Step:** 
- Python 3 also allows us to slice a string by defining a step through which we can skip characters in the string.
- The default step is 1, so we iterate through the string one character at a time.
- Syntax, Slicing with a Step
```
  string[start:end:step]
```
- Sample code for slicing with step
```
  my_string = "This is MY string!"
  print(my_string[0:7])  # A step of 1
  print(my_string[0:7:2])  # A step of 2  -> "Ti s"
  print(my_string[0:7:5])  # A step of 5  -> "Ti"
```
**Partial Slicing:** 
- For String slicing specifying the start and end indices is optional.
- If **start** is not provided, the substring will have all the characters until the **end** index.
- If **end** is not provided, the substring will begin from the start index and go all the way to the **end**.
```
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
```
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
```
  my_string = "%i + %i = %i" % (1,2,3)
  print(my_string) # '1 + 2 = 3'
```

**Inserting Floats Within a String**
- %f is used to substitute floats within a string. 
- Note, string1 includes extra zeroes. To limit to two decimal places, we can use %.2f.
- If we pass a float that’s greater than two decimal places, then %.2f will round off the number to 2 decimal places.
```
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
```
  val = None
  print(val) # prints "None" and returns None
  print (type(val))
```
- None is not a default value for the variable that has not yet been assigned a value.
- None is not the same as False.
- None is not an empty string.
- None is not 0

## Operators
- In general, Python’s operators follow the **in-fix** or **prefix** notations.
- **In-fix** operators appear between two operands (values on which the operator acts) and hence, are usually known as **binary operators**
- A **prefix** operator usually works on one operand and appears before it. Hence, prefix operators are known as **unary operators**.
- The 5 main operator types in Python are below
    -  arithmetic operators
    -  comparison operators
    -  assignment operators
    -  logical operators
    -  bitwise operators

### Arithmetic Operators
|Operator|	Purpose|	Notation|
|------------- |------------- |------------- |
|()|	Parentheses|	Encapsulates the Precedent Operation|
|**	|Exponent	|In-fix|
|%, *, /, //|	Modulo, Multiplication, Division, Floor Division|	In-fix
|+, -|	Addition, Subtraction|	In-fix|

- **Addition**:
```
  print(10 + 5)

  float1 = 13.65
  float2 = 3.40
  print(float1 + float2)

  num = 20
  flt = 10.5
  print(num + flt)
```
- Summing an integer and floating-point number gives us a floating-point number.
- Python automatically converts the integer to a floating-point number.  
    - This applies to all arithmetic operations.
    
- **Subtraction**:
```
  print(10 - 5)

  float1 = -18.678
  float2 = 3.55
  print(float1 - float2)

  num = 20
  flt = 10.5
  print(num - flt)
```

- **Multiplication**:
```
  print(40 * 10)

  float1 = 5.5
  float2 = 4.5
  print(float1 * float2)

  print(10.2 * 3)
```
- **Division**:
```
  print(40 / 10)

  float1 = 5.5
  float2 = 4.5
  print(float1 / float2)
  print(12.4 / 2)
```
- **Floor Division (Integer Division):** In floor division, the result is floored to the nearest smaller integer.
- For floor division, we must use the // operator.
- Unlike normal division, floor division between two integers results in an integer.
```
  print(43 // 10)

  float1 = 5.5
  float2 = 4.5
  print(5.5 // 4.5)
  print(12.4 // 2)
```
- **Modulo:** A number’s modulo with another number can be found using the % operator:
```
  print(10 % 2)

  twenty_eight = 28
  print(twenty_eight % 10)

  print(-28 % 10)  # The remainder is positive if the right-hand operand is positive
  print(28 % -10)  # The remainder is negative if the right-hand operand is negative
  print(34.4 % 2.5)  # The remainder can be a float
```
**Precedence**
- An arithmetic expression containing different operators will be computed on the basis of operator precedence
- Whenever operators have equal precedence, the expression is computed from the left side:
```
# Different precedence
  print(10 - 3 * 2)  # Multiplication computed first, followed by subtraction

  # Same precedence
  print(3 * 20 / 5)  # Multiplication computed first, followed by division
  print(3 / 20 * 5)  # Division computed first, followed by multiplication
```
- An expression which is enclosed inside parentheses will be computed first, regardless of operator precedence:
```
  print((10 - 3) * 2)  # Subtraction occurs first
  print((18 + 2) / (10 % 8))  # Addition (18 + 2) and Modulo (10 % 8) occurs first, then division
```

**Note:**  Python offers many other arithmetic operators.

### Comparison Operators
|Operator|	Purpose	|Notation|
|--------|----------|--------|
|>|	Greate| Than|	In-fix|
|<	|Less Than	|In-fix|
|>=	|Greater Than or Equal To	|In-fix|
|<=	|Less Than or Equal To	|In-fix|
|==	|Equal To	|In-fix|
|!=	|Not Equal To	|In-fix|
|is	|Equal To (Identity)	|In-fix|
|is not|	Not Equal To (Identity)|	In-fix|