# Python

## Introduction
### "Hello, world!" Program
Let's write our first python program. It's a simple one-liner that prints *'Hello, world!'* to the stdout (screen)

```python
print("Hello, world!")
```
```
Hello, world!
```

### Variables
A variable is a named location used to store data in the memory

#### Assigning value to a variable

```python
a = 2021
```
```a``` is a variable. We have assigned ```2021``` to variable ```a```

You can think of variables as a bag to store books in it and that book can be replaced at any time.

#### Changing the value of a variable
```python
a = 2021
print("a =", a)
# assigning a new value to a
a = "hello"
print("a =", a)
```
```
a = 2021
a = hello
```
Initially, integer value ```2021``` is assigned to the variable ```a```. Later, it was changed to string value ```hello```

#### Assigning multiple values to multiple variables

```python
a, b, c = 2021, 3.14, "hello"

print (a)
print (b)
print (c)
```
```
2021
3.14
hello
```

If we want to assign the same value to multiple variables at once, we can do this as:
```python
a = b = c = "same"

print (a)
print (b)
print (c)
```
```
same
same
same
```

### Constants

A constant is a type of variable whose value cannot be changed. It is helpful to think of constants as containers that hold information which cannot be changed later.

*In reality, Python doesn't have constants. Naming them in all capital letters is a convention to separate them from variables, however, it does not actually prevent reassignment.*

#### Declaring and assigning value to a constant

1. Create a ```constant.py```
```python
PI = 3.14
GRAVITY = 9.8
```
2. Edit ```main.py```
```python
import constant

print(constant.PI)
print(constant.GRAVITY)
```
```
3.14
9.8
```

### Operators

Operators are special symbols that carry out operations on operands (variables and values). Arithmetic operators are used to perform mathematical operations like addition, subtraction, multiplication etc.

| Operator |                                              Meaning                                             |  Example |
|:--------:|:------------------------------------------------------------------------------------------------:|:--------:|
|     +    |                                  Add two operands or unary plus                                  | x + y+ 2 |
|     -    |                        Subtract right operand from the left or unary minus                       | x - y- 2 |
|     *    |                                       Multiply two operands                                      |   x * y  |
|     /    |                 Divide left operand by the right one (always results into float)                 |   x / y  |
|     %    |                 Modulus - remainder of the division of left operand by the right                 |   x % y  |
|    //    | Floor division - division that results into whole number adjusted to the left in the number line |  x // y  |
| **       |                       Exponent - left operand raised to the power of right                       |   x**y   |

```python
x = 14
y = 4

# Add two operands
print('x + y =', x+y) # Output: x + y = 18

# Subtract right operand from the left
print('x - y =', x-y) # Output: x - y = 10

# Multiply two operands
print('x * y =', x*y) # Output: x * y = 56

# Divide left operand by the right one 
print('x / y =', x/y) # Output: x / y = 3.5

# Floor division (quotient)
print('x // y =', x//y) # Output: x // y = 3

# Remainder of the division of left operand by the right
print('x % y =', x%y) # Output: x % y = 2

# Left operand raised to the power of right (x^y)
print('x ** y =', x**y) # Output: x ** y = 38416
```

Assignment operators are used to assign values to variables. You have already seen the use of ```=``` operator. Let's try some more assignment operators
```python
x = 5

# x += 5 ----> x = x + 5
x +=5
print(x) # Output: 10

# x /= 5 ----> x = x / 5
x /= 5
print(x) # Output: 2.0
```

### User Input

In Python, you can use input() function to take input from user
```python
a = input('Enter your name:')
print('Your name:', a)
```
```
Enter your name: doublegrey
Your name: doublegrey
```

### Comments
```python
# This is a comment
```
```python
  """This is a 
    multiline
    comment."""
```
```python
  '''This is also a
     multiline
     comment.'''
```

### Type Conversion
The process of converting the value of one data type (integer, string, float, etc.) to another is called type conversion. Python has two types of type conversion

