# Python Learnings
### Author: Viraj Ranaware

This sections describes **Data Structures** in Python.

## Data Structures in Python
Python is equipped with several built-in data structures to help us efficiently handle large amounts of data.

The four primary built-in data structures offered in Python are:
- List
- Tuple
- Dictionary
- Set

### List:
- The contents of a list are enclosed by square brackets, [].
- Lists are **ordered**.
- Elements are stored linearly at a specific **index**.
- Lists are **mutable**
<img width="523" alt="image" src="https://user-images.githubusercontent.com/112779376/235376902-f4500ac9-9a58-4ef3-a76a-63f4a55f8933.png">

- Creating a List:
```python
  empty_list = []

  // List with data
  mylist = ["apple", "banana", "cherry"]
  print(mylist)

  # Indexing
  print(mylist[0])

  # Length
  print(len(mylist))
```
Using **range():**
- A range can be converted into a list by using the list() casting.
```python
  num_seq = range(0, 10)  # A sequence from 0 to 9
  num_list = list(num_seq)  # The list() method casts the sequence into a list
  print(num_list)

  num_seq = range(3, 20, 3)  # A sequence from 3 to 19 with a step of 3
  print(list(num_seq))
```

**Using Nested List:**
- List can contain another list
- The nested lists do not need to be of the same size
```python
  world_cup_winners = [[2006, "Italy"], [2010, "Spain"],
                       [2014, "Germany"], [2018, "France"]]
  print(world_cup_winners)
```

**Using Sequential Indexing:** 
- To access the elements of a list or a string which exists inside another list, we can use the sequential indexing.
- Each level of indexing takes us one step deeper into the list
- Sequential Indexing allows us to access any element in a complex list.
```python
  world_cup_winners = [[2006, "Italy"], [2010, "Spain"],
                       [2014, "Germany"], [2018, "France"]]
  print(world_cup_winners[1])
  print(world_cup_winners[1][1])  # Accessing 'Spain'
  print(world_cup_winners[1][1][0])  # Accessing 'S'
```

**Merging Lists:**
- Using **+** operator to merege lists
```python
  part_A = [1, 2, 3, 4, 5]
  part_B = [6, 7, 8, 9, 10]
  merged_list = part_A + part_B
  print(merged_list)
```

- Using **extend()** property of a list to add the elements of one list at the end of another
```python
  part_A = [1, 2, 3, 4, 5]
  part_B = [6, 7, 8, 9, 10]
  part_A.extend(part_B)
  print(part_A)
```

**Adding Elements:**
- The **append()** method can be used to add a new element at the end of a list
```python
  a_list.append(newElement)
```

- To add an element at a particular index in the list, we can use the **insert()** method.
```python
  a_list.insert(index, newElement)
```

**Removing Elements:**
- The pop() method removes & returns the last element from the list.
```python
  houses = ["Gryffindor", "Hufflepuff", "Ravenclaw", "Slytherin"]
  last_house = houses.pop()
  print(last_house)
  print(houses)
```


```python
```


```python
```


```python
```


```python
```
