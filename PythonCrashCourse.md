# Python Crash Course #

python crash course ( basic )

## Objectives ##

- Syntax
- Variables
- Data Types
- Numbers
- Strings
- Boolean Values
- Operations
- Loops
- Functions
- Classes

### Comments ###

```python
#this is a comment in python
```

### Variables ###

```python
x=10
#this is a variable
print(x)
#this will print out the variable x
```

### Changing the type of a variable once it is set ###

```python
x = str(10)
#this is a variable casted as a string using python casting. The variable x has been casted as a string of the value 10
print(x)
#will print out the string x to the console

y = int(3)
#this is a variable casted as a int
print(y)
#will print out the integer y to the console

z = float(3)
#this is a variable casted as a floa (floating point number, in C++ this is similar to a double or float cast)

print(z)
#will print out the decimal representation, printing out the float z to the console
```

### Single or Double Quotes ###

string varaibles can be declared using single or double quotes. Note that varaibles are case sensitive

```python
A="python"
a='variables'
print(A)
print(a)
#both are strings and will be outputted in the same way
```

### Data Types ###

Python builtin datatypes:

- str                 :: text
- int,float           :: numeric
- list, tuple, range  :: sequence
- bool                :: boolean types

How can you get the datatype

```python
x=5

print(type(x))
#this will print out the data type of the variable x, which is an integer
```

### Numbers ###

variables of numeric types are created when you define a value to them

```python
x=5
y=-5
#integers are either postive or negative, but cannot contain a decimal
z=3.5
a=1.5
#floating point numbers are decimal numbers both positve or negative
```

### Strings ###

```python
print("hello")
#this is a literal string
print('hello')
#this is also a literal string
```

#### Multi Lined Strings ###

```python
x = """You can create a multi line string using three quotation marks, When connected to a variable, it creates a value. Strings in python are arrays of multicharacters. You can use square brackets to traverse the string like an array
"""
print(x[0])
#will print out the character 'Y'
```

you can use the `len` function to print out the length of the string

```python
x = "this is a string of length 29"
print(len(x))
#will print out the length of the string stored within the variable x, which is a string of length 29 characters
```

### Booleans ###

Booleans represent either true or false (1/0). They are used to evaluate a conditional state of a variable. Generally a null boolean is false and a boolean with a value is true

```python
print(10 > 9) #true
print(10 == 9) # false
print(10 < 9) #false

x=bool("helloworld")
print(x) #will produce true

```

### Conditional ###

when running an if statement in python, it will evaluate to either true or false

```python
a = 100
b = 50
if b > a:
    print("b is greater than a")
else:
    print("a is greater than b")
```

if 0 is passed to a bool it will evalaute to false, if any other number is passed it will evaluate to true. The same applies to strings, if a string is an empty string it will evalute to false, if it contains values it will evaluate to true

```python
x=bool(1)#true
y=bool(0)#false

print(x)#will evaluate to true
print(y)#will evaluate to false

t=bool(True)#true
f=bool(False)#false

print(t)#will evaluate to true
print(f)#will evaluate to false
```

you can also use the `elif` keyword in order to add an additional if conditional following the initial one

```python
a = 100
b = 50
if b > a:
    print("b is greater than a")
elif b == a:
    print("b is equal to a")
else:
    print("a is greater than b")
```

### Operators ###

- `+` addition
- `-` subtraction
- `*` multiplication
- `%` modulus ( remainder division )
- `+=` addition assignmnet
- `-=` subtraction assignment
- `*=` multiplication assignment
- `%=` modulus assignment
- `=` assignment operation

#### Comparison Operations ####

- `==` comparison operation of equals
- `<=` less than or equal operation
- `>=` greater than or equal operation
- `>` greater than operation
- `<` less than operation

the assignment operations are the same as doing the following:

`x -= 4` is the same as `x = x - 4` and so forth for the remaining assignment operations

## Basic Built-in Data Structures ##

### Lists ###

lists are one of the built in data types of python, they are arrays of variables. They are created using the square brackets for arrays

