# shakib_s_Python_all
Python List Basics
List Properties
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

List Methods
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


#### Python Tuple Basics
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






    
URL: https://www.hackerrank.com/challenges/py-if-else/problem?isFullScreen=true
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
