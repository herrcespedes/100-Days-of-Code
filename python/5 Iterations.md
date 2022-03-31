# Python for Everybody : Elements of Python3

100 Days of Code *Day 3: 01/02/22*



#### Chapter 5: Iterations

[fcc bookmark](https://www.freecodecamp.org/learn/scientific-computing-with-python/python-for-everybody/loops-and-iterations)

loops have iteration variables that change each time through a loop. Often these iteration variables go through a sequence of numbers.

```flow
st=>start
op1=>operation: n=5
op2=>operation: print(n)
op3=>operation: n=n-1
op4=>operation: print('Blast Off')
cond1=>condition: n>0?
e=>end

st->op1->cond1
cond1(no, left)->op4->e
cond1(yes, bottom)->op2
op2->op3
op3(right)->cond1
```

```python
n = 5
while n > 0:
    print(n)
    n = n - 1
print('Blast Off')
```

in this case the iteration variable or *iteration counter* is **n**

#### Break and Continue

The **break** statement ends the current loop and jumps put to the statement immediately following the loop. 

```python
#ask for user input. if the user types 'done' the loop prints what the user typed and exits

while True:
    line = input()
    if line == 'done':
        break
	print(line)
print('Done')
```

The **continue** statement stops the iteration and restarts the loop.

```python
#ask for user input. if the user types 'any line beginning with #' the loop restarts and asks for line again, if the user types 'done', the loop prints what the user typed and exits

while True:
    line = input()
    if line[0] == '#':
        continue
	if line[0] == 'done':
        break
	print(line)
print('Done')
```

*Infinite loops* are errors in programming where a loop has no escape mechanism and the program locks up in the loop

while loops are indefinite loops

for loops are definite loops.

#### For Loop

[fcc bookmark](https://www.freecodecamp.org/learn/scientific-computing-with-python/python-for-everybody/iterations-definite-loops)

```flow
st=>start: start
cond1=>condition: Done?
op1=>operation: Move Ahead
op2=>operation: print('i')
op3=>operation: print('BlastOff')

st->cond1
cond1(yes, right)->op3
cond1(no, bottom)->op1->op2(left)->cond1

```



```python
for i in [5,4,3,2,1]:
    print(i)
print('Blastoff!')
```

Definite Loops are those that we know how many times it will repeat. It may iterate over elements in a list, or use an iteration counter to process the iterations. etc.

in the loop above, **i** is the iteration variable. 

- The **iteration variable** *iterates* through the sequence (ordered set)
- The **block** of code is executed once for each value in the sequence

#### Loop Idioms

loop idioms are patterns in which loops are grouped. this is the idea of how to analyze problems to make them *loopable*.  Some basic steps.

1. Set some variables to initial values

2. `for thing in data:` 

   Look for something or do something to each entry separately, updating a variable.

3. Look at the variables

> The trick is "knowing" something about the whole loop when you are stuck writing code that only sees one entry at a time

The exercise is given a sequence of numbers, find the largest. the excercise is to design an algorithm, which is a fancy way to say, process. to do this with a loop. now the loop cannot see all values at once, it can only see one value at a time... 

the solution is to create a variable called "largest value so far", initialize this variable to -1 and test every value against this variable. if the value is larger than the variable, then the variable takes this new value and keeps iterating. at the end of the loop, the variable will hold the value that tested the largest and the problem is solved.

```flow
st=>start: start
op1=>operation: largest =  -1  
op2=>operation: continue
op3=>operation: store x to largest
cond1=>condition: is x > largest?



st(right)->op1->cond1
cond1(no)->op2(right)->cond1
cond1(yes)->op3(left)->cond1
```

```python
largest = -1
for num in [9, 41, 52, 66, 2, 13]:
    if num > largest:
        largest = num
print(largest)
```

```python
#smart snippet for finding the smallest value. notice the use of None

smallest = None
print("Before:", smallest)
for itervar in [3, 41, 12, 9, 74, 15]:
    if smallest is None or itervar < smallest:
        smallest = itervar
        
    print("Loop:", itervar, smallest)
print("Smallest:", smallest)
```

> ==Value **None** indicates empty, nothing.==

count how many items in an array:

```python
count = 0
for value in [9, 18, 2, 43, 5, 13, 4]:
    count = count + 1
```

sum all the items in an array:

```python
sum = 0
for value in [9, 18, 2, 43. 5. 13. 4]:
    sum = sum + value
```

so if we have these two values we can calculate the average.

```python
count = 0
sum = 0
for value in [9, 18, 2, 43, 5, 13, 4]:
    count = count + 1
    sum = sum + value
avg = sum / count
print(avg)
```

[fcc bookmark scroll to min 16](https://www.freecodecamp.org/learn/scientific-computing-with-python/python-for-everybody/iterations-more-patterns)

#### "is" and "is not" Operators

**"is"** logical operator, similar to **==** but it is more strict

```python
0 == 0.0
>>> true
0 is 0.0
>>> false 

#this is so because == checks for value and is checks for all., in this case it returns false cause they are different types. 
```

**"is not"** works in the same but opposite way.

