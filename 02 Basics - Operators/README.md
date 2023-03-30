# Python Learnings
### Author: Viraj Ranaware


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
- Comparison operators can be used to compare values in mathematical terms.

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

- The result of a comparison is always a bool.
- If the comparison is correct, the value of the bool will be True. Otherwise, its value will be False.
- The == and != operators compare the values of both operands.
- The identity operators, is and is not, check whether the two operands are the exact same object.  
**Examples demonstrating comparison operators**
```
  num1 = 5
  num2 = 10
  num3 = 10
  list1 = [6,7,8]
  list2 = [6,7,8]

  print(num2 > num1)  # 10 is greater than 5
  print(num1 > num2)  # 5 is not greater than 10

  print(num2 == num3)  # Both have the same value
  print(num3 != num1)  # Both have different values

  print(3 + 10 == 5 + 5)  # Both are not equal
  print(3 <= 2)  # 3 is not less than or equal to 2

  print(num2 is not num3)  # Both have the same object
  print(list1 is list2)  # Both have the different objects
```

### Assignment Operators
- Summary of Assignment Operators below:

|Operator	Purpose						|Notation 	|
|-----------|---------------------------|-----------|
| =			| Assign					|In-fix   	|
| +=			| Add and Assign			|In-fix		|
| -=			| Subtract and Assign		|In-fix		|
| *=			| Multiply and Assign		|In-fix		|
| /=			| Divide and Assign			|In-fix		|
| //=		| Divide, Floor, and Assign	|In-fix		|
| ** =		| Raise power and Assign	|In-fix		|
|%=			| Take Modulo and Assign	|In-fix		|
||=			| OR and Assign				|In-fix		|
|&=			| AND and Assign			|In-fix		|
|^=			| XOR and Assign			|In-fix		|
|>>=		| Right-shift and Assign	|In-fix		|
|<<=		| Left-shift and Assign		|In-fix		|
