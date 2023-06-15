# Python Learnings
### Author: Viraj Ranaware

This sections describes **Data Structures** in Python.

## Data Structures in Python
Python is equipped with several built-in data structures to help us efficiently handle large amounts of data.

### Primary Data Structures in Python
The four primary built-in data structures offered in Python are:
- List
- Tuple
- Dictionary
- Set

### 1. List:
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
- If we need to delete a particular value from a list, we can use the remove() method. 
Syntax
```python
  a_list.remove(element_to_be_deleted)
```
Example
```python
  houses = ["Gryffindor", "Hufflepuff", "Ravenclaw", "Slytherin"]
  print(houses)
  houses.remove("Ravenclaw")
  print(houses)
```

**List Slicing**
- Slicing a list gives us a sublist
```python
  num_list = [1, 2, 3, 4, 5, 6, 7, 8]
  print(num_list[2:5]) # returns elements from index 2 - 4 => [3, 4, 5]
  print(num_list[0::2]) # returns every 2nd element startig from 0 => [1, 3, 5, 7]
```

**Index Search**
- The index() method returns the index of a given value.
```python
  cities = ["London", "Paris", "Los Angeles", "Beirut"]
  print(cities.index("Los Angeles"))  # It is at the 2nd index
```

**Check Existence in List**
- We just want to verify the existence of an element in a list by using the **in** operator:
```python
  cities = ["London", "Paris", "Los Angeles", "Beirut"]
  print("London" in cities) # prints True
  print("London" not in cities) # prints False
```

**Sorting the List**
- We can sort the list using **sort()** method
```python
  num_list = [20, 40, 10, 50.4, 30, 100, 5]
  num_list.sort()
  print(num_list) # prints [5, 10, 20, 30, 40, 50.4, 100]
```

