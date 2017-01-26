# Solum Style Guide
This guide describes how code, documentation, and resources should be formatted for inclusion in Solum.

## Motivation
Having a consistent style throughout the project makes it easier to maintain, as well as making it easier for new developers to become accustomed to working with the code.

# Code Guidelines
The following guidelines refer to the standards of code found in Solum.

## Naming

### Schemes
- **CamelCase** refers to names that start with an uppercase letter and has an uppercase letter for each new word.
- **lowerCamelCase** refers to names that start with a lowercase letter and has an uppercase letter for each new word.
- **snake_case** refers to names that are fully comprised of lowercase letters and has words separated with an underscore.
- **UPPER_SNAKE_CASE** refers to names that are fully comprised of uppercase letters and has words separated with an underscore.
- **Camel_Snake_Case** refers to names that start with an uppercase letter and has an uppercase letter for each new word, as well as having words separated with an underscore.
- **prefixed_CamelCase** refers to names that start with a lowercase prefix and an underscore, then proceeds to have an uppercase letter for each new word.

### Namespaces
Namespaces are formatted as **CamelCase**.

### Files and Folders
Files are formatted as **CamelCase**. If a file implements a majority of a class, name it after the class. If a file implements a single function, name it after that function.

### Classes
Classes are formated as **CamelCase**. If a class contains an acronym, brand, or proper noun, it should be spelled as such.

Example:
```cpp
class SwapChain; // Named for 'Swap Chain'.
class OpenGLRenderer; // Named for 'OpenGL Renderer'.
```

### Functions
Functions are formatted as **CamelCase**, with arguments formatted as **lowerCamelCase**.

Example:
```cpp
auto ExampleMethod(char myLetter, int argument) -> int;
```

Member functions in a class should be named in an imperative tone, meaning that they should be named after direct commands.

Example:
```cpp
auto Open() -> bool;
auto SendNumber(int number) -> bool;
```

A way to think about the above scenario is that classes are nouns, and member functions are verbs.

### Variables
In general, variables are formatted as **lowerCamelCase**. Variable names should be descriptive, but should not be exceedingly verbose. Variable names should not be cryptic.

Example:
```cpp
int lastCommand; // Good
int lastCommandThatWasIssued; // Not so good
int lastCommandThatWasIssuedByRendererInContext; // Bad
int lCmdI; // Bad
```

Variable names for iterators and loop variables can be short, as they are commonly expressed as such.

Example:
```cpp
int i; // Ok, outer loop
int j; // Ok, inner loop
std::vector<int>::iterator iter; // Ok
```

##### Constants
Constants should be declared as either **Camel_Snake_Case** or **UPPER_SNAKE_CASE**, depending on the context.
- **UPPER_SNAKE_CASE** is used for global constants.
- **Camel_Snake_Case** is used for local constants or enumation constants.

##### Member Variables
Variables that are members of a class are declared as either **prefixed_CamelCase** or **CamelCase**, depending on the context.
- **prefixed_CamelCase** is used for class member variables.
- **CamelCase** is used for struct member variables.

##### Global Variables
Global variables should never be used. If a global variable becomes necessary, rethink your design and refactor code to make it unnecessary.

## Formatting
Your text editor or IDE should be able to handle most of the formatting tasks presented here.

### New Lines
##### Braces
- The opening bracket should be placed on the line of the previous statement.
- The closing bracket should be placed on its own line.
- Single line statements do not need braces.

Example:
```cpp
auto main(int argc, char** argv) -> int {
	for (int i = 0; i < 100; i++) {
		if (i == 87) continue;
		std::cout << "Woo: " << i << std::endl;
	}
}
```

##### Else and Catch
Both the `else` and `catch` statements should go on their own lines.
Example:
```cpp
try {
	// Do Stuff
}
catch (const std::exception& e) {
	// Deal With Stuff
}

if (i == 38) {
	// Do Stuff
}
else if (i == 14) {
	// Do Other Stuff
}
else {
	// Do Some Other Stuff
}
```

### Indentation
Each block should be indented by a single tab character per indent level. Spaces can be used to align characters within a line so they always line up regardless of tab size.

Example:
```cpp
auto main(int argc, char** argv) -> int {
	// Single Tab in!
	BigFunction("Hello, World", "Goodbye, World", "Solum is the best library!",
	            42, 8675309); // This is aligned using spaces.
}
```

### Line Length
The maximum line length is 120 characters, however the recommended line length is 80 characters.

### Header Guards
The header guard statement `#pragma once` should be in every header file immediately after the top comments and before any code.

## Functions
Functions should be declared using the [trailing return type](https://cppstyle.wordpress.com/trailing-return-type/) syntax. This allows us to use deduced return types when necessary while still keeping a consistent style.

Example:
```cpp
int FunctionA(); // Bad
auto FunctionB() -> int; // Good

template <typename T1, typename T2>
auto FunctionC(T1 lhs, T2 rhs) -> decltype(T1 * T2);
```

### Arguments
- Modifiable arguments are passed by pointer.
- Constant arguments are passed by reference or value.
	- References are used when the object would be expensive to copy.
	- Values are used otherwise.

## Namespaces
Namespaces should not be directly imported with the `using` statement. Rather, individual classes should be imported (and preferrably aliased). The `using` keyword should not be used in headers unless they are found internally in class definitions.

Example:
```cpp
using namespace std; // Bad
using std::list; // Fine

template <typename T>
using List = std::list<T>; // Good

class MyClass {
public:
	using List = std::list<MyClass>; // Good
};
```

## Classes
Classes are used for defining objects.

### Inheritance
- Classes should only inherit from a single class that has data.
- It may inherit from multiple abstract classes.

## Structs
Structs should be used only for *POD* (Plain Old Data) types.
- They should not contain any functions
	- This includes constructors and destructors.
- They should not be inherited from.

## Enumerations
- Standard C enumerations should be avoided.
	- Use C++'s `enum class` instead.