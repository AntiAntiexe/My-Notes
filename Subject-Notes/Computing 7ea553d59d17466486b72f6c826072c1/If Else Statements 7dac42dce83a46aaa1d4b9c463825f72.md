# If Else Statements

- If/else statements are essential building blocks in programming that allow you to make decisions and controls the flow of your code.
- They enable your program to execute different blocks of codes based on certain condition. in simple terms, it's like making choices in real life.

# **Comparison operators to create conditions:**

- >(greater than)
- <(less than)
- >=(greater than or equal to)
- <=(less than or equal to)
- == (equal to)
- !=(not equal to)

### equation

- % finds the remainder of a fraction

## **Logical Operators:**

- They are used to combine multiple conditions together. There are 3 main logical operators in python.
    - and: Returns True if both conditions on either side of the operator are true
    - or: returns True if at least one of conditions on either side of the operator is true
    - not: returns the opposite of the condition after the operation

## Basic Syntax

```python
if (condition):
		# Code block to be executed if the conditions is true
else:
		# Code block to be executed if the conditions are false
```

- We need to remember our indents. If you want something to run in the "if" code block, we indent right after the colon.
- To exit the code block, move the indent back to match the starting statement of the code block.

The if keyword is used to start the if/else statement followed by the condition

If the condition evaluated to True, the code block under the if statement will be executed

If the condition is False, The code block under the else statement will be executed.

## Nested if and else statements

- We can also use multiple if/else statements together, creating what is known as "nested" if/else statements
- Use nested if/else statements when we need to evaluate multiple condition and perform different actions based on those conditions.
- Nested if/else statements are particularly useful when we need to consider various scenarios and outcomes.
- This allows you to handle more complex decisions-making situations.

```python
if condition 1:
		# Code block to be executed if condition 1 is true
		if condition 2:
				# Code block to be executed if both condition 1 and condition 2is true
		else:
				# Code block to be executed if condition 1 is true but 2 is false
else:
		# Code block to be executed if condition 1 is false
```

**Elif (Else if)**

- In python elif is short for "else if". It is a keyword used in conditional statements to check multiple conditions one after another.
- When the if condition is not met, elif allows you to specify an additional condition to be checked without having to restate another if statement.

```python
if condition 1:
		# code block to be executed if condition 1 is true
elif condition 2:
		# code block to be executed if condition 1 is false and 2 is true
else:
		# code block to be executed if both condition 1 and 2 are false.
```

- You should use elif is when the condition is mutually exclusive. E.g.
    
    ```python
    age = input("Enter your age: ")
    if age > 65:
    		print(age)
    elif age > 35:
    		print(age)
    elif age > 16:
    		print(age)
    else:
    		print("Unknown")
    ```
    

# Logical operators

- These are used to combine multiple conditions together. There are 3 main logical operators in python

## and

- Returns true if both conditions on either side of the operator are true

```python
x = 5
if x >= 3 and x <= 6:
  print("kael")
#output:
kael
```

```python
kael
```

## or

- returns true if at least on of the conditions on either side of the operator is true

```python
x = 6
if x == 3 or x == 6:
  print("kael")
```

```python
kael
```

## not

- in the “if” statements and is used if it is not in there example:

```python
li = ["a", "b", " c"]

if "F" not in li:
    print("it is in")
```

```python
it is in
```