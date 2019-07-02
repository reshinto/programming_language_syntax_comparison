# PROGRAMMING LANGUAGE SYNTAX
## Interpreted Language
* python, javascript
## Compiled Language
* java, c++
## Hello World
### python 2
```python
    print "Hello World"
```
### python 3
```python
    print("Hello World")
```
### javascript
```javascript
    console.log("Hello World");
```
### java
```java
    public class HelloWorld {
        public static void main(String args[]) {
            System.out.println("Hello World");
        }
    }
```
### c++
```c++
    #include <iostream>

    int main() 
    {
        std::cout << "Hello, World!";
        return 0;
    }
```
## Comments
### python 2 & 3
* single line
```python
    # Single line comment
```
* multiline
```python
    """
    multi-line comments
    """
```
### javascript
* single line
```javascript
    // Single line comment
```
* multiline
```javascript
    /*
    multi-line comments
    */
```
### java
* single line
```java
    // Single line comment
```
* multiline
```java
    /*
    multi-line comments
    */
```
### c++
* single line
```c++
    // Single line comment
```
* multiline
```c++
    /*
    multi-line comments
    */
```
## Variable declaration: integer ...-2, -1, 0, 1, 2...
### python 2 
#### int: -2147483648 ~ 2147483647
* integer_name = 123
#### long: -9223372036854775808L ~ 9223372036854775807L
* long_name = 123L  # int beyond int size will automatically be converted to long
### python 3: int and long are combined into int
* integer_name = 123
### javascript ES5
* var integer_name; integer_name = 123;  // accessible within the function
* var integer_name = 123;
### javascript ES6
* let integer_name; integer_name = 123;  // accessible only within the block {}
* let integer_name = 123;
* const integer_name = 123;  // variable value cannot be reassigned
### java
* public/private/protected static final byte/short/int/long integer_name = 123;
    * public: visible to all classes
    * protected: visible to class they belong and any subclasses
    * private (most restricted): visible only to class they belong
    * static: can be accessed without creating a class instance
    * final: constant value, value cannot be changed
#### byte: -128 ~ 127, 8 bits
* byte byte_name = 123;
#### short: -32768 ~ 32767, 16 bits
* short short_name = 123;
#### int: -2147483648 ~ 2147483647, -2_147_483_648 ~ 2_147_483_647, 32 bits
* int integer_name; integer_name = 123;
* int integer_name = 123;  // default is visible within the same package
#### long: -9223372036854775808L ~ 9223372036854775807L, can use _ same as int, 64 bits
* long long_name = 123l;
* long long_name = 123L;
### c++
* const unsigned char/short/int/long/long long integer_name = 123;
    * const: constant value, value cannot be changed
    * integer are signed by default: can assign both positive & negative values
    * unsigned integer (use when dealing with bit values): 0 ~ ...
        * e.g. char: -128 ~ 127
        * e.g. unsigned char: 0 ~ 255  // 128 + 127 = 255
