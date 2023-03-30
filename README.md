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
