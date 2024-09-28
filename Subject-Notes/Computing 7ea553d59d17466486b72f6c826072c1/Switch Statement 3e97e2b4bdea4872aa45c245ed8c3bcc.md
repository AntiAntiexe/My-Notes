# Switch Statement

# C++ switch

- The `switch` statement is something that is unique to C++. It can be compare to how dictionaries work in Python.
- Switch structure:

```cpp
switch(expression) {
  case x:
    // code block
    break;
  case y:
    // code block
    break;
  default:
    // code block
}
```

- The value of the expression is compared with the values of each case.
- If there is a match with the expression and the cases, the associated block of code is executed.
- The  `switch` and `default` keywords are optional. However, if none of the cases match the expression then the default code block will be executed.

```cpp
char oper;

cout << "Enter an operator: ";
cin >> oper;

switch (oper) {
    case '+':
        cout << "Plus";
        break;
    case '-':
        cout << "Minus";
        break;
    case '*':
        cout << "Multiply";
        break;
    case '/':
        cout << "Divide";
        break;
    default:
        cout << "Unknown operator!";
}
```

```cpp
Enter an operator: /
Divide
```

- To test out the `default` keyword we can enter nothing and see what is outputs:

```cpp
Enter an operator: ^
Unknown operator!
```