```python
listA = ["apples", "bananas", "oranges"]
print(listA)
print(len(listA))#will print the length of the list which is 3
```

lists are indexed values ( an array ) and allow for multiple values

### Tuples ###

are used to store multiple types/items in 1 variable. It is a built in Data Type, and are used to store collections of data, immuttable. Note as mentioned the Tuple is unchangable once it has been defined

```python
this_tuple = ("apples", "bananas", "oranges")
one_tuple = ("apples",)#this is a single item tuple, it must end with a `,` in order to tell python it is a tuple

print(len(this_tuple))#will produce the length of 3
print(len(one_tuple))# will produce the length of 1
print(this_tuple)
print(this_tuple[0])#they are also indexed so this will produce the item 0 :"apples"

#tuples are similar to lists/arrays, but they are immutable
```

### Sets ###

are a built-in Data Type that contain multiple items in a variable, they are unordered and unindexed. Sets are written with `{}`, and CANNOT have duplicate values

```python
sets = {"a", "b", "c", "a"}#duplicate values will be ignored

print(len(sets)) #will produce the size of the set (3) - the duplicate
```

### Dictionary ###

are a built-in Data Type that are key value pairs, they may also be referred to as a map in other languages. In python 3.7+ they are ordred. They are stil changable and are defined also with curly brackets, but still do not accept duplicates. `key:value`

```python
my_dictionary = {
    "key1":"value1",
    "key2":"value2",
    "key3":3,
    "key4":4.5
}

print(my_dictionary)#will display the dictionary to the console

print(len(my_dictionary))#will produce the amount of pairs in the dictionary ( entries )
```

To reference a value in the dictionary insteead of using an index we use the key or keyname

```python
my_dictionary = {
    "key1":"value1",
    "key2":"value2",
    "key3":3,
    "key4":4.5
}

print(my_dictionary["key1"])#will produce the value "value1"
```

## Syntax ##

python relies on indentation, if the indentation is off in python you will get an indentation error and it might not compile. The indentation in python allows for the compiler to break the code into blocks more easiler in order to understand the code.

## Loops ##

a loop is used to do something multiple times or itterate through a list, dictionary, or set

### while loop ###

```python
i = 1 #this is the index variable

while i < 6:
    print(i)
    i += 1
#this will print 1 through 6

while i < 6:
    print(i)
    i+= 1
    if i == 5:
        break #this is a break statement that will break out of the loop when the condition is met, only printing 1 through 4


while i < 6:
    print(i)
    i+= 1
    if i == 4:
        continue # this is the opposite of the break statement, and in this set up of the loop won't do anything. The continue statement just says that if this condition is met, then continue to the next itteration of the loop. It can be used to skip an itteration if a certain condition is met.
    elif i == 5:
        break #this is a break statement that will break out of the loop when the condition is met, only printing 1 through 4

while i < 6:
    print(i)
    i+= 1
else:
    print("i is greater than 6")
# you can also use the else statement with a while loop to create an exit action for the loop
```

### For loops ###

are used for itterating a sequence as mentioned. Recall that strings are also sequences. `break` and `continue` can also be used in `for` loops

```python
fruits = ["apples", "bananas", "tomatoes"]

for x in fruits:
    print(x)#will print out every value of the sequence on a seperate line
else:
    print("I'm Done")
```

for loops cannot itterate over empty sequences. But if you put in a `pass` statement it can avoid an error

## Functions ##

functions can be called for later use

```python
def function_a():
    print("hello I am a function")

function_a()# will print out "hello I am a function"
```

functions can also take arguments. They are passed if parameters are defined. An argument is the actual value passed, a parameter is the placeholder in the definition of the function. As seen above, a function is defined using a `def` keyword

```python
def name(myName):
    print(myName)

name("This is my Name")
#will print out "this is my Name"

def storeNameAsTuple(myName)
    return (myName,)

#this will return your name as a tuple

print(storeNameAsTuple("someOne"))
#this will print the function return output to the console, therefore printing the tuple to the console

```