#### char: 1 byte, -128 ~ 127, use C code to print "#include＜stdio.h＞ printf("%d", char_name);"
* char char_name; char_name = 123;
* similar to the rest of int variable declaration
#### short/short int: 16 bits, 2 bytes, -32768 ~ 32767
* short short_name; short_name = 123;
* short int short_name; short_name = 123;
* similar to the rest of int variable declaration
#### int: 16 bits, 4 bytes, -2147483648 ~ 2147483647
* int integer_name; integer_name = 123;  // uninitialized
* int integer_name = 123;  // C-like initialization
* int integer_name (123);  // Constructor initialization
* int age {123};  // C++11 list initialization syntax
#### long/long int: 32 bits, 4 bytes, -2147483648 ~ 2147483647 bytes
* long long_name; long_name = 123;
* long int long_name; long_name = 123;
* similar to the rest of int variable declaration
#### long long/long long int: 64 bits, 8 bytes, -9223372036854775808 ~ 9223372036854775807
* long long long_name; long_name = 123;
* long long int long_name; long_name = 123;
* similar to the rest of int variable declaration
## Variable declaration: float, double
### python 2 & 3
* float_name = 1.123
* float_name = 0.1123e1  # equals to 1.123
* float_name = 0.1123E1  # equals to 1.123
* float_name = 1123e-3  # equals to 1.123
* float_name = 1123E-3  # equals to 1.123
### javascript ES5
* var float_name = 1.123;
### javascript ES6
* var float_name = 1.123;
* let float_name = 1.123;
* const float_name = 1.123;
### java:
#### float: 32 bits, 4 bytes
* float float_name = 1.123f;  // have 7 decimal digits
* float float_name = (float) 1.123;
#### double: 64 bits, 8 bytes
* double double_name = 1.123d;  // have 16 decimal digits
* double double_name = 1.123;
### c++
#### float: 4 bytes
* float float_name; float_name = 1.123;  // have 7 decimal digits
* similar to the rest of int variable declaration
#### double: 8 bytes
* double double_name; double_name = 1.123;  // have 15 decimal digits
* similar to the rest of int variable declaration
#### long double: 12 bytes
* long double double_name; double_name = 1.123;  // have 19 decimal digits
* similar to the rest of int variable declaration
## Strings
### python 2 & 3
```python
    string_name = "string"
    string_name = 'string'
    # back slash not required, but will produce a new line if not given
    string_name = """multi-line \
    string\
    """
```
### javascript ES5
```javascript
    var string_name = "string";
    var string_name = 'string';
    // back slash required
    var string_name = "multi-line \
    string"
```
### javascript ES6  // Almost all of ES5 are included in ES6
```javascript
    // back slash not required, but will produce a new line if not given
    var string_name = `multi-line \
    string`
    let string_name = "string";
    const string_name = "string";
```
### java
#### character: 16 bits, 2 bytes, only 1 letter or symbol, must use single quotes ''
* char char_name = 'a';
* char char_name = '\u0061';  // unicode character for the letter a
#### strings: must use double quotes ""
```java
    String string_name = "string";
    String string_name = "multi-line " +
                         "string";
```
### c++
#### character: only have 1 character, must use single quotes ''
* char char_name; char_name = 'a';
* char char_name = 'a';
* char char_name ('a');
* char char_name {'a'};
#### strings
##### C-style strings: an ARRAY of characters, must use double quotes ""
* THIS IS NOT A TRUE STRING, IT IS AN ARRAY OF CHARACTERS!!!!!!!
* char * string_name = "string";
* const char * string_name = "string";  // const is normally used
* char string_name[] = "string";  // creates array of 7 chars, last char is null "\0"
* char string_name[7] = "string";  // need give 7 slots for chars and null char
* char string_name[7] = {'s', 't', 'r', 'i', 'n', 'g', 0};  // no 0 = error
* char string_name[7] = {'s', 't', 'r', 'i', 'n', 'g', '\0'};  // no '\0' = error
##### C++ strings: must add at the top "#include＜string＞", must use double quotes ""
```c++
    std::string string_name; string_name = "string";
    // back slash not required, but can use if want to
    std::string string_name = "multi-line"
                  "string";
    std::string string_name ("string");
    std::string string_name {"string"};
```
## Boolean
### python 2 & 3
* boolean_name = True
* boolean_name = False
### javascript ES5
* var boolean_name; boolean_name = true;
* var boolean_name = false;
### javascript ES6
* let boolean_name; boolean_name = true;
* let boolean_name = false;
* const boolean_name = true;
### java
* boolean boolean_name = true;
* boolean boolean_name = false;
### c++: 8 bits
* bool boolean_name; boolean_name = true;  // produces a 1 output
* bool boolean_name = false;  // produces a 0 output
* bool boolean_name (true);
* bool boolean_name {false};
## Arithmetic Operators
### python 2
* addition: +
* subtraction: -
* multiplication: *
* division: 3.0/2  # output 1.5, 3/2 output 1
* modulus: %
* exponent: **
* floor division: 3//2  # output 1
### python 3
* division: 3/2  # output 1.5
* floor division: 3//2  # output 1
### javascript
* addition: +
* subtraction: -
* multiplication: *
* division: 3/2  // output 1.5
* modulus: %
* exponent: **
* floor division: 3//2  // output 1
### java
* addition: +
* subtraction: -
* multiplication: *
* division: double double_name = 3.0/2;  // output 1.5, 3/2 output 1
* modulus: %
* exponent: Math.pow(3, 2);  // output 9
* floor division: int integer_name = 3/2;  // output 1
### c++
* addition: +
* subtraction: -
* multiplication: *
* division: double double_name = 3.0/2  // output 1.5, 3/2 output 1
* modulus: %
* exponent:
    * must add this to the top "#include＜cmath＞"
    * int integer_name = pow(3, 2);  // output 9
* floor division: 3/2  // output 1
## Comparison Operators
### python 2 & 3
* ==  # condition is True if both operand have equal contents
* is  # condition is True if both operand points to the same identical object
* !=  # condition is True if both operand do not have equal contents
* is not  # condition is True if both operand do not points to the same identical object
* ＜＞ # py2 only, condition is True if both operands do not equal contents
* ＞  # condition is True if right operand is less than left operand
* ＜  # condition is True if left operand is less than right operand
* ＞=  # condition is True if right operand is less than or equal to left operand
* ＜=  # condition is True is left operand is less than or equal to right operand
### javascript
* ==  // string or int will be automatically converted before comparison
    * var x = 5;
        * x == 5;  // is true
        * x == "5"  // is also true