#### Implicit Type Conversion
Implicit conversion doesn't need any user involvement
```python
num_int = 123  # integer type
num_flo = 1.23 # float type

num_new = num_int + num_flo

print("Value of num_new:",num_new)
print("datatype of num_new:",type(num_new))
```
```
Value of num_new: 124.23
datatype of num_new: datatype of num_new: <class 'float'>
```
Here, num_new has float data type because Python always converts smaller data type to larger data type to avoid the loss of data

**Here is an example where Python interpreter cannot implicitly type convert**
```python
num_int = 123     # int type
num_str = "456"   # str type

print(num_int+num_str)
```
```
TypeError: unsupported operand type(s) for +: 'int' and 'str'
```
However, Python has a solution for this type of situation which is know as explicit conversion

#### Explicit Conversion
In case of explicit conversion, you convert the datatype of an object to the required data type. We use predefined functions like int(), float(), str() etc. to perform explicit type conversion
```python
num_int = 123  # int type
num_str = "456" # str type

# explicitly converted to int type
num_str = int(num_str) 

print(num_int+num_str)
```
```
576
```

### Data Structures

#### Lists
A list is created by placing all the items (elements) inside a square bracket ```[]``` separated by commas.

It can have any number of items and they may be of different types (integer, float, string etc.)
```python
# empty list
my_list = []

# list of integers
my_list = [1, 2, 3]

# list with mixed data types
my_list = [1, "Hello", 3.4]
```

```python
language = ["French", "German", "English", "Polish"]

# Accessing first element
print(language[0])


# Accessing fourth element
print(language[3])
```
```
French
Polish
```
You can use the index operator ```[]``` to access an item in a list. Index starts from 0. So, a list having 10 elements will have index from 0 to 9.

Python also allows negative indexing for its sequences. The index of -1 refers to the last item, -2 to the second last item and so on
```python
language = ["French", "German", "English", "Polish"]

print(language[-1])
print(language[-2])
```
```
Polish
English
```

The remove() method removes the first matching element (which is passed as an argument) from the list
```python
# create a list
prime_numbers = [2, 3, 5, 7, 9, 11]

# remove 9 from the list
prime_numbers.remove(9)


# Updated prime_numbers List
print('Updated List: ', prime_numbers)
```
```
 Updated List:  [2, 3, 5, 7, 11]
```

#### Tuples
Tuple is similar to a list except you cannot change elements of a tuple once it is defined. Whereas in a list, items can be modified.

Basically, list is mutable whereas tuple is immutable
```python
language = ("French", "German", "English", "Polish")

print(language[1])
print(language[3])
print(language[-1])
```
```
German
Polish
Polish
```

You cannot delete elements of a tuple, however, you can entirely delete a tuple itself using del operator
```python
language = ("French", "German", "English", "Polish")
del language

print(language)
```
```
NameError: name 'language' is not defined
```

#### String
```python
# all of the following are equivalent
my_string = 'Hello'
print(my_string)

my_string = "Hello"
print(my_string)

my_string = '''Hello'''
print(my_string)

# triple quotes string can extend multiple lines
my_string = """Hello, welcome to
           the world of Python"""
print(my_string)
```
You can access individual characters of a string using indexing (in a similar manner like lists and tuples)
```python
str = 'test!'
print('str = ', str)

print('str[0] = ', str[0])

print('str[-1] = ', str[-1])

print('str[1:5] = ', str[1:5])

print('str[3:-2] = ', str[5:-2])
```
```
str = test
str[0] = t
str[-1] = !
str[1:5] = est!
str[1:-2] = es
```

Strings are immutable. You cannot change elements of a string once it is assigned. However, you can assign one string to another. Also, you can delete the string using ```del``` operator.

Concatenation is probably the most common string operation. To concatenate strings, you use ```+``` operator. Similarly, the ```*``` operator can be used to repeat the string for a given number of times

```python
str1 = 'Hello '
str2 ='world!'

print(str1 + str2)

print(str1 * 3)
```
```
Hello world!
Hello Hello Hello
```

