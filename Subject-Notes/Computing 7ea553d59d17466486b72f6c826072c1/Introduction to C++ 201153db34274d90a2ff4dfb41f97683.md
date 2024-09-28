# Introduction to C++

# Syntax

- Before we get into anything too complicated we will first have a look at an example piece of code to understand the syntax.

```cpp
#include <iostream>
using namespace std;

int main() {
  cout << "Hello World!";
  return 0;
}
```

- Line 1:

```cpp
#include <iostream>
```

- Line 2:

```cpp
using namespace std;
```

- Don't worry if you don't understand how `#include <iostream>` and `using namespace std` works. Just think of it as something that (almost) always appears in your program.
- Line 4:

```cpp
int main() {
```

- Line 5:

```cpp
cout << "Hello World!";
```

- Line 6:

```cpp
return 0;
```

# Omitting Namespace

- You don’t need to have the `using namespace std` line. It can be removed but then you must use the `std` keyword, followed by the `::` operator for some objects:

```cpp
#include <iostream>

int main() {
  std::cout << "Hello World!";
  return 0;
}
```