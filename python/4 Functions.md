# Python for Everybody : Elements of Python3

100 Days of Code *Day 3: 01/02/22*

[fcc bookmark](https://www.freecodecamp.org/learn/scientific-computing-with-python/python-for-everybody/build-your-own-functions)

#### Chapter 4: Functions

Functions are a way to create reusable code. Functions are a little process that takes inputs, does something with it and gives you an output. functions can be written to do pretty much whatever you need them to do but they must be created (*defined*) and used (*called*)

#### Defining Functions

Functions are created with a **def** statement like so:

```python
def thing(argument1,argument2):
    print('Hello')
    print('World')
```

this def statement actually does not run in the program, but it gives python the recipe for the function.  when the function is *called*, the code nested in it will run.

==the name *thing* was assigned by us when we defined the function.==

statements like `print()` and other are actually functions, they're just prebuilt functions.

parts of a function:

```python
big = max('Hello World')
```

where:

`big` is the assignment.

`max` is the function name and 

`('hello world')` is the arguments. 

*def runs whenever*

#### Arguments

![image-20220102015126164](G:\My Drive\100DaysofCode\images\image-20220102015126164.png)

Arguments are values passed into the function as its input when we call the function. We use arguments to direct the function to do different work when we call it different times. Arguments are in parentheses after the name of the function.

when defining functions, arguments are called *parameters*. they serve as placeholders for the function later to access its arguments. 

```python
def greet(language):
    if language == 'spanish':
        print('Hola')
	elif language == 'french':
        print('Bonjour')
	else:
        print('Hello')
```

this function can be called and it will output the following:

```python
greet(spanish)
>>> Hola
greet(french)
>>> Bonjour
```

parameters/arguments can be more than one. they are just in order

```python
def addtwo(a, b):
    added = a + b
    return added
```



#### Return Values

The *Return* statement does two things:

- it stops the execution of the function
- specifies what is wanted as the result of running the function

> a *fruitful* function is one that produces a result (or return value)

the same script as before rewritten with the return function:

```python
def greet(language):
    if language == 'spanish':
        return 'Hola'
    elif language == 'french':
        return 'Bonjour'
    else:
        return 'Hello'
```

non fruitful functions or non return functions are called **void** functions. 

should I write a fun