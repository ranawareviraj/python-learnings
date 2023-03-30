# Python Learnings
### Author: Viraj Ranaware


## Data Types
Python does not place a strong emphasis on defining the data type of an object.

Python has three main data types:
- Numbers
- Strings
- Booleans

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

## Numbers

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


 
