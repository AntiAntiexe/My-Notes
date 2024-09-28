# For Loops and While Loops

- For loops are used to iterate over an **iterable** object. An iterable object can be many different things. Lists are a great example and are most commonly used.

```python
list = [1,2,3,4,5]
for i in list:
  print(i)
```

```python
1
2
3
4
5
```

# Using range() with for loops

- using range() through number will start from 0 then move onwards

```python
for i in range(5)
print(i)
```

```python
0
1
2
3

```

- now if you want to start at 1 then:

```python
for i in range(1,5)
print(i)
```

```python
1
2
3
4
```

- now if you want to count down from 5:

```python
for i in range(5,0,-1)
print(i)
```

```python
5
4
3
2
1
```

- You can iterate through a range of numbers using range()

```python
for i in range(4):
	  print("Hello")

```

```python
Hello
Hello
Hello
Hello
```

- range() also counts from 0 onwards

```python
for i in range(4):
	  print(i)
```

```python
0
1
2
3
```

- However, after every line it starts a new line. If you want to put all of it into 1 line then:

```python
x = ""
for i in range(4):
	  x += str(i)
print(x)
```

```python
0123
```

- Now say you want to add all these numbers up, by changing *x = “”*  to *x = int(0*) it basically adds a empty equation to add all these things up to, like *“”*  acts as an empty string.

```python
x = int(0)
for i in range(4):
  x += int(i)
print(x)
#output:
6
```

# Using range() and len()

The len() function , short form for length, finds the length of an iterable

```python
message = "hello"
print(len(message))
```

```python
5
```

- You can iterate through any iterable object such as lists

```python
message = "kael"
for i in range(len(message)):
  print("Hello")
```

```python
Hello
Hello
Hello
Hello
```

```python
message = "kael"
for i in range(len(message)):
  print(i)
```

```python
0
1
2
3
```

# While loops

- While loops allow to execute a block of code as long as a condition is true.
- It will only terminate once the condition becomes false

# While loops setup

```python
#EXAMPLE
count = 0
while count < 6:
  count += 1
  print(count)
```

```python
1
2
3
4
5
```

- when using a while loop, you need a loop initialisation to get the user into the while loop, in this case our loop initialisation is:

```python
count = 0
```

- now we need to termination condition  so that we can get in and out of the while loop, our termination condition in this case is:

```python
while count < 6:
```

- the body of code inside of the while loop is now running and in this case the thing running is:

```python
print(count)
```

- as well as a changing the variable in the initialisation loop so then it doesn’t run infinite times, in this case:

```python
count += 1
```

# While loop with string

- now when wanting to use with string:

```python
word = input("Favourite food: ")
while word != "potato":
  print("pick a better food")
  word = input("new favourite food: ")
print("good choice!")
```

```python
Favourite food: #carrots
pick a better food
new favourite food: #potato
good choic
```

- now say you wanted to say that chicken and potato were good choices, then:

```python
x = 'wrong'
while x == 'wrong':
  f = input("Favorite food: ")
  if f == "chicken" or f == "potato":
    x = 'right'
    print("good choice")
  else:
    print("pick a better food")
```

```python
Favourite food: #fish
pick a better food #chicken
good choice
```

```python
Favourite food: #fish
pick a better food #potato
good choice
```