* ===  // string or int will NOT be converted before comparison
    * var x = 5;
        * x === 5;  // is true
        * x === "5"  // is false
* !=
* !==
* ＞
* ＜
* ＞=
* ＜=
### java
* ==
* !=
* ＞
* ＜
* ＞=
* ＜=
### c++
* ==
* !=
* ＞
* ＜
* ＞=
* ＜=
## Increment
### python 2 & 3
* x = x + 1  # increment
* x += 1
### javascript
* x = x + 1;  // add 1 now
* x += 1;  // add 1 now
* ++x;  // preincrement, add 1 now
* x++;  // postincrement, display without addition now then add 1 later when called again
### java
* x = x + 1;
* x += 1;
* ++x;  // preincrement, add 1 now
* x++;  // postincrement, display without addition now then add 1 later when called again
### c++
* x = x + 1;
* x += 1;
* ++x;  // preincrement, add 1 now
* x++;  // postincrement, display without addition now then add 1 later when called again
## Arrays & Lists
### python 2 & 3
```python
    # Empty list
    list_name = []
    # List with elements
    list_name = [1, "one", True]
    # Nested lists
    list_name = [1, ["two", 3]]
    
    # Add element to list (left to right)
    list_name.append(element)
    
    # Modify an element
    list_name[index] = element
    
    # Access an element
    list_name[index]
    
    # Remove element from list (right to left)
    list_name.pop()
    
    # Add element to list at index
    list_name.insert(index, element)
    
    # Remove element from list at index
    list_name.pop(index)
    
    # Find list size
    len(list_name)
    
    # Method 1: remove all elements
    del list_name[:]
    # Method 2: remove all elements
    list_name = []
    # Method 3: remove all elements, only in python 3
    list_name.clear()
```
### javascript
```javascript
    // Method 1: empty list
    var list_name = [];
    // Method 2: empty list
    var list_name = new Array();
    // List with elements
    var list_name = [1, "one", true];
    // Nested lists
    var list_name = [1, ["two", 3]];
    
    // Modify an element
    list_name[index] = element;
    
    // Access an element
    list_name[index];
    
    // Remove element from list (right to left)
    list_name.pop();
    // Remove element from list (left to right)
    list_name.shift();
    // Remove number of elements (left to right) from index and insert new elements (left to right)
    list_name.splice(index, number_of_element);
    
    // Add element to list (left to right)
    list_name.push(element);
    // Add element to list (right to left)
    list_name.unshift(element);
    // Add element to list at index (left to right)
    list_name.splice(index, 0, new_element1, new_element2...);
    // Add & Remove elements to & from list at index (left to right)
    list_name.splice(index, number_of_element, new_element1, new_element2...);
    
    // Returns the selected elements in an array, as a new array object
    list.name.slice();
    // Selects the elements starting at the given 1st argument, and ends at, but does not include, the given 2nd argument
    list_name.slice(1, 3);
    
    // Find list size
    list_name.length;
    // Remove all elements
    list_name = [];
```
### java
```java
    // Arrays: can only have 1 data type: string, int, etc.
    // Empty string array of desired array size
    String[] string_array = new String[length_of_desired_array];
    // New string array with elements inside
    String [] string_array = new String [] {string1, string2,...};  // Method 1
    String[] string_array = {string1, string2,...};  // Method 2
    
    // Add string array element, limited to array size
    // Modify string array element value
    string_array[index] = element;
    
    // Access an element
    string_array[index];
    
    // Find array size
    string_array.length;


    // Arraylists: can only have 1 data type: string, int, etc.
    import java.util.ArrayList;  // Must import to use
    
    // Empty string arrayList
    ArrayList<String> string_arrayList = new ArrayList<String>();
    
    // Add string element to string arrayList (left to right)
    string_arrayList.add(element);
    
    // Modify an element at index
    string_arrayList.set(index, element);
    
    // Access an element
    string_arrayList.get(index);
    
    // Remove element from arrayList at index
    string_arrayList.remove(index);
    
    // Find arrayList size
    string_arrayList.size();
    
    // Remove all elements
    string_arrayList.clear();
```
### c++
```c++
    // Arrays
    // Empty int array of desired array size
    int int_array[length_of_desired_array];
    // New int array with elements inside
    int int_array [length_of_desired_array] {element1, element2,...};  // size declared
    int int_array[] = {element1, element2,...};  // size automatically calculated
    
    // Assign int element, limited to array size
    // Modify int element value
    int_array[index] = element;
    
    // Access an element
    int_array[index];
    
    // Find array size: size of array (bytes) / size of an element of an array (bytes)
    sizeof(int_array) / sizeof(int_array[0]);


    // Vectors: a type of dynamic array
    #include <vector>  // Must import to use
    
    // Empty int vector of desired vector size, each element of 0 value will automatically be included
    std::vector <int> int_vector (length_of_desired_array);
    // New int vector with elements inside
    std::vector <int> int_vector {element1, element2,...};
    // New int vector with length of desired array and all value in parameter
    // Method 1
    std::vector <int> int_vector (length_of_desired_array, constant_value_for_all_elements);
    // Method 2
    std::vector <int> int_vector;
    int_vector.assign(length_of_desired_array, constant_value_for_all_elements);
    
    // Assign int element
    int_vector[index] = element;
    
    // Access an element
    int_vector[index];
    int_vector.at(index);
    
    // Add element to vector (left to right), vector size will automatically increase
    int_vector.push_back(element);
    // Add element to vector at index
    std::vector<int>::iterator it;  // Must create iterator for inserting or emplacing to work
    it = int_vector.begin()  // Set it at index 0
    // insert method: copies or moves the elements into the container by calling copy constructor or move constructor
    int_vector.insert(it + index, element);  // Add element at index
    // emplace method: elements are constructed in place, no copy or move operations are performed (better performance)
    int_vector.emplace(it + index, element);  // Add element at index
    
    // Remove element from vector at index
    std::vector<int>::iterator it;  // Must create iterator for erase to work
    it = int_vector.begin()  // Set it at index 0
    int_vector.erase(it + index)  // Remove element at index
    int_vector.erase(it + index, it + index)  // Remove a range of elements in the vector
    // Remove element from vector (right to left)
    int_vector.pop_back();  // does not return value
    
    // Find vector size
    int_vector.size();
    
    // Resize vector
    int_vector.resize(length_of_desired_array);
    
    // Remove all elements
    int_vector.clear();
```
## Conditional Statement
### python 2 & 3
```python
    # If else statement
    if condition_a:
        do_A
    elif condition_b:
        do_B
    else:
        do_something_else

    # Ternary operator
    do_A if condition_a else do_B

    # Switch Statement is not available in python, but can create similar function
    def switch(choice):
        case = {
            1: do_A,
            2: do_B,
        }
        case.get(choice, do_something_else)
```
### javascript
```javascript
    // If else statement
    if (condition_a) {
        do_A;
    } else if (condition_b) {
        do_B;
    } else {
        do_something_else;
    }

    // Ternary operator
    condition_a ? do_A : do_B;

    // Switch statement
    switch(choice) {
        case choice_A:
            do_A;
            break;
        case choice_B:
            do_B;
            break;
        default:
            do_something_else;
    }
```
### java
```java
    // If else statement
    if (condition_a) {
        do_A;
    } else if (condition_b) {
        do_B;
    } else {
        do_something_else;
    }

    // {} not required if statement is a single line
    if (condition_a)
        do_A;  // Single line statement
    else if (condition_b)
        do_B;  // Single line statement
    else
        do_something_else;  // Single line statement

    // Ternary operator
    condition_a ? do_A : do_B;

    // Switch statement
    switch(choice) {
        case choice_A:
            do_A;
            break;
        case choice_B:
            do_B;
            break;
        default:
            do_something_else;
            break;  // not required, but good to have in Java
    }
```
### c++
```c++
    // If else statement
    if (condition_a) {
        do_A;
    } else if (condition_b) {
        do_B;
    } else {
        do_something_else;
    }

    // {} not required if statement is a single line
    if (condition_a)
        do_A;  // Single line statement
    else if (condition_b)
        do_B;  // Single line statement
    else
        do_something_else;  // Single line statement

    // Ternary operator
    condition_a ? do_A : do_B;

    // Switch statement
    switch(choice) {
        case choice_A:
            do_A;
            break;
        case choice_B:
            do_B;
            break;
        default:
            do_something_else;
    }
```
## Loops
### python 2
```python
    # While loop
    # declare_initial_conditional_value
    i = 0
    # Set condition
    while i<5:  # Start from 0 to 4
        do_this
        # Include condition_increment_or_decrement
        i += 1
        # Can use break, continue, and pass statements to add additional functionality, or not use any
        break  # Breaks out of the current closest enclosing loop
        continue  # Goes to the top of the closest enclosing loop
        pass  # Does nothing at all


    # For loop
    # range() creates a list in python 2
    # Looping with xrange()
    for i in xrange(5):  # Starts from 0 to 4 (5 - 1)
        do_this
        # Can use break, continue, and pass statements to add additional functionality, or not use any
        break  # Breaks out of the current closest enclosing loop
        continue  # Goes to the top of the closest enclosing loop
        pass  # Does nothing at all
        
    # Looping with xrange() and multiple parameters
    for i in xrange(0, 5, 2):  # Start from 0 to 4 at every 2 steps (0,2,4)
        do_this
        
    # Reverse loop
    for i in xrange(4, -1, -1):  # Start from 4 to 0 at every -1 steps
        do_this


    # Looping and getting each value
    for value in list_name:  # [i1_value, i2_value, i3_value,...]
        print value


    # Looping and getting index and value
    for index, value in enumerate(list_name):
        print index, value  # output index, value
```
### python 3
```python
    # For loop
    # Looping with range()
    for i in range(5):  # Starts from 0 to (5 - 1)
        do_this
        # Can use break, continue, and pass statements to add additional functionality, or not use any
        break  # Breaks out of the current closest enclosing loop
        continue  # Goes to the top of the closest enclosing loop
        pass  # Does nothing at all
        
    # Looping with range() and multiple parameters
    for i in range(0, 5, 2):  # Start from 0 to 4 at every 2 steps (0,2,4)
        do_this
        
    # Reverse loop
    for i in range(4, -1, -1):  # Start from 4 to 0 at every -1 steps
        do_this


    # Looping and getting each value
    for value in list_name:  # [value1, value2, value3,...]
        print(value)


    # Looping and getting index and value
    for index, value in enumerate(list_name):
        print(index, value)  # output index, value
```
### javascript ES5
```javascript
    // While loop
    // declare_initial_conditional_value
    var i = 0;
    // Set condition
    while (i<5) {  // Start from 0 to 4
        do_this;
        // Include condition_increment_or_decrement;
        i++;
        // Can use break or continue to add additional functionality, or not use any
        break;  // Breaks out of the current closest enclosing loop
        continue;  // Goes to the top of the closest enclosing loop
    }


    // For loop
    for (var i=0; i<5; i++) {  // Start from 0 to 4
        do_this;
        // Can use break or continue to add additional functionality, or not use any
        break;  // Breaks out of the current closest enclosing loop
        continue;  // Goes to the top of the closest enclosing loop
    }
    
    // Reverse loop
    for (var i=4; i>=0; i--) {  // Start from 4 to 0
        do_this;
    }
    
    // forEach loop
    // Looping through a list while calling a function
    list_name.forEach(function(value, index, list){  // do not need to include all 3 parameters, but must be in order
        console.log(index, value, list);  // outputs index value list
    });
```
### javascript ES6: Use let in loops when declaring
```javascript
    // For of loop
    // Looping and getting each value
    for (let value of list_name) {  // [value1, value2, value3,...]
        console.log(value);  // output value
    }
    // Looping and getting index and value
    for (let index_and_value of list_name.entries()) {
        console.log(index_and_value);  // output a list [index, value]
    }
    
    // For in loop
    for (let index in list_name) {
        console.log(list_name[index]);
    }
    // For in loop normally used to get values from objects (hash table, dictionaries) than to arrays
    // object = {key1:value1, key2:value2,...}
    for (let index in object) {
        console.log(object[index]);  // outputs value, normally calling this way will not output value from objects
    }
```
### java
```java
    // While loop
    // declare_initial_conditional_value
    int i = 0;
    // Set condition
    while (i<5) {  // Start from 0 to 4
        do_this;
        // Include condition_increment_or_decrement;
        i++;
        // Can use break or continue to add additional functionality, or not use any
        break;  // Breaks out of the current closest enclosing loop
        continue;  // Goes to the top of the closest enclosing loop
    }
    
    // Do while loop: execute first before setting conditions
    // declare_initial_conditional_value
    int i = 0;
    do {  // Start from 0 to 4
        do_this;
        // Include condition_increment_or_decrement;
        i++;
    // Set condition
    } while (i<5);

    // For loop
    for (int i=0; i<5; i++) {  // Start from 0 to 4
        do_this;
        // Can use break or continue to add additional functionality, or not use any
        break;  // Breaks out of the current closest enclosing loop
        continue;  // Goes to the top of the closest enclosing loop
    }
    // Reverse loop
    for (int i=4; i>=0; i--) {  // Start from 4 to 0
        do_this;
    }
```
### c++
```c++
    // While loop
    // declare_initial_conditional_value
    int i = 0;
    // Set condition
    while (i<5) {  // Start from 0 to 4
        do_this;
        // Include condition_increment_or_decrement;
        i++;
        // Can use break or continue to add additional functionality, or not use any
        break;  // Breaks out of the current closest enclosing loop
        continue;  // Goes to the top of the closest enclosing loop
    }
    
    // Do while loop: execute first before setting conditions
    // declare_initial_conditional_value
    int i = 0;
    do {  // Start from 0 to 4
        do_this;
        // Include condition_increment_or_decrement;
        i++;
    // Set condition
    } while (i<5);

    // For loop
    for (int i=0; i<5; i++) {  // Start from 0 to 4
        do_this;
        // Can use break or continue to add additional functionality, or not use any
        break;  // Breaks out of the current closest enclosing loop
        continue;  // Goes to the top of the closest enclosing loop
    }
    // Reverse loop
    for (int i=4; i>=0; i--) {  // Start from 4 to 0
        do_this;
    }

    // Range-based for loop
    // Looping and getting each value
    for (int value : int_array) {
        cout << value << endl;  // output value per line
    }
    // Use auto to automatically detect array data type
    for (auto value : array_name) {
        cout  << value << endl;
    }

    // Infinite for loops
    for (;;)
        cout << "This will print forever" << endl;
```
## Instantiation
### python 2 & 3
```python
    t = Thing()  # everything
```
### javascript
```javascript
    v = getValue();  // plain function
    t = new Thing();  // instantiation
```
### java
```java
    v = getValue();  // plain function
    t = new Thing();  // instantiation
```
### c++
```c++
    v = getValue();  // plain function
    t = new Thing();  // instantiation
```
## Functions
### python 2 & 3
```python
    # Normal function
    def myFunction():
        do_something
    
    # Normal function with arguments
    def myFunction(a):
        do_something_with_a
        
    # Default parameters
    def myFunction(a=value):
        do_something_with_a
        
    # Lambda function: a small anonymous function
    # can take any number of arguments, but can only have 1 expression
    myFunction = lambda a : do_something_with_a
    myFunction = lambda a, b : do_something_with_a_and_b
```
### javascript ES5
```javascript
    // Normal function
    function myFunction() {
        do_something;
    }
    // Normal function with arguments
    function myFunction(a) {
        do_something_with_a;
    }
    
    // Function expression
    let myFunction = function() {
        do_something;
    }
    // Function expression with arguments
    let myFunction = function(a) {
        do_something_with_a;
    }
    
    // Arrow function: do not have their own "this" keyword
    // 1 line arrow function
    let myFunction = () => do_something;  // () at (do_something) not necessary if on single line
    // 1 line arrow function with arguments
    let myFunction = (a) => (
        do_something_with_a
    );
    // arrow function, must use return keyword
    let myFunction = () => {
        return do_something
    };
    // arrow function with arguments
    let myFunction = (a) => {
        return do_something_with_a
    };
    
    // Immediately Invoked Function Expressions (IIFE)
    // method 1
    (function() {
        do_something;
    })();
    // method 2
    (function() {
        do_something;
    }());
    // method 3: no returning of value
    !function() {
        do_something;
    }();
```
### javascript ES6
```javascript
    // Default parameters
    function myFunction(a=value) {
        do_something_with_a;
    }
```
### java

