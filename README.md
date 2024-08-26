# shakib_s_Python_all
## Python List Basics
#### List Properties
- Ordered: Items maintain their order.
- Changeable: You can modify, add, and remove items.
- Allows Duplicates: Items with the same value are allowed.

 
```python 
#Create a List:
my_list = ["apple", "banana", "cherry", 5, 6.2]

#Access Elements:
print(my_list[0])    # First item
print(my_list[-1])   # Last item

#Slice a List:
print(my_list[2:4])  # From index 2 to 3
print(my_list[:3])   # From start to index 2
print(my_list[3:])   # From index 3 to end
```

#### List Methods
```python 
#Add Elements:
my_list.append("orange")     # Add to the end
my_list.insert(1, "blueberry")  # Insert at index 1

#Remove Elements:
my_list.remove("banana")  # Remove by value
my_list.pop(2)            # Remove by index
my_list.clear()           # Remove all elements

#Modify Elements:
my_list[1] = "mango"      # Change value at index 1

#Copy List:
new_list = my_list.copy()  # Creates a shallow copy

#Combine Lists:
my_list.extend(["grape", "melon"])  # Add elements of another list

#Find Elements:
idx = my_list.index("cherry")   # Get index of element
count = my_list.count("cherry") # Count occurrences

#Sorting and Reversing:
my_list.sort()     # Sort the list (ascending by default)
my_list.reverse()  # Reverse the order

#The general syntax for slicing a list is:
list[start:stop:step]
#using slicing reverse list examble
list1 = [100, 200, 300, 400, 500]
newlist = list1[::-1]  # This creates a new list that is the reverse of list1
print(newlist)         # Prints the reversed list
```

List Constructor
```python 
#Create List with Constructor:
this_list = list(("apple", "banana", "cherry"))

#Advanced Tips
#Check Existence:

if "apple" in my_list:
    print("Exists!")

#List Comprehensions:
squared = [x**2 for x in range(10)]  # Create list with comprehension
```


## Python Tuple Basics
##### Tuple Properties

- Ordered: Items maintain their order.
- Immutable: You cannot change, add, or remove items after the tuple is created.
- Allows Duplicates: Items with the same value are allowed.


```python
#Create a Tuple:
my_tuple = ("apple", "banana", "cherry", 5, 6.2)

#Single-Element Tuple:
single_element_tuple = ("apple",)  # Note the comma

#Access Elements:
print(my_tuple[0])    # First item
print(my_tuple[-1])   # Last item

#Slice a Tuple:
print(my_tuple[2:4])  # From index 2 to 3
print(my_tuple[:3])   # From start to index 2
print(my_tuple[3:])   # From index 3 to end
```

Tuple Methods
```python
#Find Elements:
idx = my_tuple.index("cherry")   # Get index of element
count = my_tuple.count("banana") # Count occurrences

```
##### Tuple Operations
```python
#Concatenate Tuples:
new_tuple = my_tuple + ("grape", "melon")

#Repeat Tuples:
repeated_tuple = my_tuple * 2
```
#Advanced Tips
#Tuple Packing and Unpacking:
```python
packed_tuple = 1, 2, "apple"  # Tuple packing
a, b, c = packed_tuple        # Tuple unpacking
```

#Check Existence:
```python
if "apple" in my_tuple:
    print("Exists!")
```

#Immutable but Can Contain Mutable Elements:
```python 
my_tuple = ("apple", [1, 2, 3])
my_tuple[1][0] = 4  # You can change mutable elements like lists within a tuple
```
```python 
#Create Tuple with Constructor:
this_tuple = tuple(("apple", "banana", "cherry"))

#Applications of Tuples
Function Arguments: Tuples are often used to pass multiple arguments to functions.
Return Multiple Values: Functions can return multiple values as a tuple

```

## Python Set Basics

#### Set Properties

- Unordered: Items do not have a defined order.
- Unindexed: Items cannot be accessed by index.
- No Duplicates: Sets do not allow duplicate values. Adding a duplicate value will have no effect.

```python 
#Create Set with Constructor:
this_set = set(("apple", "banana", "cherry"))
```

#### Set Methods
```python 
#Add Elements:
my_set.add("orange")  # Add a single element
my_set.update(["grape", "melon"])  # Add multiple elements

#Remove Elements:
my_set.remove("banana")  # Remove specified element; raises KeyError if not found
my_set.discard("banana")  # Remove specified element; does not raise an error if not found
my_set.pop()  # Remove and return an arbitrary element
my_set.clear()  # Remove all elements

#Subset and Superset:
is_subset = set1.issubset(set2)  # Check if set1 is a subset of set2
is_superset = set1.issuperset(set2)  # Check if set1 is a superset of set2

#Disjoint Sets: Check if two sets have no common elements
is_disjoint = set1.isdisjoint(set2)


```