**Note:** Official List [documentation](https://docs.python.org/3/tutorial/datastructures.html).


### 2. Tuples:
- A tuple is very similar to a list, except for the fact that its contents cannot be changed. i.e, a tuple is **immutable**. 
- The contents of a tuple are enclosed in parentheses, ().
- They Tuples are ordered, and hence, follow the linear index notation.
- Creating a Tuple
```python
  car = ("Ford", "Raptor", 2019, "Red")
  print(car)

  # Length
  print(len(car))

  # Indexing
  print(car[1])

  # Slicing
  print(car[2:])
```
- Merging Tuples
```python
  heroes1 = ("Batman", "Bruce Wayne")
  heroes2 = ("Wonder Woman", "Diana Prince")
  avengers = heroes1 + heroes2
  print(avengers)
```
- Check Existence in a Tuples - use **in** operator
```python
  cities = ("London", "Paris", "Los Angeles", "Tokyo")
  print("Moscow" in cities)
```
- Get the index of a particular value - use **index()** function
```python
  cities = ("London", "Paris", "Los Angeles", "Tokyo")
  print(cities.index("Tokyo")) # prints 3 
```
- **Note:** Since tuples are immutable, we can’t add or delete elements from them. Furthermore, it isn’t possible to append another tuple to an existing tuple.

### 3. Dictionaries:
- A dictionary stores key-value pairs, where each unique key is an index which holds the value associated with it.
- Dictionaries are unordered because the entries are not stored in a linear structure.

<img width="677" alt="image" src="https://user-images.githubusercontent.com/112779376/235673897-b69ceb95-ad69-479c-b5ca-ebda26f9ec33.png">

**Creating a Dictionary **
```python
  empty_dict = {}   # Empty dictionary - most popular approach
  print(empty_dict) # prints: {} 

  phone_book = {"Batman": 468426,
                "Cersei": 237734,
                "Ghostbusters": 44678}
  print(phone_book)   # prints: {'Batman': 468426, 'Cersei': 237734, 'Ghostbusters': 44678}
```
- We can use the **dict()** Constructor to create dictionary.
```python
  empty_dict = dict()  # Empty dictionary
  print(empty_dict)

  phone_book = dict(Batman=468426, Cersei=237734, Ghostbusters=44678)
  # Keys will automatically be converted to strings
  print(phone_book)

  # Alternative approach
  phone_book = dict([('Batman', 468426),
                     ('Cersei', 237734),
                     ('Ghostbusters', 44678)])
  print(phone_book)
```

**Accessing Values:**
- We can access a value by enclosing its **key** in square brackets, **[]**.
```python
a_dictionary[key]
```
- We can also access a value by using the **get()** method.
```python
a_dictionary.get(key)
```
- Example
```python
  phone_book = {"Batman": 468426,
                "Cersei": 237734,
                "Ghostbusters": 44678}
  print(phone_book["Cersei"])
  print(phone_book.get("Ghostbusters"))
```

**Adding/Updating Entries:**
- We can add new entries in a dictionary by simply assigning a value to a key. Python automatically creates the entry.
```python
  phone_book = {"Batman": 468426,
                "Cersei": 237734,
                "Ghostbusters": 44678}

  phone_book["Godzilla"] = 46394  # New entry
  print(phone_book)

  phone_book["Godzilla"] = 9000  # Updating entry
  print(phone_book)
```
Note: If a key already exists, then its value will be updated.

**Removing Entries:**
- We can delete an entry using **del** keyword
```python
  del phone_book["Batman"]
```
- If we want to use the deleted value, we can use the **pop()** or **popitem()** method.
- The **pop()** method deletes and return entry for the key
```python
  cersei = phone_book.pop("Cersei")
  print(cersei)
```
- The **popitem()** method removes and returns the last inserted pair, as a tuple
```python
  lastAdded = phone_book.popitem()
  print(lastAdded)
```
**Length of a Dictionary:**
```python
len(my_dict)
```
**Checking Key Existence:**
- We can use the **in** keyword to check if a key exists
```python
  phone_book = {"Batman": 468426,
                "Cersei": 237734,
                "Ghostbusters": 44678}
  print("Batman" in phone_book)   # prints: True
  print("Godzilla" in phone_book) # prints: False
```

**Copying Contents from one dictionary to another**
- To copy the contents of one dictionary to another, we can use the **update()** method.
```python
  phone_book = {"Batman": 468426,
                "Cersei": 237734,
                "Ghostbusters": 44678}

  second_phone_book = {"Catwoman": 67423, 
                      "Jaime": 237734, 
                      "Godzilla": 37623}

  # Add second_phone_book to phone_book
  phone_book.update(second_phone_book)
  print(phone_book)
```

**Dictionary Comprehension:**
- We can create new key-value pairs based on an existing dictionary.
- To iterate the dictionary, we use the **dict.items()** operation which turns a dictionary into a **list of (key, value) tuples**.
```python
  houses = {1: "Gryffindor", 2: "Slytherin", 3: "Hufflepuff", 4: "Ravenclaw"}
  new_houses = {n**2: house + "!" for (n, house) in houses.items()}

  print(new_houses)   # prints:  {16: 'Ravenclaw!', 1: 'Gryffindor!', 4: 'Slytherin!', 9: 'Hufflepuff!'}
```

### 4. Set:
- A set is an unordered collection of unique data items.

**Creating a Set:**
- By encapsulating elements of a set in curly brackets, **{}**
```python
  random_set = { "Test Item", 1408, 3.142, (True, False) }
  print(random_set)
```
- Using a set() Constructor
```python
  empty_set = set()
  print(empty_set)

  random_set = set({"Test Item", 1408, 3.142, (True, False)})
  print(random_set)
```
Note: A set() Constructor allows us to create an empty constructor.

**Adding Elements:**
- To add a single item, we can use the **add()** method.
```python
  my_set.add(1)
```

- To add a multiple items (another set, list, tuple, or string), we can use the **update()** method.


```python
  my_set = set()

  # Add list to the set
  my_set.update([2, 3, 4, 5, 6])
```

**Deleting Elements:**
- We can use the **discard()** or **remove()** methods to delete a particular item from a set
```python
  my_set = set({"Test Item", 1408, 3.142, (True, False)})
  print(my_set)

  my_set.discard(1408)  
  print(random_set)

  my_set.remove((True, False))
  print(random_set)
```
**Note:** 
  - The **discard()** method **does not throw an error** if the item **doesnt exist** in the set 
  - The **remove()** method **throws an error** if the item **doesnt exist** in the set 

**Iterating a Set**
- Like other Data Structures, for loop can be used to iterate over all items in the set.
```python
  my_set = {9, 10, 11, 12, 13, 14, 15, 16, 17}
  
  # Numbers will be printed in random order
  for num in my_set:
    print(num)
```

**Set Theory Operations:**
- **Union:** The union of two sets can be obtained using the pipe operator, **|**, or the **union()** method
```python
  set_A = {1, 2, 3, 4}
  set_B = {'a', 'b', 'c', 'd'}

  set_C = set_A | set_B   # Alternately, set_C = set_A.union(set_B)
  print(set_C)            # prints: {1, 2, 3, 4, 'd', 'c', 'a', 'b'}
```

- **Intersection:**  The intersection of two sets can be found using either the **&** operator or the **intersection()** method:
```python
  set_A = {1, 2, 3, 4}
  set_B = {2, 8, 4, 16}

  set_C = set_A & set_B   # Alternately, set_C = set_A.intersection(set_B)
  print(set_C)            # prints: {2, 4}
```
- **Difference:** the difference between two sets can be found using either the **-** operator or the **difference()** method.
```python
  set_A = {1, 2, 3, 4}
  set_B = {2, 8, 4, 16}
  
  # returns the elements which are only present in set_A
  print(set_A - set_B)            # alternatively, set_A.difference(set_B)

  # returns the elements which are only present in set_B
  print(set_B - set_A)            # alternatively, set_B.difference(set_A)
```

### Data Structure Conversion
- General format for converting from one data structure to another
```python
destination_structure_name(source_structure_name)
```

**Converting to a List**
- We can convert a tuple, set, or dictionary to a list using the list() constructor
```python
  star_wars_tuple = ("Anakin", "Darth Vader", 1000)
  star_wars_set = {"Anakin", "Darth Vader", 1000}

  star_wars_list = list(star_wars_tup)  # Converting from tuple
  star_wars_list = list(star_wars_set)  # Converting from set
```
- While converting a dictionary to list, only the keys will be converted to a list.
```python
  star_wars_dict = {1: "Anakin", 2: "Darth Vader", 3: 1000}

  # Converting from dictionary
  star_wars_list = list(star_wars_dict)   
  print(star_wars_list)                   # prints: [1, 2, 3]
```
- In case of dictionaries dict.items() convert it into an iterable of (key, value) tuples. Which can be casted to a list.
```python
  star_wars_dict = {1: "Anakin", 2: "Darth Vader", 3: 1000}

  # Get a list of dict entries as tuples
  star_wars_list = list(star_wars_dict.items())

  print(star_wars_list)     # prints list: [(1, 'Anakin'), (2, 'Darth Vader'), (3, 1000)]
```

**Converting to a Tuple**
- Any data structure can be converted to a tuple using the tuple() constructor.
```python
  star_wars_list = ["Anakin", "Darth Vader", 1000]
  star_wars_set = {"Anakin", "Darth Vader", 1000}
  star_wars_dict = {1: "Anakin", 2: "Darth Vader", 3: 1000}

  star_wars_tuple = tuple(star_wars_list)   # Converting from list
  print(star_wars_tuple)                    # prints:('Anakin', 'Darth Vader', 1000)

  star_wars_tuple = tuple(star_wars_set)    # Converting from set
  print(star_wars_tuple)                    # prints:(1000, 'Anakin', 'Darth Vader')

  star_wars_tuple = tuple(star_wars_dict)   # Converting from dictionary - only keys will be converted
  print(star_wars_tuple)                    # prints: (1, 2, 3)
```

**Converting to a Set**
- The set() constructor can be used to create a set out of any other data structure.
- In the case of a dictionary, only the keys will be converted to a set.
```python
  star_wars_list = ["Anakin", "Darth Vader", 1000]
  star_wars_tuple = ("Anakin", "Darth Vader", 1000)
  star_wars_dict = {1: "Anakin", 2: "Darth Vader", 3: 1000}

  star_wars_set = set(star_wars_list)   # Converting from list
  print(star_wars_set)                  # prints: {1000, 'Anakin', 'Darth Vader'}

  star_wars_set = set(star_wars_tuple)  # Converting from tuple
  print(star_wars_set)                  # prints: {1000, 'Anakin', 'Darth Vader'}

  star_wars_set = set(star_wars_dict)   # Converting from dictionary
  print(star_wars_set)                  # prints:{1, 2, 3} 
```

**Converting to a Dictionary**
- The dict() constructor cannot be used in the same way as the others because it requires key-value pairs instead of just values.
- To convert another data structure to a dictionary the data must be stored in a format where pairs exist.  
  - e.g For example, a list of tuples where the length of each tuple is 2 can be converted into a dictionary.
```python
  star_wars_list = [[1,"Anakin"], [2,"Darth Vader"], [3, 1000]]
  star_wars_tuple = ((1, "Anakin"), (2, "Darth Vader"), (3, 1000))
  star_wars_set = {(1, "Anakin"), (2, "Darth Vader"), (3, 1000)}

  star_wars_dict = dict(star_wars_list)   # Converting from list
  print(star_wars_dict)                   # prints: {1: 'Anakin', 2: 'Darth Vader', 3: 1000}

  star_wars_dict = dict(star_wars_tuple)  # Converting from tuple
  print(star_wars_dict)                   # prints: {1: 'Anakin', 2: 'Darth Vader', 3: 1000}

  star_wars_dict = dict(star_wars_set)  # Converting from set
  print(star_wars_dict)                   # prints: {1: 'Anakin', 2: 'Darth Vader', 3: 1000}
```

### Additional important Data Structures in Python
Below are the data structures that are frequently used in Python in addition to primary data structure:
- deque
- defaultdict
- heap
- Counter

### 1. deque:
- Deques are a generalization of stacks and queues.
- Deques support memory efficient appends and pops from either side of the deque with O(1) performance in either direction.
- A deque accepts a maxlen argument which sets the bounds for the deque. Otherwise the deque will grow to an arbitrary size.
- When a bounded deque is full, any new items added will cause the same number of items to be popped off the other end.
- As a general rule,
    - If we need **fast appends or fast pop**s, use a **deque**.
    - If we need **fast random access**, use a **list**.
```python
  # Declaration: we will use deque from the collections module
  import from collections import deque
  queue = deque()
  
  # If we want to initialize deque with some initial values:
  queue = deque([1, 2, 3])
  
  # Enqueueing/adding elements (added to right):
  queue.append(4)   # Now queue is: [1, 2, 3, 4]
  queue.append(5)   # Now queue is: [1, 2, 3, 4, 5]
  
  # Dequeuing/removing elements:
  queue.popleft() # returns 1  Now queue is: [2, 3, 4, 5]
  queue.popleft() # returns 2  Now queue is: [3, 4, 5]
  
  # Check element at front of queue (next element to be removed)
  queue[0] # 3
  
  # Get size
  len(queue) # 3

  # Adding elements to the left (start of the queue:
  queue.appendleft(2)   # Now queue is: [2, 3, 4, 5]
  queue.appendleft(1)   # Now queue is: [1, 2, 3, 4, 5]
  
  # Removing elements from right (end of the queue):
  queue.pop() # returns 5  Now queue is: [1, 2, 3, 4]
  queue.pop() # returns 4  Now queue is: [1, 2, 3]

  # Iterating over queue:
  while queue:
    print(queue.popleft())

  # Checks if queue is empty
  if not queue:
    print("Queue is empty!")
```
### 2. defaultdict:
The **defaultdict** is a subclass of Python’s dict class.

**Counting the occurrence of words: Regular dict**
```python
  sentence = "The red for jumped over the fence and ran to the zoo for food"
  words = sentence.split(' ')
  reg_dict = {}
  
  for word in words:
      if word in reg_dict:
          reg_dict[word] += 1
      else:
          reg_dict[word] = 1
  
  print(reg_dict)
```

**Counting the occurrence of words: defaultdict**
```python
default_dict = defaultdict(int)
  for word in words:
      default_dict[word] += 1
  
  print(default_dict)
```
- The defaultdict will automatically assign zero as the value to any key it doesn’t already have in it.
- Setting the default_factory (first argument to defaultdict(default_factory)) to int makes it useful for counting

**The defaultdict from list**
```python
  from collections import defaultdict
  
  my_list = [(1234, 100.23), (345, 10.45), (1234, 75.00),
             (345, 222.66), (678, 300.25), (1234, 35.67)]
  
  my_dict = defaultdict(list)
  for acct_num, value in my_list:
      my_dict[acct_num].append(value)
  
  # alternatively: 
  # for key, value in my_list:
  #     my_dict.setdefault(key, []).append(value)
  
  print(my_dict)
```
### 3. heapq:
- The **heapq** module provides an implementation of the **heap queue** or **priority queue** algorithm.
- The heapq only implements min heaps
```python
  # In Python, we use the heapq module for heap ds
  from heapq import *
  
  # Declaration: heapq does not give you a heap data structure.
  # You just use a normal list, and heapq provides you with
  # methods that can be used on this list to perform heap operations

  # Declare a heap
  heap = []
  
  # Add to heap
  heappush(heap, 1)
  heappush(heap, 2)
  heappush(heap, 3)
  heappush(heap, 4)
  
  # Check minimum element
  print(heap[0]) # prints 1
  
  # Pop minimum element
  heappop(heap) # removes 1 - min element
  
  # Get size
  len(heap) # 3
  
  # The numbers will be printed in sorted order
  while heap:
    print(heapq.heappop(heap)) # 1 2 3 4
  
  # Convert a list to a heap in linear time
  nums = [43, 2, 13, 634, 120]
  heapify(nums)
  
  # Now, we can use heappush and heappop on nums
  # and nums[0] will always be the minimum element
```
