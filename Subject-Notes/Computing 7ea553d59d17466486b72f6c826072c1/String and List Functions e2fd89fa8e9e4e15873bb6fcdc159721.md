# String and List Functions

# .upper()

- .upper() will turn all the letters in your string into upper case

```python
x = 'kael'
x = x.upper()
print(x)
```

```python
KAEL
```

# .lower()

- .lower() does the opposite thing of .upper(), it just makes all letters lowercase

```python
x = 'KAEL'
x = x.lower()
print(x)
```

```python
kael
```

# .split()

- .split() will create a list of everything that is separate by a space:

```python
data = input("subjects: ")
subjects = data.split()
print(subjects)
```

```python
subjects: #english math science foodtech
['english', 'math', 'science', 'foodtech']
```

- this could also be shown in a for loop

```python
data = input("subjects: ")
subjects = data.split()
for i in subjects:
  print(i)
```

```python
subjects: #english math science foodtech
english
math
science
foodtech
```

# .append()

- .append() adds another item to the end of a list

```python
pets = ['dog', 'mouse', 'lion']
pets.append('kael')
print(pets)
```

```python
['dog', 'mouse', 'lion', 'kael']
```

# .sort()

- .sort() sorts the items in a list in alphabetical order if string or ascending order if number

```python
pets = ['dog', 'mouse', 'lion', 'kael']
pets.sort()
print(pets)
```

```python
['dog', 'kael', 'lion', 'mouse']
```

# .reverse()

- .reverse() goes through the list backwards starting from the last item

```python
pets = ['dog', 'mouse', 'lion', 'kael']
pets.reverse()
print(pets)

```

```python
['kael', 'lion', 'mouse', 'dog'] 
```

# .join()

- basically the opposite of .split() so it joins everything back

```python
x = input("kael wants ur letters ")
x = x.split()
print("".join(x))
```

```python
kael wants ur letters #a s d f g h
asdfgh
# basically
# print([what u want to seperate ur list with].join([variable including list]))
```

# .insert

```python

```

# .pop

- The pop() method **removes the last element from an array and returns that value to the caller**.
- when .pop() is written the last number of the list is removed

Example:

```python
my_list = [1, 2, 3]
item = my_list.pop(1)
print(item)
print(my_list)
```

output:

```python
2
[1, 3]
```