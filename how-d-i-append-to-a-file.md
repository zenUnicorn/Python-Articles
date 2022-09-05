---
title: "How do I check if a list is empty?"
description: "How to check if a list in python is empty."
date: "2022-08-28"
draft: false
link: "How do I check if a list is empty?"
author: "Shittu Olumide"
---

Everyday as a developer or programmer we are faced with different problems and it gets a little too confusing to solve them. Programming questions can be really hectic and difficult to solve because they require lots of thinking and trials. 

You may be in an hackathon or in a live coding test and you are given a data structure test where you are asked to perform different operations such as loop, conditionals, error handling, and lots more. 

I'll explain how you can quickly check if a python list is empty in this article


### List in python
In python a list is made by enclosing elements in square brackets [  ] and separating them with commas and they are quite are useful for storing multiple elements in a single variable.


### Why check if a list is empty in Python?
The iterability of lists is a key feature that most developers employ while working with them. This makes the list useful for loops specifically because you can iterate across the values in the list. Additionally useful when working with strings and mathematical operations. Therefore, it is a good idea to make sure a list is empty before moving further.

All iterables, such as dictionaries, tuples, etc., still hold true to this.

### How to check if a list is empty in Python
Python treats empty lists as **False**, therefore if a list were supplied as an argument, the `bool()` function would return False. Placing a list within an if statement, utilizing the `len()` method, or comparing it to an empty list are additional ways to determine if a list is empty.

Now that that is out of the way, let's have a look at the different Python techniques that can be used to determine whether a list is empty.


#### 1. Using PEP 8 recommended method
This is a method that allows us to determine whether a list in Python is empty. Since an empty list is **False**, the condition is false and hence we are able to identify an empty list. It is the most Pythonic method of checking if a list is empty. 

```python
FirstList = ["Good", "Better", "Best"]

SecondList = []

if SecondList:
    print("This list is not empty")
else:
    print("This list is empty")

```

**Output**:
```python
# This list is empty
```

Another common method is with the implication of a **not**.

```python
a = []
if not a:
    print("This is an empty list")

```

**Output**:
```python
# This is an empty list
```

#### 2. Using the len() function
To determine whether a list is empty in this solution, we utilize the `len()` function, which returns the length of the input supplied. Additionally, python may be used to determine whether a list is empty because an empty list has a length of 0.

```python
ListOne = ["Asia", "Africa", "Europe", "America", "Australia"]

ListTwo = []

if len(ListTwo):
    print("list is not empty")
else:
    print("Empty list")

```

**Output**:
```python
# Empty list
```

Additionally, you can use the comparison operator with `len()` to check the empty list.
```python
def AnotherList(BigList):
    if len(BigList) == 0:
        return 0
    else:
        return 1
 

BigList = []
if AnotherList(BigList):
    print("The list is not empty")
else:
    print("This is an Empty List")

```

**Output**:
```python
# This is an Empty List
```

#### 3. Using the bool() function
We use the `bool()` function to determine if a list is empty, which is similar to the PEP8 approach. The `bool()` function gives an object's boolean value, or whether it is true or false.

```python
list1 = ["Football", "Basktball", 1, 2.8, True]

list2 = []

if len(list2) == 0:
    print("This list is empty")
else:
    print("This list is not empty")

```
**Output**:
```python
# This list is empty
```
To check if the list is not empty, you just change the 0 to 1

```python
list1 = ["Football", "Basktball", 1, 2.8, True]

list2 = []

if len(list2) == 1:
    print("This list is empty")
else:
    print("This list is not empty")

```
**Output**:
```python
# This list is not empty
```

#### 4. Using the exception and iter()
The `iter()` method returns an iterator for the given argument. Then an occurrence that takes place during the execution of a program that obstructs the regular flow of the program's instructions is referred to as an exception. A Python script typically raises an exception when it comes into a scenario that it cannot handle.

```python
x = [] #the list
try:
    next(iter(x))
    # list has elements
except StopIteration:
    print("List is empty")

```

**Output**:
```python
# List is empty
```

#### 5. Using the Numpythonic way
The earlier techniques that we employed in standard Python don't work with numpy. If we have a numPy array, using `.size` is always the right course of action. This size verifies the arrays' size and returns True or False in accordance.

```python
import numpy
 
def ListExample(ListEx):
    return(numpy.array(ListEx))
 
 
# Driver Code
ListEx = []
if ListExample(ListEx).size:
    print("Not Empty")
else:
    print("Empty List")

```

**Output**:
```python
# Empty list
```

## Conclusion

As you can see, Python has a variety of methods for determining whether a list is empty. Additionally, using this condition before and then nesting your if or for loops is a good practice as it will help to minimize unintended errors. It all depends on your preference but the PEP 8 method is highly recommended as it usually pays off in performance.