### c++


## Higher order functions
### python 2
```python
    # Map: applies a given function to each item of an iterable (list, tuple etc.) and returns a list of the results
    # map(function, iterable, ...)
    arr = [1, 2, 3]
    def add(n):
        return n + n
    map(add, arr)  # return <map object at 0x10473e518>
    list(map(add, arr))  # return [2, 4, 6]
    
    
    # Filter: filter and return a new array based on the conditions
    # filter(function, iterable)
    arr = [1, 2, 3]
    def condition(n):
        if n < 3:
            return n
    filter(condition, arr)  # return <filter object at 0x10473e550>
    list(filter(condition, arr))  # return [1, 2]
    
    
    # Reduce: executes a function on each element, resulting in a single output value
    arr = [1, 2, 3]
    def compute(n, m):
        return n * m
    reduce(compute, arr)  # return 6
```
### python 3
```python
    # Reduce: executes a function on each element, resulting in a single output value
    arr = [1, 2, 3]
    def compute(n, m):
        return n * m
    from functools import reduce  # requires import in python 3
    reduce(compute, arr)  # return 6
```
### javascript
```javascript
    // Map: create a new array from a current array
    // array.map(element, currentIndex, originalArray)
    const companies = [
        {name: "company1", category: "industry1"},
        {name: "company2", category: "industry2"}
    ];
    // callback method
    const companyNames = companies.map(function(company) {
        return company.name;
    }
    // arrow function method
    const companynames = companies.map((company) => company.name);
    
    
    // Filter: creates a new array with all elements that pass the condition implemented by the provided function
    // array.filter(element, currentIndex, originalArray)
    const ages = [age1, age2, age3];
    // callback method
    const canDrink = ages.filter(function(age) {
        if (condition) {
            return true;
        }
    }
    // arrow function method
    const canDrink = ages.filter(age => condition);
    
    
    // Reduce: executes a function on each element of the array, resulting in a single output value
    // array.reduce(function(accumulator, currentValue){ do_something }, initialValue)
    let arr = [1, 2, 3];
    // no initial value
    arr.reduce(function(accumulator, currentValue) {
        return accumulator + currentValue;
    });  // returns a value of 6
    /*
    accumulator | currentValue | returned value
        1       |       2      |        3
        3       |       3      |        6
    */
    
    // initial value included
    arr.reduce(function(accumulator, currentValue) {
        return accumulator + currentValue;
    }, 10);  // returns a value of 16
    /*
    accumulator | currentValue | returned value
        10      |       1      |        11
        11      |       2      |        13
        13      |       3      |        16
    */
    
    
    // Sort: sorts the elements of an array in place and returns the sorted array
    // array.sort(compareFunction)
    // if compareFunction is not used, all sorted elements will be sorted based on it's string value
    let array = ["1", 30, 4, 21, 100000];
    array.sort();  // returns ["1", 100000, 21, 30, 4]
    
    // sort in ascending order
    array.sort((a, b) => a - b);  // returns ["1", 4, 21, 30, 100000]
    
    // sort in descending order
    array.sort((a, b) => b - a);  // returns [100000, 30, 21, 4, "1"]
```
### java