you need to call the function with the correct number of arguments in it. If you call a function without the correct number of arguments then you will recieve a type error. The name and the number of arguments of the function is called the function signature. A function with different number of parameters but the same name is called an overloaded function. This allows you to do various tasks depending on the number of parameters passed. You can also set a default argument to a parameter by using the assignment operator `=` in the parameter definition.

```python
def defaultFunction(param1 = None):
    if param1 is not None:
        print(param1)
    else:
        print("no arguments were passed")
```

## Objects ##

python is an OOP language, meaning it is an object oriented language. It uses objects to classify things and run them accordingly, comapred to sequential langauge that will render the program based on the order they are listed. This can be more complicated to understand for some.

A class is a blueprint for creating objects. When a class is `instantiated` it is used to create an object from that class. A class generally has a constructor that is called when the object is instatiated. When a constructor of a class is called it is said to be `initializing` the class object with a certain set of variable. Initialization is intializing the variables of an object, this occurs when you defined a variable.

## Classes ##

Classes are created using the keyword `class`

```python
class MyClass():
    x = 5 #this is the initialization of the variable x within the class

new = MyClass() #this is instatiating the class object 'new'

print(new.x)#and this will print out the value stored in x in the class
```

this is a basic example of a class in python

## Non-Built-in Data structures ##

One of my favorite data structures is the linked list. It is a little more complicated to understand. It uses entries called nodes, which contain data and a pointer. A pointer is a variable that points to the next node in the list. The first node in a linked list is called the root node. Some may refer to it as the 'head' node instead, since it is the head of the list. The reference of 'head' node comes from another more advanced data structure called a tree, which has various flavors, such as a B-Tree, Binary Tree, or a heap.

The link List node is structured with generally two types. A data section and a pointer section to the next node. A linked list with two pointers, one pointing forward and one pointing back is known as a double linked list. If the last node of the list points to the first node in the list, it is known as circular linked list.

In a regular linked list, the last node will point to null, or in python `None`

```python
class Node(object):
    def __init__(self, dat, nod = None ):
        #this is a constructor, the first value is self, the second is the data in the node, and the last parameter is an optional parameter which points to the next value of the list
        self.data = dat
        self.next_node = nod
    
    #precondition: The list is not empty
    #postcondition: returns the next node in the list
    def get_next (self):
        return self.next_node
    #precondition: Takes the argument nod which is an object of type Node, pointing to the next node in the list
    #postcondition: Sets the current Node object ( self ) to have the next_node of nod
    def set_next (self, nod):
        self.next_node = nod
    #precondition: None
    #postcondition: Returns the data stored in the Node
    def get_data (self):
        return self.data
    
    #precondition: Takes the argument dat which is the data to be stored in the list
    #postcondition: Sets the current Node object ( self ) to have the data of dat
    def set_data (self, dat):
        self.data = dat

class LinkedList(object):
    def __init__(self, rt = None):
        self.root = rt
        self.size = 0
    #initializes the root to rt and the size to 0
    #precondition:
    #postcondition:
    def get_size (self):
        return self.size
    def add (self, dat):
        new_node = Node(dat, self.root)
        self.root = new_node
        self.size += 1
    def remove (self, dat):
        this_node = self.root
        prev_node = None
        while this_node:
            if this_node.get_data() == dat:
                if prev_node:
                    prev_node.set_next(this_node.get_next())
                else:
                    self.root = this_node
                self.size -= 1
                return True #data is removed
            else:
                prev_node = this_node
                this_node = this_node.get_next()
        return False #data is not removed succesfully
    def find (self, dat):
        this_node = self.root
        while this_node:
            if this_node.get_data() == dat:
                return dat
            else:
                this_node = this_node.get_next()
        return None

myList = LinkedList()
myList.add(5)
myList.add(8)
myList.add(12)
myList.add("st")
print("size before removing a node")
print(myList.get_size())
myList.remove(8)
print("Is 12 in the list?")
print(myList.find(12))
print("size after removing a node")
print(myList.get_size())

```