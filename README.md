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