### c++


## Hash Tables, Dictionaries, Objects
### python 2 & 3
```python
    # Create dictionary
    newDict = {}
    
    # Create dictionary and assign key value pairs
    # method 1
    newDict = {
        "key1": "value1",
        "key2": 123,
        "key3": True,
        "key4": myFunction
    }
    # method 2
    newDict = dict(key1="value1", key2="value2")
    
    # Add or reassign key value pair
    newDict["Key"] = "Value"  # method 1
    newDict.update({"key": "value"})
    
    # Set multiple keys with a similar value
    newKeys = ("key1", "key2", "key3")
    newValue = value
    newDict = dict.fromkeys(newKeys, newValue)
    
    # Return value of the item with the specified key
    # If the key does not exist, insert the key, with the specified value
    newVariable = newDict.setdefault("key", "newValue")
    
    # Get value
    newDict["key"]  # method 1
    newDict.get("key")  # method 2
    
    # Loop through Dictionary and get each key
    # method 1
    for key in newDict:
        print(key)
    # method 2
    for key in newDict.keys():
        print(key)
        
    # Loop through Dictionary and get each value
    # method 1
    for key in newDict:
        print(newDict[key])
    # method 2
    for value in newDict.values():
        print(value)
        
    # Loop through both keys and values
    for key, value in newDict.items():
        print(key, value)
        
    # Check if key exists
    if "key" in newDict:
        return True
        
    # Get dictionary length
    len(newDict)
    
    # Copy dictionary
    # cannot copy just from dict2 = dict1 as it is just referencing to dict1
    # method 1
    newDict2 = newDict.copy()
    # method 2
    newDict2 = dict(newDict)
    
    # Remove items
    newDict.pop("key")  # method 1
    del newDict["key1"]  # method 2
    
    # Remove last inserted item
    newDict.popitem()
    
    # Delete entire dictionary
    del newDict  # method 1
    newDict.clear()  # method 2
```
### javascript ES5
```javascript
    // Objects
    // Create object
    let newObj = new Object();  // method 1
    let newObj = {};  // method 2
    
    // Create object and assign values
    // keys can only be strings without quotes
    let newObj = {
        key1: "stringValue",
        key2: 123,
        key3: true,
        key4: ["array", "array2"],
        key5: {anotherKey: anotherValue},
        key6: function(arg){return do_something_with_arg}
    };
    
    // Creates a new object, using an existing object as the prototype of the newly created object
    let newObj2 = Object.create(newObj);  // method 1
    let newObj2 = Object.assign({}, newObj);  // method 2
    
    // Assign and Reassign values
    newObj["key1"] = "newString";  // method 1
    newObj.key1 = "newString2";  // method 2
    
    // Copy the values of all enumerable own properties from one or more source objects to a target object
    // return the target object
    const target = { a: 1, b: 2 };
    const source = { b: 4, c: 5 };
    const newObj = Object.assign(target, source);  // newObj, target = { a: 1, b: 4, c: 5 }
    
    // Get value
    newObj["key1"];  // method 1
    newObj.key1;  // method 2

    // Get an array of keys
    Object.keys(newObj);
    
    // Get an array of values
    Object.values(newObj);
    
    // Loop through all key value pairs
    // must be (key, value)
    for (let [key, value] of newObj.entries()) {console.log(`Key: ${key}, Value: ${value}`);}
    
    // Defines a new property directly on an object, or modifies an existing property on an object, and returns the object
    // Object.defineProperty(obj, propertyName, descriptor)
    Object.defineProperty(newObj, property1, {value: "123", writable: true});  // newObj.property1 = 123
    
    // Seals an object
    // prevent addition of properties, however defined properties still can be changed
    Object.seal(newObj);
    
    // Freeze an object
    // makes the object immutable, meaning no change to defined property allowed, unless they are objects.
    Object.freeze(newObj);
```
### javascript ES6
```javascript
    // Maps or Hash tables
    // Create new Map or hash table
    const newDict = new Map();
    
    // Add key value pair data
    // keys does not need to be strings, can be numbers, booleans, etc.
    newDict.set(key1, value1);
    newDict.set(key2, value2);
    
    // Get all keys
    newDict.keys();
    
    // Get all values
    newDict.values();
    
    // Iterate over Maps to get each key
    for (let key of newDict.keys()) {
        console.log(key);
    }
    
    // Iterate over Maps to get each value
    for (let value of newDict.values()) {
        console.log(value);
    }
    
    // Get value
    newDict.get(key);
    
    // Get hash table size
    newDict.size;
    
    // Check if key value pair exist with key input
    newDict.has(key);
    
    // Loop through all key value pairs
    // method 1, must be (value, key)
    newDict.forEach((value, key) => console.log(`Key: ${key}, Value: ${value}`));
    // method 2, must be (key, value)
    for (let [key, value] of newDict.entries()) {console.log(`Key: ${key}, Value: ${value}`);}
    
    // Delete key value pair
    newDict.delete(key);
    // Delete all key value pairs
    newDict.clear()
    
    
    // WeakMap: similar to Map, but all keys must be objects
    // Create new weak map
    const newDict = new WeakMap();
    
    // Add key value pair data
    // key MUST be and Object
    newDict.set(obj1, value1);
    newDict.set(obj2, value2);
    
    // Get value
    newDict.get(obj);
    
    // Delete key value pair
    newDict.delete(obj);
    
    // Check if key value pair exist with key input
    newDict.has(obj);
```
### java

