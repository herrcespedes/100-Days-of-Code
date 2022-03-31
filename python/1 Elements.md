# Python for Everybody : Elements of Python3

100 Days of Code *Day 1: 12/31/21*

freecodecamp python for everybody course with Dr Charles Severance.

#### Chapter 1: Elements

**Reserved words** are words that have a specific meaning and cannot be used for other things than what python expects. Reserved words are.  ** there may be others*

|        |        |        |        |          |
| ------ | ------ | ------ | ------ | -------- |
| false  | class  | return | is     | finally  |
| None   | if     | for    | lambda | continue |
| true   | def    | from   | while  | nonlocal |
| and    | del    | global | not    | with     |
| as     | elif   | try    | or     | yield    |
| assert | else   | import | pass   |          |
| break  | except | in     | raise  |          |

**Formatted Sentences.** In python things look a certain way, and will only work if they are formatted in that certain way.

| Sentence                  | Meaning                           |
| ------------------------- | --------------------------------- |
| `x = 2`                   | assignment.                       |
| `x = x + 2`               | assignment with expression        |
| `print()`                 | Print statement (*function call*) |
| ```while x : x = x + 1``` | one line statements               |

**Python Scripts** .py text files that are run by python

#### Chapter 2: Constants and Variables

> A **variable** is a named place in the memory where the programmer can store data and later retrieve it using the variable "name"

> A **constant** is a piece of data that does and cannot change.

variable names must start with a letter or underscore. variable names are case sensitive.

![image-20211231133805540](G:\My Drive\100DaysofCode\images\image-20211231133805540.png)

*naming variables intelligently is important*

[fcc bookmark](https://www.freecodecamp.org/learn/scientific-computing-with-python/python-for-everybody/variables-expressions-and-statements)

------------

**Expressions** are sentences that are evaluated. e.g..  ` x = 2 + 3 `. expressions have operators just like in math:

| Operator | Operation         |
| -------- | ----------------- |
| +        | Addition          |
| -        | Subtraction       |
| *        | Multiplication    |
| /        | Division          |
| **       | Power             |
| %        | Reminder (Modulo) |

the operators follow standard rules of precedence. (parentheses, powers, multiplication and division, ahead of addition, and subtraction) when operations are found in the same level of precedence, they are done top to bottom and left to right.

-------------

**Data Types** are the type of data anything is. e.g.. integer, string, etc.. (I think these are classes)

| Category       | Types                        |
| -------------- | ---------------------------- |
| Text Types     | str                          |
| Numeric Types  | int, float, complex          |
| Sequence Types | list, tuple, range           |
| Mapping Type   | dict                         |
| Set Types      | set, frozenset               |
| Boolean Type   | Bool                         |
| Binary Types   | bytes, bytearray, memoryview |

ref: [pydoc ch3](https://docs.python.org/3/reference/datamodel.html#objects-values-and-types)

types have methods to them, and accept operators in expressions. for instance 

- int + int = adds the integers
- str + str = concatenates strings

`type(x)` inquires the type of the value held in the variable.

`int(x)` convers x from its original type, to the int type. 

- integer division produces floats 

`str(x)` converts x from its original type to string. e.g.. `str(4)` outputs an 4 with type integer. `str(this is a sentence)` raises an error

---

**INPUT**. User input can be gotten with the function input(). e.g..  *the function returns a string*

```python
name = input('Who are you?')
```

---

**Comments**. Comments are lines of code that are ignored by python. Denote a comment by adding a #
