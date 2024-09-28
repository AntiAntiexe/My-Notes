# lists and dictionaries

## **LISTS:**

Lists are ordered collections of elements, and each element can be of any data type.

Lists are **mutable,** meaning you can add, remove or modify elements.

Here is an example of lists:

```python
numbers = [1,2,3,4,5]
names = ["Alice","Bob","Charlie"]
numbers[1] = 20
numbers.insert(0,9)
numbers.append(55)
```

### MAIN example:

```python
shop_list = ["bananas", "bread", "milk", "eggs"]
shop_list.append("juice")
shop_list.remove("bread")
if "bananas" in shop_list:
	print("Bananas are on the shop list")
print("shop list:")
for item in shop_list:
print("- " + item)
```

- we use the **append** method to add “juice” off the list
- We use the r**emove** method to take “bread” off the list
- The **in** operator helps us check if  “bananas” are in the shopping list
- Finally, we display the complete shopping list using a **for** loop

**when to use lists:**

- lists are versatile and useful for storing sequences of elements when the order matters
- They are appropriate for scenarios where elements need to be added, removed, or modified frequently.

## Dictionaries/ Associative Array:

```python
student_grades = {"Alice":90, "Bob":85, "Charlie":78}
```

Dictionaries are collections of key-value pairs. Each key is associated with a value, and they allow quick access to element using their keys.

To create these key value pairs, the syntax should be **KEY : VALUE**

To retrieve the VALUE, we use the associated KEY rather than the index Eg.

```python
print(student_grades[”Alice”])
```

### MAIN example

```python
shop_list = {"bread":1, "apples": 3, "bananas": 5, "milk": 2, "eggs": 12}
shop_list["juice"] = 2
shop_list["bananas"] += 3
del shop_list["bread"]
if "bananas" in shop_list: 
    print("Bananas are on the shopping list.")  
    
print(shop_list["bananas"])
print(shop_list["juice"])
print(shop_list)
```

- In this example we create a dictionary called **shopping_list,** where each item is a key, and the quantity is the corresponding value.
- We add or update the items and their quantities using key-value pairs.
- The **del** statement is used to remove “bread” from the dictionary.
- Finally, we display the value through referencing the appropriate key

**When to use dictionaries / associative arrays**

- Dictionaries are ideal for scenarios where you need to retrieve values based on specific keys efficiently.
- They are commonly used for storing data with unique identifiers, like student names and corresponding grades.

### Linked list

- A linked list in Python is a way to organize data where each piece of information (node) holds some value and has a connection (pointer) to the next node.
- It’s like a chain of elements, and you can easily add or remove elements at the beginning, middle, or end of the chain. The last node points to None, indicating the end of the list
- This data structure is flexible and useful for dynamic data storage.

## Stacks

- A stack is a linear data structure that follows the Last-ln-First-Out (LIFO) principle.
- It is a collection of elements with two main operations: push and pop.
- The push operation placing something at the back of the stack
- The pop operation removes/retrieves the last element of the stack

### MAIN example:

```python
stack = [1,2,3,4,5]
stack.append(6)
stack.append(9)
stack.pop()
print(stack)
```

What will it print:

```python
[1, 2, 3, 4, 5, 6]
```

When to use: 

- Stacks are ideal for scenarios that involve backtracking, undo operations, or managing nests data structures
- They are commonly used in parsing expressions, depth-first search algorithms, and other algorithms that require a last-in-first-out approach

## Queues

- A queue is a linear data structure that follows the First-In-First-Out (FIFO) principle
- It is a collection of element where items are added at the rear (enqueue) and removed from the first (dequeue)
- The first element added to the queue will be the first one to be removed

### MAIN example

```python
queue = [1,2,3,4,5]
queue.append(6)
queue.pop(0)
queue.pop(0)
print (queue)
```

```python
[3, 4, 5, 6]
```

When to use Queues:

- Queues are suitable for tasks involving scheduling, order processing, or any scenario where elements need to be processed in the order they arrive
- Queues are useful with data processing reliant on maintaining it sequence.