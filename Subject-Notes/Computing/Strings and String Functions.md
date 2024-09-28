# Strings and String Functions

# Strings in C++

- To use string you must include an additional library header file in the source code, the `<string>` library:

```cpp
#include <string>
```

# String Concatenation

- The `+` operator can be used between strings to add them together to make a new string. This is called concatenation:

```cpp
string firstName = "John ";
string lastName = "Doe";
string fullName = firstName + lastName;
cout << fullName;
```

```powershell
John Doe
```

- We can also add a space by adding a space with quotes:

```cpp
string firstName = "John";
string lastName = "Doe";
string fullName = firstName + " " + lastName;
cout << fullName;
```

```cpp
John Doe
```

# Append

- You can also concatenate strings using the `append()` function:

```cpp
string firstName = "John ";
string lastName = "Doe";
string fullName = firstName.append(lastName);
cout << fullName;
```

```cpp
John Doe
```

# String Length

- To get the length of a string we can use the `length()` function:

```cpp
string txt = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
cout << "The length of the txt string is: " << txt.length();
```

```cpp
The length of the txt string is: 26
```

- You might see in some C++ programs that use the `size()` function to get the length. This is just an alias of `length()`.

# Access Strings

- You can access characters in a string by referring to its index number inside square brackets `[]`.

```cpp
string myString = "Hello";
cout << myString[0];
```

```cpp
H
```

- Strings indexes start with 0: `[0]` is the first character. `[1]` is the second character and so on.
- To print the last character of a string:

```cpp
string myString = "Hello";
cout << myString[myString.length() - 1];
```

```cpp
o
```

# Change String Characters

- To change the value of a specific character in a string, refer to the index number and use single quotes:

```cpp
string myString = "Hello";
myString[0] = 'J';
cout << myString;
```

```cpp
Jello
```

# The `at()` function

- All this can also be done with the at function:

```cpp
string myString = "Hello";
cout << myString; // Outputs Hello

cout << myString.at(0);  // First character
cout << myString.at(1);  // Second character
cout << myString.at(myString.length() - 1);  // Last character

myString.at(0) = 'J';
cout << myString;  // Outputs Jello
```

# User Input wit Strings

- cin considers a space (whitespace, tabs, etc) as a terminating character, which means that is can only store a single word:

```cpp
string fullName;
cout << "Type your full name: ";
cin >> fullName;
cout << "Your name is: " << fullName;
```

```cpp
Type your full name: John Doe
Your name is: John
```

- This is why when working with strings we often use the `getline()` function to read a line of text. It takes `cin` as the first parameter, and the string variable as a second:

```cpp
string fullName;
cout << "Type your full name: ";
getline (cin, fullName);
cout << "Your name is: " << fullName;
```

```cpp
Type your full name: John Doe
Your name is: John Doe
```