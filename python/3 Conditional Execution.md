# Python for Everybody : Elements of Python3

100 Days of Code *Day 2: 01/01/22*

#### Chapter 3: Conditional Execution

#### Conditional Steps

[fcc Bookmark](https://www.freecodecamp.org/learn/scientific-computing-with-python/python-for-everybody/conditional-execution)

Conditional Steps control flow by branching.

```flow
op1=>operation: x=5
op2=>operation: print('Smaller')
op3=>operation: print('Bigger')
op4=>operation: print('Finis')

cond1=>condition: x < 10?
cond2=>condition: x > 20?

op1->cond1
cond1(yes)->op2
cond1(no)->cond2
op2->cond2
cond2(yes)->op3
cond2(no)->op4
op3->op4

```

this code translates to:

```python
x = 5
if x < 10:
    print('Smaller')
if x > 20:
    print('Bigger')
print('Finis')
```

if statements test the expression. if the expression tests true, the code indented runs. Otherwise the code indented is ignored.

#### Boolean Operators

Boolean expression operators:

| Operator | Meaning                  |
| -------- | ------------------------ |
| <        | Less Than                |
| <=       | Less than or equal to    |
| ==       | Equal to                 |
| >=       | Greater than or equal to |
| >        | Greater than             |
| !=       | Not equal to             |



---

**NOTE**

`=` is different from `==`  . The first is used for assignment, the latter for testing expressions.

---



#### Indentation

```python
if 0 == x:
    if y == 10:
        print("Yes")
```

Python uses indentation to define the program flow, where other languages use curly braces. Indentations mark the "ownership" of code. this is called **nesting**. For instance an if statement uses the indented text to run if the condition tests true.

Indentation should be 4 spaces. no tabs. ==Some IDEs allow for the automatic substitution of tabs for spaces.== the reason not to indent with tabs is that it is unreliable and errors might raise

---

**==WARNING==**

do not indent with tabs, but use 4 spaces

---

#### Nested decisions: If Else

![image-20220101040528883](G:\My Drive\100DaysofCode\images\image-20220101040528883.png)

```python
x = 42
if x > 1:
    print('More than One')
    if x < 100:
        print('Less than 100')
print('All Done')
```



two+ way decisions are done with the else with the **else** statement:

```flow
op1=>operation: x=4
op2=>operation: print('Not Bigger')
op3=>operation: print('Bigger')
op4=>operation: print('All Done')
cond1=>condition: x>2

op1->cond1
cond1(yes, right)->op3
cond1(no, left)->op2
op2->op4
op3->op4

```

```python
x = 4
if x>2:
    print('Bigger')
else:
    print('Not Bigger')
print('All Done')
```



Multiway decisions are done with the **elif** statement:

```flow
cond1=>condition: x<2
cond2=>condition: x<10
op1=>operation: print('small')
op2=>operation: print('medium')
op3=>operation: print('large')
op4=>operation: print('All Done')

cond1(yes, right)->op1
cond1(no)->cond2
cond2(yes, right)->op2
cond2(no)->op3
op3->op4
op1->op4
op2->op4
```

```python
if x < 2:
    print('small')
elif x < 10:
    print('medium')
else:
    print('large')
print('All Done')
```



#### Try .. Except

this structure is used to catch exceptions. if the code in the *try* throws an exception, the *except* code runs.

*exceptions, tracebacks and errors are all the same*

```python
# When the conversion fails, it just drops to the except
# and the variable is assigned -1 (which by convention means error)
# the program continues. does not crash.

str = 'Hello Bob'
try:
    istr = int(str)
except:
    istr = -1
print('First', istr)
```



