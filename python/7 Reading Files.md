# Python for Everybody : Elements of Python3

100 Days of Code *Day 4: 01/08/22*

#### Chapter 7: Reading Files

[fcc bookmark](https://www.freecodecamp.org/learn/scientific-computing-with-python/python-for-everybody/files-as-a-sequence)

Files can be thought as a sequence of lines, 

files need to be opened to be operated on with the function **open()**

files can be read line by line in a for loop 

```python
fhand = open('mbox.txt')
for line in fhand:			# iterate thru every line
    print(line)  			# process the line
```

we can also read every character

```python
fhand = open('mbox.txt')
inp = fhand.read()			# r
print(len(inp))				# print how many characters are held in imp
```