#### Set Operations
```python 
#Union: Combine two sets
set1 = {"apple", "banana"}
set2 = {"cherry", "orange"}
union_set = set1.union(set2)  # {'apple', 'banana', 'cherry', 'orange'}

#Intersection: Get common elements
intersection_set = set1.intersection(set2)

#Difference: Get elements in one set but not in the other
difference_set = set1.difference(set2)

#Symmetric Difference: Get elements in either set, but not both
sym_diff_set = set1.symmetric_difference(set2)
```

#### Advanced Tips
```python 
#Convert List to Set (Remove Duplicates):
my_list = [1, 2, 2, 3]
my_set = set(my_list)  # {1, 2, 3}

#Frozen Sets (Immutable Sets):
frozen = frozenset({"apple", "banana", "cherry"})
```

## Python Dictionary Basics

```python
#Create Dictionary with Constructor:
this_dict = dict(name="Alice", age=25, city="New York")

#Create a Dictionary:
my_dict = {"name": "Alice", "age": 25, "city": "New York"}

#Access Values:
print(my_dict["name"])  # Access by key

#Get All Keys and Values:
keys = my_dict.keys()       # Returns a view of all keys
values = my_dict.values()   # Returns a view of all values
items = my_dict.items()     # Returns a view of all key-value pairs
```
#### Dictionary Methods
```python 
#Add or Update Elements:
my_dict["email"] = "alice@example.com"  # Add new key-value pair
my_dict["age"] = 26                     # Update existing value

#Remove Elements:
my_dict.pop("age")           # Remove key-value pair by key
del my_dict["city"]          # Remove key-value pair by key
my_dict.clear()              # Remove all key-value pairs

#Check if Key Exists:
if "name" in my_dict:
    print("Key exists")

#Set Default: Return value if key exists, otherwise set it
value = my_dict.setdefault("age", 30)  # Adds "age": 30 if "age" doesn't exist

#Get Value Safely:
age = my_dict.get("age", 0)  # Returns 0 if "age" key is not found
```
#### Dictionary Operations
```python 
#Merge Dictionaries:
dict1 = {"a": 1, "b": 2}
dict2 = {"b": 3, "c": 4}
merged_dict = {**dict1, **dict2}  # {'a': 1, 'b': 3, 'c': 4}

#Iterate Over Dictionary:
for key, value in my_dict.items():
    print(f"{key}: {value}")

#Dictionary Comprehension:
squares = {x: x**2 for x in range(6)}  # {0: 0, 1: 1, 2: 4, 3: 9, 4: 16, 5: 25}

#Nested Dictionaries:
nested_dict = {
    "person1": {"name": "Alice", "age": 25},
    "person2": {"name": "Bob", "age": 30}
}

#Defaultdict (from collections module):
from collections import defaultdict
dd = defaultdict(int)  # Creates a dictionary with a default value of 0 for any new key
dd["apples"] += 1
```

## Traversing 
- List & Tuple: Traverse using for loop or enumerate() for index and value.
- Set: Traverse using for loop (unordered, no index).
- Dictionary: Traverse keys with a for loop, or use items() for key-value pairs, keys() for keys, and values() for values.

#### Traversing a List
```python 
#Using a for loop:
my_list = ["apple", "banana", "cherry"]
for item in my_list:
    print(item)

#Using enumerate() (to get index and value):
for index, value in enumerate(my_list):
    print(index, value)
```

#### Traversing a Tuple
```python
#Using a for loop:
my_tuple = ("apple", "banana", "cherry")
for item in my_tuple:
    print(item)

#Using enumerate() (to get index and value):
for index, value in enumerate(my_tuple):
    print(index, value)
```
#### Traversing a Set
```python
#Using a for loop:
my_set = {"apple", "banana", "cherry"}
for item in my_set:
    print(item)
```
#### Traversing a Dictionary
```python
#Using a for loop (keys only):
my_dict = {"name": "Alice", "age": 25, "city": "New York"}
for key in my_dict:
    print(key)
#Using items() (to get both keys and values):
for key, value in my_dict.items():
    print(key, value)
#Using keys() (explicitly, though not necessary):
for key in my_dict.keys():
    print(key)

#Using values() (to get values only):
for value in my_dict.values():
    print(value)
```


URL: https://pynative.com/python-list-exercise-with-solutions/#h-exercise-1-reverse-a-list-in-python
```python
#Given:list1 = [100, 200, 300, 400, 500]
#Expected output:[500, 400, 300, 200, 100]

list1 = [100, 200, 300, 400, 500]
#Option 1: Reverse In-Place and Print the Original List
list1.reverse()
print(list1)

#Option 2: Use Slicing to Reverse and Assign to a New List
newlist=list1[::-1] #list[start:stop:step]

#Option 3: Use reversed() Function
newlist = list(reversed(list1))  # reversed() returns an iterator, list() converts it back to a list
```

