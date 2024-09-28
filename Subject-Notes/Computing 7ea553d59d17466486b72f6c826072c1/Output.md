# Output

# Output (Print text)

- In C++ the  `cout` object is together with the `<<` operator, to print out values:

```cpp
#include <iostream>
using namespace std;

int main() {
  cout << "Hello World!";
  return 0;
}
```

```powershell
Hello World!
```

# Displaying Variables

- You can display variables using `cout` and use `<<` to separate them:

```cpp
int myAge = 15;

cout << "I am " << myAge << " years old.";
```

```powershell
I am 15 years old.
```