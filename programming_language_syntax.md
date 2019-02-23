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
    # Singale line comment
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
* var integer_name; integer_name = 123;
* let integer_name; integer_name = 123;  // accessible only within the block {}
* var integer_name = 123;
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
### javascript ES6
```javascript
    var string_name = "string";
    var string_name = 'string';
    // back slash required
    var string_name = "multi-line \
    string"
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
* var boolean_name; boolean_name = true;
* var boolean_name = false;
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
* addition: +
* subtraction: -
* multiplication: *
* division: 3/2  # output 1.5
* modulus: %
* exponent: **
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
    * var x = 5; x == 5;  // is true, x == "5"  // is also true
* ===  // string or int will NOT be converted before comparison
    * var x = 5; x === 5;  // is true, x === "5"  // is false
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
    // Add element to list (left to right)
    list_name.push(element);
    // Add element to list (right to left)
    list_name.unshift(element);
    // Modify an element
    list_name[index] = element;
    // Access an element
    list_name[index];
    // Remove element from list (right to left)
    list_name.pop();
    // Remove element from list (left to right)
    list_name.shift();
    // Add element to list at index (left to right)
    // Remove number of elements (left to right) from index and insert new elemeents (left to right)
    // Add & Remove elements to & from list at index (left to right)
    list_name.spice(index, number_of_element, new_element1, new_element2...);
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
    String[] string_array = {string1, string2,...};
    // Add string element, limited to array size
    // Modify string element value
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
    std::vector<int>::iterator it;  // Must create iterator for inserting or emplacing to work to work
    it = int_vector.begin()  // Set it at index 0
    // insert method: copies or moves the elements into the container by calling copy constructor or move constructor
    int_vector.insert(it + index, element);  // Add element at index
    // emplace method: elements are constructed in place, no copy or move operations are performed (better performance)
    int_vector.emplace(it + index, element);  // Add element at index
    // Remove element from vector at index
    std::vector<int>::iterator it;  // Must create iterator for erase to work to work
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

## Hash Tables, Dictionaries, Objects

### python 2 & 3

### javascript

### java

### c++


## Conditional Statement

### python 2 & 3

### javascript

### java

### c++


## Loops

### python 2 & 3

### javascript

### java

### c++


## Functions

### python 2 & 3

### javascript

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