URL: https://pynative.com/python-list-exercise-with-solutions/#h-exercise-2-concatenate-two-lists-index-wise
```python
#Given:
#list1 = ["M", "na", "i", "Ke"]
#list2 = ["y", "me", "s", "lly"]
#Expected output:
#['My', 'name', 'is', 'Kelly']


list1 = ["A", "B", "C"]
list2 = ["1", "2", "3"]
# Concatenate two lists index-wise
concatenated_list = [i + j for i, j in zip(list1, list2)]
print(concatenated_list)



#Example with Different Lengths (you might want to use itertools.zip_longest() from the itertools module to fill in missing values.)
from itertools import zip_longest
list1 = ["A", "B", "C", "D"]
list2 = ["1", "2", "3"]
# Concatenate two lists index-wise, filling missing values with an empty string
concatenated_list = [i + j for i, j in zip_longest(list1, list2, fillvalue="")]
print(concatenated_list)
```

URL: https://pynative.com/python-list-exercise-with-solutions/#h-exercise-3-turn-every-item-of-a-list-into-its-square
```python
#Solution 1: Using loop and list method
list=[1, 2, 3, 4, 5, 6, 7]
newList=[]
for i in list:
  newList.append(i*i)
print(newList)

#Solution 2: Use list comprehension
list=[1, 2, 3, 4, 5, 6, 7]
newlist= [i*i for i in list]
print(newlist)
```

```python
list1 = [10, 20, 30, 40] 
list2 = [100, 200, 300, 400]
for   i,j in zip(list1,list2[::-1]):
  print(i,j)
```

##### Problem: Iterate both lists simultaneously
##### URL: https://pynative.com/python-list-exercise-with-solutions/#h-exercise-5-iterate-both-lists-simultaneously
```python
#solution
list1 = [10, 20, 30, 40] 
list2 = [100, 200, 300, 400]
for   i,j in zip(list1,list2[::-1]):
  print(i,j)
```


##### Problem: Remove empty strings from the list of strings
##### URL: https://pynative.com/python-list-exercise-with-solutions/#h-exercise-6-remove-empty-strings-from-the-list-of-strings
```python
list1 = ["Mike", "", "Emma", "Kelly", "", "Brad"]
newList= list(filter(None,list1))
print( newList) 
```


##### problem: Add new item to list after a specified item
##### URL: https://pynative.com/python-list-exercise-with-solutions/#h-exercise-7-add-new-item-to-list-after-a-specified-item
```python
def traverse_list(nested_list,value_to_insert):
    for i, element in enumerate(nested_list):
        if isinstance(element, list):
            traverse_list(element,value_to_insert)  # Recursively traverse sublist
        else:
            print(element)
            if element==6000:
                nested_list.insert(i+1,value_to_insert)
                return
value_to_in =7000
list1 = [10, 20, [300, 400, [5000, 6000], 500], 30, 40]
traverse_list(list1,value_to_in)
print("Modified list:", list1)
```


##### URL:https://pynative.com/python-list-exercise-with-solutions/#h-exercise-8-extend-nested-list-by-adding-the-sublist
##### Extend nested list by adding the sublist
```python
list1 = ["a", "b", ["c", ["d", "e", ["f", "g"], "k"], "l"], "m", "n"]

# Sub list to add
sub_list = ["h", "i", "j"]
list1[2][1][2].extend(sub_list)
print(list1)
```

##### URL: https://pynative.com/python-list-exercise-with-solutions/#h-exercise-9-replace-list-s-item-with-new-value-if-found
##### Replace list’s item with new value if found, Write a program to find value 20 in the list, and if it is present, replace it with 200. every occurance
```python
list1 = [5, 10, 15, 20, 25, 50, 20]
for i,ele in enumerate(list1):
    if ele==20:
        index_value20=list1.index(20)
        list1[index_value20]=200
        continue
print(list1)
```

##### URL: https://pynative.com/python-list-exercise-with-solutions/#h-exercise-10-remove-all-occurrences-of-a-specific-item-from-a-list
##### write a program to remove all occurrences of item 20.
```python
list1 = [5, 10, 15, 20, 25, 50, 20]
for i,ele in enumerate(list1):
    if ele==20:
        index_value20=list1.index(20)
        list1.pop(index_value20)            # Remove by index
        continue
print(list1)
```

### Python Set Exercise with Solutions