#### Sets
A set is an unordered collection of items where every element is unique (no duplicates)
```python
# set of integers
my_set = {1, 2, 3}
print(my_set)

# set of mixed datatypes
my_set = {1.0, "Hello", (1, 2, 3)}
print(my_set)
```
Sets are mutable. You can add, remove and delete elements of a set. However, you cannot replace one item of a set with another as they are unordered and indexing have no meaning

Let's try commonly used set methods: ```add()```, ```update()``` and ```remove()```
```python
# set of integers
my_set = {1, 2, 3}

my_set.add(4)
print(my_set) # Output: {1, 2, 3, 4}

my_set.add(2)
print(my_set) # Output: {1, 2, 3, 4}

my_set.update([3, 4, 5])
print(my_set) # Output: {1, 2, 3, 4, 5}

my_set.remove(4)
print(my_set) # Output: {1, 2, 3, 5}
```

```python
A = {1, 2, 3}
B = {2, 3, 4, 5}

# Equivalent to A.union(B) 
# Also equivalent to B.union(A)
print(A | B) # Output: {1, 2, 3, 4, 5}

# Equivalent to A.intersection(B)
# Also equivalent to B.intersection(A)
print (A & B) # Output: {2, 3}

# Set Difference
print (A - B) # Output: {1}

# Set Symmetric Difference
print(A ^ B)  # Output: {1, 4, 5}
```

#### Dictionaries
Dictionary is an unordered collection of items. While other compound data types have only value as an element, a dictionary has a ```key: value``` pair

```python
# empty dictionary
my_dict = {}

# dictionary with integer keys
my_dict = {1: 'apple', 2: 'ball'}

# dictionary with mixed keys
my_dict = {'name': 'John', 1: [2, 4, 3]}
```

Use key to access dict value
```python
person = {'name':'doublegrey', 'age': 19}
print(person['age']) # Output: 19
```

Here's how you can change, add or delete dictionary elements
```python
person = {'name':'doublegrey', 'age': 18}

person['age'] = 19 

person['profession'] = 'programmer'

del person['age']
```

#### range()
```range()``` returns an immutable sequence of numbers between the given start integer to the stop integer
```python
numbers = range(1, 6)
print(list(numbers)) # Output: [1, 2, 3, 4, 5]
```
```step``` parameter
```python
numbers = range(1, 6, 2)
print(list(numbers)) # Output: [1, 3, 5]
numbers = range(5, 0, -1)
print(list(numbers)) # Output: [5, 4, 3, 2, 1]
```

#### if/else
```python
num = -1

if num > 0:
    print("Positive number")
elif num == 0:
    print("Zero")
else:
    print("Negative number")
    
# Output: Negative number
```
There can be zero or more ```elif``` parts, and the ```else``` part is optional

#### while
```python
n = 100

sum = 0
i = 1

while i <= n:
    sum = sum + i
    i = i+1

print("The sum is", sum)

# Output: The sum is 5050
```

#### for
```for``` loop is used to iterate over a sequence (list, tuple, string) or other iterable objects

```python
numbers = [6, 5, 3, 8, 4, 2]

sum = 0

for val in numbers:
  sum = sum+val

print("The sum is", sum)

# Output: The sum is 28
```


#### break
The ```break``` statement terminates the loop containing it

```python
for val in "string":
    if val == "r":
        break
    print(val)

print("end")
```
```
s
t
end
```

#### continue
The ```continue``` statement is used to skip the rest of the code inside a loop for the current iteration only. Loop does not terminate but continues on with the next iteration

```python
for val in "string":
    if val == "r":
        continue
    print(val)

print("end")
```
```
s
t
i
n
g
end
```

#### Function
A function is a group of related statements that perform a specific task. You have to call the function to run the codes inside it
```python
def greet():
  print("hello, stranger")
  print("hello, user")
  
# function call
greet()
```
```
hello, stranger
hello, user
```
Function can accept arguments and return values
```python
def add_numbers(a, b):
  sum = a + b
  return sum

value = add_numbers(4, 5)
print(value)
# Output: 9
```