### c++


## Destructuring
### python 2 & 3
```python
    # Tuples
    xVariable, yVariable = (xValue, yValue)
    
    # Arrays
    xVariable, yVariable = [xValue, yValue]
    
    # String
    xVariable, yVariable = "xy"
    
    # Dictionaries
    xKey, yKey = {"xKey": xValue, "yKey": yValue}
```
### javascript ES6
```javascript
    // Arrays
    const [xVariable, yVariable] = [xValue, yValue];
    
    // Objects
    const obj = {
        xKey: xValue,
        yKey: yValue
    }
    // declaring variables
    const {xKey, yKey} = obj;  // variable names must be the same as object key names
    
    // assigning different variable names
    const {xKey: xNewKey, yKey: yNewKey} = obj;
```
### java

### c++


## Spread Operator
### python 2 & 3
```python
    # *args (splat)
    # Takes an array and transform (unpacks) it into single values
    # Must utitlize all of the element of the array to work
    myFunction(a, b, c)  // normal method
    myFunction(*Tuple)  // (a, b, c)
    myFunction(*List)  // [a, b, c]
    myFunction(*String)  // "abc"
    myFunction(*Dict)  // {"a": value1, "b": value2}  only utilize the keys
    
    # **kwargs
    myFunction(**Dict) // {"a": value1, "b": value2}  utilize both keys and values
```
### javascript ES6
```javascript
    // Takes an array and transform (unpacks) it into single values
    // Must utitlize all of the element of the array to work
    let arr = [a, b, c];
    myFunction(a, b, c);  // normal method
    myFunction.apply(null, arr)  // using the apply() method
    myFunction(...arr);  // spread method
    
    // join multiple arrays together
    let arr1 = [a, b, c];
    let arr2 = [d, e, f];
    let totalArr = arr1.concat(arr2);  // concat method
    let totalArr = [...arr1, ...arr2];
```
### java

### c++


## Rest parameters
### python 2 & 3
```python
    # *args
    # Receive a couple of single values and transform them into an array
    def myFunction(*args):
        newArr = args  # args is an array of arugments

    # **kwargs
    # Receive a couple of keys and values and transform them into a dictionary
    def myFunction(**kwargs):
        newDict = kwargs  # kwargs is a dictionary of keys and values
    # calling example
    myFunction(var1=value1, var2=value2)
```
### javascript ES6
```javascript
    // Receive a couple of single values and transform them into an array
    function myFunction(...args) {
        let argsArr = args;  // args is an array of arguments
    }
```
### java

### c++


## Class

### python 2 & 3

### javascript

### java

### c++


## Importing Libraries

### python 2 & 3

### javascript

### java

### c++


## Type Conversions

### python 2 & 3

### javascript

### java

### c++


## String Concatenation

### python 2 & 3

### javascript

### java

### c++