##### Exercise 1: Add a list of elements to a set
##### URL: https://pynative.com/python-set-exercise-with-solutions/#h-exercise-1-add-a-list-of-elements-to-a-set
```python
#Given:
sample_set = {"Yellow", "Orange", "Black"}
sample_list = ["Blue", "Green", "Red"]
#Expected output:
{'Green', 'Yellow', 'Black', 'Orange', 'Red', 'Blue'}
#Note: Set is unordered.


#Solution one:
sample_set.update(sample_list)
print(sample_set)

#Solution two:
list_to_set= set(sample_list)
sample_set.union(list_to_set)
print(sample_set)
#####################################


 
##### Exercise 2: Return a new set of identical items from two sets
#### URL: https://pynative.com/python-set-exercise-with-solutions/#h-exercise-2-return-a-new-set-of-identical-items-from-two-sets

#Given:

set1 = {10, 20, 30, 40, 50}
set2 = {30, 40, 50, 60, 70}
#Expected output: {40, 50, 30}

print(set1.intersection(set2))
#set1.intersection_update(set2) 
#use intersection_update if you want keep modification update

##### Exercise 3: Get Only unique items from two sets
#### URL: https://pynative.com/python-set-exercise-with-solutions/#h-exercise-3-get-only-unique-items-from-two-sets

#Given:

set1 = {10, 20, 30, 40, 50}
set2 = {30, 40, 50, 60, 70}
#Expected output: {70, 40, 10, 50, 20, 60, 30}

print( set1.union(set2))


##### Exercise 4: Update the first set with items that don’t exist in the second set
#### URL: https://pynative.com/python-set-exercise-with-solutions/#h-exercise-4-update-the-first-set-with-items-that-don-t-exist-in-the-second-set

#Given:
set1 = {10, 20, 30}
set2 = {20, 40, 50}
#Expected output: set1 {10, 30}
#method set1.difference_update(set2) is used in Python to modify set1 by removing all elements found in set2
set1.difference_update(set2)

print( set1)
###################################

##### Exercise 5: Update the first set with items that don’t exist in the second set
#### URL: https://pynative.com/python-set-exercise-with-solutions/#h-exercise-4-update-the-first-set-with-items-that-don-t-exist-in-the-second-set

#Given:
set1 = {10, 20, 30}
set2 = {20, 40, 50}
#Expected output: set1 {10, 30}
#method set1.difference_update(set2) is used in Python to modify set1 by removing all elements found in set2
set1.difference_update(set2)

print( set1)
###################################
#The symmetric_difference_update and symmetric_difference methods in Python are both used to compute the symmetric difference between two sets, but they differ in how they handle the original set.

Modification of Original Set:

    symmetric_difference: Does not modify the original set; instead, it returns a new set.
    symmetric_difference_update: Modifies the original set in place.

Return Value:

    symmetric_difference: Returns a new set with the symmetric difference.
    symmetric_difference_update: Returns None (the operation is done in place).

Use Case:

    Use symmetric_difference when you need to keep the original set unchanged and work with a new set containing the symmetric difference.
    Use symmetric_difference_update when you want to update the original set with the symmetric difference directly.



##### Exercise 6: Return a set of elements present in Set A or B, but not both
#### URL: https://pynative.com/python-set-exercise-with-solutions/#h-exercise-6-return-a-set-of-elements-present-in-set-a-or-b-but-not-both

#Given:
set1 = {10, 20, 30, 40, 50}
set2 = {30, 40, 50, 60, 70}
#Expected output: {20, 70, 10, 60}

#method The symmetric_difference method returns a new set containing these unique elements 
#set1 ^ set2 will do same
print(set1.symmetric_difference(set2))
 
###################################


##### Exercise 8: Update set1 by adding items from set2, except common items
##### URL: https://pynative.com/python-set-exercise-with-solutions/#h-exercise-8-update-set1-by-adding-items-from-set2-except-common-items

#Given:
set1 = {10, 20, 30, 40, 50}
set2 = {30, 40, 50, 60, 70}
#Expected output: {70, 10, 20, 60}

set1.symmetric_difference_update(set2)
print(set1)
 
###################################

##### Exercise7: Check if two sets have any elements in common. If yes, display the common elements
##### URL: https://pynative.com/python-set-exercise-with-solutions/#h-exercise-7-check-if-two-sets-have-any-elements-in-common-if-yes-display-the-common-elements

#Given:
set1 = {10, 20, 30, 40, 50}
set2 = {60, 70, 80, 90, 10}
#Expected output:Two sets have items in common {10}


if set1.isdisjoint(set2):
    print("no two set have common item")
else:
    print(" two set have common item")
    print(set1.intersection(set2))
 
###################################

```






#URL: https://www.hackerrank.com/challenges/py-if-else/problem?isFullScreen=true
```python 
    n = int(input().strip())
if n%2 != 0:
    print("Weird")
else:
    if 2<= n<= 5:
        print("Not Weird")
    elif 6<= n <= 20:
        print("Weird")
    elif n>20:
        print("Not Weird")
```
